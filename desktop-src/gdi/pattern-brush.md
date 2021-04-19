---
description: Se crea un pincel de patrón (o personalizado) a partir de un mapa de bits definido por la aplicación o un mapa de bits independiente del dispositivo (DIB). Los siguientes rectángulos se han pintado mediante diferentes pinceles de patrón.
ms.assetid: 0de89a6f-d9c7-4f33-8088-c24a48a3ceee
title: Pincel de patrón
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66d39dd499d6a95b3fb61624b2aab8b421f51c34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988282"
---
# <a name="pattern-brush"></a><span data-ttu-id="a60e7-104">Pincel de patrón</span><span class="sxs-lookup"><span data-stu-id="a60e7-104">Pattern Brush</span></span>

<span data-ttu-id="a60e7-105">Se crea un pincel de patrón (o personalizado) a partir de un mapa de bits definido por la aplicación o un mapa de bits independiente del dispositivo (DIB).</span><span class="sxs-lookup"><span data-stu-id="a60e7-105">A pattern (or custom) brush is created from an application-defined bitmap or device-independent bitmap (DIB).</span></span> <span data-ttu-id="a60e7-106">Los siguientes rectángulos se han pintado mediante diferentes pinceles de patrón.</span><span class="sxs-lookup"><span data-stu-id="a60e7-106">The following rectangles were painted by using different pattern brushes.</span></span>

![Ilustración que muestra tres cuadros, cada uno rellenado con un patrón diferente](images/csbru-05.png)

<span data-ttu-id="a60e7-108">Para crear un pincel de patrón lógico, una aplicación debe crear primero un mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="a60e7-108">To create a logical pattern brush, an application must first create a bitmap.</span></span> <span data-ttu-id="a60e7-109">Después de crear el mapa de bits, la aplicación puede crear el pincel del modelo lógico mediante una llamada a la función [**CreatePatternBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush) o [**CreateDIBPatternBrushPt**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt) , proporcionando un identificador que identifica el mapa de bits (o DIB).</span><span class="sxs-lookup"><span data-stu-id="a60e7-109">After creating the bitmap, the application can create the logical pattern brush by calling the [**CreatePatternBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush) or [**CreateDIBPatternBrushPt**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt) function, supplying a handle that identifies the bitmap (or DIB).</span></span> <span data-ttu-id="a60e7-110">Los pinceles que aparecen en la ilustración anterior se crearon a partir de mapas de bits monocromáticos.</span><span class="sxs-lookup"><span data-stu-id="a60e7-110">The brushes that appear in the preceding illustration were created from monochrome bitmaps.</span></span> <span data-ttu-id="a60e7-111">Para obtener una descripción de los mapas de bits, DIB y las funciones que los crean, vea [mapas de bits](bitmaps.md).</span><span class="sxs-lookup"><span data-stu-id="a60e7-111">For a description of bitmaps, DIBs, and the functions that create them, see [Bitmaps](bitmaps.md).</span></span>

 

 



