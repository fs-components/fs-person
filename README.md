# fs-person
<fs-person> web component is used to display a person

```html
<fs-person src="ABCD-123"></fs-person>
```

## Installation

```bash
$ npm install git+https://github.com/fs-components/fs-person.git
```

## Attributes

| Attribute      | Description |
| -------------- | ----------- |
| src            | The 8 character id of the person to display or a JSON string representing the person. If using the id, the person will be fetched from the server. |
| hide-life-span | Don't show the life span of the person in the output |
| hide-id        | Don't show the id of the person in the output |
| hide-gender    | Don't show the gender of the person in the output |
| full-life-span | Display the day and month of the life span |
| icon-size      | Size of the gender icon, `small` (default) or `medium` |
| portrait       | Show a large picture of the person if `portraitUrl` is set on the person |

## Person object structure

```js
var personObj = {
  "id": "KWN5-3PH",
  "name": "Huckleberry Finn",
  "gender": "MALE",
  "lifeSpan": "1832-1912",
  "fullLifeSpan": "23 February 1832 &ndash; 10 September 1912",
  "portraitUrl": "https://path/to/portrait.png"
}
```

## JavaScript API

```js
person = new fsPerson();

// you can either set the `src` to the id or use `setPerson()` and pass a object representing the person (so you don't have to JSON stringify it first).
person.src = 'ABCD-123';
// OR
person.setPerson(personObj);

document.body.appendChild(person);
```

## License
Copyright © 2014 by Intellectual Reserve, Inc. See the LICENSE file for license rights and limitations.