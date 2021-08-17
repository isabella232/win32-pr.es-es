---
description: La función StretchBlt escala un mapa de bits realizando una transferencia de bloque de bits desde un rectángulo de un contexto de dispositivo de origen a un rectángulo en un contexto de dispositivo de destino.
ms.assetid: 34390ff9-8d5f-497e-87aa-a1019d01bba6
title: Escalado de mapa de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14975f884906fb95bf07fbf3ab5277b89c5cbfd2612864202eb64eedc5df646b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117699903"
---
# <a name="bitmap-scaling"></a>Escalado de mapa de bits

La [**función StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) escala un mapa de bits realizando una transferencia de bloque de bits desde un rectángulo de un contexto de dispositivo de origen a un rectángulo en un contexto de dispositivo de destino. Sin embargo, a diferencia de la función [**BitBlt,**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) que duplica las dimensiones del rectángulo de origen en el rectángulo de destino, **StretchBlt** permite a una aplicación especificar las dimensiones de los rectángulos de origen y de destino. Cuando el mapa de bits de destino es menor que el mapa de bits de origen, el sistema combina filas o columnas de datos de color (o ambos) en el mapa de bits antes de representar la imagen correspondiente en el dispositivo para mostrar. El sistema combina los datos de color según el modo de ajuste especificado, que la aplicación define mediante una llamada a la [**función SetStretchBltMode.**](/windows/desktop/api/Wingdi/nf-wingdi-setstretchbltmode) Cuando el mapa de bits de destino es mayor que el mapa de bits de origen, el sistema escala o amplía cada píxel de la imagen resultante en consecuencia.

 

 



