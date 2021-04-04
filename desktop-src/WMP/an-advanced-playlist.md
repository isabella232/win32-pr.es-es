---
title: Una lista de reproducción avanzada
description: Una lista de reproducción avanzada
ms.assetid: 3f27562f-bc3b-4b7f-a83b-78317d3ad612
keywords:
- Listas de reproducción de metarchivos de Windows Media, ejemplos de listas de reproducción
- listas de reproducción, ejemplos de listas de reproducción
- listas de reproducción de metarchivos, ejemplos de listas de reproducción
- Listas de reproducción de metarchivos de Windows Media, listas de reproducción de ejemplo
- listas de reproducción, listas de reproducción de ejemplo
- listas de reproducción de metarchivos, listas de reproducción de ejemplo
- Listas de reproducción de metarchivos de Windows Media, listas de reproducción de ejemplo
- listas de reproducción, listas de reproducción de ejemplo
- listas de reproducción de metarchivos, listas de reproducción de ejemplo
- Listas de reproducción de metarchivos de Windows Media, ejemplo de código
- listas de reproducción, ejemplo de código
- listas de reproducción de metarchivos, ejemplo de código
- Listas de reproducción de metarchivos de Windows Media, ejemplo de lista de reproducción avanzada
- listas de reproducción, ejemplo de lista de reproducción avanzada
- listas de reproducción de metarchivos, ejemplo de lista de reproducción avanzada
- Media Player de Windows, ejemplos de lista de reproducción
- Windows Media Player, listas de reproducción de ejemplo
- Windows Media Player, listas de reproducción de ejemplo
- Windows Media Player, ejemplo de lista de reproducción avanzada
- ejemplos de listas de reproducción
- listas de reproducción de ejemplo
- listas de reproducción de ejemplo
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f52251fedb13d41be5c94706bee4460c3f13c1e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075512"
---
# <a name="an-advanced-playlist"></a>Una lista de reproducción avanzada

