---
description: Las paletas de semitonos están pensadas para usarse siempre que el modo de estiramiento de un contexto de dispositivo se establezca en semitonos.
ms.assetid: ee171379-2ab3-4c38-8e86-ff80fa63a357
title: Paleta de semitono y ajuste de color
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b3e6708aff92387b792424f07e9b82a1f6125ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544478"
---
# <a name="halftone-palette-and-color-adjustment"></a><span data-ttu-id="d0e1f-103">Paleta de semitono y ajuste de color</span><span class="sxs-lookup"><span data-stu-id="d0e1f-103">Halftone Palette and Color Adjustment</span></span>

<span data-ttu-id="d0e1f-104">Las paletas de semitonos están pensadas para usarse siempre que el modo de estiramiento de un contexto de dispositivo se establezca en semitonos.</span><span class="sxs-lookup"><span data-stu-id="d0e1f-104">Halftone palettes are intended to be used whenever the stretching mode of a device context is set to HALFTONE.</span></span> <span data-ttu-id="d0e1f-105">Una aplicación crea una paleta de semitonos mediante la función [**CreateHalftonePalette**](/windows/desktop/api/Wingdi/nf-wingdi-createhalftonepalette) .</span><span class="sxs-lookup"><span data-stu-id="d0e1f-105">An application creates a halftone palette by using the [**CreateHalftonePalette**](/windows/desktop/api/Wingdi/nf-wingdi-createhalftonepalette) function.</span></span> <span data-ttu-id="d0e1f-106">La aplicación debe seleccionar y obtener esta paleta en el contexto del dispositivo antes de llamar a la función [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) o [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) .</span><span class="sxs-lookup"><span data-stu-id="d0e1f-106">The application must select and realize this palette into the device context before calling the [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) or [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) function.</span></span>

<span data-ttu-id="d0e1f-107">El sistema ajusta automáticamente el color de entrada de los mapas de bits de origen cada vez que las aplicaciones llaman a las funciones [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) y [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) y el modo de ajuste de un contexto de dispositivo se establece en semitonos.</span><span class="sxs-lookup"><span data-stu-id="d0e1f-107">The system automatically adjusts the input color of source bitmaps whenever applications call the [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) and [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) functions and the stretching mode of a device context is set to HALFTONE.</span></span> <span data-ttu-id="d0e1f-108">Estos ajustes de color afectan a ciertos atributos de la imagen, como el contraste y el brillo.</span><span class="sxs-lookup"><span data-stu-id="d0e1f-108">These color adjustments affect certain attributes of the image, such as contrast and brightness.</span></span> <span data-ttu-id="d0e1f-109">Una aplicación puede establecer los valores de ajuste de color mediante la función [**SetColorAdjustment**](/windows/desktop/api/Wingdi/nf-wingdi-setcoloradjustment) .</span><span class="sxs-lookup"><span data-stu-id="d0e1f-109">An application can set the color adjustment values by using the [**SetColorAdjustment**](/windows/desktop/api/Wingdi/nf-wingdi-setcoloradjustment) function.</span></span> <span data-ttu-id="d0e1f-110">La aplicación puede recuperar los valores de ajuste de color para el contexto de dispositivo especificado mediante la función [**GetColorAdjustment**](/windows/desktop/api/Wingdi/nf-wingdi-getcoloradjustment) .</span><span class="sxs-lookup"><span data-stu-id="d0e1f-110">The application can retrieve the color adjustment values for the specified device context by using the [**GetColorAdjustment**](/windows/desktop/api/Wingdi/nf-wingdi-getcoloradjustment) function.</span></span>

 

 



