---
title: Lista de reproducción avanzada
description: Lista de reproducción avanzada
ms.assetid: 3f27562f-bc3b-4b7f-a83b-78317d3ad612
keywords:
- Windows Listas de reproducción de metarchivo multimedia, ejemplos de listas de reproducción
- listas de reproducción, ejemplos de listas de reproducción
- listas de reproducción de metarchivo, ejemplos de listas de reproducción
- Windows Listas de reproducción de metarchivo multimedia, listas de reproducción de ejemplo
- listas de reproducción, listas de reproducción de ejemplo
- listas de reproducción de metarchivo, listas de reproducción de ejemplo
- Windows Listas de reproducción de metarchivo multimedia, listas de reproducción de ejemplo
- listas de reproducción, listas de reproducción de ejemplo
- listas de reproducción de metarchivo, listas de reproducción de ejemplo
- Windows Listas de reproducción de metarchivo multimedia, ejemplo de código
- listas de reproducción, ejemplo de código
- listas de reproducción de metarchivo, ejemplo de código
- Windows Listas de reproducción de metarchivo multimedia, ejemplo de lista de reproducción avanzada
- listas de reproducción, ejemplo de lista de reproducción avanzada
- listas de reproducción de metarchivo, ejemplo de lista de reproducción avanzada
- Reproductor de Windows Media,ejemplos de lista de reproducción
- Reproductor de Windows Media listas de reproducción de ejemplo
- Reproductor de Windows Media,listas de reproducción de ejemplo
- Reproductor de Windows Media de lista de reproducción avanzada
- ejemplos de lista de reproducción
- listas de reproducción de ejemplo
- listas de reproducción de ejemplo
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6573d5bef05c8af943368a12d03677526a9783915d6915b6cc5f1516bc9942f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583262"
---
# <a name="an-advanced-playlist"></a>Lista de reproducción avanzada

En el ejemplo de lista de reproducción siguiente se muestra cómo usar un conjunto más completo de elementos de lista de reproducción. Al escribir su propio código, deberá cambiar todas las direcciones URL y los nombres de archivo por nombres de archivo válidos que sean accesibles para su Reproductor de Windows Media.

Código de ejemplo


``` XML
<ASX version = "3.0">
    <TITLE>Advanced Playlist Demo</TITLE>
    <ABSTRACT>More Information at this website</ABSTRACT>
    <MOREINFO HREF="https://www.microsoft.com/windows/windowsmedia" />
    <BANNER HREF = "..\samples\home.gif">
        <ABSTRACT>MSN website</ABSTRACT>
        <MOREINFO HREF = "https://www.msn.com" />
    </BANNER>
    <PARAM name="track" value="1"/>
    <ENTRY ClientSkip="no">
        <BANNER HREF = "..\sample\contact.gif">
            <ABSTRACT>Visit Our website</ABSTRACT>
            <MOREINFO HREF = "https://www.msn.com" />
        </BANNER>
        <MOREINFO HREF = "https://www.msn.com" />
        <!-- This is the ToolTip text for Title/Author/Copyright text -->
        <ABSTRACT>Visit the YourImage website</ABSTRACT>
        <TITLE>The first entry in an advanced playlist</TITLE>
        <AUTHOR>YourImage</AUTHOR>
        <COPYRIGHT>(c)2000 YourImage</COPYRIGHT>
        <!-- This is a comment.  Change the following path to point to 
            your Windows Media file -->
         <REF HREF = "..\media\laure.wma" />
    </ENTRY>

    <ENTRY>
        <TITLE>The second entry in the advanced playlist</TITLE>
        <AUTHOR>Microsoft Corporation</AUTHOR>
        <COPYRIGHT>(c)2000 Microsoft Corporation</COPYRIGHT>
        <!-- This is the ToolTip text for Title text -->
        <ABSTRACT>This is where you can include your tool tips</ABSTRACT>
        <!-- This is a comment.  Change the following path to point to 
            your Windows Media file -->
        <REF HREF = "..\media\mellow.wma" />
    </ENTRY>
</ASX>

```