En el siguiente ejemplo de lista de reproducción se muestra cómo usar un conjunto más completo de elementos de lista de reproducción. Al escribir su propio código, tendrá que cambiar todas las direcciones URL y los nombres de archivo a nombres de archivo válidos a los que se pueda tener acceso desde el Media Player de Windows.

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
| `<ASX version = "3.0">`                                                                     | El elemento [ASX](asx-element.md) identifica el cliente (Windows Media Player) que es una lista de reproducción de metarchivo de Windows Media. El atributo **version** especifica el número de versión de los elementos de metarchivo.                                                                                                                    |
| `<TITLE>Advanced Playlist Demo</TITLE>`                                               | El elemento [title](title-element--metafile.md) identifica el título de la lista de reproducción en su conjunto. Windows Media Player muestra estos metadatos como el título de la muestra.                                                                                                                                                                        |
| `<ABSTRACT>More Information at this Web Site< /ABSTRACT>`                             | El elemento [abstracto](abstract-element.md) proporciona la información sobre herramientas para el título de presentación.                                                                                                                                                                                                                                                   |
| `<MOREINFO HREF ="https://www.microsoft.com/windows/windowsmedia" />`                        | El elemento [MOREINFO](moreinfo-element.md) vincula el título de la presentación a una dirección URL. Al pausar el puntero del mouse sobre el título Mostrar, se obtiene acceso a la información sobre herramientas, si se define. Al seleccionar el título de la presentación, se abre la dirección URL designada.                                                                                                                |
| `<BANNER HREF = "..\\samples\\home.gif">`                                                   | El elemento [banner](banner-element.md) crea un Banner publicitario en Windows Media Player. El atributo **href** especifica el gráfico de banner (que debe tener de 194 píxeles de ancho y 32 píxeles de alto).                                                                                                                                  |
| `<ABSTRACT>MSN website</ABSTRACT>`                                                    | El elemento [abstracto](abstract-element.md) proporciona la información sobre herramientas para el **banner**.                                                                                                                                                                                                                                                   |
| `<MOREINFO HREF = "https://www.msn.com" </ABSTRACT>`                                      | El elemento [MOREINFO](moreinfo-element.md) vincula el gráfico de **banner** a una dirección URL. Al mantener el puntero del mouse sobre el **banner** se accede a una información sobre herramientas, si se define. Al seleccionar el **banner** se abrirá la dirección URL designada.                                                                                                                |
| <PARAM name = "track" value="1"/>                                                         | El elemento [param](param-element.md) define un parámetro personalizado. El atributo **Name** define el nombre del parámetro personalizado como "Track". El atributo **Value** define el valor de "Track" para que sea "1".                                                                                                                          |
| `</BANNER>`                                                                                 | Cierra el elemento **banner**                                                                                                                                                                                                                                                                                                           |
| `<ENTRY ClientSkip="no">`                                                                   | Comienza el bloque de elementos de [entrada](entry-element.md) . Este elemento define un clip en una lista de reproducción mediante la especificación de un vínculo en el elemento **ref** . Establecer **ClientSkip** en "no" significa que el usuario no puede avanzar o saltar rápidamente al siguiente clip                                                                                             |
| `<BANNER HREF = "..\\samples\\contact.gif">`                                                | Crea un Banner publicitario. El **href** es el gráfico de banner (194x32 píxeles).                                                                                                                                                                                                                                                      |
| `<ABSTRACT>Visit Our website< /ABSTRACT>`                                             | Proporciona la información sobre herramientas para el banner.                                                                                                                                                                                                                                                                                                    |
| `<MOREINFO HREF = "https://www.msn.com" />`                                                  | Proporciona un vínculo a la dirección URL del banner. Al seleccionar el banner se conecta a la dirección URL.                                                                                                                                                                                                                                                    |
| `</BANNER>`                                                                                 | Cierra el elemento **banner**                                                                                                                                                                                                                                                                                                           |
| `<MOREINFO HREF = "https://www.msn.com" />`                                                  | Proporciona un vínculo a la dirección URL del texto del **título** del clip.                                                                                                                                                                                                                                                                                 |
| `<!--This is the ToolTip text for the Title text -->`                                       | Comentario. Los [comentarios](comments.md) solo están visibles cuando se ve el código.                                                                                                                                                                                                                                                        |
| `<Abstract>Visit the YourImage website</abstract>`                                    | Proporciona la información sobre herramientas para el texto del **título** del clip.                                                                                                                                                                                                                                                                                       |
| `<TITLE>The first entry in an advanced playlist</TITLE>`                              | Identifica el título del clip. Es el **título** del clip porque está anidado dentro de un elemento de **entrada** . Windows Media Player muestra estos metadatos como el título del clip.                                                                                                                                                             |
| `<AUTHOR>YourImage</AUTHOR>`                                                          | Identifica al autor del clip multimedia. Estos metadatos se muestran como el **autor** del clip mediante Windows Media Player.                                                                                                                                                                                                                     |
| `<COPYRIGHT>(c)2000 YourImage</COPYRIGHT>`                                            | El elemento [Copyright](copyright-element.md) especifica los derechos de autor asociados con el clip multimedia. Windows Media Player muestra estos metadatos como el COPYRIGHT del clip.                                                                                                                                                              |
| `<!-- This is a comment. Change the following path to point to your Windows Media file -->` | Un comentario, en el mismo formato que los comentarios **XML** .                                                                                                                                                                                                                                                                                      |
| `<REF HREF = "..\\media\\laure.wma" />`                                                     | Dirección URL para el contenido multimedia. El elemento [ref](ref-element.md) identifica la línea como un puntero a contenido multimedia. El atributo **href** es la dirección URL del archivo. Tenga en cuenta el uso del cierre de tipo XML del elemento "/>" en lugar de " &lt; /ref &gt; ". Dado que este elemento no tiene elementos secundarios, se cierra a sí mismo.<br/> |
| `</ENTRY>`                                                                                  | Especifica el final de del primer elemento de **entrada** .                                                                                                                                                                                                                                                                                |
| `<ENTRY>`                                                                                   | Comienza el segundo elemento **entry** .                                                                                                                                                                                                                                                                                                    |
| `<TITLE>The second Entry in the advanced playlist</TITLE>`                            | Identifica el título del segundo clip.                                                                                                                                                                                                                                                                                                |
| `<AUTHOR>Microsoft Corporation</AUTHOR>`                                              | Identifica al autor del segundo clip multimedia.                                                                                                                                                                                                                                                                                         |
| `<!--This is the ToolTip text for the Title/Author/Copyright text -->`                      | Comentario. Solo estará visible cuando se vea el código.                                                                                                                                                                                                                                                                             |
| `<ABSTRACT>This is where you can include your tool tips</ABSTRACT>`                   | Este es el texto de la información sobre herramientas para el texto del **título** del clip.                                                                                                                                                                                                                                                                            |
| `<!-- This is a comment. Change the following path to point to your Windows Media file -->` | Comentario. Solo estará visible cuando se vea el código.                                                                                                                                                                                                                                                                             |
| `<REF HREF = ..\\media\\mellow.wma" />`                                                     | Identifica la línea como un puntero a contenido multimedia. El atributo **href** es la dirección URL del archivo.                                                                                                                                                                                                                                       |
| `</ENTRY>`                                                                                  | Especifica el final del segundo elemento **entry** .                                                                                                                                                                                                                                                                                      |
| `</ASX>`                                                                                    | Especifica el final de la lista de reproducción.                                                                                                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Crear listas de reproducción de metarchivo**](creating-metafile-playlists.md)
</dt> <dt>

[**Listas de reproducción de ejemplo**](example-playlists.md)
</dt> <dt>

[**Listas de reproducción de metarchivos**](metafile-playlists.md)
</dt> <dt>

[**Referencia de elementos de metarchivo de Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Guía de metarchivo de Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 





