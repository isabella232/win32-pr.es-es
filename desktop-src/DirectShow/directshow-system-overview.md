---
description: Información general del sistema DirectShow
ms.assetid: aea1ab83-4c48-4b61-8a20-0ee6ad62ebe3
title: Información general del sistema DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833fed4031c95ddb4ecbf91e7bb27c27741acc18
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536592"
---
# <a name="directshow-system-overview"></a>Información general del sistema DirectShow

**El reto de los elementos multimedia**

Trabajar con multimedia presenta varios desafíos principales:

-   Las secuencias multimedia contienen grandes cantidades de datos, que se deben procesar muy rápidamente.
-   El audio y el vídeo deben estar sincronizados para que se inicie y se detenga al mismo tiempo y se reproduzcan a la misma velocidad.
-   Los datos pueden provienen de varios orígenes, como archivos locales, redes de equipos, difusiones de televisión y cámaras de vídeo.
-   Los datos tienen una variedad de formatos, como Audio-Video intercalados (AVI), el formato de streaming avanzado (ASF), el grupo de expertos en imágenes de movimiento (MPEG) y vídeo digital (DV).
-   El programador no sabe de antemano qué dispositivos de hardware estarán presentes en el sistema del usuario final.

**La solución de DirectShow**

DirectShow está diseñado para abordar cada uno de estos desafíos. Su objetivo de diseño principal es simplificar la tarea de crear aplicaciones multimedia digitales en la plataforma Windows, aislando las aplicaciones de las complejidades de los transportes de datos, las diferencias de hardware y la sincronización.

Para lograr el rendimiento necesario para transmitir vídeo y audio, DirectShow usa Direct3D y DirectSound siempre que sea posible. Estas tecnologías representan los datos de forma eficaz en las tarjetas de sonido y gráficos del usuario. DirectShow sincroniza la reproducción encapsulando los datos multimedia en muestras con marca de tiempo. Para controlar la variedad de orígenes, formatos y dispositivos de hardware que son posibles, DirectShow utiliza una arquitectura modular, en la que la aplicación se mezcla y coincide con los distintos componentes de software denominados *filtros*.

DirectShow proporciona filtros que admiten dispositivos de captura y optimización basados en el Modelo de controlador de Windows (WDM), así como filtros que admiten tarjetas de captura antiguas de vídeo para Windows (VfW) y códecs escritos para las interfaces del administrador de compresión de audio (ACM) y el administrador de compresión de vídeo (VCM).

En el diagrama siguiente se muestra la relación entre una aplicación, los componentes de DirectShow y algunos de los componentes de hardware y software compatibles con DirectShow.

![arquitectura de alto nivel](images/arch-oview2.png)

Como se muestra aquí, los filtros de DirectShow se comunican con y controlan una amplia variedad de dispositivos, como el sistema de archivos local, tarjetas de captura de vídeo y sintonizador de TV, códecs VfW, la pantalla de vídeo (a través de DirectDraw o GDI) y la tarjeta de sonido (a través de DirectSound). Por lo tanto, DirectShow aísla la aplicación de muchas de las complejidades de estos dispositivos. DirectShow también proporciona filtros de compresión y descompresión nativos para determinados formatos de archivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de DirectShow](about-directshow.md)
</dt> </dl>

 

 



