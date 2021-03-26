---
description: Para crear un mapa de bits, use las funciones CreateBitmap, CreateBitmapIndirect o CreateCompatibleBitmap, CreateDIBitmap y CreateDiscardableBitmap.
ms.assetid: 313072fc-68c9-4ece-95bb-2748ccbd7f57
title: Creación de mapas de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d00a0bc5a39d1b5e6053a34a87c28d6792a42b0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276025"
---
# <a name="bitmap-creation"></a><span data-ttu-id="2cf6b-103">Creación de mapas de bits</span><span class="sxs-lookup"><span data-stu-id="2cf6b-103">Bitmap Creation</span></span>

<span data-ttu-id="2cf6b-104">Para crear un mapa de bits, use las funciones [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap), [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect)o [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) , [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)y [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap).</span><span class="sxs-lookup"><span data-stu-id="2cf6b-104">To create a bitmap, use the [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap), [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect), or [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) function, [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap), and [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap).</span></span>

<span data-ttu-id="2cf6b-105">Estas funciones permiten especificar el ancho y el alto, en píxeles, del mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="2cf6b-105">These functions allow you to specify the width and height, in pixels, of the bitmap.</span></span> <span data-ttu-id="2cf6b-106">Las funciones [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) y [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect) también permiten especificar el número de planos de color y el número de bits necesarios para identificar el color.</span><span class="sxs-lookup"><span data-stu-id="2cf6b-106">The [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) and [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect) function also allow you to specify the number of color planes and the number of bits required to identify the color.</span></span> <span data-ttu-id="2cf6b-107">Por otro lado, las funciones [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) y [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap) utilizan un contexto de dispositivo especificado para obtener el número de planos de color y el número de bits necesarios para identificar el color.</span><span class="sxs-lookup"><span data-stu-id="2cf6b-107">On the other hand, the [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) and [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap) functions use a specified device context to obtain the number of color planes and the number of bits required to identify the color.</span></span>

<span data-ttu-id="2cf6b-108">La función [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap) crea un mapa de bits dependiente del dispositivo a partir de un mapa de bits independiente del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2cf6b-108">The [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap) function creates a device-dependent bitmap from a device-independent bitmap.</span></span> <span data-ttu-id="2cf6b-109">Contiene una tabla de colores que describe cómo se corresponden los valores de píxeles con los valores de color RGB.</span><span class="sxs-lookup"><span data-stu-id="2cf6b-109">It contains a color table that describes how pixel values correspond to RGB color values.</span></span> <span data-ttu-id="2cf6b-110">Para obtener más información, consulte [mapas de bits dependientes del dispositivo](device-dependent-bitmaps.md) y [mapas de bits independientes del dispositivo](device-independent-bitmaps.md).</span><span class="sxs-lookup"><span data-stu-id="2cf6b-110">For more information, see [Device-Dependent Bitmaps](device-dependent-bitmaps.md) and [Device-Independent Bitmaps](device-independent-bitmaps.md).</span></span>

<span data-ttu-id="2cf6b-111">Una vez creado el mapa de bits, no se puede cambiar su tamaño, el número de planos de color o el número de bits necesario para identificar el color.</span><span class="sxs-lookup"><span data-stu-id="2cf6b-111">After the bitmap has been created, you cannot change its size, number of color planes, or number of bits required to identify the color.</span></span>

<span data-ttu-id="2cf6b-112">Cuando ya no necesite un mapa de bits, llame a la función [**DeleteObject**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject) para eliminarlo.</span><span class="sxs-lookup"><span data-stu-id="2cf6b-112">When you no longer need a bitmap, call the [**DeleteObject**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject) function to delete it.</span></span>

 

 



