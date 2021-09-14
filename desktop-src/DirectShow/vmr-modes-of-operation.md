---
description: Modos de funcionamiento de VMR
ms.assetid: 98244af1-5934-4d1c-b9c3-7a414b065fe7
title: Modos de funcionamiento de VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43427c4119bb912d2bc2cf92b1c740b1d22e1bf2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127272831"
---
# <a name="vmr-modes-of-operation"></a>Modos de funcionamiento de VMR

La arquitectura de componentes de VMR permite a las aplicaciones configurarla de varias maneras, en función de cómo se realice la representación. En la tabla siguiente se muestran los tres modos de presentación y los dos modos de combinación, y los componentes que están presentes para cada configuración.



| Modo       | Secuencia única                                                                     | Varias Secuencias (modo de combinación)                                                                                             |
|------------|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| Ventana   | Unidad de sincronización allocator-presenterCore<br/> Administrador de ventanas<br/> | MixerCompositor\*<br/> Allocator-presenter<br/> Unidad de sincronización principal<br/> Administrador de ventanas<br/> |
| Sin ventanas | Unidad de sincronización allocator-presenterCore<br/>                           | MixerCompositor\*<br/> Allocator-presenter<br/> Unidad de sincronización principal<br/>                           |
| Sin representación | Allocator-presenter (proporcionado por la aplicación)Unidad de sincronización principal<br/> | MixerCompositor\*<br/> Allocator-presenter (proporcionado por la aplicación)<br/> Unidad de sincronización principal<br/> |



 

\* Indica que la aplicación tiene la opción de proporcionar un componente personalizado o usar el componente predeterminado.

En todas las configuraciones, el punto principal que se debe recordar al crear gráficos de filtro con vmr es que debe configurar el VMR antes de conectarlo.

Para todas las configuraciones, los pins no se pueden agregar ni quitar dinámicamente después de que el VMR esté conectado al filtro ascendente, pero se pueden conectar y desconectar. Si la aplicación no está segura de cuántos pines se van a necesitar, debe configurar el VMR para el número máximo que podría ser necesario. La presencia de pines de entrada no usados en el filtro no degrada el rendimiento de la representación. A diferencia de la versión Mixer, la máquina virtual no tiene ningún pin de salida porque no requiere un filtro independiente para la administración de ventanas.

En las secciones siguientes se describe cómo configurar vmr para un modo determinado:

-   [Modo de ventana de VMR (compatibilidad)](vmr-windowed--compatibility--mode.md)
-   [Modo sin ventanas de VMR](vmr-windowless-mode.md)
-   [VMR con varias Secuencias (modo de combinación)](vmr-with-multiple-streams--mixing-mode.md)
-   [Modo de combinación de YUV](yuv-mixing-mode.md)
-   [Colocar y mover rectángulos de vídeo en el espacio de composición](positioning-and-moving-video-rectangles-in-composition-space.md)
-   [Modo de reproducción sin representación de VMR (asignador-presentadores personalizados)](vmr-renderless-playback-mode--custom-allocator-presenters.md)
-   [Modo exclusivo de DirectDraw](directdraw-exclusive-mode.md)

 

 




