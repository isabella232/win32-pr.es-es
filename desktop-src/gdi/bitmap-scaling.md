---
description: La función StretchBlt escala un mapa de bits mediante la realización de una transferencia de bloque de bits desde un rectángulo en un contexto de dispositivo de origen a un rectángulo en un contexto de dispositivo de destino.
ms.assetid: 34390ff9-8d5f-497e-87aa-a1019d01bba6
title: Escala de mapas de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4011b06e6a7269be29e1834e90928c4f531b1023
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155693"
---
# <a name="bitmap-scaling"></a>Escala de mapas de bits

La función [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) escala un mapa de bits mediante la realización de una transferencia de bloque de bits desde un rectángulo en un contexto de dispositivo de origen a un rectángulo en un contexto de dispositivo de destino. Sin embargo, a diferencia de la función [**bitblt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) , que duplica las dimensiones del rectángulo de origen en el rectángulo de destino, **StretchBlt** permite que una aplicación especifique las dimensiones de los rectángulos de origen y de destino. Cuando el mapa de bits de destino es menor que el mapa de bits de origen, el sistema combina filas o columnas de datos de color (o ambos) en el mapa de bits antes de representar la imagen correspondiente en el dispositivo de pantalla. El sistema combina los datos de color según el modo de stretch especificado, que la aplicación define mediante una llamada a la función [**SetStretchBltMode**](/windows/desktop/api/Wingdi/nf-wingdi-setstretchbltmode) . Cuando el mapa de bits de destino es mayor que el mapa de bits de origen, el sistema escala o amplía cada píxel de la imagen resultante en consecuencia.

 

 



