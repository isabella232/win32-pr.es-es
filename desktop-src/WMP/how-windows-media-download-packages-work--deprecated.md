---
title: Cómo Windows paquetes de descarga multimedia (en desuso)
description: Cómo Windows paquetes de descarga multimedia (en desuso)
ms.assetid: 8bab1764-93da-4abc-a8b7-17bc44b381ce
keywords:
- Windows Metarchivos multimedia, Windows paquetes de descarga multimedia
- Reproductor de Windows Media,Windows de descarga multimedia
- metarchivos, Windows paquetes de descarga multimedia
- Windows Media,Windows paquetes de descarga multimedia
- Windows Paquetes de descarga multimedia, acerca de
- Windows Paquetes de descarga multimedia, cómo funcionan los paquetes
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1db477791bb93cd599dcef38a90b230c6cd7ddde
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476229"
---
# <a name="how-windows-media-download-packages-work-deprecated"></a>Cómo Windows paquetes de descarga multimedia (en desuso)

En esta página se documenta una característica que puede no estar disponible en versiones futuras de Reproductor de Windows Media y Reproductor de Windows Media SDK.

Un Windows de descarga multimedia se inicia desde un sitio web cuando un usuario hace clic en un vínculo en un explorador web, como Microsoft Internet Explorer. Esta acción abre Reproductor de Windows Media y, a continuación, descarga y desenlaza el paquete de descarga de Windows multimedia en el disco duro del usuario en una carpeta predeterminada.

Una vez que los archivos se han extraído del paquete de descarga multimedia de Windows, Reproductor de Windows Media busca una lista de reproducción de metarchivo multimedia de Windows con una extensión de nombre de archivo .asx entre los archivos empaquetados. Si encuentra una, el reproductor crea una lista de reproducción basada en el metarchivo incluido. Los archivos que contienen contenido multimedia se agregan a la biblioteca.

Reproductor de Windows Media también busca un **elemento SKIN** en el metarchivo. Si el **elemento SKIN** contiene una referencia a un archivo de borde con una extensión de nombre de archivo .wmz, el reproductor carga el borde en el **panel Reproducción** ahora. A continuación, el reproductor comienza a reproducir el contenido proporcionado en el paquete.

En el diagrama siguiente se muestra cómo el contenido se empaqueta en un archivo de descarga multimedia de Windows, se publica en un sitio web, se descarga y se reproduce en un equipo cliente mediante Reproductor de Windows Media.

![cómo se obtiene y reproduce un archivo de descarga multimedia de Windows.](images/wmd-image.png) Windows Descarga de medios

En la tabla siguiente se describen los tres elementos que Windows paquete de descarga multimedia.



| Elemento Package    | Función                                                                                                                                                                                                                                        | Extensiones de nombre de archivo                     |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| Borde             | Interfaz de usuario personalizada y fija creada por el propietario del contenido para mostrar, vincular y reproducir todos los medios empaquetados en el paquete Windows descarga multimedia. Las técnicas usadas para crear bordes son similares a las que se usan para crear máscaras. | .wmz                                     |
| Lista de reproducción de metarchivo  | Metarchivo Windows multimedia que contiene elementos **ENTRY,** información de lista de reproducción e identidad de elemento **SKIN** para archivos de contenido.                                                                                                             | .asx                                     |
| Contenido multimedia | Un archivo que contiene cualquier formato de audio o vídeo que sea compatible con Reproductor de Windows Media.                                                                                                                                                          | .wma, .wmv, .asf, .wav, .avi, .mpg, .mp3 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Windows Paquetes de descarga de medios (en desuso)**](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




