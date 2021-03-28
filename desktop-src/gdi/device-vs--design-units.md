---
description: Una aplicación puede recuperar las métricas de fuente de una fuente física solo después de que se haya seleccionado la fuente en un contexto de dispositivo.
ms.assetid: 3eaabc8b-e244-4b65-918b-a20043afa535
title: Dispositivo frente a unidades de diseño
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fb52a671727a2fa84d5514b469be5bd320f3318
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908496"
---
# <a name="device-vs-design-units"></a><span data-ttu-id="6ce47-103">Dispositivo frente a unidades de diseño</span><span class="sxs-lookup"><span data-stu-id="6ce47-103">Device vs. Design Units</span></span>

<span data-ttu-id="6ce47-104">Una aplicación puede recuperar las métricas de fuente de una fuente física solo después de que se haya seleccionado la fuente en un contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6ce47-104">An application can retrieve font metrics for a physical font only after the font has been selected into a device context.</span></span> <span data-ttu-id="6ce47-105">Cuando se selecciona una fuente en un contexto de dispositivo, se escala para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6ce47-105">When a font is selected into a device context, it is scaled for the device.</span></span> <span data-ttu-id="6ce47-106">Las métricas de fuente específicas del dispositivo se conocen como unidades de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6ce47-106">The font metrics specific to the device are known as device units.</span></span>

<span data-ttu-id="6ce47-107">Las métricas portátiles en fuentes se conocen como unidades de diseño.</span><span class="sxs-lookup"><span data-stu-id="6ce47-107">Portable metrics in fonts are known as design units.</span></span> <span data-ttu-id="6ce47-108">Para aplicar a un dispositivo especificado, las unidades de diseño deben convertirse en unidades de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6ce47-108">To apply to a specified device, design units must be converted to device units.</span></span> <span data-ttu-id="6ce47-109">Utilice la siguiente fórmula para convertir las unidades de diseño en unidades de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6ce47-109">Use the following formula to convert design units to device units.</span></span>

<span data-ttu-id="6ce47-110">*DeviceUnits* = (*DesignUnits* / *unitsPerEm*) \* (*puntuación*/72) \* *DeviceResolution*</span><span class="sxs-lookup"><span data-stu-id="6ce47-110">*DeviceUnits* = (*DesignUnits*/*unitsPerEm*) \* (*PointSize*/72) \* *DeviceResolution*</span></span>

<span data-ttu-id="6ce47-111">Las variables de esta fórmula tienen los significados siguientes.</span><span class="sxs-lookup"><span data-stu-id="6ce47-111">The variables in this formula have the following meanings.</span></span>



| <span data-ttu-id="6ce47-112">Variable</span><span class="sxs-lookup"><span data-stu-id="6ce47-112">Variable</span></span>           | <span data-ttu-id="6ce47-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ce47-113">Description</span></span>                                                                                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ce47-114">*DeviceUnits*</span><span class="sxs-lookup"><span data-stu-id="6ce47-114">*DeviceUnits*</span></span>      | <span data-ttu-id="6ce47-115">Especifica la métrica de fuente *DesignUnits* convertida en unidades de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6ce47-115">Specifies the *DesignUnits* font metric converted to device units.</span></span> <span data-ttu-id="6ce47-116">Este valor se encuentra en las mismas unidades que el valor especificado para *DeviceResolution*.</span><span class="sxs-lookup"><span data-stu-id="6ce47-116">This value is in the same units as the value specified for *DeviceResolution*.</span></span>                          |
| <span data-ttu-id="6ce47-117">*DesignUnits*</span><span class="sxs-lookup"><span data-stu-id="6ce47-117">*DesignUnits*</span></span>      | <span data-ttu-id="6ce47-118">Especifica la métrica de fuente que se va a convertir en unidades de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6ce47-118">Specifies the font metric to be converted to device units.</span></span> <span data-ttu-id="6ce47-119">Este valor puede ser cualquier métrica de fuente, incluido el ancho de un carácter o el valor ascendente de una fuente completa.</span><span class="sxs-lookup"><span data-stu-id="6ce47-119">This value can be any font metric, including the width of a character or the ascender value for an entire font.</span></span> |
| <span data-ttu-id="6ce47-120">*unitsPerEm*</span><span class="sxs-lookup"><span data-stu-id="6ce47-120">*unitsPerEm*</span></span>       | <span data-ttu-id="6ce47-121">Especifica el tamaño del cuadrado em de la fuente.</span><span class="sxs-lookup"><span data-stu-id="6ce47-121">Specifies the em square size for the font.</span></span>                                                                                                                                 |
| <span data-ttu-id="6ce47-122">*PointSize*</span><span class="sxs-lookup"><span data-stu-id="6ce47-122">*PointSize*</span></span>        | <span data-ttu-id="6ce47-123">Especifica el tamaño de la fuente, en puntos.</span><span class="sxs-lookup"><span data-stu-id="6ce47-123">Specifies size of the font, in points.</span></span> <span data-ttu-id="6ce47-124">(Un punto es igual a 1/72 de pulgada).</span><span class="sxs-lookup"><span data-stu-id="6ce47-124">(One point equals 1/72 of an inch.)</span></span>                                                                                                 |
| <span data-ttu-id="6ce47-125">*DeviceResolution*</span><span class="sxs-lookup"><span data-stu-id="6ce47-125">*DeviceResolution*</span></span> | <span data-ttu-id="6ce47-126">Especifica el número de unidades de dispositivo (píxeles) por pulgada.</span><span class="sxs-lookup"><span data-stu-id="6ce47-126">Specifies number of device units (pixels) per inch.</span></span> <span data-ttu-id="6ce47-127">Los valores típicos pueden ser 300 para una impresora láser o 96 para una pantalla VGA.</span><span class="sxs-lookup"><span data-stu-id="6ce47-127">Typical values might be 300 for a laser printer or 96 for a VGA screen.</span></span>                                                |



 

<span data-ttu-id="6ce47-128">Esta fórmula no debe utilizarse para volver a convertir las unidades de dispositivo en unidades de diseño.</span><span class="sxs-lookup"><span data-stu-id="6ce47-128">This formula should not be used to convert device units back to design units.</span></span> <span data-ttu-id="6ce47-129">Las unidades de dispositivo siempre se redondean al píxel más cercano.</span><span class="sxs-lookup"><span data-stu-id="6ce47-129">Device units are always rounded to the nearest pixel.</span></span> <span data-ttu-id="6ce47-130">El error de redondeo propagado puede llegar a ser muy grande, sobre todo cuando una aplicación trabaja con tamaños de pantalla.</span><span class="sxs-lookup"><span data-stu-id="6ce47-130">The propagated round-off error can become very large, especially when an application is working with screen sizes.</span></span>

<span data-ttu-id="6ce47-131">Para solicitar unidades de diseño, cree una fuente lógica cuyo alto se especifique como *unitsPerEm*.</span><span class="sxs-lookup"><span data-stu-id="6ce47-131">To request design units, create a logical font whose height is specified as *unitsPerEm*.</span></span> <span data-ttu-id="6ce47-132">Las aplicaciones pueden recuperar el valor de *unitsPerEm* llamando a la función [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) y comprobando el miembro **ntmSizeEM** de la estructura [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) .</span><span class="sxs-lookup"><span data-stu-id="6ce47-132">Applications can retrieve the value for *unitsPerEm* by calling the [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) function and checking the **ntmSizeEM** member of the [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) structure.</span></span>

 

 



