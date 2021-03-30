---
title: Cómo funcionan los paquetes de descarga de Windows Media (en desuso)
description: Cómo funcionan los paquetes de descarga de Windows Media (en desuso)
ms.assetid: 8bab1764-93da-4abc-a8b7-17bc44b381ce
keywords:
- Metaarchivos de Windows Media, paquetes de descarga de Windows Media
- Windows Media Player, paquetes de descarga de Windows Media
- metaarchivos, paquetes de descarga de Windows Media
- Windows Media, paquetes de descarga de Windows Media
- Paquetes de descarga de Windows Media, acerca de
- Paquetes de descarga de Windows Media, cómo funcionan los paquetes
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1db477791bb93cd599dcef38a90b230c6cd7ddde
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148792"
---
# <a name="how-windows-media-download-packages-work-deprecated"></a>Cómo funcionan los paquetes de descarga de Windows Media (en desuso)

En esta página se documenta una característica que puede no estar disponible en versiones futuras de Windows Media Player y el SDK de Windows Media Player.

Un paquete de descarga de Windows Media se inicia desde un sitio web cuando un usuario hace clic en un vínculo en un explorador Web, como Microsoft Internet Explorer. Esta acción abre Windows Media Player y, a continuación, descarga y desempaqueta el paquete de descarga de Windows Media en el disco duro del usuario en una carpeta predeterminada.

Una vez extraídos los archivos del paquete de descarga de Windows Media, Windows Media Player busca una lista de reproducción de metarchivo de Windows Media con una extensión de nombre de archivo. ASX entre los archivos empaquetados. Si encuentra uno, el reproductor crea una lista de reproducción basada en el metarchivo incluido. Los archivos que contienen contenido multimedia se agregan a la biblioteca.

Windows Media Player también busca un elemento de **máscara** en el metarchivo. Si el elemento **Skin** contiene una referencia a un archivo de borde con la extensión de nombre de archivo. WMZ, el reproductor carga el borde en el panel **reproducción en curso** . A continuación, el reproductor comienza a reproducir el contenido proporcionado en el paquete.

En el diagrama siguiente se muestra cómo se empaqueta el contenido en un archivo de descarga de Windows Media, se envía a un sitio web, se descarga y se reproduce en un equipo cliente mediante Windows Media Player.

![Cómo se obtiene y se reproduce un archivo de descarga de Windows Media.](images/wmd-image.png) Descarga de Windows Media

En la tabla siguiente se describen los tres elementos que componen un paquete de descarga de Windows Media.



| Elemento Package    | Función                                                                                                                                                                                                                                        | Extensiones de nombre de archivo                     |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| Borde             | Una interfaz de usuario fija y personalizada creada por el propietario del contenido para mostrar, vincular y reproducir todos los medios empaquetados en el paquete de descarga de Windows Media. Las técnicas utilizadas para crear bordes son similares a las que se usan para crear máscaras. | .wmz                                     |
| Lista de reproducción de metarchivo  | Metarchivo de Windows Media que contiene elementos de **entrada** , información de lista de reproducción y una identidad de elemento de **máscara** para los archivos de contenido.                                                                                                             | .asx                                     |
| Contenido multimedia | Archivo que contiene cualquier formato de audio o vídeo compatible con Windows Media Player.                                                                                                                                                          | . WMA,. wmv,. ASF,. wav,. avi,. mpg,. mp3 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Paquetes de descarga de Windows Media (en desuso)**](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




