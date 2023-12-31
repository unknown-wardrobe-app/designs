# Clothing item management

## Specification methods

### 1) Item name

- Can be a regular text input field on a form.
- Name uniqueness is not required, but would be nice to show similarly named items if available.
- **Required** for all clothing items

### 2) Category

- Refers to the type of an clothing item
- A dropdown menu will help ensure clothing items are grouped into a finite number of groups
    - Tops
    - Bottoms
    - Dresses
    - Footwear (socks/shoes)
    - Sleepwear
- May want to allow user's to specify their own
    - Can sort be done through the tags/keyword system

### 3) Color

- Dropdown of color presets
- Color refinement available through a color picker widget
- *Nice to have*: determine the color based on image of clothing 

### 4) Brand

- Simple regular text input field
- Suggest existing brand names if available before creating a new one (with dropdown?)

### 5) Size

- Simple text field
- User should just use what is on the item's tag 

### 6) Fabric

- Simple text field
- User should just use what is on the item's tag

### 7) Purchase date

- Date picker widget of some sort

### 8) Price

- Text field restricted to valid floating number
- Need to consider localization

### 9) Wear frequency

- A datepicker widget of some sort
- QoL: a "wear today" button of some sort to quickly indicate last worn date is *today*

### 10) Occasions

- A select all that apply for a clothing item
- May be a section of tags 

### 11) Seasons

- Also select all that apply 
- May be a section of tags

### 12) Image 

- Provided as a image file (obviously)
- *Nice to have*: procedurally generate an image based on other provided attributes
    - Makes image optional, as it would be helpful for visualizing outfits
    
### 13) Notes

- Free form text for any additional user provided information

### 14) Availability

- Dropdown of possible clothing states

## Creating a clothing item

### Required information 

- Item name 
- Item category
- Item last worn date
- Item image *or* item color
- Item availability state

### Additional information

- Item brand
- Item purchase date
- Item price
- Item fabric
- Item size
- Color
- Occasions tags
- Seasonal tags
- Aditional notes

### Wireframe

![Create Item Mockup](./figures/create-item-mockup.drawio.svg)

## Viewing a clothing item

### Searchability

- By name (default)
- By tags
    - `tagkey:tagvalue` (category:tops)
    - Can be multiple tags listed
    - Any known attribute can be a tag key
    - Tag modifiers
        - is: exact match: `name:is:red shirt` searches for a clothing item that is named "red shirt"
        - like: fuzzy match: `name:like:red` search for clothing items that contain the string "red"
        - not: opposing match: `name:not:like:red` searches for clothing items that **do not** contain the string "red"
        - absence of modifier defaults to fuzzy

### Results

- Wardrobe inventory listed alphabetically by name (default view)
- Search bar filters for desired items
- Overview
    - Picture
    - Name
    - Last worn
    - Availability
- Detailed (Overview +)
    - Any other details provided

### Wireframes

![View Item Mockup](./figures/view-item-mockup.drawio.svg)

## Updating a clothing item

### Quick actions

- Wear today: sets the last worn date to today (only available if status if "Ready")
- Washed today: sets the status of the item to "Ready" (only availabe is item is awaiting cleaning)

### Revise item record

- Floating action button to edit an existing clothing record from its **detailed view**
- All fields shown, even if not defined
- Image is updated by tapping/clicking on current image

### Wireframes

![Update Item Mockup](./figures/update-item-mockup.drawio.svg)

## Deleting a clothing item

1) Tap/click on the red "delete" button in the **detailed view**
2) Confirm deletion if it is OK to delete (Item cannot be deleted if part of an outfit)

![Delete Item Mockup](./figures/delete-item-mockup.drawio.svg)

## Clothing item FSM

![Clothing State Machine](./figures/clothing-state.drawio.svg)
