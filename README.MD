Dynamic component creation using Lighting
This code involves

1) Winter 18 developer edition.

2) Dynamically creating the force:recordedit component and save button and wiring the save button to call the recordsave (event). Because I used force:recordedit component I now get to use recordsavesuccess.

<aura:handler name="onSaveSuccess" event="force:recordSaveSuccess" action="{!c.start}"/>
3) An event that can self handle itself : I created the custom event just to call the handleedit function by passing the selected record ID from the list of challenge records in my component. From here we can start creating the dynamic components as required.

Ref: https://developer.salesforce.com/docs/atlas.en-us.lightning.meta/lightning/events_component_fire.htm

4)Idea taken from this post (Aura Id of dynamic component is coming back as undefined) Aura:Id of dynamically created compontns cannot be accessed

5) A modal concept to mimic force:recordedit event (note I have created force:recordedit component and mimicked it to look like $A.get("e.force:editRecord") event)

http://www.sfdcmonkey.com/2017/04/15/modal-box-lightning-component-salesforce/

[![screenshot](https://github.com/Rao6308/Dynamiccomponentcreation/blob/master/src/)]