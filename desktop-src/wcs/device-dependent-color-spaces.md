---
title: Espacios de color dependientes del dispositivo
description: La mayoría de los espacios de colores dependen del dispositivo.
ms.assetid: 657ec64b-8605-4d05-a7d6-9f8bb71e6a71
keywords:
- Sistema de color de Windows (WCS), espacios de colores dependientes del dispositivo
- WCS (sistema de colores de Windows), espacios de colores dependientes del dispositivo
- Administración del color de imagen, espacios de colores dependientes del dispositivo
- Administración del color, espacios de colores dependientes del dispositivo
- colores, espacios de colores dependientes del dispositivo
- espacios de colores, dependientes del dispositivo
- espacios de colores dependientes del dispositivo
- punto blanco
- colorants
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22a1523ee6ba81dcdc3b69a468546871cfd21913
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/26/2021
ms.locfileid: "105721129"
---
# <a name="device-dependent-color-spaces"></a><span data-ttu-id="39e3b-112">Espacios de color dependientes del dispositivo</span><span class="sxs-lookup"><span data-stu-id="39e3b-112">Device-Dependent Color Spaces</span></span>

<span data-ttu-id="39e3b-113">La mayoría de los [espacios de colores](c.md) dependen del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="39e3b-113">Most [color spaces](c.md) are device dependent.</span></span> <span data-ttu-id="39e3b-114">Aunque un dispositivo determinado, como una impresora, puede usar el espacio de colores CMYK, los colores que representa para valores CMYK específicos suelen ser ligeramente diferentes de los demás tipos de impresoras.</span><span class="sxs-lookup"><span data-stu-id="39e3b-114">Even though a particular device, such as a printer, may use the CMYK color space, the colors it renders for specific CMYK values are often slightly different than all other types of printers..</span></span> <span data-ttu-id="39e3b-115">Por esta razón, el sistema de administración del color WCS 1,0 es tan útil.</span><span class="sxs-lookup"><span data-stu-id="39e3b-115">It is precisely for this reason that the WCS 1.0 color management system is so useful.</span></span>

<span data-ttu-id="39e3b-116">Todos los espacios de colores tienen un *punto blanco*, que se define como el blanco más blanco que se puede producir en ese espacio de colores.</span><span class="sxs-lookup"><span data-stu-id="39e3b-116">All color spaces have a *white point*, which is defined as the whitest white that can be produced in that color space.</span></span> <span data-ttu-id="39e3b-117">Dado que los dispositivos pueden diferir entre sí, sus puntos blancos también pueden ser diferentes.</span><span class="sxs-lookup"><span data-stu-id="39e3b-117">Since devices can differ from one another, their white points can also differ.</span></span> <span data-ttu-id="39e3b-118">Todos los colores que un dispositivo puede producir son relativos a su punto blanco.</span><span class="sxs-lookup"><span data-stu-id="39e3b-118">All colors that a device can produce are relative to its white point.</span></span> <span data-ttu-id="39e3b-119">Por lo tanto, un sistema de administración del color debe ser capaz de asignar el punto blanco de un espacio de colores a otro y conservar las ubicaciones relativas de todos los colores.</span><span class="sxs-lookup"><span data-stu-id="39e3b-119">Therefore, a color management system must be able to map the white point of one color space into another and preserve the relative locations of all colors.</span></span> <span data-ttu-id="39e3b-120">También debe poder asignar un color de un espacio de colores a la coincidencia más cercana en otro espacio de colores, independientemente de las diferencias en los puntos blancos.</span><span class="sxs-lookup"><span data-stu-id="39e3b-120">It must also be able to map a color in one color space to its closest match in another color space regardless of the differences in the white points.</span></span> <span data-ttu-id="39e3b-121">WCS 1,0 puede realizar ambas tareas.</span><span class="sxs-lookup"><span data-stu-id="39e3b-121">WCS 1.0 is able to accomplish both of these tasks.</span></span>

<span data-ttu-id="39e3b-122">El espacio de colores RGB se usa a menudo en monitores de equipos.</span><span class="sxs-lookup"><span data-stu-id="39e3b-122">The RGB color space is often used on computer monitors.</span></span> <span data-ttu-id="39e3b-123">Como tal, depende del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="39e3b-123">As such, it is device dependent.</span></span> <span data-ttu-id="39e3b-124">Las impresoras suelen usar [COLORANTS](c.md)CMYK.</span><span class="sxs-lookup"><span data-stu-id="39e3b-124">Printers typically use CMYK [colorants](c.md).</span></span> <span data-ttu-id="39e3b-125">Cada impresora implementa su propia versión del espacio de colores CMYK.</span><span class="sxs-lookup"><span data-stu-id="39e3b-125">Each printer implements its own version of the CMYK color space.</span></span> <span data-ttu-id="39e3b-126">Es posible que las imágenes digitales no almacenen realmente colores en ellas.</span><span class="sxs-lookup"><span data-stu-id="39e3b-126">Digital images may not actually store colors in them.</span></span> <span data-ttu-id="39e3b-127">Pueden almacenar números de índice en una paleta de colores.</span><span class="sxs-lookup"><span data-stu-id="39e3b-127">They may store index numbers into a palette of colors.</span></span> <span data-ttu-id="39e3b-128">El resultado es que es muy difícil para los desarrolladores de aplicaciones individuales usar o proporcionar un método estandarizado para mover imágenes de color de un dispositivo a otro.</span><span class="sxs-lookup"><span data-stu-id="39e3b-128">The result is that it is very hard for individual application developers to use or provide a standardized method of moving color images from one device to another.</span></span> <span data-ttu-id="39e3b-129">Los profesionales de la creación de imágenes suelen experimentar la frustración de la creación de una imagen gráfica en la pantalla de un equipo y de que se convierta de forma muy diferente cuando se imprima.</span><span class="sxs-lookup"><span data-stu-id="39e3b-129">Imaging professionals commonly experience the frustration of creating a graphic image on a computer screen and having it turn out very differently when it is printed.</span></span> <span data-ttu-id="39e3b-130">WCS 1,0 aborda estas necesidades de creación de imágenes.</span><span class="sxs-lookup"><span data-stu-id="39e3b-130">WCS 1.0 addresses these imaging needs.</span></span>

 

 




