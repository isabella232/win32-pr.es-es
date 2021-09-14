---
description: Componentes de filtro de VMR
ms.assetid: 86fd8d6f-a742-457d-bb30-d04542431a0a
title: Componentes de filtro de VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b597f6ac1b52f81ddc26d18e3fe0c6d16bae9515
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127272844"
---
# <a name="vmr-filter-components"></a>Componentes de filtro de VMR

VmR emplea un diseño modular que permite a las aplicaciones configurarlo para muchos escenarios de representación diferentes. En función de su configuración, vmr contiene de dos a cinco subcomponentes (además de sus pines de entrada).

![vmr en modo de ventana con varias secuencias](images/vmr-multiple-streams.png)

**Mixer:** El mezclador es un objeto COM responsable de mezclar varias secuencias. El desenlazado también se produce dentro del mezclador. La máquina virtual carga el mezclador cuando se detectan varios flujos de entrada o cuando el vídeo de entrada está entrelazado. El mezclador recopila información sobre cada flujo de entrada y ordena las secuencias en el orden Z correcto. Es responsable de determinar cuándo cada pin de entrada recibe una muestra y de indicar al compositor de la imagen en el momento adecuado que realice la mezcla real. El mezclador también calcula la marca de tiempo que se va a aplicar a cada imagen de salida. Cuando la aplicación proporciona un mapa de bits que se va a mostrar en la parte superior de la imagen compuesta, el mezclador es responsable de garantizar que el mapa de bits se muestra en la parte superior incluso si se modifica el orden Z de los flujos de entrada.

**Image Compositor:** Image Compositor es un objeto COM que realiza la mezcla real de los flujos de entrada en una sola superficie DirectDraw o Direct3D proporcionada por el asignador-presentador. VmR proporciona un compositor de imágenes predeterminado que permite a las aplicaciones realizar efectos de combinación alfa 2D. Las aplicaciones pueden proporcionar un compositor de imágenes personalizado para habilitar otros efectos 2D y 3D, como aplicar texturas a partes de la imagen, combinación alfa por píxel, asignar la imagen a objetos 3D estacionados o móviles, y así sucesivamente.

**Allocator-Presenter:** El asignador-presentador es un objeto COM que asigna el objeto DirectDraw o Direct3D y controla la comunicación con la tarjeta gráfica. El dibujo se puede realizar como un volteo o como una blit. Puede conectar su propio asignador-presentador para crear y controlar el objeto DirectDraw o Direct3D, o para obtener acceso a los bits de vídeo en el momento de la presentación.

**Administrador de ventanas:** El Administrador de ventanas solo se usa en modo de ventana. El Administrador de ventanas admite las interfaces [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) e [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) heredadas para la compatibilidad con versiones anteriores.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la representación de mezcla de vídeo](about-the-video-mixing-render.md)
</dt> </dl>

 

 



