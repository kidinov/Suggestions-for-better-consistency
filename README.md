# Suggestions for better consistency

### Code convention

As well as 99% of app is written following [java code convention](http://www.oracle.com/technetwork/java/codeconventions-150003.pdf), I think we should follow it for consistency.

### Generic constants of color and dimens with generic names

We need mostly use generic constant for colors and dimens. For example:

    <color name="colorPrimary">#F55B5F</color>
    <color name="colorPrimaryDark">#f44348</color>
    <color name="colorAccent">#ffffff</color>

    <color name="gray0">#f9f9f9</color>
    <color name="gray1">#f2f2f2</color>
    <color name="gray2">#e0e0e0</color>
    <color name="gray3">#b2b2b2</color>
    <color name="gray4">#666666</color>
    <color name="gray5">#494949</color>
    
**for colors**

    <!-- Default screen margins, per the Android Design guidelines. -->
    <dimen name="default_margin">16dp</dimen>
    <dimen name="default_small_margin">8dp</dimen>
    
    <!--Font sizes-->
    <dimen name="header_font_size">26sp</dimen>
    <dimen name="large_font_size">20sp</dimen>
    <dimen name="middle_font_size">18sp</dimen>
    <dimen name="big_small_font_size">16sp</dimen>
    <dimen name="small_font_size">14sp</dimen>
    
**for dimens**

In case if some specific dimen or color needed, just use it within layout, without creating a link to dimens/colors file.

### Units

Use **SP** instead of **DP** for text, but in places where hight must be set as specific value, use DP instead. Don't use **DIP**. Don't use **fill_parrent**.

### Resources naming convention

* **Strings**: *\<screen_name\>\_\<description\>*, for example: **profile_age** / **buy_now_description**. With that naming convention, there is no need to split strings file in many files. Strings can be just grouped toogether in one file. Generic names can be named just with description.
* **Layout/Menu files**: *\<screen_name\>\_\<type\>*, for example: **profile_fragment** / **buy_now_list_item**
* **View ids**: *\<screen_name\>\_\<type\>\_\<description\>*, for example: **profile_image_person** / **buy_now_text_sex_value**
* **Drawables**: *\<type\>\_\<description\>\_\<color\>\_\<size\>*, for example: **ic_add_manual_measurement_white_24dp.
* **Files**: *\<screen_name\>\_\<type\>*, for example: **ProfileFragment** / **ProfileListAdapter**
