---
title: Lista de reproducción básica
description: Lista de reproducción básica
ms.assetid: fdd87959-861a-456e-b903-f5a27b4f6221
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
- Windows Listas de reproducción de metarchivo multimedia, ejemplo de lista de reproducción básica
- listas de reproducción, ejemplo de lista de reproducción básica
- listas de reproducción de metarchivo, ejemplo de lista de reproducción básica
- Reproductor de Windows Media,ejemplos de lista de reproducción
- Reproductor de Windows Media, listas de reproducción de ejemplo
- Reproductor de Windows Media,listas de reproducción de ejemplo
- Reproductor de Windows Media ejemplo de lista de reproducción básica
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
ms.openlocfilehash: c8284acfe86cb204293902c0fb8664e74b12f3d2cc176d762f1aff079faac0cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004585"
---
# <a name="a-basic-playlist"></a>Lista de reproducción básica

En el ejemplo de lista de reproducción siguiente se muestra un conjunto básico de elementos de lista de reproducción. Al escribir su propio código, tendrá que cambiar todas las direcciones URL y los nombres de archivo por nombres de archivo válidos que sean accesibles para su Reproductor de Windows Media.

**Ejemplo de código**


```XML
<ASX version = "3.0">
<TITLE>Basic Playlist Demo</TITLE>
    <ENTRY>
        <TITLE>An Entry in a basic playlist</TITLE>
        <AUTHOR>Microsoft Corporation</AUTHOR>
        <COPYRIGHT>(c)2000 Microsoft Corporation</COPYRIGHT>
        <REF HREF = "mms://proseware.com/path/Yourfile.wma" />
    </ENTRY>
</ASX>

```



En la tabla siguiente se proporcionan detalles sobre el uso de cada elemento en el código de ejemplo.



| Línea                                                                                            | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \<ASX version = "3.0">                                                                     | El [elemento ASX](asx-element.md) identifica para el cliente (Reproductor de Windows Media) que se trata de una lista Windows de metarchivo multimedia. El **atributo version** especifica el número de versión de los elementos del metarchivo.                                                                                                                                                                                                                                                                                                                                           |
| \<TITLE>Demostración básica de lista de reproducción\</TITLE>                                                  | El [elemento TITLE](title-element--metafile.md) identifica el título de la lista de reproducción en su conjunto. Reproductor de Windows Media muestra estos metadatos como título para mostrar.                                                                                                                                                                                                                                                                                                                                                                                               |
| \<ENTRY>                                                                                   | Comienza el [elemento ENTRY.](entry-element.md) Un **elemento ENTRY** es una manera de definir un clip determinado en una lista de reproducción                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| \<TITLE>Una entrada en una lista de reproducción básica\</TITLE>                                         | Identifica el título del clip de la lista de reproducción. Es diferente del elemento **TITLE** anterior porque está anidado dentro de un **elemento ENTRY.** Reproductor de Windows Media muestra estos metadatos como título del clip.                                                                                                                                                                                                                                                                                                                                         |
| \<AUTHOR>Microsoft Corporation\</AUTHOR>                                              | El [elemento AUTHOR](author-element.md) identifica al autor del clip multimedia. Reproductor de Windows Media muestra estos metadatos como el clip **AUTHOR**.                                                                                                                                                                                                                                                                                                                                                                                                         |
| \<!-- This is a comment. Change the following path to point to your Windows media file --> | Comentario. [Los](comments.md) comentarios solo son visibles cuando se ve el código y tienen el mismo formato que **los comentarios XML.**                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| \<REF HREF = "mms://proseware.com/path/Yourfile.wma" />                                    | Puntero real al archivo multimedia. El [elemento REF](ref-element.md) identifica la línea como un puntero al contenido multimedia, mientras que el atributo **HREF** es la dirección URL del archivo multimedia. En este caso, la dirección URL usa el protocolo MMS, por lo que apunta a un Windows multimedia. Normalmente, los archivos multimedia del servidor multimedia no se mantienen en la misma ubicación que los documentos HTML.<br/> Tenga en cuenta el uso del cierre de tipo XML del elemento , "/>", en lugar de " &lt; /REF &gt; ". Dado que este elemento no tiene elementos secundarios, se cierra a sí mismo.<br/> |
| \</ENTRY>                                                                                  | Especifica el final del **elemento ENTRY.**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| \</ASX>                                                                                    | Especifica el final de la lista de reproducción.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

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

 

 





