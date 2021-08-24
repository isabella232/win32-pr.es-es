---
description: Características de VMR
ms.assetid: a809045b-b60d-4092-bc4d-0e70e17d2913
title: Características de VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66c78fc34be3097beedb73ac3989bc468cff0851143355902e3236f672797a83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819557"
---
# <a name="features-of-the-vmr"></a>Características de VMR

El representador de mezcla de vídeo 7 (VMR-7) admite las siguientes características nuevas:

-   Mezcla real de varias secuencias de vídeo mediante las funcionalidades de combinación alfa de los dispositivos de hardware Direct3D.
-   La capacidad de conectar su propio componente de composición para implementar efectos y transiciones entre varias secuencias de vídeo que entran en vmr.
-   Representación sin ventanas verdadera. Ya no es necesario convertir la ventana de reproducción de vídeo en un elemento secundario de la ventana de la aplicación para que contenga la reproducción de vídeo. El nuevo modo de representación sin ventanas de VMR permite a las aplicaciones hospedar fácilmente la reproducción de vídeo dentro de cualquier ventana sin tener que reenviar mensajes de ventana al representador para el procesamiento específico del representador.
-   Nuevo modo de reproducción sin representación en el que las aplicaciones pueden proporcionar su propio componente de asignador para obtener acceso a la imagen de vídeo descodificada antes de que se muestre en la pantalla.
-   Compatibilidad mejorada con equipos equipados con varios monitores.
-   Compatibilidad con la nueva arquitectura de aceleración de vídeo directX de Microsoft.
-   Compatibilidad con la reproducción de vídeo de alta calidad simultáneamente en varias ventanas.
-   Compatibilidad con el modo exclusivo de DirectDraw
-   Compatibilidad 100 % con versiones anteriores con aplicaciones existentes.
-   Compatibilidad con la ejecución paso a paso de fotogramas y una manera confiable de capturar la imagen actual que se muestra.
-   La capacidad de las aplicaciones para combinar fácilmente alfanuméricos sus propios datos de imagen estática (como logotipos de canal o componentes de interfaz de usuario) con el vídeo de una manera sin parpadeos.

VMR-9 admite todas las características enumeradas anteriormente, además de:

-   La capacidad de procesar datos de vídeo directamente con las API de Direct3D, como los sombreadores de píxeles.
-   Se ha mejorado la compatibilidad con el contenido de vídeo entrelazado.
-   Compatibilidad con cualquier plataforma compatible con DirectX.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la representación de mezcla de vídeo](about-the-video-mixing-render.md)
</dt> </dl>

 

 



