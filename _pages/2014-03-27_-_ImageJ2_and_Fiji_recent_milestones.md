---
autogenerated: true
title: 2014-03-27 - ImageJ2 and Fiji recent milestones
breadcrumb: 2014-03-27 - ImageJ2 and Fiji recent milestones
layout: page
categories: News,ImageJ2
description: test description
---

Every so often, it is good to look back at a project's progress over the past couple of years. [ImageJ2](ImageJ2 "wikilink") and [Fiji](Fiji "wikilink") have made great strides; what follows is a summary of some of the biggest achievements in recent history.

The most important feature of Fiji (the ImageJ distribution for the life sciences) is most certainly the [updater](updater "wikilink"). Two years ago, the updater source code was moved from Fiji into ImageJ2. Ever since, when you call Help\>Update Fiji, it is actually the ImageJ2 updater performing her duties. Rationale for the move: Fiji and ImageJ2 collaborate very closely (consistent with {% include person content='Schindelin' %} joining [LOCI](http://loci.wisc.edu/), the home of ImageJ2, in the fall of 2011), and it was obvious that ImageJ2 should play the role of generic image processing core while Fiji is dedicated to support the life sciences.

In the wake of the transition, many latent bugs were discovered and fixed, hardening the updater. It also allowed us to offer a very cool feature: personal update sites. Anybody with a Fiji wiki account (which in this case just serves as a convenient vehicle for ImageJ2) can register their personal update site onto which they can upload plugins and even macros. By adding the site to the {% include list-of-update-sites%}
 page, every ImageJ2 user (which includes all Fiji users; Fiji includes ImageJ2\!) can follow that update site by pressing the "Manage update sites" button in the updater and checking the appropriate site's checkbox. Just like the Fiji wiki and the other ImageJ2 web resources, the update sites are served from LOCI's web servers.

The list of update sites sees [continued growth](http://{% include servername%}
/index.php?title=List_of_update_sites&action=history), and we encourage their use e.g. for macros or plugins associated with publications. It simply enhances the impact of a paper if its methods are available at the users' fingertips.

Another really important component that made it from Fiji to ImageJ2 and was stabilized there is the [launcher](launcher "wikilink"). Its intent is to pre-configure the Java Virtual Machine "magically"; i.e., such that users need to configure as little as possible. Typically, no configuration is required, yet the appropriate amount of RAM is allocated, native libraries are found, Java3D support on MacOSX is up-to-date, all without having the user change a thing\! The launcher is indeed so useful that it was modified to be able to launch not only Fiji and ImageJ2, but bare-bones ImageJ 1.x as well.

The ImageJ2 project focuses on robustness—particularly important if you want to collaborate between more than one developer. That entails a [continuous integration server](http://jenkins.imagej.net/) whose sole purpose is to ensure that all the automated regression tests run on the newest source code revisions. The same server also makes sure that the [ImageJ launcher is built](http://jenkins.imagej.net/job/ImageJ-launcher/) for all the supported platforms: Windows (32/64 bit), MacOSX (32/64 bit, also PPC64) and Linux (32/64 bit). The same server also [builds installers for the latest ImageJ 1.x releases](http://jenkins.imagej.net/job/ImageJ1-releases/), whenever they come out.

While we obviously spend a lot of effort to support existing ImageJ 1.x users (for the same reason we try to keep ImageJ2's look and feel close to ImageJ 1.x's: continuity), ImageJ2 is not neglected\! For activity statistics, see the [ImageJ2 page on Ohloh](https://www.ohloh.net/p/imagej2). All of our source code is [developed openly and collaboratively](https://github.com/imagej), using the great open source resource GitHub.

In addition to supporting users on the ImageJ mailing list, a lot of developer support has been happening, too, resulting in powerful new plugins such as [TrackMate](TrackMate "wikilink")—an extensible tracking framework—and the [BigDataViewer](BigDataViewer "wikilink")—a multi-dimensional viewer for huge datasets.

Both are based on [ImgLib2](ImgLib2 "wikilink"), the data processing library serving as the core of ImageJ2. You see, whenever we found that a component we use in ImageJ2 would be useful to other projects, too, we put in that extra effort to make it so. You can use ImgLib2 without using ImageJ.

To put the importance of ImgLib2 into perspective: the industry-grade data mining environment [KNIME](KNIME "wikilink") started to [support image processing](http://tech.knime.org/community/image-processing) using exactly that library. This collaboration led to an amazing hackathon two weeks ago, the {% include github org='imagej ' repo='imagej-ops ' label='results of which ' %} you can be certain to hear about soon ;-).

Likewise, the file input/output layer of ImageJ2 was abstracted into a general-purpose library called [SCIFIO](SCIFIO "wikilink"). Not only can it be used outside ImageJ easily, developers can also provide file readers and writers without having to modify SCIFIO at all. [Bio-Formats](Bio-Formats "wikilink") is wrapped in SCIFIO so that you can read/write all those formats. New formats can be added with minimal effort. SCIFIO can even be used in C++ projects, as demonstrated by ITK support for SCIFIO \[{% include github org='scifio ' repo='scifio-itk-bridge ' label='1 ' %}, {% include github org='scifio ' repo='scifio-imageio ' label='2 ' %}\].

While our main focus with Fiji is to support life scientists to the point of enabling them to develop their own software (e.g., by providing [video tutorials how to start developing plugins from scratch](https://www.youtube.com/channel/UCOXCsWKZNGez9QOQMWw-Qww)), it is equally important to offer development interfaces attractive to computer vision experts. Providing all of Fiji and ImageJ in industry standard [Maven](Maven "wikilink") projects is one way we do that. The [MOSAIC group](http://mosaic.mpi-cbg.de/)'s update site may serve as an example of computer vision experts benefiting from these efforts.

Our focus on a flexible and powerful infrastructure pays off in a particularly nice way with the [OpenSPIM](http://openspim.org/) project: while the hardware had to be designed from scratch, the software is based on Fiji in form of Stephan Preibisch's [multi-angle reconstruction plugins](SPIM_Registration "wikilink"), and on [Micro-Manager](http://www.micro-manager.org/), served from—you guessed it—an update site. The OpenSPIM-specific extensions also benefit tremendously from ImgLib2, which facilitates the data processing necessary for the efficient operation of an OpenSPIM setup.

Looking forward, 2014 will be a big year for ImageJ2: we are targeting a stable release of the ImageJ2 core this summer, with a focus on continued compatibility and synergy with ImageJ 1.x development. We will continue to post updates on this site as well as on the [Mailing Lists](Mailing_Lists "wikilink") keeping the community apprised of developments in ImageJ2 and Fiji.

 