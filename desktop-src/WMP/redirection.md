---
title: Redireccionamiento
description: Redireccionamiento
ms.assetid: c8e3b43f-c11a-4ca7-b85c-038f0bfc3eb3
keywords:
- Windows Listas de reproducción de metarchivo multimedia,redireccionamiento
- listas de reproducción, redireccionamiento
- listas de reproducción de metarchivo, redireccionamiento
- Reproductor de Windows Media,redireccionamiento
- redirección
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e335250777c92634a805221a2d4f915a0dcadcad152cd03091cc9c79a662193d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117934160"
---
# <a name="redirection"></a>Redireccionamiento

La lista de reproducción redirigirá el explorador a Reproductor de Windows Media reproducir el archivo multimedia o el flujo multimedia designados. La lista de reproducción de metarchivo más básica solo contiene el localizador uniforme de recursos (URL) de un archivo multimedia.

Para crear una lista de reproducción básica de metarchivo, abra su editor de texto favorito, como Microsoft Bloc de notas, y escriba el código de ejemplo siguiente.


```XML
<ASX version="3.0">
   <ENTRY>
      <REF HREF="PathToYourFile"/>
   </ENTRY>
</ASX>

```



Sustituya una ruta de acceso válida al archivo Windows media mediante la sintaxis de la tabla siguiente.



| Origen de contenido                                                                                 | Syntax                                    |
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| El contenido es un archivo en un servidor Windows Media                                                       | mms://ServerName/Path/FileName.wma        |
| El contenido es una multidifusión de difusión a la que se accede desde Windows Media Station                    | https://WebServerName/Stations/kxyz.nsc    |
| El contenido es una unidifusión de difusión a la que se accede desde un punto de publicación en un Windows multimedia | mms://ServerName/PublishingPointAlias     |
| El contenido es un archivo en un servidor web                                                                 | https://WebServerName/Path/Filename.wma    |
| El contenido es un archivo en un disco duro local                                                            | file://c: Ruta \\ de acceso \\ Filename.wma             |
| El contenido es un archivo en un recurso compartido de red                                                              | file:// \\ \\ serverName \\ Path \\ Filename.wma |
| El contenido es un archivo en un servidor Windows Media                                                       | mms://ServerName/Path/FileName.wmv        |



 

Guarde el archivo que ha creado con un nombre de archivo y una extensión como se describe en [Extensiones de nombre de archivo](file-name-extensions.md). Haga doble clic en él en Windows Explorador. Reproductor de Windows Media abrir e iniciar la transmisión del contenido. Puede guardar el archivo en el servidor web, junto con las páginas web, y vincularlo con un **elemento HREF,** o bien insertarlo en una página web mediante la etiqueta **Reproductor de Windows Media OBJECT.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Listas de reproducción de metarchivo**](metafile-playlists.md)
</dt> <dt>

[**Uso de listas de reproducción de metarchivo**](using-metafile-playlists.md)
</dt> <dt>

[**Windows Referencia de elementos de metarchivo multimedia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Guía de metarchivo multimedia**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




