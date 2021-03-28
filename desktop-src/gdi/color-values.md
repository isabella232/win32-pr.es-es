---
description: El color se define como una combinación de tres colores primarios, rojo, verde y azul.
ms.assetid: 6e44935c-2b3b-4062-8273-f1f3e70300d2
title: Valores de color
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67e46cd7ee87871c660702bed120958e7096745d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155656"
---
# <a name="color-values"></a><span data-ttu-id="e334b-103">Valores de color</span><span class="sxs-lookup"><span data-stu-id="e334b-103">Color Values</span></span>

<span data-ttu-id="e334b-104">El color se define como una combinación de tres colores primarios, rojo, verde y azul.</span><span class="sxs-lookup"><span data-stu-id="e334b-104">Color is defined as a combination of three primary colors red, green, and blue.</span></span> <span data-ttu-id="e334b-105">el sistema identifica un color asignándole un valor de color (a veces denominado tripledo RGB), que consta de valores de 3 8 bits que especifican las intensidades de sus componentes de color.</span><span class="sxs-lookup"><span data-stu-id="e334b-105">the system identifies a color by giving it a color value (sometimes called an RGB triplet), which consists of three 8-bit values specifying the intensities of its color components.</span></span> <span data-ttu-id="e334b-106">Black tiene la intensidad mínima para rojo, verde y azul, por lo que el valor de color para Black es (0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="e334b-106">Black has the minimum intensity for red, green, and blue, so the color value for black is (0, 0, 0).</span></span> <span data-ttu-id="e334b-107">Blanco tiene la intensidad máxima de rojo, verde y azul, por lo que su valor de color es (255, 255, 255).</span><span class="sxs-lookup"><span data-stu-id="e334b-107">White has the maximum intensity for red, green, and blue, so its color value is (255, 255, 255).</span></span>

> [!Note]  
> <span data-ttu-id="e334b-108">Si la coincidencia de color de imagen está habilitada, la definición de color y el significado de un valor de color depende del tipo de espacio de colores que está establecido actualmente para el contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e334b-108">If image color matching is enabled, the definition of color and the meaning of a color value depends on the type of color space that is currently set for the device context.</span></span>

 

<span data-ttu-id="e334b-109">El sistema y las aplicaciones usan parámetros y variables que tienen el tipo [COLORREF](colorref.md) para pasar y almacenar los valores de color.</span><span class="sxs-lookup"><span data-stu-id="e334b-109">The system and applications use parameters and variables having the [COLORREF](colorref.md) type to pass and store color values.</span></span> <span data-ttu-id="e334b-110">Por ejemplo, la función [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) identifica el color de cada lápiz estableciendo el miembro **lopnColor** de una estructura [**logpen (**](/windows/win32/api/wingdi/ns-wingdi-logpen) en un valor de color.</span><span class="sxs-lookup"><span data-stu-id="e334b-110">For example, the [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) function identifies the color of each pen by setting the **lopnColor** member in a [**LOGPEN**](/windows/win32/api/wingdi/ns-wingdi-logpen) structure to a color value.</span></span> <span data-ttu-id="e334b-111">Las aplicaciones pueden extraer los valores individuales de los componentes rojo, verde y azul de un valor de color mediante el uso de las macros [**GetRValue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue), [**GetGValue**](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue)y [**GetBValue**](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="e334b-111">Applications can extract the individual values of the red, green, and blue components from a color value by using the [**GetRValue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue), [**GetGValue**](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue), and [**GetBValue**](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue) macros, respectively.</span></span> <span data-ttu-id="e334b-112">Las aplicaciones pueden crear un valor de color a partir de valores de componentes individuales mediante la macro [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) .</span><span class="sxs-lookup"><span data-stu-id="e334b-112">Applications can create a color value from individual component values by using the [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) macro.</span></span> <span data-ttu-id="e334b-113">Al crear o examinar una paleta lógica, una aplicación utiliza la estructura [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) para definir los valores de color y para examinar los valores de los componentes individuales.</span><span class="sxs-lookup"><span data-stu-id="e334b-113">When creating or examining a logical palette, an application uses the [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) structure to define color values and to examine individual component values.</span></span>

 

 



