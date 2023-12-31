# Outfit management

## Outfit specification

### 1) Outfit name

- A string that names or describes the outfit
- Should be something that helps identify the combination
- A single line of text should suffice

### 2) Items list

- A collection of clothing items that make up the outfit
- Must be clothing items that exist in the user's wardrobe
- Items can be used in 0 or more outfits
- Items are selected based on wear were they are worn (identified as slots)
    - A headwear slot would show clothing items that can be worn on the head 
    - A torso slot would show items like shirts
- Slots can stack clothing items (so a sweater/flanel can be worn on top of a shirt)

### 3) Last worn

- The date an outfit was last worn
- Independent from any item's last worn date that is part of an outfit
- Wearing an outfit sets both the outfits last worn date and all associated item's last worn date

### 4) Availability

- Status of the outfits availability, depends on all associated items availability status 
- Outfit is available if all associated items are also available 
- Outfit is unavailable if any associated item is also not available

### 5) Image

- Derived from images of clothing items
- Compact view can use a carousel of items
- Detailed view can lay them out in a equipment menu style

### 6) Keywords/tags

- Similar to clothing item season/ocassion tags

### 7) Notes

- Any extra notes regarding an outfit
- Free form text

## Creating an outfit

- Outfits are created by dragging and dropping articles of clothing to appropriate slots
- Slots only accepts clothing that is worn on that part of the body
    1) Headwear 
    2) Torso 
    3) Legs
    4) Footwear
- Slots can be layered to express layering of clothing

![Create Outfit mockup](./figures/create-outfit-mockup.drawio.svg)

## Viewing an outfit

- Outfits can be viewed in a simple or detailed view 
- Detailed viewing lays out the outfits components which options to modify
- Simple views are carousels of the components and have a option to move to the detailed view

![Detailed Outfit View](./figures/view-outfit-mockup.drawio.svg)

## Updating an outfit

- Can be done from the detailed outfit view 
- Has similar feel to creating an outfit 
- Outfit user fields can be modified when saving changes
- Outfit revision message is optional to show details in revision history

![Modify Outfit](./figures/update-outfit-mockup.drawio.svg)

## Deleting an outfit

- Can be done from the detailed outfit view
- User must address confirmation message before deletion occurs

## Outfits as clothing items

- Outfits can show up on wardrobe clothing item listing
- They can be filtered and view just like regular clothing items
- The simplified view has a carousel of the components instead of a single image

