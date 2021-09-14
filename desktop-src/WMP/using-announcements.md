---
title: Uso de anuncios
description: Uso de anuncios
ms.assetid: c372a4f8-2355-4c69-bba2-72b224879c4d
keywords:
- Windows Listas de reproducción de metarchivo multimedia, anuncios
- listas de reproducción, anuncios
- listas de reproducción de metarchivo, anuncios
- Reproductor de Windows Media, anuncios
- anuncios
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0c16fafee1984d08992b96c39d7c3893ea54f682
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073190"
---
# <a name="using-announcements"></a>Uso de anuncios

Un anuncio es un archivo que contiene información sobre la dirección URL de una secuencia multimedia, incluida la dirección IP de multidifusión, el puerto, el formato de secuencia y otras configuraciones de estación. Los anuncios los crea el Windows multimedia cuando se crea una secuencia de publicación de unidifusión o multidifusión. El cliente puede cargar rápidamente el archivo de anuncio y, a continuación, continuar para acceder al archivo multimedia de streaming.

Para un punto de publicación de unidifusión, se abre la secuencia multimedia del punto de publicación. Para un punto de publicación de multidifusión, la dirección URL se extrae de un archivo de estación de difusión con una extensión .nsc y se accede a los medios de streaming. A diferencia de una secuencia de unidifusión, no hay información de encabezado contenida en una secuencia de multidifusión. Esa información procede del archivo de estación de difusión con una extensión .nsc. Reproductor de Windows Media abre primero un archivo de anuncio, que es un uso para las listas de reproducción de metarchivo, que apunta a la ubicación del archivo de estación de difusión.

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

[**Creación de listas de reproducción de metarchivo**](creating-metafile-playlists.md)
</dt> <dt>

[**Uso de listas de reproducción de metarchivo**](using-metafile-playlists.md)
</dt> </dl>

 

 




