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
# <a name="bitmap-scaling"></a><span data-ttu-id="37dc0-103">Escala de mapas de bits</span><span class="sxs-lookup"><span data-stu-id="37dc0-103">Bitmap Scaling</span></span>

<span data-ttu-id="37dc0-104">La función [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) escala un mapa de bits mediante la realización de una transferencia de bloque de bits desde un rectángulo en un contexto de dispositivo de origen a un rectángulo en un contexto de dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="37dc0-104">The [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) function scales a bitmap by performing a bit-block transfer from a rectangle in a source device context into a rectangle in a destination device context.</span></span> <span data-ttu-id="37dc0-105">Sin embargo, a diferencia de la función [**bitblt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) , que duplica las dimensiones del rectángulo de origen en el rectángulo de destino, **StretchBlt** permite que una aplicación especifique las dimensiones de los rectángulos de origen y de destino.</span><span class="sxs-lookup"><span data-stu-id="37dc0-105">However, unlike the [**BitBlt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) function, which duplicates the source rectangle dimensions in the destination rectangle, **StretchBlt** allows an application to specify the dimensions of both the source and the destination rectangles.</span></span> <span data-ttu-id="37dc0-106">Cuando el mapa de bits de destino es menor que el mapa de bits de origen, el sistema combina filas o columnas de datos de color (o ambos) en el mapa de bits antes de representar la imagen correspondiente en el dispositivo de pantalla.</span><span class="sxs-lookup"><span data-stu-id="37dc0-106">When the destination bitmap is smaller than the source bitmap, the system combines rows or columns of color data (or both) in the bitmap before rendering the corresponding image on the display device.</span></span> <span data-ttu-id="37dc0-107">El sistema combina los datos de color según el modo de stretch especificado, que la aplicación define mediante una llamada a la función [**SetStretchBltMode**](/windows/desktop/api/Wingdi/nf-wingdi-setstretchbltmode) .</span><span class="sxs-lookup"><span data-stu-id="37dc0-107">The system combines the color data according to the specified stretch mode, which the application defines by calling the [**SetStretchBltMode**](/windows/desktop/api/Wingdi/nf-wingdi-setstretchbltmode) function.</span></span> <span data-ttu-id="37dc0-108">Cuando el mapa de bits de destino es mayor que el mapa de bits de origen, el sistema escala o amplía cada píxel de la imagen resultante en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="37dc0-108">When the destination bitmap is larger than the source bitmap, the system scales or magnifies each pixel in the resultant image accordingly.</span></span>

 

 



