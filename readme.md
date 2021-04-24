# vue-composition-decorator

## Usage

```ts
import { defineComponent, Ref, Watch } from 'vue-composition-decorator';

export default defineComponent({
  setup() {
    @Ref()
    const number = 1;

    @Watch(() => number)
    const onNumberChange = (prev, next) => {
      console.log('number changed.');
    };

    return {
      number,
    };
  },
  template: `
    <div>
      {{ number }}
    </div>
  `,
});
```
