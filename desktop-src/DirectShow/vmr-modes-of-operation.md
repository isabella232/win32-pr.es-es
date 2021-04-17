---
description: Modos de funcionamiento de VMR
ms.assetid: 98244af1-5934-4d1c-b9c3-7a414b065fe7
title: Modos de funcionamiento de VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43427c4119bb912d2bc2cf92b1c740b1d22e1bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666770"
---
# <a name="vmr-modes-of-operation"></a>Modos de funcionamiento de VMR

La arquitectura de componentes de VMR permite a las aplicaciones configurarlo de varias maneras, dependiendo de cómo se realice la representación. En la tabla siguiente se muestran los tres modos de presentación y los dos modos de combinación, y los componentes que están presentes para cada configuración.



| Mode       | Flujo único                                                                     | Varias secuencias (modo de combinación)                                                                                             |
|------------|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| Ventanas   | Allocator: unidad de sincronización presenterCore<br/> Administrador de ventanas<br/> | MixerCompositor\*<br/> Allocator-Presenter<br/> Unidad de sincronización básica<br/> Administrador de ventanas<br/> |
| Sin ventana | Allocator: unidad de sincronización presenterCore<br/>                           | MixerCompositor\*<br/> Allocator-Presenter<br/> Unidad de sincronización básica<br/>                           |
| No rendered | Allocator-Presenter (proporcionado por la aplicación) unidad de sincronización principal<br/> | MixerCompositor\*<br/> Allocator: presentador (proporcionado por la aplicación)<br/> Unidad de sincronización básica<br/> |



 

\* Indica que la aplicación tiene la opción de proporcionar un componente personalizado o usar el componente predeterminado.

En todas las configuraciones, el punto principal a recordar al crear gráficos de filtros con la VMR es que debe configurar la VMR antes de conectarla.

Para todas las configuraciones, los PIN no se pueden agregar ni quitar dinámicamente después de que el VMR esté conectado al filtro de nivel superior, pero se pueden conectar y desconectar. Si la aplicación no está seguro de cuántos PIN serán necesarios, debe configurar la VMR para el número máximo que podría ser necesario. La presencia de clavijas de entrada sin usar en el filtro no degrada el rendimiento de la representación. A diferencia del mezclador de superposición anterior, VMR no tiene ningún PIN de salida porque no requiere un filtro independiente para la administración de ventanas.

En las secciones siguientes se describe cómo configurar la VMR para un modo determinado:

-   [Modo de ventana de VMR (compatibilidad)](vmr-windowed--compatibility--mode.md)
-   [Modo sin ventana de VMR](vmr-windowless-mode.md)
-   [VMR con varias secuencias (modo de combinación)](vmr-with-multiple-streams--mixing-mode.md)
-   [Modo de mezcla YUV](yuv-mixing-mode.md)
-   [Colocar y mover rectángulos de vídeo en el espacio de composición](positioning-and-moving-video-rectangles-in-composition-space.md)
-   [Modo de reproducción no representativo de VMR (asignador personalizado)](vmr-renderless-playback-mode--custom-allocator-presenters.md)
-   [Modo exclusivo de DirectDraw](directdraw-exclusive-mode.md)

 

 