En la tabla siguiente se describe la lista de reproducción avanzada anterior.



| Línea                                                                                            | Descripción                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<ASX version = "3.0">`                                                                     | El [elemento ASX](asx-element.md) identifica para el cliente (Reproductor de Windows Media) que se trata de una lista de reproducción Windows metarchivo multimedia. El **atributo version** especifica el número de versión de los elementos del metarchivo.                                                                                                                    |
| `<TITLE>Advanced Playlist Demo</TITLE>`                                               | El [elemento TITLE](title-element--metafile.md) identifica el título de la lista de reproducción como un todo. Reproductor de Windows Media muestra estos metadatos como título para mostrar.                                                                                                                                                                        |
| `<ABSTRACT>More Information at this Web Site< /ABSTRACT>`                             | El [elemento ABSTRACT](abstract-element.md) proporciona la información sobre herramientas para el título de presentación.                                                                                                                                                                                                                                                   |
| `<MOREINFO HREF ="https://www.microsoft.com/windows/windowsmedia" />`                        | El [elemento MOREINFO](moreinfo-element.md) vincula el título de presentación a una dirección URL. Al pausar el puntero del mouse sobre el título de presentación, se accede a la información sobre herramientas, si se define. Al seleccionar el título de la presentación, se abrirá la dirección URL designada.                                                                                                                |
| `<BANNER HREF = "..\\samples\\home.gif">`                                                   | El [elemento BANNER](banner-element.md) crea un banner de publicidad en Reproductor de Windows Media. El **atributo HREF** especifica el gráfico de banner (que debe tener 194 píxeles de ancho por 32 píxeles de alto).                                                                                                                                  |
| `<ABSTRACT>MSN website</ABSTRACT>`                                                    | El [elemento ABSTRACT](abstract-element.md) proporciona la información sobre herramientas para **banner.**                                                                                                                                                                                                                                                   |
| `<MOREINFO HREF = "https://www.msn.com" </ABSTRACT>`                                      | El [elemento MOREINFO](moreinfo-element.md) vincula el **gráfico BANNER** a una dirección URL. Si se mantiene el puntero del mouse sobre **el BANNER,** se accede a una información sobre herramientas, si se define. Al seleccionar **banner,** se abrirá la dirección URL designada.                                                                                                                |
| <PARAM name = "track" value="1"/>                                                         | El [elemento PARAM](param-element.md) define un parámetro personalizado. El **atributo name** define el nombre del parámetro personalizado como "track". El **atributo** value define el valor de "track" como "1".                                                                                                                          |
| `</BANNER>`                                                                                 | Cierra el elemento **BANNER**                                                                                                                                                                                                                                                                                                           |
| `<ENTRY ClientSkip="no">`                                                                   | Comienza el bloque de elementos [ENTRY.](entry-element.md) Este elemento define un clip en una lista de reproducción especificando un vínculo en el **elemento REF.** Establecer **ClientSkip en** "no" significa que el usuario no puede avanzar rápidamente ni saltar al siguiente clip.                                                                                             |
| `<BANNER HREF = "..\\samples\\contact.gif">`                                                | Crea un banner de publicidad. HREF **es** el gráfico de banner (194 x 32 píxeles).                                                                                                                                                                                                                                                      |
| `<ABSTRACT>Visit Our website< /ABSTRACT>`                                             | Proporciona la información sobre herramientas para el banner.                                                                                                                                                                                                                                                                                                    |
| `<MOREINFO HREF = "https://www.msn.com" />`                                                  | Proporciona un vínculo a la dirección URL del banner. Al seleccionar el banner se conecta a la dirección URL.                                                                                                                                                                                                                                                    |
| `</BANNER>`                                                                                 | Cierra el elemento **BANNER**                                                                                                                                                                                                                                                                                                           |
| `<MOREINFO HREF = "https://www.msn.com" />`                                                  | Proporciona un vínculo a la dirección URL del texto del título **del** clip.                                                                                                                                                                                                                                                                                 |
| `<!--This is the ToolTip text for the Title text -->`                                       | Comentario. [Los](comments.md) comentarios solo son visibles cuando se ve el código.                                                                                                                                                                                                                                                        |
| `<Abstract>Visit the YourImage website</abstract>`                                    | Proporciona la información sobre herramientas para el texto **del título del** clip.                                                                                                                                                                                                                                                                                       |
| `<TITLE>The first entry in an advanced playlist</TITLE>`                              | Identifica el título del clip. Es el clip **TITLE** porque está anidado dentro de un **elemento ENTRY.** Reproductor de Windows Media muestra estos metadatos como título del clip.                                                                                                                                                             |
| `<AUTHOR>YourImage</AUTHOR>`                                                          | Identifica el autor del clip multimedia. Estos metadatos se muestran como el clip **AUTHOR** Reproductor de Windows Media.                                                                                                                                                                                                                     |
| `<COPYRIGHT>(c)2000 YourImage</COPYRIGHT>`                                            | El [elemento COPYRIGHT](copyright-element.md) especifica los derechos de autor asociados al clip multimedia. Reproductor de Windows Media muestra estos metadatos como el clip COPYRIGHT.                                                                                                                                                              |
| `<!-- This is a comment. Change the following path to point to your Windows Media file -->` | Comentario, en el mismo formato que los **comentarios XML.**                                                                                                                                                                                                                                                                                      |
| `<REF HREF = "..\\media\\laure.wma" />`                                                     | Dirección URL del contenido multimedia. El [elemento REF](ref-element.md) identifica la línea como un puntero al contenido multimedia. El **atributo HREF** es la dirección URL del archivo. Observe el uso del cierre de tipo XML del elemento , "/>" en lugar de " &lt; /REF &gt; ". Dado que este elemento no tiene elementos secundarios, se cierra a sí mismo.<br/> |
| `</ENTRY>`                                                                                  | Especifica el final del del primer **elemento ENTRY.**                                                                                                                                                                                                                                                                                |
| `<ENTRY>`                                                                                   | Comienza el segundo **elemento ENTRY.**                                                                                                                                                                                                                                                                                                    |
| `<TITLE>The second Entry in the advanced playlist</TITLE>`                            | Identifica el título del segundo clip.                                                                                                                                                                                                                                                                                                |
| `<AUTHOR>Microsoft Corporation</AUTHOR>`                                              | Identifica el autor del segundo clip multimedia.                                                                                                                                                                                                                                                                                         |
| `<!--This is the ToolTip text for the Title/Author/Copyright text -->`                      | Comentario. Solo estará visible cuando se vea el código.                                                                                                                                                                                                                                                                             |
| `<ABSTRACT>This is where you can include your tool tips</ABSTRACT>`                   | Este es el texto de información sobre herramientas para el texto **TITLE** del clip.                                                                                                                                                                                                                                                                            |
| `<!-- This is a comment. Change the following path to point to your Windows Media file -->` | Comentario. Solo estará visible cuando se vea el código.                                                                                                                                                                                                                                                                             |
| `<REF HREF = ..\\media\\mellow.wma" />`                                                     | Identifica la línea como un puntero al contenido multimedia. El **atributo HREF** es la dirección URL del archivo.                                                                                                                                                                                                                                       |
| `</ENTRY>`                                                                                  | Especifica el final del segundo **elemento ENTRY.**                                                                                                                                                                                                                                                                                      |
| `</ASX>`                                                                                    | Especifica el final de la lista de reproducción.                                                                                                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de listas de reproducción de metarchivo**](creating-metafile-playlists.md)
</dt> <dt>

[**Listas de reproducción de ejemplo**](example-playlists.md)
</dt> <dt>

[**Listas de reproducción de metarchivo**](metafile-playlists.md)
</dt> <dt>

[**Windows Referencia de elementos de metarchivo multimedia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Guía de metarchivo multimedia**](windows-media-metafile-guide.md)
</dt> </dl>

 

 





