---
description: Componentes del filtro VMR
ms.assetid: 86fd8d6f-a742-457d-bb30-d04542431a0a
title: Componentes del filtro VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b597f6ac1b52f81ddc26d18e3fe0c6d16bae9515
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546038"
---
# <a name="vmr-filter-components"></a>Componentes del filtro VMR

La VMR emplea un diseño modular que permite a las aplicaciones configurarlo para muchos escenarios de representación diferentes. En función de su configuración, la VMR contiene de dos a cinco subcomponentes (además de sus clavijas de entrada).

![VMR en modo de ventana con varias secuencias](images/vmr-multiple-streams.png)

**Mezclador:** El mezclador es un objeto COM responsable de la combinación de varias secuencias. El desentrelazado también se produce dentro del mezclador. VMR carga el mezclador cuando se detectan varios flujos de entrada o cuando el vídeo de entrada está entrelazado. El mezclador recopila información sobre cada flujo de entrada y ordena los flujos en el orden Z correcto. Es responsable de determinar cuándo cada pin de entrada recibe un ejemplo y para indicar al compositor de la imagen en el momento adecuado que realice la mezcla real. El mezclador también calcula la marca de tiempo que se va a aplicar a cada imagen de salida. Cuando la aplicación está proporcionando un mapa de bits que se va a mostrar en la parte superior de la imagen compuesta, el mezclador es responsable de garantizar que el mapa de bits se muestre en la parte superior aunque se modifique el orden Z de los flujos de entrada.

**Compositor de imágenes:** El compositor de imágenes es un objeto COM que realiza la combinación real de los flujos de entrada en una única superficie DirectDraw o Direct3D proporcionada por el asignador-presentador. VMR proporciona un compositor de imágenes predeterminado que permite a las aplicaciones realizar efectos de mezcla alfa 2D. Las aplicaciones pueden proporcionar un compositor de imágenes personalizado para habilitar otros efectos 2D y 3D, como la aplicación de texturas a partes de la imagen, la combinación alfa por píxel, la asignación de la imagen a objetos 3D fijos o móviles, etc.

**Allocator-Presenter:** Allocator-Presenter es un objeto COM que asigna el objeto DirectDraw o Direct3D y controla la comunicación con la tarjeta gráfica. El dibujo puede realizarse como volteo o como blit. Puede conectar su propio asignador-presentador para crear y controlar el objeto DirectDraw o Direct3D, y/o para obtener acceso a los bits de vídeo en el momento de la presentación.

**Administrador de ventanas:** El administrador de ventanas solo se usa en modo de ventana. El administrador de ventanas admite las interfaces heredadas [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) y [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) para la compatibilidad con versiones anteriores.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la presentación de la combinación de vídeo](about-the-video-mixing-render.md)
</dt> </dl>

 

 



