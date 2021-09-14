---
title: Redireccionamiento
description: Redireccionamiento
ms.assetid: c8e3b43f-c11a-4ca7-b85c-038f0bfc3eb3
keywords:
- Windows Listas de reproducción de metarchivo multimedia, redireccionamiento
- listas de reproducción, redirección
- listas de reproducción de metarchivo, redireccionamiento
- Reproductor de Windows Media, redirección
- redirección
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bf1bb4d690c8aa6808e009a45a7bff1d6efada72
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073221"
---
# <a name="redirection"></a>Redireccionamiento

La lista de reproducción redirigirá el explorador a Reproductor de Windows Media reproducir el archivo multimedia o el flujo multimedia designado. La lista de reproducción de metarchivo más básica solo contiene el localizador uniforme de recursos (URL) de un archivo multimedia.

Para crear una lista de reproducción de metarchivo básica, abra el editor de texto que quiera, como Microsoft Bloc de notas, y escriba el código de ejemplo siguiente.


```XML
<ASX version="3.0">
   <ENTRY>
      <REF HREF="PathToYourFile"/>
   </ENTRY>
</ASX>

```



Sustituya una ruta de acceso válida al Windows multimedia mediante la sintaxis de la tabla siguiente.



| Origen del contenido                                                                                 | Sintaxis                                    |
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| El contenido es un archivo en un Windows multimedia                                                       | mms://ServerName/Path/FileName.wma        |
| El contenido es una multidifusión de difusión a la que se accede desde una Windows Media                    | https://WebServerName/Stations/kxyz.nsc    |
| El contenido es una unidifusión de difusión a la que se accede desde un punto de publicación en un Windows multimedia | mms://ServerName/PublishingPointAlias     |
| El contenido es un archivo en un servidor web                                                                 | https://WebServerName/Path/Filename.wma    |
| El contenido es un archivo en un disco duro local                                                            | file://c: Ruta \\ de acceso \\ Filename.wma             |
| El contenido es un archivo en un recurso compartido de red                                                              | file:// \\ \\ serverName \\ Path \\ Filename.wma |
| El contenido es un archivo en un Windows multimedia                                                       | mms://ServerName/Path/FileName.wmv        |



 

Guarde el archivo que ha creado con un nombre de archivo y una extensión como se describe en [Extensiones de nombre de archivo](file-name-extensions.md). Haga doble clic en él en Windows Explorer. Reproductor de Windows Media abrir e iniciar la transmisión del contenido. Puede guardar el archivo en el servidor web, junto con las páginas web, y vincularlo con un **elemento HREF,** o bien insertarlo en una página web mediante la etiqueta **Reproductor de Windows Media OBJECT.**

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

 

 




