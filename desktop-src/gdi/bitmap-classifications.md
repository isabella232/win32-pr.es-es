---
description: Clasificaciones de mapa de bits
ms.assetid: 669ffaef-55c5-4cbc-b23a-de3d66bd6ab2
title: Clasificaciones de mapa de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69e7942b6c5c133da5107eec37e14e9a7e707d5993f212063b1939e56abe0da8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966425"
---
# <a name="bitmap-classifications"></a>Clasificaciones de mapa de bits

Hay dos clases de mapas de bits:

-   [Mapas de bits independientes del dispositivo](device-independent-bitmaps.md) (DIB). El formato de archivo DIB se diseñó para garantizar que los gráficos con mapa de bits creados con una aplicación se puedan cargar y mostrar en otra aplicación, conservando la misma apariencia que el original.

-   Los mapas de bits [dependientes](device-dependent-bitmaps.md) del dispositivo (DDB), también conocidos como mapas de bits GDI, eran los únicos mapas de bits disponibles en las primeras versiones de Microsoft Windows de 16 bits (antes de la versión 3.0). Sin embargo, a medida que la tecnología de visualización mejoró y a medida que aumentaba la variedad de dispositivos de pantalla disponibles, se mostraron ciertos problemas inherentes que solo se podían resolver mediante DIB. Por ejemplo, no había ningún método para almacenar (o recuperar) la resolución del tipo de pantalla en el que se creó un mapa de bits, por lo que una aplicación de dibujo no pudo determinar rápidamente si un mapa de bits era adecuado para el tipo de dispositivo de visualización de vídeo en el que se estaba ejecutando la aplicación.

    A pesar de estos problemas, las DDB (también conocidas como mapas de bits compatibles) siguen siendo útiles para mejorar el rendimiento de GDI y para otras situaciones.

 

 



