## Source files, data, and assets for generating public presentations.

## Organisation

The content is organized around the idea that one has a collection of
Slides, from which one picks and chooses an ordered subset to compose
a presentation. Each Slide is a largely independent unit of Content that
contains visual, numerical, and textual information. Slides are largely
shared across multiple presentations, but may be updated when new
information becomes available. While each slide contains its own content,
they all should share a common set of brand assets, themes, and layouts to
give a consistent look to the overall presentation.

All content is organised under a version control system, with branches and
clear release tags to mark a snapshot at the moment of publication.
Therefore, old versions of slides are not kept in the active collection,
but may be viewed by checking out older versions of the source tree.
Further, alternative messages and presentations are captured on distinct
branches of the source tree.

Slides are published by rendering them as a static HTML website or to PDF
format. These documents can then be distributed by email, uploaded to
a CRM, or hosted on a static file server or CDN.

## Slides

While there are many different types of slides, they all form a basic type
hierarchy. Each slide will have a title, a core headline/subtitle, a piece
of primary visual content, and speakers notes. Each slide is analogous to
a section of a document, composing a Figure, caption, section header, and
text. Jade, the underlying template language, allows for sophisticated
inheritance of common attributes of slides.

Each slide should be a largely autonomous piece of content, and contain
its own source data, text, analytical code, etc. Core dependencies should
not be contained within or exported by individual slides, but reside
higher up in the file hierarchy. 

Images and text will largely be local to their slides unless part of core
brand assets. Javascript, SVG symbols, and layout partials should be kept
in centralized core libraries **if** used more than once. 
