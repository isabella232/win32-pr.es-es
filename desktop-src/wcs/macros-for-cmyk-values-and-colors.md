---
title: Macros para valores y colores CMYK
description: Las siguientes macros son útiles para manipular valores CMYK.
ms.assetid: e5d107fb-e010-400b-9ec5-90c2c0381dbe
keywords:
- Sistema de color de Windows (WCS), macros CMYK
- WCS (sistema de colores de Windows), macros CMYK
- Administración del color de imagen, macros CMYK
- Administración del color, macros CMYK
- colores, macros CMYK
- Referencia WCS, macros CMYK
- referencia de las macros WCS, CMYK
- CMYK (macros)
- Aguamarina fucsia amarillo negro (CMYK)
- CMYK (aguamarina fucsia amarillo negro)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a0efcbb6b0dc25f8f93f420113cc8c0797cba46
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/26/2021
ms.locfileid: "105721150"
---
# <a name="macros-for-cmyk-values-and-colors"></a><span data-ttu-id="03318-113">Macros para valores y colores CMYK</span><span class="sxs-lookup"><span data-stu-id="03318-113">Macros for CMYK Values and Colors</span></span>

<span data-ttu-id="03318-114">Las siguientes macros son útiles para manipular valores CMYK.</span><span class="sxs-lookup"><span data-stu-id="03318-114">The following macros are useful in manipulating CMYK values.</span></span>



| <span data-ttu-id="03318-115">Macro</span><span class="sxs-lookup"><span data-stu-id="03318-115">Macro</span></span>                          | <span data-ttu-id="03318-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="03318-116">Description</span></span>                                                                  |
|--------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="03318-117">**CMYK**</span><span class="sxs-lookup"><span data-stu-id="03318-117">**CMYK**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-cmyk)           | <span data-ttu-id="03318-118">Crea un valor CMYK a partir de los valores individuales de cian, magenta, amarillo y negro.</span><span class="sxs-lookup"><span data-stu-id="03318-118">Builds a CMYK value from individual cyan, magenta, yellow, and black values.</span></span> |
| [<span data-ttu-id="03318-119">**GetCValue**</span><span class="sxs-lookup"><span data-stu-id="03318-119">**GetCValue**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getcvalue) | <span data-ttu-id="03318-120">Recupera el valor de color aguamarina de un valor de color CMYK.</span><span class="sxs-lookup"><span data-stu-id="03318-120">Retrieves the cyan color value from a CMYK color value.</span></span>                      |
| [<span data-ttu-id="03318-121">**GetKValue**</span><span class="sxs-lookup"><span data-stu-id="03318-121">**GetKValue**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getkvalue) | <span data-ttu-id="03318-122">Recupera el valor de color negro de un valor de color CMYK.</span><span class="sxs-lookup"><span data-stu-id="03318-122">Retrieves the black color value from a CMYK color value.</span></span>                     |
| [<span data-ttu-id="03318-123">**GetMValue**</span><span class="sxs-lookup"><span data-stu-id="03318-123">**GetMValue**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getmvalue) | <span data-ttu-id="03318-124">Recupera el valor magenta de un valor de color CMYK.</span><span class="sxs-lookup"><span data-stu-id="03318-124">Retrieves the magenta value from a CMYK color value.</span></span>                         |
| [<span data-ttu-id="03318-125">**GetYValue**</span><span class="sxs-lookup"><span data-stu-id="03318-125">**GetYValue**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getyvalue) | <span data-ttu-id="03318-126">Recupera el valor de color amarillo de un valor de color CMYK.</span><span class="sxs-lookup"><span data-stu-id="03318-126">Retrieves the yellow color value from a CMYK color value.</span></span>                    |



 

<span data-ttu-id="03318-127">Las macros siguientes se utilizan con el color.</span><span class="sxs-lookup"><span data-stu-id="03318-127">The following macros are used with color.</span></span>



| <span data-ttu-id="03318-128">Macro</span><span class="sxs-lookup"><span data-stu-id="03318-128">Macro</span></span>                                | <span data-ttu-id="03318-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="03318-129">Description</span></span>                                                                                                                                           |
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="03318-130">**GetBValue**</span><span class="sxs-lookup"><span data-stu-id="03318-130">**GetBValue**</span></span>](/windows/win32/api/wingdi/nf-wingdi-getbvalue)       | <span data-ttu-id="03318-131">Obtiene un valor de color azul RGB.</span><span class="sxs-lookup"><span data-stu-id="03318-131">Gets an RGB blue value.</span></span>                                                                                                                               |
| [<span data-ttu-id="03318-132">**GetGValue**</span><span class="sxs-lookup"><span data-stu-id="03318-132">**GetGValue**</span></span>](/windows/win32/api/wingdi/nf-wingdi-getgvalue)       | <span data-ttu-id="03318-133">Obtiene un valor de color verde RGB.</span><span class="sxs-lookup"><span data-stu-id="03318-133">Gets an RGB green value.</span></span>                                                                                                                              |
| [<span data-ttu-id="03318-134">**GetRValue**</span><span class="sxs-lookup"><span data-stu-id="03318-134">**GetRValue**</span></span>](/windows/win32/api/wingdi/nf-wingdi-getrvalue)       | <span data-ttu-id="03318-135">Obtiene un valor rojo RGB.</span><span class="sxs-lookup"><span data-stu-id="03318-135">Gets an RGB red value.</span></span>                                                                                                                                |
| <span data-ttu-id="03318-136">[**PALETTEINDEX**](/previous-versions//dd162770(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="03318-136">[**PALETTEINDEX**](/previous-versions//dd162770(v=vs.85))</span></span> | <span data-ttu-id="03318-137">Acepta un índice para una entrada de la paleta de colores lógicos y devuelve un especificador de entrada de paleta.</span><span class="sxs-lookup"><span data-stu-id="03318-137">Accepts an index to a logical-color palette entry and returns a palette-entry specifier.</span></span>                                                              |
| [<span data-ttu-id="03318-138">**PALETTERGB**</span><span class="sxs-lookup"><span data-stu-id="03318-138">**PALETTERGB**</span></span>](/windows/win32/api/wingdi/nf-wingdi-palettergb)     | <span data-ttu-id="03318-139">Acepta tres valores que representan las intensidades relativas de rojo, verde y azul, y devuelve un especificador rojo, verde, azul (RGB) relativo a la paleta.</span><span class="sxs-lookup"><span data-stu-id="03318-139">Accepts three values that represent the relative intensities of red, green, and blue and returns a palette-relative red, green, blue (RGB) specifier.</span></span> |
| [<span data-ttu-id="03318-140">RGB</span><span class="sxs-lookup"><span data-stu-id="03318-140">RGB</span></span>](/windows/win32/api/wingdi/nf-wingdi-rgb)                       | <span data-ttu-id="03318-141">Selecciona un color rojo, verde y azul (RGB) en función de los argumentos proporcionados y las capacidades de color del dispositivo de salida.</span><span class="sxs-lookup"><span data-stu-id="03318-141">Selects a red, green, blue (RGB) color based on the arguments supplied and the color capabilities of the output device.</span></span>                               |



 

 

 