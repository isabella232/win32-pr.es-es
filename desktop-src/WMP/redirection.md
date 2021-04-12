---
title: Redireccionamiento
description: Redireccionamiento
ms.assetid: c8e3b43f-c11a-4ca7-b85c-038f0bfc3eb3
keywords:
- Listas de reproducción de metarchivos de Windows Media, redirección
- listas de reproducción, redirección
- listas de reproducción de metarchivo, redirección
- Media Player de Windows, redirección
- redirección
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bf1bb4d690c8aa6808e009a45a7bff1d6efada72
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356746"
---
# <a name="redirection"></a>Redireccionamiento

La lista de reproducción redirigirá el explorador a Windows Media Player para reproducir el archivo multimedia o la secuencia de medios designada. La lista de reproducción de metarchivos más básica contiene solo el localizador uniforme de recursos (URL) de un archivo multimedia.

Para crear una lista de reproducción de metarchivo básica, abra el editor de texto que prefiera, como el Bloc de notas de Microsoft, y escriba el código de ejemplo siguiente.


```XML
<ASX version="3.0">
   <ENTRY>
      <REF HREF="PathToYourFile"/>
   </ENTRY>
</ASX>

```



Sustituya una ruta de acceso válida al archivo de Windows Media mediante la sintaxis de la tabla siguiente.



| Origen de contenido                                                                                 | Sintaxis                                    |
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| El contenido es un archivo de un servidor de Windows Media                                                       | mms://ServerName/Path/FileName.wma        |
| El contenido es una multidifusión de difusión a la que se tiene acceso desde una estación de Windows Media.                    | https://WebServerName/Stations/kxyz.nsc    |
| El contenido es una unidifusión de difusión a la que se tiene acceso desde un punto de publicación en un servidor de Windows Media. | mms://ServerName/PublishingPointAlias     |
| El contenido es un archivo de un servidor Web                                                                 | https://WebServerName/Path/Filename.wma    |
| El contenido es un archivo de un disco duro local                                                            | file://c: \\ ruta de acceso \\ nombreDeArchivo. WMA             |
| El contenido es un archivo de un recurso compartido de red                                                              | file:// \\ \\ ServerName \\ rutaDeAcceso \\ nombreDeArchivo. WMA |
| El contenido es un archivo de un servidor de Windows Media                                                       | mms://ServerName/Path/FileName.wmv        |



 

Guarde el archivo que ha creado con un nombre de archivo y una extensión, tal y como se describe en [extensiones de nombre de archivo](file-name-extensions.md). Haga doble clic en él en el explorador de Windows. Windows Media Player debe abrir e iniciar el streaming del contenido. Puede guardar el archivo en el servidor Web, junto con las páginas web, y vincularlo con un elemento **href** , o insertarlo en una página web mediante la etiqueta de **objeto** de Media Player de Windows.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Listas de reproducción de metarchivos**](metafile-playlists.md)
</dt> <dt>

[**Usar listas de reproducción de metarchivo**](using-metafile-playlists.md)
</dt> <dt>

[**Referencia de elementos de metarchivo de Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Guía de metarchivo de Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




