---
description: Características de VMR
ms.assetid: a809045b-b60d-4092-bc4d-0e70e17d2913
title: Características de VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7c4a5a34be9fb3b3bb08df18091b88fbe7d7432
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677199"
---
# <a name="features-of-the-vmr"></a>Características de VMR

El representador de mezcla de vídeo 7 (VMR-7) admite las siguientes características nuevas:

-   Combinación real de varias secuencias de vídeo con las capacidades de combinación alfa de los dispositivos de hardware de Direct3D.
-   La capacidad de conectar su propio componente de composición para implementar efectos y transiciones entre varias secuencias de vídeo que entran en la VMR.
-   Representación sin ventana verdadera. Ya no es necesario que la ventana de reproducción de vídeo sea un elemento secundario de la ventana de la aplicación para que contenga reproducción de vídeo. El nuevo modo de representación sin ventanas de VMR permite a las aplicaciones hospedar fácilmente la reproducción de vídeo en cualquier ventana sin tener que reenviar los mensajes de ventana al representador para el procesamiento específico del representador.
-   Un nuevo modo de reproducción no representativo en el que las aplicaciones pueden proporcionar su propio componente de asignador para obtener acceso a la imagen de vídeo descodificada antes de que se muestre en la pantalla.
-   Compatibilidad mejorada para equipos equipados con varios monitores.
-   Compatibilidad con la nueva arquitectura de aceleración de vídeo de DirectX de Microsoft.
-   Compatibilidad con la reproducción de vídeo de alta calidad simultáneamente en varias ventanas.
-   Compatibilidad con el modo exclusivo de DirectDraw
-   100% de compatibilidad con versiones anteriores con aplicaciones existentes.
-   Compatibilidad con la ejecución de fotogramas y una manera confiable de capturar la imagen actual que se muestra.
-   La capacidad de las aplicaciones de alphamente mezclar sus propios datos de imagen estáticos (por ejemplo, logotipos de canal o componentes de interfaz de usuario) con el vídeo sin complicaciones.

VMR-9 es compatible con todas las características enumeradas anteriormente, además de:

-   La capacidad de procesar datos de vídeo directamente con las API de Direct3D, como los sombreadores de píxeles.
-   Compatibilidad mejorada para el contenido de vídeo entrelazado.
-   Compatibilidad con cualquier plataforma compatible con DirectX.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la presentación de la combinación de vídeo](about-the-video-mixing-render.md)
</dt> </dl>

 

 



