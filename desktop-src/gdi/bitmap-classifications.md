---
description: Clasificaciones de mapas de bits
ms.assetid: 669ffaef-55c5-4cbc-b23a-de3d66bd6ab2
title: Clasificaciones de mapas de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9632b2617eda6fc94ec4836f0e0aa4cc927af113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276026"
---
# <a name="bitmap-classifications"></a>Clasificaciones de mapas de bits

Hay dos clases de mapas de bits:

-   [Mapas de bits independientes del dispositivo](device-independent-bitmaps.md) (DIB). El formato de archivo DIB se diseñó para asegurarse de que los gráficos de mapa Dete creados mediante una aplicación se pueden cargar y mostrar en otra aplicación, conservando el mismo aspecto que el original.

-   Los [mapas de bits dependientes del dispositivo](device-dependent-bitmaps.md) (DDB), también conocidos como mapas de bits GDI, eran los únicos mapas de bits disponibles en las primeras versiones de Microsoft Windows de 16 bits (antes de la versión 3,0). Sin embargo, a medida que la tecnología de visualización se ha mejorado y, a medida que aumenta el número de dispositivos de pantalla disponibles, se muestran algunos problemas inherentes que solo se pueden resolver mediante Dib. Por ejemplo, no había ningún método para almacenar (o recuperar) la resolución del tipo de presentación en el que se creó un mapa de bits, por lo que una aplicación de dibujo no podía determinar rápidamente si un mapa de bits era adecuado para el tipo de dispositivo de pantalla de vídeo en el que se ejecutaba la aplicación.

    A pesar de estos problemas, los DDBs (también conocidos como mapas de bits compatibles) siguen siendo útiles para mejorar el rendimiento de la GDI y para otras situaciones.

 

 



