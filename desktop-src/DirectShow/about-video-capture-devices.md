---
description: Acerca de los dispositivos de captura de vídeo
ms.assetid: 1bf6e64f-c3cf-45a4-9f87-1b8cf503d98b
title: Acerca de los dispositivos de captura de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff3fff9f3d009006e300afdbe9986bfdc8d0a32ea618fdd2748efe0bd650b5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118160188"
---
# <a name="about-video-capture-devices"></a>Acerca de los dispositivos de captura de vídeo

La mayoría de los nuevos dispositivos de captura de vídeo usan controladores Windows Driver Model (WDM). En la arquitectura wdm, Microsoft proporciona un conjunto de controladores independientes del hardware, denominados controladores de clase, y el proveedor de hardware proporciona minidriveres específicos del hardware. Un minidriver implementa todas las funciones que son específicas del dispositivo; para la mayoría de las funciones, el minidriver llama al controlador de clase de Microsoft.

En un gráfico DirectShow filtro, cualquier dispositivo de captura wdm aparece como filtro de captura [de vídeo de WDM.](wdm-video-capture-filter.md) El filtro captura de vídeo de WDM se configura en función de las características del controlador. Aparece con un nombre proporcionado por el controlador: no verá un filtro denominado "Filtro de captura de vídeo WDM" en ninguna parte del gráfico.

Algunos dispositivos de captura más antiguos siguen utilizando Video Windows controladores de Windows (VFW). Aunque estos controladores ahora están obsoletos, se admiten en DirectShow a través del filtro [de captura de VFW.](vfw-capture-filter.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la captura de vídeo en DirectShow](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



