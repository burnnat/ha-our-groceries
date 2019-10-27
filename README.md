
# Home Assistant Our Groceries Sensor

Gets your our groceries lists.

---

[![GitHub Release][releases-shield]][releases]
[![License][license-shield]](LICENSE.md)

![Project Maintenance][maintenance-shield]
[![GitHub Activity][commits-shield]][commits]

## Installation

* Add the `ourgroceries` folder in your `custom_components` folder


## Options

| Name | Type | Requirement | `default` Description
| ---- | ---- | ------- | -----------
| username | string | **Required** | your our groceries username
| password | string | **Required** | your our groceries password


In your `configuration.yaml` file add:

```yaml
ourgroceries:
  username: !secret our_groceries_username
  password: !secret our_groceries_password
```

## Scriptable Services

### Add to list

Adds one or more items to a list.

| Name | Type | Requirement | `default` Description
| ---- | ---- | ------- | -----------
| list_id | string | **Required** | name or ID of the OurGroceries list
| items | string OR string[] | **Required** | item(s) to be added to the list

```yaml
service: ourgroceries.add_to_list
data:
  list_id: "My List"
  items:
    - "Milk"
    - "Eggs"
```

### Remove from list

Removes one or more items from a list.

| Name | Type | Requirement | `default` Description
| ---- | ---- | ------- | -----------
| list_id | string | **Required** | name or ID of the OurGroceries list
| items | string OR string[] | **Required** | item(s) to be removed from the list

```yaml
service: ourgroceries.remove_from_list
data:
  list_id: "My List"
  items:
    - "Milk"
    - "Eggs"
```

### Copy to list

Copies all items from one list to another.

| Name | Type | Requirement | `default` Description
| ---- | ---- | ------- | -----------
| list_id | string | **Required** | name or ID of the destination OurGroceries list
| from_list_id | string | **Required** | name or ID of the source OurGroceries list
| unique_only | boolean | Optional | `false` When true, only copies items that are not already on the destination list

```yaml
service: ourgroceries.remove_from_list
data:
  list_id: "My List"
  items:
    - "Milk"
    - "Eggs"
```

---

Enjoy my card? Help me out for a couple of :beers: or a :coffee:!

[![coffee](https://www.buymeacoffee.com/assets/img/custom_images/black_img.png)](https://www.buymeacoffee.com/JMISm06AD)


[commits-shield]: https://img.shields.io/github/commit-activity/y/ljmerza/ha-our-groceries.svg?style=for-the-badge
[commits]: https://github.com/ljmerza/ha-our-groceries/commits/master
[license-shield]: https://img.shields.io/github/license/ljmerza/ha-our-groceries.svg?style=for-the-badge
[maintenance-shield]: https://img.shields.io/badge/maintainer-Leonardo%20Merza%20%40ljmerza-blue.svg?style=for-the-badge
[releases-shield]: https://img.shields.io/github/release/ljmerza/ha-our-groceries.svg?style=for-the-badge
[releases]: https://github.com/ljmerza/ha-our-groceries/releases

