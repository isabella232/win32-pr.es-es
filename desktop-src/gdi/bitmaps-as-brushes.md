---
description: Un número de funciones usa el pincel seleccionado actualmente en un contexto de dispositivo para realizar operaciones de mapa de bits.
ms.assetid: 98fb2fd5-9cf4-4016-9e30-ec724e77cebc
title: Mapas de bits como pinceles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c693e3c144dec2d26eccca1f1b628252dea187c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276021"
---
# <a name="bitmaps-as-brushes"></a><span data-ttu-id="fbb9c-103">Mapas de bits como pinceles</span><span class="sxs-lookup"><span data-stu-id="fbb9c-103">Bitmaps as Brushes</span></span>

<span data-ttu-id="fbb9c-104">Un número de funciones usa el pincel seleccionado actualmente en un contexto de dispositivo para realizar operaciones de mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="fbb9c-104">A number of functions use the brush currently selected into a device context to perform bitmap operations.</span></span> <span data-ttu-id="fbb9c-105">Por ejemplo, la función [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) replica el pincel en una región rectangular dentro de una ventana y la función [**FloodFill**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill) replica el pincel dentro de un área de una ventana enlazada por el color especificado (a diferencia de **PatBlt**, **FloodFill** no rellena formas no rectangulares).</span><span class="sxs-lookup"><span data-stu-id="fbb9c-105">For example, the [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) function replicates the brush in a rectangular region within a window, and the [**FloodFill**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill) function replicates the brush inside an area in a window bounded by the specified color (unlike **PatBlt**, **FloodFill** does fill nonrectangular shapes).</span></span>

<span data-ttu-id="fbb9c-106">La función [**FloodFill**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill) replica el pincel dentro de una región limitada por un color especificado.</span><span class="sxs-lookup"><span data-stu-id="fbb9c-106">The [**FloodFill**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill) function replicates the brush within a region bounded by a specified color.</span></span> <span data-ttu-id="fbb9c-107">Sin embargo, a diferencia de la función [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) , **FloodFill** no combina los datos de color del pincel con los datos de color de los píxeles de la pantalla. simplemente establece el color de todos los píxeles de la región incluida en la pantalla en el color del pincel seleccionado actualmente en el contexto del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fbb9c-107">However, unlike the [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) function, **FloodFill** does not combine the color data for the brush with the color data for the pixels on the display; it simply sets the color of all pixels within the enclosed region on the display to the color of the brush that is currently selected into the device context.</span></span>

 

 



