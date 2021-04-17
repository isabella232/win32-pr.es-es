---
title: Usar anuncios
description: Usar anuncios
ms.assetid: c372a4f8-2355-4c69-bba2-72b224879c4d
keywords:
- Listas de reproducción de metarchivos de Windows Media, anuncios
- listas de reproducción, anuncios
- listas de reproducción de metarchivos, anuncios
- Media Player de Windows, anuncios
- anuncios
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0c16fafee1984d08992b96c39d7c3893ea54f682
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704625"
---
# <a name="using-announcements"></a>Usar anuncios

Un anuncio es un archivo que contiene información sobre la dirección URL de una secuencia multimedia, incluida la dirección IP de multidifusión, el puerto, el formato de secuencia y otras configuraciones de la estación. Los anuncios los crea el administrador de Windows Media cuando se crea una secuencia de publicación de unidifusión o multidifusión. El cliente puede cargar rápidamente el archivo de anuncio y, después, continuar para acceder al archivo multimedia de streaming.

En el caso de un punto de publicación de unidifusión, se abre la secuencia de medios del punto de publicación. En el caso de un punto de publicación de multidifusión, se extrae la dirección URL de un archivo de la estación de difusión con una extensión. NSC y se tiene acceso a los medios de streaming. A diferencia de una secuencia de unidifusión, no hay información de encabezado en una secuencia de multidifusión. Esa información procede del archivo de la estación de difusión con una extensión. NSC. Windows Media Player suele abrir primero un archivo de anuncio, que es un uso para listas de reproducción de metarchivos, que apunta a la ubicación del archivo de la estación de difusión.

Código de ejemplo


```XML
<ASX VERSION="3.0">
    <TITLE>title</TITLE>
    <ENTRY>
        <REF HREF="mms://proseware.com/pubpoint"/>
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Crear listas de reproducción de metarchivo**](creating-metafile-playlists.md)
</dt> <dt>

[**Usar listas de reproducción de metarchivo**](using-metafile-playlists.md)
</dt> </dl>

 

 




