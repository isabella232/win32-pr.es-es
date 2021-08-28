---
description: DirectShow Información general del sistema
ms.assetid: aea1ab83-4c48-4b61-8a20-0ee6ad62ebe3
title: DirectShow Información general del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0fb7855277029adc563cc032740d3a59b3691fcf12ed2b2595d37a1abd0d923
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966355"
---
# <a name="directshow-system-overview"></a>DirectShow Información general del sistema

**El desafío de multimedia**

Trabajar con multimedia presenta varios desafíos importantes:

-   Los flujos multimedia contienen grandes cantidades de datos, que se deben procesar muy rápidamente.
-   El audio y el vídeo deben sincronizarse para que se inicie y se detenga al mismo tiempo y se resalte a la misma velocidad.
-   Los datos pueden proceden de muchos orígenes, incluidos archivos locales, redes informáticas, difusión de televisión y cámaras de vídeo.
-   Los datos se incluyen en diversos formatos, como Audio-Video Interleaved (AVI), Advanced Streaming Format (ASF), Motion Picture Experts Group (MPEG) y Digital Video (DV).
-   El programador no sabe de antemano qué dispositivos de hardware estarán presentes en el sistema del usuario final.

**La DirectShow de seguridad**

DirectShow está diseñado para abordar cada uno de estos desafíos. Su objetivo de diseño principal es simplificar la tarea de crear aplicaciones multimedia digitales en la plataforma Windows, aislando las aplicaciones de las complejidades de los transportes de datos, las diferencias de hardware y la sincronización.

Para lograr el rendimiento necesario para transmitir vídeo y audio, DirectShow direct3D y Direct Sound siempre que sea posible. Estas tecnologías representan los datos de forma eficaz en las tarjetas de sonido y gráficos del usuario. DirectShow la reproducción mediante la encapsulación de datos multimedia en ejemplos con marca de tiempo. Para controlar la variedad de orígenes, formatos y dispositivos de hardware que son posibles, DirectShow usa una arquitectura modular, en la que la aplicación combina y coincide con distintos componentes de software denominados *filtros*.

DirectShow proporciona filtros que admiten dispositivos de captura y ajuste basados en el modelo de controlador de Windows (WDM), así como filtros que admiten tarjetas de captura de vídeo para Windows (VfW) anteriores y códecs escritos para las interfaces del Administrador de compresión de audio (ACM) y el Administrador de compresión de vídeo (VCM).

En el diagrama siguiente se muestra la relación entre una aplicación, los componentes DirectShow y algunos de los componentes de hardware y software que DirectShow admite.

![arquitectura de alto nivel](images/arch-oview2.png)

Como se muestra aquí, los filtros de DirectShow se comunican con una amplia variedad de dispositivos, entre los que se incluyen el sistema de archivos local, las tarjetas de captura de vídeo y de tv, los códecs VfW, la presentación de vídeo (a través de DirectDraw o GDI) y la tarjeta de sonido (a través de Direct Sound). Por lo tanto, DirectShow aísla la aplicación de muchas de las complejidades de estos dispositivos. DirectShow también proporciona filtros de compresión y descompresión nativos para determinados formatos de archivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de DirectShow](about-directshow.md)
</dt> </dl>

 

 



