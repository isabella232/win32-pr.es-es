---
description: Para copiar un mapa de bits en un paralelogramo; Use la función PlgBlt, que realiza una transferencia de bloque de bits de un rectángulo en un contexto de dispositivo de origen a un paralelogramo en un contexto de dispositivo de destino.
ms.assetid: fd5b3d9f-fdce-485e-bff8-464d96b8db34
title: Rotación de mapas de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c8711189182646c55aee414ef92409a6de20ca3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997428"
---
# <a name="bitmap-rotation"></a><span data-ttu-id="efdc0-103">Rotación de mapas de bits</span><span class="sxs-lookup"><span data-stu-id="efdc0-103">Bitmap Rotation</span></span>

<span data-ttu-id="efdc0-104">Para copiar un mapa de bits en un paralelogramo; Use la función [**PlgBlt**](/windows/desktop/api/Wingdi/nf-wingdi-plgblt) , que realiza una transferencia de bloque de bits de un rectángulo en un contexto de dispositivo de origen a un paralelogramo en un contexto de dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="efdc0-104">To copy a bitmap into a parallelogram; use the [**PlgBlt**](/windows/desktop/api/Wingdi/nf-wingdi-plgblt) function, which performs a bit-block transfer from a rectangle in a source device context into a parallelogram in a destination device context.</span></span> <span data-ttu-id="efdc0-105">Para girar el mapa de bits, una aplicación debe proporcionar las coordenadas, en unidades universales, que se usarán para las esquinas del paralelogramo.</span><span class="sxs-lookup"><span data-stu-id="efdc0-105">To rotate the bitmap, an application must provide the coordinates, in world units, to be used for the corners of the parallelogram.</span></span> <span data-ttu-id="efdc0-106">(Para obtener más información sobre la rotación y las unidades universales, vea [espacios de coordenadas y transformaciones](coordinate-spaces-and-transformations.md)).</span><span class="sxs-lookup"><span data-stu-id="efdc0-106">(For more information about rotation and world units, see [Coordinate Spaces and Transformations](coordinate-spaces-and-transformations.md).)</span></span>

 

 



