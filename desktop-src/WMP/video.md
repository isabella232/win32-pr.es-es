---
title: Vídeo (Reproductor de Windows Media SDK)
description: Vídeo
ms.assetid: 3c654494-19b5-401e-bed8-02f7cc7d7f4e
keywords:
- Reproductor de Windows Media Máscaras móviles, vídeo
- máscaras, vídeo
- referencia de máscaras,vídeo
- vídeo en máscaras, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb3d505acec3f6917c7ed3d182c656ff5e9f29f0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070800"
---
# <a name="video-windows-media-player-sdk"></a>Vídeo (Reproductor de Windows Media SDK)

Una pantalla de vídeo permite al usuario ver archivos de vídeo digitales. El área de visualización del vídeo solo es visible cuando el vídeo se reproduce o se pausa. Al diseñar la máscara, querrá reservar espacio en la imagen de fondo para que contenga la presentación del vídeo. Si no lo hace, la pantalla de vídeo puede superponerse a cualquier arte visible, como el archivo de fondo, los botones y las barras de seguimiento, lo que evitará que el usuario controle los controles en la máscara.

La sección Vídeo del archivo de definición de máscara debe comenzar con esta línea:


```C++
[ Video ]

```



A continuación, debe agregar una línea que especifique la ubicación y el tamaño del área de presentación del vídeo en la máscara.


```C++
0,38,240,172

```



Puede usar la siguiente plantilla para la sección Vídeo del archivo de definición de máscara:


```C++
//  <Location>
//  ----------

```



En las secciones siguientes se proporcionan más detalles.

-   [Ubicación del vídeo](video-location.md)
-   [Origen de imagen de vídeo](video-image-source.md)
-   [Tamaño del vídeo](video-size.md)
-   [Sección de vídeo de ejemplo](sample-video-section.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de máscara**](skin-reference.md)
</dt> </dl>

 

 




