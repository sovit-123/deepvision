## Welcome to Deep Vision 
Here, you will find everything related to computer vision, machine learning, and deep learning.

title: useful-markdown-card
cards:

  # Some controlls for demo purposes
  - type: vertical-stack
    cards:

    - type: entities
      entities:
        - input_number.x_pos

    - type: horizontal-stack
      cards:
        - type: entity-button
          entity: light.bed_light
          name: " "
          tap_action: {action: toggle}

        - type: entity-button
          entity: sun.sun
          icon: mdi:numeric-1
          name: " "
          tap_action: {action: navigate, navigation_path: "#subpage1"}

    - type: horizontal-stack
      cards:
        - type: entity-button
          entity: sun.sun
          icon: mdi:numeric-2
          name: " "
          tap_action: {action: navigate, navigation_path: "#subpage2"}

        - type: entity-button
          entity: sun.sun
          icon: mdi:numeric-3
          name: " "
          tap_action: {action: navigate, navigation_path: "#subpage3"}


  # A default markdown card for comparison
  - type: markdown
    title: Default markdown card
    content: &markdown |
      # Title
      ## Subtitle
      - list
      - items

      [A link](https://google.com)

      [[ light.bed_light.state ]]
      [[ light.bed_light ]]
      [[ light.bed_light.attributes.friendly_name ]]

      Username: [[ {user} ]] Browser ID: [[ {browser} ]]
      Current URL hash: [[ {hash} ]]

      [[ if(light.bed_light == "on", "The lights are on", "It's dark") ]]
      [[ if(input_number.x_pos <= 30, "small", if(input_number.x_pos <= 70, "Medium", "LARGE")) ]]

  # And finally, the useful-markdown-card with a copy of the same content
  - type: custom:useful-markdown-card
    title: Useful markdown card
    content: *markdown
