<script setup>
import { onMounted, ref } from "vue";

const root = ref(null);
const observer = ref(null);

const onElementObserved = (entries) => {
  entries.forEach(({ target, isIntersecting }) => {
    const id = target.getAttribute("id");

    if (isIntersecting) {
      root.value.querySelector(`a[href="#${id}"]`).classList.add("active");
    } else {
      root.value.querySelector(`a[href="#${id}"]`).classList.remove("active");
    }
  });
};

onMounted(() => {
  observer.value = new IntersectionObserver(onElementObserved, {
    root: root.value,
    threshold: 0.37,
  });

  root.value.querySelectorAll("section[id]").forEach((section) => {
    observer.value.observe(section);
  });
});
</script>

<template>
  <main ref="root" class="flex justify-center">
    <nav class="flex flex-col gap-1 h-screen overflow-hidden w-48 pt-32">
      <a class="hover:text-gray-600" href="#feline-frenzy">Feline Frenzy</a>
      <a class="hover:text-gray-600" href="#paws-itively-adorable"
        >Paws-ititvely Adorable</a
      >
      <a class="hover:text-gray-600" href="#whisker-wonderland"
        >Whisker Wonderland</a
      >
    </nav>

    <div class="h-screen overflow-y-auto pt-16">
      <div class="max-w-[600px]">
        <h1 class="text-2xl h-16">Cats and Kittens</h1>

        <section id="feline-frenzy">
          <h2 class="text-xl mb-5">Feline Frenzy</h2>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Cumque
            dolorem repellat delectus quaerat esse in, sunt sit. Suscipit
            impedit nesciunt nemo totam delectus tempora ipsum blanditiis
            ratione, asperiores aliquam incidunt.
          </p>
          <p>
            Itaque placeat accusamus unde suscipit quasi odio, quidem,
            veritatis, reiciendis architecto reprehenderit rerum explicabo
            nulla? Et quaerat ratione ullam dolore, porro autem illo neque,
            itaque, debitis cum eveniet ut fugiat.
          </p>
          <p>
            Consequuntur a itaque maxime repellat? Non at placeat fuga
            praesentium eius, iure quam sapiente perspiciatis dolorem? Aliquid
            praesentium ipsa a repudiandae aperiam voluptas voluptatem,
            accusamus laudantium eligendi consequuntur reprehenderit quas.
          </p>
          <p>
            Voluptatibus accusamus tempore, laboriosam praesentium quisquam non
            provident placeat, iure fugit nesciunt repellat atque voluptas
            maiores culpa. Blanditiis repudiandae nesciunt amet saepe quis,
            natus asperiores maiores eveniet quisquam officia recusandae.
          </p>
          <p>
            Dolorem cumque repudiandae eligendi necessitatibus aliquid ipsam
            nisi. Esse aliquid assumenda voluptatem ratione aperiam quaerat
            reiciendis molestias fugit expedita consequuntur qui quos nulla eum
            a ab vel magnam, quas tempora?
          </p>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Cumque
            dolorem repellat delectus quaerat esse in, sunt sit. Suscipit
            impedit nesciunt nemo totam delectus tempora ipsum blanditiis
            ratione, asperiores aliquam incidunt.
          </p>
          <p>
            Itaque placeat accusamus unde suscipit quasi odio, quidem,
            veritatis, reiciendis architecto reprehenderit rerum explicabo
            nulla? Et quaerat ratione ullam dolore, porro autem illo neque,
            itaque, debitis cum eveniet ut fugiat.
          </p>
          <p>
            Consequuntur a itaque maxime repellat? Non at placeat fuga
            praesentium eius, iure quam sapiente perspiciatis dolorem? Aliquid
            praesentium ipsa a repudiandae aperiam voluptas voluptatem,
            accusamus laudantium eligendi consequuntur reprehenderit quas.
          </p>
          <p>
            Voluptatibus accusamus tempore, laboriosam praesentium quisquam non
            provident placeat, iure fugit nesciunt repellat atque voluptas
            maiores culpa. Blanditiis repudiandae nesciunt amet saepe quis,
            natus asperiores maiores eveniet quisquam officia recusandae.
          </p>
          <p>
            Dolorem cumque repudiandae eligendi necessitatibus aliquid ipsam
            nisi. Esse aliquid assumenda voluptatem ratione aperiam quaerat
            reiciendis molestias fugit expedita consequuntur qui quos nulla eum
            a ab vel magnam, quas tempora?
          </p>
        </section>

        <section id="paws-itively-adorable">
          <h2 class="text-xl mb-5">Paws-itively Adorable</h2>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Cumque
            dolorem repellat delectus quaerat esse in, sunt sit. Suscipit
            impedit nesciunt nemo totam delectus tempora ipsum blanditiis
            ratione, asperiores aliquam incidunt.
          </p>
          <p>
            Itaque placeat accusamus unde suscipit quasi odio, quidem,
            veritatis, reiciendis architecto reprehenderit rerum explicabo
            nulla? Et quaerat ratione ullam dolore, porro autem illo neque,
            itaque, debitis cum eveniet ut fugiat.
          </p>
          <p>
            Consequuntur a itaque maxime repellat? Non at placeat fuga
            praesentium eius, iure quam sapiente perspiciatis dolorem? Aliquid
            praesentium ipsa a repudiandae aperiam voluptas voluptatem,
            accusamus laudantium eligendi consequuntur reprehenderit quas.
          </p>
          <p>
            Voluptatibus accusamus tempore, laboriosam praesentium quisquam non
            provident placeat, iure fugit nesciunt repellat atque voluptas
            maiores culpa. Blanditiis repudiandae nesciunt amet saepe quis,
            natus asperiores maiores eveniet quisquam officia recusandae.
          </p>
          <p>
            Dolorem cumque repudiandae eligendi necessitatibus aliquid ipsam
            nisi. Esse aliquid assumenda voluptatem ratione aperiam quaerat
            reiciendis molestias fugit expedita consequuntur qui quos nulla eum
            a ab vel magnam, quas tempora?
          </p>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Cumque
            dolorem repellat delectus quaerat esse in, sunt sit. Suscipit
            impedit nesciunt nemo totam delectus tempora ipsum blanditiis
            ratione, asperiores aliquam incidunt.
          </p>
          <p>
            Itaque placeat accusamus unde suscipit quasi odio, quidem,
            veritatis, reiciendis architecto reprehenderit rerum explicabo
            nulla? Et quaerat ratione ullam dolore, porro autem illo neque,
            itaque, debitis cum eveniet ut fugiat.
          </p>
          <p>
            Consequuntur a itaque maxime repellat? Non at placeat fuga
            praesentium eius, iure quam sapiente perspiciatis dolorem? Aliquid
            praesentium ipsa a repudiandae aperiam voluptas voluptatem,
            accusamus laudantium eligendi consequuntur reprehenderit quas.
          </p>
          <p>
            Voluptatibus accusamus tempore, laboriosam praesentium quisquam non
            provident placeat, iure fugit nesciunt repellat atque voluptas
            maiores culpa. Blanditiis repudiandae nesciunt amet saepe quis,
            natus asperiores maiores eveniet quisquam officia recusandae.
          </p>
          <p>
            Dolorem cumque repudiandae eligendi necessitatibus aliquid ipsam
            nisi. Esse aliquid assumenda voluptatem ratione aperiam quaerat
            reiciendis molestias fugit expedita consequuntur qui quos nulla eum
            a ab vel magnam, quas tempora?
          </p>
        </section>

        <section id="whisker-wonderland">
          <h2 class="text-xl mb-5">Whisker Wonderland</h2>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Cumque
            dolorem repellat delectus quaerat esse in, sunt sit. Suscipit
            impedit nesciunt nemo totam delectus tempora ipsum blanditiis
            ratione, asperiores aliquam incidunt.
          </p>
          <p>
            Itaque placeat accusamus unde suscipit quasi odio, quidem,
            veritatis, reiciendis architecto reprehenderit rerum explicabo
            nulla? Et quaerat ratione ullam dolore, porro autem illo neque,
            itaque, debitis cum eveniet ut fugiat.
          </p>
          <p>
            Consequuntur a itaque maxime repellat? Non at placeat fuga
            praesentium eius, iure quam sapiente perspiciatis dolorem? Aliquid
            praesentium ipsa a repudiandae aperiam voluptas voluptatem,
            accusamus laudantium eligendi consequuntur reprehenderit quas.
          </p>
          <p>
            Voluptatibus accusamus tempore, laboriosam praesentium quisquam non
            provident placeat, iure fugit nesciunt repellat atque voluptas
            maiores culpa. Blanditiis repudiandae nesciunt amet saepe quis,
            natus asperiores maiores eveniet quisquam officia recusandae.
          </p>
          <p>
            Dolorem cumque repudiandae eligendi necessitatibus aliquid ipsam
            nisi. Esse aliquid assumenda voluptatem ratione aperiam quaerat
            reiciendis molestias fugit expedita consequuntur qui quos nulla eum
            a ab vel magnam, quas tempora?
          </p>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Cumque
            dolorem repellat delectus quaerat esse in, sunt sit. Suscipit
            impedit nesciunt nemo totam delectus tempora ipsum blanditiis
            ratione, asperiores aliquam incidunt.
          </p>
          <p>
            Itaque placeat accusamus unde suscipit quasi odio, quidem,
            veritatis, reiciendis architecto reprehenderit rerum explicabo
            nulla? Et quaerat ratione ullam dolore, porro autem illo neque,
            itaque, debitis cum eveniet ut fugiat.
          </p>
          <p>
            Consequuntur a itaque maxime repellat? Non at placeat fuga
            praesentium eius, iure quam sapiente perspiciatis dolorem? Aliquid
            praesentium ipsa a repudiandae aperiam voluptas voluptatem,
            accusamus laudantium eligendi consequuntur reprehenderit quas.
          </p>
          <p>
            Voluptatibus accusamus tempore, laboriosam praesentium quisquam non
            provident placeat, iure fugit nesciunt repellat atque voluptas
            maiores culpa. Blanditiis repudiandae nesciunt amet saepe quis,
            natus asperiores maiores eveniet quisquam officia recusandae.
          </p>
          <p>
            Dolorem cumque repudiandae eligendi necessitatibus aliquid ipsam
            nisi. Esse aliquid assumenda voluptatem ratione aperiam quaerat
            reiciendis molestias fugit expedita consequuntur qui quos nulla eum
            a ab vel magnam, quas tempora?
          </p>
        </section>
      </div>
    </div>
  </main>
</template>

<style scoped>
.active {
  font-weight: bold;
}

p {
  margin-bottom: 2em;
}
</style>
