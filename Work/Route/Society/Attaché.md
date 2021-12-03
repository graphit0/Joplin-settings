# tasks
Claim space back expansion: research tools, make screenshots

Separate advanced use from simple publishing


Hello 

This is a post listing few possible use cases for this plugin I've been procrastinating to write for some time, yet here it is. Please note that I'm aware of other approaches and software achieving the same or better result. This post is just a catalogue of ideas how this plugin could be used.
# Humorous preamble: Marrying filesystem after years of one night stands

![dangerous_proposal_by_naolito_d4r95s1.jpg](../../../_resources/dangerous_proposal_by_naolito_d4r95s1.jpg)

Let's face it, attachments in our notes are out of date. In fact, we know that and don't even care keep them "fresh". We know that editing an attachment in a note is cumbersome and doesn't quite work on mobile. 

We accepted long ago that nothing lasts forever and quietly gave up on long term relationships between our files and notes. They meet regularly, exchange a few nice sentences and go on with their life. 

Each of them has got its own organization and rituals. What can you do if they are so different? 

They've been growing apart for so long and each of them even got a lover. Notes flirt here and there with these pesky website clippings, and filesystem is always chatting with that chad dude calling himself a Cloud (yet we all know that he's just a bit distant douchebag  filesystem). Maybe they just not destined to be together? 

Well, introducing Polygamy! ***cough-cough***, oh, that's not right, um wrong meeting... What the heck... Jeffrey! I asked you to move this talk with my wife to another time! I don't care that she left me! Gosh, those amateurs...

I mean... um... Introducing Resource Replacement! 👏👏👏

With resource replacement we can tie ~~those bastards in the basement~~ filesystem and notes while allowing them to keep independent structure.



# Use cases
> Attachments ain't just files, they are idea illustrations and good ideas are always a subject of evolution

## Claim space back

So far, the main usage of this plugin - to streamline the process of photos quality reduction freeing up space on a cloud storage

It works like that:

    You install the plugin
    You write down the path of the folder in the plugin settings where you will save your new reduced in size files
    You copy your Joplin files in resource directory to the path you wrote in the settings
    You use some quality/size reducing tool to all file in that copied folder (could be done with images in bulk via RawTherapee or lightroom)
    You click "Replace resources" from tool menu in Joplin
    Done, your new files are now in Joplin and will be synced with the cloud.

The advantages of this method:

    Works in bulk of any size
    Works with any file format
    Once setup you can run it multiple times: periodically (every sync) or until you get the result you need
    There's less risk messing data due to user error


## Above and beyond
![649f7e974e9ce00f2d0d9faca57d40c2.png](../../../_resources/649f7e974e9ce00f2d0d9faca57d40c2.png)
```mermaid
flowchart TD
	subgraph model
	db[(database)] -- periodical -.-> dump --> postprocessing 
	end

	subgraph Joplin
	postprocessing -- syncthing --> rr(resource replacement) --- attachments
	postprocessing --> hotfolder -- new note --> attachments 
	end

	subgraph public
	attachments --> publish
	publish{publishing to wider audience} --> pdf(to .pdf)
	publish --> email(send it as email)
	publish --> blog(export as blog)
	publish --> domain( personal website)
	end
```

### Other personal use

Updating attachments in bulk in already existing structure


#### Long standing thumbnail
Keep an updating map of your trips
![d42fcfdd4b058c67b1bdfd2ddf0dc420.png](../../../_resources/d42fcfdd4b058c67b1bdfd2ddf0dc420.png)
Bonus:
- have a decorated note of your life milestones
- bring up a seasonal change to your notes with 

#### Portfolio of your work
Create and publish to your domain, test illustrations and work assets for the best result
![a4c643e93a8753ece83cfcd98dc1afbf.png](../../../_resources/a4c643e93a8753ece83cfcd98dc1afbf.png)
Bonus:
- Classified advertisement: paste and update the images highlighting specific features of the product

- Tableu exports and rich charts: Update professional charts when data change, keep in depth explanations

#### QR code updates when link changes
![0e8115793610dea10a515d05f2a985c8.png](../../../_resources/0e8115793610dea10a515d05f2a985c8.png)

#### Technical documentation hosted on GitHub pages
Easily update all the assets in bulk in existing structure when UI, requirements or mood of your boss changes. 
Get inspired to craft rich(er) documents with more illustrative or runnable assets. 
![tech-doc.png](../../../_resources/tech-doc.png)
Bonus:
- Article / presentation mockups: create a mockup of the document, split the visualization and text writing work among different people.

- Editorial work: split a document by chapters and attach the combined rendered product to every chapter

#### Public event organizer
Announce tickets sold, sits taken, places booked, neighbourhood parking spots available on a rendered printable document
![c6739f2b439ab439ba0e29231a8bbe3e.png](../../../_resources/c6739f2b439ab439ba0e29231a8bbe3e.png)
![ef8d59a5a38143bbf172d32e271b2576.png](../../../_resources/ef8d59a5a38143bbf172d32e271b2576.png)

##### Advanced use



#### Document preview (WIP)
Attach a file preview on save 
![5986c19de71d8990f1307d22507701a1.png](../../../_resources/5986c19de71d8990f1307d22507701a1.png)
#### Advanced: Mobile drawing update
Be able to save updates of your drawing on mobile

![Screenshot_20211201_131821_net.cozic.joplin.jpg](../../../_resources/Screenshot_20211201_131821_net.cozic.joplin.jpg)

#### Advanced: Combined dashboard
Compile a custom dashboard from many different informational sources with page screenshots and script automation

Basic use can include setting up Google docs based workflow: Forms > Spreadsheets > Charts or pivots > publishing a link to image > script to save the image in resource replacement folder
![ffcfddd65c15babbefcac6f5c8a7033c.png](../../../_resources/ffcfddd65c15babbefcac6f5c8a7033c.png)


## Professional use: intranet projects, open source sharepoint

Discussion board and proposal review (meeting minutes): Multiple pages with a single asset, focusing on different perspectives. Application architecture review, budget and analysis review

Cafe menu, coffee shop week's special

Placeholder for company policies: Guidelines for quality, corporate style sheet, getting started for new employee

Project overview: Attendance, vacation, project scheduling

Joplin as HR portal: An employee profile linked with other sources of information: payroll database, vacation schedule, permission map, a role in organisational structure and shift charts

Online course catalogue: every note is a lesson. The files are things subjected to change like examples of code executed on live data.

Decks for employee accessible technical documentation: network, vpn configuration, periodical research findings updates

Corporate knowledge base: metadatabase, tables description, actual table dump sample you can preview and query

Reporting landing page: collection of files summarizing a time period

***
## Epics

Right click replace the resource

File picker for the folder. Either dialogue to set it up or default folder

Preview of saved files. Filed attached automatically opened and the screenshot is saved.

Joplin repository where every file is well documented. Sync with GitHub and other file storage. Download the remote resource as local and update on change.

Dashboard with the latest results

## Features

Keeping the new file in the original folder.

Indication what resources are tracked.

Create resources for future replacement. Templates for new tightly linked files could be created.

Software that would keep a link with other systems: deciding if file should be fetched, fetch a file. Rclone, syncthing.

Replace the text as well.

 

 ----- 
 HackMD Note URL: https://hackmd.io/50rVKAt2T0OGLaecFR-XYw