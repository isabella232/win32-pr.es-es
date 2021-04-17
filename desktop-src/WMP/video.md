---
title: Vídeo (SDK de Windows Media Player)
description: Vídeo
ms.assetid: 3c654494-19b5-401e-bed8-02f7cc7d7f4e
keywords:
- Windows Media Player las máscaras móviles, vídeo
- máscaras, vídeo
- referencia de las máscaras, vídeo
- vídeo en máscaras, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb3d505acec3f6917c7ed3d182c656ff5e9f29f0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105705095"
---
# <a name="video-windows-media-player-sdk"></a>Vídeo (SDK de Windows Media Player)

Una pantalla de vídeo permite al usuario ver archivos de vídeo digital. El área de presentación de vídeo solo está visible cuando el vídeo se reproduce o está en pausa. Al diseñar la máscara, querrá reservar espacio en la imagen de fondo para que contenga la pantalla del vídeo. Si no lo hace, es posible que la pantalla de vídeo se superponga sobre cualquier arte visible, como el archivo de fondo, los botones y el trackbars, lo que evitará que el usuario opere con los controles de la máscara.

La sección de vídeo del archivo de definición de máscara debe comenzar con esta línea:


```C++
[ Video ]

```



A continuación, debe agregar una línea que especifique la ubicación y el tamaño del área de presentación de vídeo en la máscara.


```C++
0,38,240,172

```



Puede usar la siguiente plantilla para la sección vídeo del archivo de definición de máscara:


```C++
//  <Location>
//  ----------

```



En las secciones siguientes se proporcionan más detalles.

-   [Ubicación del vídeo](video-location.md)
-   [Origen de imagen de vídeo](video-image-source.md)
-   [Tamaño de vídeo](video-size.md)
-   [Sección de vídeo de ejemplo](sample-video-section.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de máscara**](skin-reference.md)
</dt> </dl>

 

 




