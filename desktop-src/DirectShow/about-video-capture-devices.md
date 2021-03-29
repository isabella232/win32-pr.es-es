---
description: Acerca de los dispositivos de captura de vídeo
ms.assetid: 1bf6e64f-c3cf-45a4-9f87-1b8cf503d98b
title: Acerca de los dispositivos de captura de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98ab9797c11b5c22f6196a5b4e781e50ce34edec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805930"
---
# <a name="about-video-capture-devices"></a>Acerca de los dispositivos de captura de vídeo

La mayoría de los dispositivos de captura de vídeo nuevos usan controladores Modelo de controlador de Windows (WDM). En la arquitectura de WDM, Microsoft proporciona un conjunto de controladores independientes del hardware, denominados controladores de clase, y el proveedor de hardware proporciona los minicontroladores específicos de hardware. Un minicontrolador implementa las funciones que son específicas del dispositivo; para la mayoría de las funciones, el minicontrolador llama al controlador de clases de Microsoft.

En un gráfico de filtros de DirectShow, cualquier dispositivo de captura WDM aparece como el filtro de [captura de vídeo WDM](wdm-video-capture-filter.md) . El filtro de captura de vídeo WDM se configura a sí mismo en función de las características del controlador. Aparece bajo un nombre proporcionado por el controlador; no verá un filtro denominado "filtro de captura de vídeo WDM" en cualquier lugar del gráfico.

Algunos dispositivos antiguos de captura siguen usando los controladores de vídeo para Windows (VFW). Aunque estos controladores están ahora obsoletos, se admiten en DirectShow a través del filtro de [captura VFW](vfw-capture-filter.md) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la captura de vídeo en DirectShow](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



