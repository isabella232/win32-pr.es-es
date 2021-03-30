---
title: Usar una lista de reproducción de metarchivo
description: Usar una lista de reproducción de metarchivo
ms.assetid: e6cbdb76-4405-409e-93c3-38a3baa7c231
keywords:
- Listas de reproducción de metarchivos de Windows Media, usar
- listas de reproducción de metarchivos, usar
- listas de reproducción, usar
- Listas de reproducción de metarchivos de Windows Media, acerca de
- listas de reproducción de metarchivos, acerca de
- listas de reproducción, acerca de
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a5f1832c0c739874fbbd4db219f2c622fc2debfa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775385"
---
# <a name="using-a-metafile-playlist"></a>Usar una lista de reproducción de metarchivo

Dado que no se puede vincular directamente desde una página web a un servidor multimedia de streaming, se usan listas de reproducción de metarchivo. Las listas de reproducción de metarchivos contienen la información que necesita Windows Media Player y se almacenan en un servidor Web. Después, puede vincular desde el documento Web a una lista de reproducción de metarchivo. Cuando se abre una lista de reproducción de metarchivo, el control se transfiere a Windows Media Player, que procesa el archivo, se conecta al servidor de streaming multimedia y reproduce el contenido especificado.

En primer lugar, el explorador descarga la lista de reproducción del metarchivo en el directorio de caché del usuario. Dado que la lista de reproducción del metarchivo es pequeña, se trata de un paso muy rápido. A continuación, el equipo del usuario busca en su tabla asociaciones de archivo la Asociación de la lista de reproducción del metarchivo con Windows Media Player. Windows Media Player abre e interpreta el scripting en la lista de reproducción de metarchivos, que contiene, entre otras cosas, la dirección URL del contenido de streaming. Windows Media Player usa la dirección URL para buscar el contenido e iniciar el flujo. El scripting de lista de reproducción de metarchivo controla la experiencia de streaming.

Dado que las listas de reproducción de metarchivos funcionan a través de una aplicación auxiliar asociada con el tipo ASXMIME (Application/Mplayer2 o video/x-MS-ASF), son compatibles con cualquier explorador que admita aplicaciones auxiliares. Los ejemplos que se muestran en este documento funcionarán con Microsoft Internet Explorer 4,0 y versiones posteriores, y con Netscape Navigator 4,0 y versiones posteriores en las plataformas Microsoft Win32® y Apple Macintosh. En todos los ejemplos, tendrá que asegurarse de que los archivos multimedia digitales a los que se hace referencia tienen rutas de acceso y nombres de archivo válidos para el entorno.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de metarchivo de Windows Media**](windows-media-metafile-guide.md)
</dt> <dt>

[**Referencia de metarchivos de Windows Media**](windows-media-metafile-reference.md)
</dt> <dt>

[**Información general de los metaarchivos de Windows Media**](windows-media-metafiles-overview.md)
</dt> </dl>

 

 




