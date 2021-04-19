---
title: Una lista de reproducción básica
description: Una lista de reproducción básica
ms.assetid: fdd87959-861a-456e-b903-f5a27b4f6221
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
- Listas de reproducción de metarchivos de Windows Media, ejemplo de lista de reproducción básica
- listas de reproducción, ejemplo básico de lista de reproducción
- listas de reproducción de metarchivos, ejemplo básico de lista de reproducción
- Media Player de Windows, ejemplos de lista de reproducción
- Windows Media Player, listas de reproducción de ejemplo
- Windows Media Player, listas de reproducción de ejemplo
- Windows Media Player, ejemplo básico de lista de reproducción
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
ms.openlocfilehash: 804bc69c9ab3b243030cd2c87545e6362ccfca79
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314788"
---
# <a name="a-basic-playlist"></a>Una lista de reproducción básica

En el siguiente ejemplo de lista de reproducción se muestra un conjunto básico de elementos de lista de reproducción. Al escribir su propio código, tendrá que cambiar todas las direcciones URL y los nombres de archivo a nombres de archivo válidos a los que se pueda tener acceso desde el Media Player de Windows.

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
| \<ASX version = "3.0">                                                                     | El elemento [ASX](asx-element.md) identifica el cliente (Windows Media Player) que es una lista de reproducción de metarchivo de Windows Media. El atributo **version** especifica el número de versión de los elementos de metarchivo.                                                                                                                                                                                                                                                                                                                                           |
| \<TITLE>Demostración básica de listas de reproducción\</TITLE>                                                  | El elemento [title](title-element--metafile.md) identifica el título de la lista de reproducción en su conjunto. Windows Media Player muestra estos metadatos como el título de la muestra.                                                                                                                                                                                                                                                                                                                                                                                               |
| \<ENTRY>                                                                                   | Comienza el elemento de [entrada](entry-element.md) . Un elemento de **entrada** es una manera de definir un clip determinado en una lista de reproducción.                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| \<TITLE>Una entrada en una lista de reproducción básica\</TITLE>                                         | Identifica el título del clip de la lista de reproducción. Es diferente del elemento de **título** anterior porque este está anidado dentro de un elemento de **entrada** . Windows Media Player muestra estos metadatos como el título del clip.                                                                                                                                                                                                                                                                                                                                         |
| \<AUTHOR>Microsoft Corporation\</AUTHOR>                                              | El elemento [Author](author-element.md) identifica el autor del clip multimedia. Windows Media Player muestra estos metadatos como **autor** del clip.                                                                                                                                                                                                                                                                                                                                                                                                         |
| \<!-- This is a comment. Change the following path to point to your Windows media file --> | Comentario. Los [comentarios](comments.md) solo están visibles cuando se ve el código y tienen el mismo formato que los comentarios **XML** .                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| \<REF HREF = "mms://proseware.com/path/Yourfile.wma" />                                    | Puntero real al archivo multimedia. El elemento [ref](ref-element.md) identifica la línea como un puntero a contenido multimedia, mientras que el atributo **href** es la dirección URL del archivo multimedia. En este caso, la dirección URL usa el protocolo MMS, por lo que apunta a un servidor de Windows Media. Los archivos multimedia del servidor multimedia normalmente no se mantienen en la misma ubicación que los documentos HTML.<br/> Observe el uso del cierre de tipo XML del elemento, "/>", en lugar de " &lt; /ref &gt; ". Dado que este elemento no tiene elementos secundarios, se cierra a sí mismo.<br/> |
| \</ENTRY>                                                                                  | Especifica el final del elemento de **entrada** .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| \</ASX>                                                                                    | Especifica el final de la lista de reproducción.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

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

 

 





