# ExpandableRecyclerView

Recycler view adapter that adds expandable / collapsible items

[![Expandable Recycler View](http://img.youtube.com/vi/2_E4ky0uXd8/0.jpg)](http://www.youtube.com/watch?v=2_E4ky0uXd8)

# Setup

Add this to your root build.gradle for all your projects

    allprojects {
      repositories {
            ...
            maven { url "https://jitpack.io" }
      }
    }

Then add this to your build.gradle dependencies for the project where you want to use it

    dependencies {
      ...
      compile 'com.github.grennis:ExpandableRecyclerView:0.9.3'
    }

# Usage

Define a recycler view adapter that derives from `ExpandableRecyclerAdapter`:

    public class PeopleAdapter extends ExpandableRecyclerAdapter<PeopleAdapter.PeopleListItem> {
      ...
    }

Define your items that derive from ExpandableRecyclerAdapter.ListItem

    public static class PeopleListItem extends ExpandableRecyclerAdapter.ListItem {
      public PeopleListItem(String group) {
        super(TYPE_HEADER);
        ...
      }
    }

Use the `TYPE_HEADER` for the expandable header items. Define other types as needed for your application.

You can set a mode to collapse other items when an item is opened:

    adapter.setMode(ExpandableRecyclerAdapter.MODE_ACCORDION);

For more information, browse the [Sample App](https://github.com/grennis/ExpandableRecyclerView/tree/master/app/src/main/java/com/innodroid/expandablerecyclerdemo).

