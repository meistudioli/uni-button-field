# uni-button-field

[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/uni-button-field) [![DeepScan grade](https://deepscan.io/api/teams/16372/projects/32024/branches/1039760/badge/grade.svg)](https://deepscan.io/dashboard#view=project&tid=16372&pid=32024&bid=1039760)

&lt;uni-button-field /> is an encapsulated Web Component built upon the foundation of the uniopen design language.

Implementation is straightforward: simply slot a standard input element inside &lt;uni-button-field />. The component instantly applies a user interface that aligns seamlessly with the uniopen design language guidelines. Furthermore, its visual styles can be dynamically adapted via native HTML attributes or JavaScript properties.

![<uni-button-field />](https://blog.lalacube.com/mei/img/preview/uni-button-field.png)

## Basic Usage

&lt;uni-button-field /> is a web component. All we need to do is put the required script into your HTML document. Then follow &lt;uni-button-field />'s html structure and everything will be all set.

- Required Script

  ```html
  <script
    type="module"
    src="https://unpkg.com/uni-button-field/mjs/wc-uni-button-field.js">        
  </script>
  ```

- Structure

  Put &lt;uni-button-field /> into HTML document. It will have different functions and looks with attribute mutation.
  
  ```html
  <uni-button-field
    appearance="filled"
    theme="main"
    size="large"
  >
    <button
      slot="button"
      type="button"
    >
      <em class="icon-plus"></em>
      button
      <em class="icon-arrow"></em>
    </button>
  </uni-button-field>
  ```

&lt;uni-button-field /> dynamically adjusts its user interface and core functionality by strictly adhering to the attributes of the encapsulated `[slot="button"]` element. Developers can leverage these capabilities and observe the corresponding behavioral shifts by modifying standard attributes—such as `disabled`—directly on the element.

```html
<uni-button-field
  appearance="filled"
  theme="main"
  size="medium"
>
  <button
    slot="button"
    type="button"
    disabled
  >
    <em class="icon-plus"></em>
    button
    <em class="icon-arrow"></em>
  </button>
</uni-button-field>
```

## JavaScript Instantiation

&lt;uni-button-field /> could also use JavaScript to create DOM element. Here comes some examples.

```html
<script type="module">
import { UniButtonField } from 'https://unpkg.com/uni-button-field/mjs/wc-uni-button-field.js';

const buttonTemplate = document.querySelector('.my-button-template');

// use DOM api
const nodeA = document.createElement('uni-button-field');
nodeA.appendChild(buttonTemplate.content.cloneNode(true));
document.body.appendChild(nodeA);

// new instance with Class
const nodeB = new UniButtonField();
nodeB.appendChild(buttonTemplate.content.cloneNode(true));
document.body.appendChild(nodeB);
</script>
```

## Style Customization

Developers could apply styles to decorate &lt;uni-button-field />'s looking.

```html
<style>
uni-button-field {
  /* filled > main */
  --uni-button-field-text-color-filled-main-normal: var(--ct_text_inverse_general);
  --uni-button-field-text-color-filled-main-disabled: var(--ct_text_inverse_general);
  --uni-button-field-text-color-filled-main-hover: var(--ct_text_inverse_general);
  --uni-button-field-text-color-filled-main-active: var(--ct_text_inverse_general);
  --uni-button-field-border-color-filled-main-normal: transparent;
  --uni-button-field-border-color-filled-main-disabled: transparent;
  --uni-button-field-border-color-filled-main-hover: transparent;
  --uni-button-field-border-color-filled-main-active: transparent;
  --uni-button-field-background-color-filled-main-normal: var(--ct_button-filled_main_enabled);
  --uni-button-field-background-color-filled-main-disabled: var(--ct_button-filled_main_disabled);
  --uni-button-field-background-color-filled-main-hover: var(--ct_button-filled_main_hover);
  --uni-button-field-background-color-filled-main-active: var(--ct_button-filled_main_active);

  /* filled > moderate */
  --uni-button-field-text-color-filled-moderate-normal: var(--ct_text_inverse_general);
  --uni-button-field-text-color-filled-moderate-disabled: var(--ct_text_inverse_general);
  --uni-button-field-text-color-filled-moderate-hover: var(--ct_text_inverse_general);
  --uni-button-field-text-color-filled-moderate-active: var(--ct_text_inverse_general);
  --uni-button-field-border-color-filled-moderate-normal: transparen);
  --uni-button-field-border-color-filled-moderate-disabled: transparen);
  --uni-button-field-border-color-filled-moderate-hover: transparen);
  --uni-button-field-border-color-filled-moderate-active: transparen);
  --uni-button-field-background-color-filled-moderate-normal: var(--ct_button-filled_moderate_enabled);
  --uni-button-field-background-color-filled-moderate-disabled: var(--ct_button-filled_moderate_disabled);
  --uni-button-field-background-color-filled-moderate-hover: var(--ct_button-filled_moderate_hover);
  --uni-button-field-background-color-filled-moderate-active: var(--ct_button-filled_moderate_active);

  /* filled > inverse */
  --uni-button-field-text-color-filled-inverse-normal: var(--ct_text_main_general);
  --uni-button-field-text-color-filled-inverse-disabled: var(--ct_text_main_general);
  --uni-button-field-text-color-filled-inverse-hover: var(--ct_text_main_general);
  --uni-button-field-text-color-filled-inverse-active: var(--ct_text_main_general);
  --uni-button-field-border-color-filled-inverse-normal: transparent;
  --uni-button-field-border-color-filled-inverse-disabled: transparent;
  --uni-button-field-border-color-filled-inverse-hover: transparent;
  --uni-button-field-border-color-filled-inverse-active: transparent;
  --uni-button-field-background-color-filled-inverse-normal: var(--ct_button-filled_inverse_enabled);
  --uni-button-field-background-color-filled-inverse-disabled: var(--ct_button-filled_inverse_disabled);
  --uni-button-field-background-color-filled-inverse-hover: var(--ct_button-filled_inverse_hover);
  --uni-button-field-background-color-filled-inverse-active: var(--ct_button-filled_inverse_active);

  /* outlined > main */
  --uni-button-field-text-color-outlined-main-normal: var(--ct_text_main_general);
  --uni-button-field-text-color-outlined-main-disabled: var(--ct_text_main_general);
  --uni-button-field-text-color-outlined-main-hover: var(--ct_text_main_general);
  --uni-button-field-text-color-outlined-main-active: var(--ct_text_main_general);
  --uni-button-field-border-color-outlined-main-normal: var(--ct_button-outlined_main_stroke);
  --uni-button-field-border-color-outlined-main-disabled: var(--ct_button-outlined_main_stroke);
  --uni-button-field-border-color-outlined-main-hover: var(--ct_button-outlined_main_stroke);
  --uni-button-field-border-color-outlined-main-active: var(--ct_button-outlined_main_stroke);
  --uni-button-field-background-color-outlined-main-normal: transparent;
  --uni-button-field-background-color-outlined-main-disabled: transparent;
  --uni-button-field-background-color-outlined-main-hover: var(--ct_button-outlined_main_container_hover);
  --uni-button-field-background-color-outlined-main-active: var(--ct_button-outlined_main_container_active);

  /* outlined > moderate */
  --uni-button-field-text-color-outlined-moderate-normal: var(--ct_text_moderate_general);
  --uni-button-field-text-color-outlined-moderate-disabled: var(--ct_text_moderate_general);
  --uni-button-field-text-color-outlined-moderate-hover: var(--ct_text_moderate_general);
  --uni-button-field-text-color-outlined-moderate-active: var(--ct_text_moderate_general);
  --uni-button-field-border-color-outlined-moderate-normal: var(--ct_button-outlined_moderate_stroke);
  --uni-button-field-border-color-outlined-moderate-disabled: var(--ct_button-outlined_moderate_stroke);
  --uni-button-field-border-color-outlined-moderate-hover: var(--ct_button-outlined_moderate_stroke);
  --uni-button-field-border-color-outlined-moderate-active: var(--ct_button-outlined_moderate_stroke);
  --uni-button-field-background-color-outlined-moderate-normal: transparent;
  --uni-button-field-background-color-outlined-moderate-disabled: transparent;
  --uni-button-field-background-color-outlined-moderate-hover: var(--ct_button-outlined_main_container_hover);
  --uni-button-field-background-color-outlined-moderate-active: var(--ct_button-outlined_main_container_active);

  /* outlined > inverse */
  --uni-button-field-text-color-outlined-inverse-normal: var(--ct_text_inverse_general);
  --uni-button-field-text-color-outlined-inverse-disabled: var(--ct_text_inverse_general);
  --uni-button-field-text-color-outlined-inverse-hover: var(--ct_text_inverse_general);
  --uni-button-field-text-color-outlined-inverse-active: var(--ct_text_inverse_general);
  --uni-button-field-border-color-outlined-inverse-normal: var(--ct_button-outlined_inverse_stroke);
  --uni-button-field-border-color-outlined-inverse-disabled: var(--ct_button-outlined_inverse_stroke);
  --uni-button-field-border-color-outlined-inverse-hover: var(--ct_button-outlined_inverse_stroke);
  --uni-button-field-border-color-outlined-inverse-active: var(--ct_button-outlined_inverse_stroke);
  --uni-button-field-background-color-outlined-inverse-normal: transparent;
  --uni-button-field-background-color-outlined-inverse-disabled: transparent;
  --uni-button-field-background-color-outlined-inverse-hover: var(--ct_button-outlined_inverse_container_hover);
  --uni-button-field-background-color-outlined-inverse-active: var(--ct_button-outlined_inverse_container_active);

  /* text > main */
  --uni-button-field-text-color-text-main-normal: var(--ct_text_main_general);
  --uni-button-field-text-color-text-main-disabled: var(--ct_text_main_general);
  --uni-button-field-text-color-text-main-hover: var(--ct_text_main_subtle);
  --uni-button-field-text-color-text-main-active: var(--ct_text_main_subtle);
  --uni-button-field-border-color-text-main-normal: transparent;
  --uni-button-field-border-color-text-main-disabled: transparent;
  --uni-button-field-border-color-text-main-hover: transparent;
  --uni-button-field-border-color-text-main-active: transparent;
  --uni-button-field-background-color-text-main-normal: transparent;
  --uni-button-field-background-color-text-main-disabled: transparent;
  --uni-button-field-background-color-text-main-hover: transparent;
  --uni-button-field-background-color-text-main-active: transparent;

  /* text > moderate */
  --uni-button-field-text-color-text-moderate-normal: var(--ct_text_moderate_general);
  --uni-button-field-text-color-text-moderate-disabled: var(--ct_text_moderate_general);
  --uni-button-field-text-color-text-moderate-hover: var(--ct_text_moderate_subtle);
  --uni-button-field-text-color-text-moderate-active: var(--ct_text_moderate_subtle);
  --uni-button-field-border-color-text-moderate-normal: transparent;
  --uni-button-field-border-color-text-moderate-disabled: transparent;
  --uni-button-field-border-color-text-moderate-hover: transparent;
  --uni-button-field-border-color-text-moderate-active: transparent;
  --uni-button-field-background-color-text-moderate-normal: transparent;
  --uni-button-field-background-color-text-moderate-disabled: transparent;
  --uni-button-field-background-color-text-moderate-hover: transparent;
  --uni-button-field-background-color-text-moderate-active: transparent;

  /* text > inverse */
  --uni-button-field-text-color-text-inverse-normal: var(--ct_text_inverse_general);
  --uni-button-field-text-color-text-inverse-disabled: var(--ct_text_inverse_general);
  --uni-button-field-text-color-text-inverse-hover: var(--ct_icon_inverse_subtle);
  --uni-button-field-text-color-text-inverse-active: var(--ct_icon_inverse_subtle);
  --uni-button-field-border-color-text-inverse-normal: transparent;
  --uni-button-field-border-color-text-inverse-disabled: transparent;
  --uni-button-field-border-color-text-inverse-hover: transparent;
  --uni-button-field-border-color-text-inverse-active: transparent;
  --uni-button-field-background-color-text-inverse-normal: transparent;
  --uni-button-field-background-color-text-inverse-disabled: transparent;
  --uni-button-field-background-color-text-inverse-hover: transparent;
  --uni-button-field-background-color-text-inverse-active: transparent;

  /* text > success */
  --uni-button-field-text-color-text-success-normal: var(--ct_text_success_general);
  --uni-button-field-text-color-text-success-disabled: var(--ct_text_success_general);
  --uni-button-field-text-color-text-success-hover: var(--ct_text_success_subtle);
  --uni-button-field-text-color-text-success-active: var(--ct_text_success_subtle);
  --uni-button-field-border-color-text-success-normal: transparent;
  --uni-button-field-border-color-text-success-disabled: transparent;
  --uni-button-field-border-color-text-success-hover: transparent;
  --uni-button-field-border-color-text-success-active: transparent;
  --uni-button-field-background-color-text-success-normal: transparent;
  --uni-button-field-background-color-text-success-disabled: transparent;
  --uni-button-field-background-color-text-success-hover: transparent;
  --uni-button-field-background-color-text-success-active: transparent;

  /* text > danger */
  --uni-button-field-text-color-text-danger-normal: var(--ct_text_danger_general);
  --uni-button-field-text-color-text-danger-disabled: var(--ct_text_danger_general);
  --uni-button-field-text-color-text-danger-hover: var(--ct_text_danger_subtle);
  --uni-button-field-text-color-text-danger-active: var(--ct_text_danger_subtle);
  --uni-button-field-border-color-text-danger-normal: transparent;
  --uni-button-field-border-color-text-danger-disabled: transparent;
  --uni-button-field-border-color-text-danger-hover: transparent;
  --uni-button-field-border-color-text-danger-active: transparent;
  --uni-button-field-background-color-text-danger-normal: transparent;
  --uni-button-field-background-color-text-danger-disabled: transparent;
  --uni-button-field-background-color-text-danger-hover: transparent;
  --uni-button-field-background-color-text-danger-active: transparent;
}
</style>
```

## Attributes

&lt;uni-button-field /> component exposes a curated set of attributes, enabling developers to dynamically adjust the user interface. This provides the flexibility to tailor the component’s appearance to seamlessly adapt to any given context.

- **size**

  The size attribute configures the overall dimensions of &lt;uni-button-field />. The component currently supports three standard options: `large`, `medium`, and `small`, defaulting to `medium`.

  ```html
  <uni-button-field
    size="medium"
  >
    <button
      slot="button"
      type="button"
    >
      button
    </button>
  </uni-button-field>
  ```

- **appearance**

  Currently, &lt;uni-button-field /> supports two distinct visual variants: `filled`, `outlined` and `text`. Developers can utilize the appearance attribute to configure the desired layout, which defaults to `filled`.

  ```html
  <uni-button-field
    appearance="filled"
  >
    <button
      slot="button"
      type="button"
    >
      button
    </button>
  </uni-button-field>
  ```

- **theme**
  
  Configures the visual theme of the &lt;uni-button-field /> to accommodate different styling requirements. It currently supports `main`, `moderate`, and `inverse` options. If the `appearance` attribute is set to `text`, `success` and `danger` options are additionally supported. The default value is `main`.

  ```html
  <uni-button-field
    theme="main"
  >
    <button
      slot="button"
      type="button"
    >
      button
    </button>
  </uni-button-field>
  ```

## Properties

| Property Name | Type | Description |
| ----------- | ----------- | ----------- |
| size | String | Getter / Setter size. `size` configures the overall dimensions of &lt;uni-button-field />. The component currently supports three standard options: `large`, `medium`, and `small`, defaulting to `medium`. |
| appearance| String | Getter / Setter appearance. `appearance` supports two distinct visual variants: `filled`, `outlined` and `text`. Developers can utilize the appearance to configure the desired layout, which defaults to `filled`. |
| theme| String | Getter / Setter theme. `theme` configures the visual theme of the &lt;uni-button-field /> to accommodate different styling requirements. It currently supports `main`, `moderate`, and `inverse` options. If the appearance is set to `text`, `success` and `danger` options are additionally supported. The default value is `main`. |

## Method
| Mathod Signature | Description |
| ----------- | ----------- |
| refresh() | Force a UI refresh on &lt;uni-button-field />. |

## Reference
- [&lt;uni-button-field /> demo](https://blog.lalacube.com/mei/webComponent_uni-button-field.html)
