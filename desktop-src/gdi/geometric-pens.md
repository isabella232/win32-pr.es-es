---
description: Las dimensiones de un lápiz geométrico se especifican en unidades lógicas.
ms.assetid: e7030490-d10c-4d1c-87ae-5b4cc4858ee1
title: Lápices geométricos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9725f6440f62458d4c87232400f16e27f9b978ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997365"
---
# <a name="geometric-pens"></a><span data-ttu-id="630d8-103">Lápices geométricos</span><span class="sxs-lookup"><span data-stu-id="630d8-103">Geometric Pens</span></span>

<span data-ttu-id="630d8-104">Las dimensiones de un lápiz geométrico se especifican en unidades lógicas.</span><span class="sxs-lookup"><span data-stu-id="630d8-104">The dimensions of a geometric pen are specified in logical units.</span></span> <span data-ttu-id="630d8-105">Por lo tanto, las líneas dibujadas con un lápiz geométrico se pueden escalar, es decir, pueden aparecer más anchas o más estrechas, dependiendo de la transformación universal actual.</span><span class="sxs-lookup"><span data-stu-id="630d8-105">Therefore, lines drawn with a geometric pen can be scaled that is, they may appear wider or narrower, depending on the current world transformation.</span></span> <span data-ttu-id="630d8-106">Para obtener más información sobre la transformación universal, vea [espacios de coordenadas y transformaciones](coordinate-spaces-and-transformations.md).</span><span class="sxs-lookup"><span data-stu-id="630d8-106">For more information about world transformation, see [Coordinate Spaces and Transformations](coordinate-spaces-and-transformations.md).</span></span>

<span data-ttu-id="630d8-107">Además de los tres atributos compartidos con los lápices estéticos (ancho, estilo y color), los lápices geométricos poseen los cuatro atributos siguientes: patrón, trama opcional, estilo de extremo y estilo de combinación.</span><span class="sxs-lookup"><span data-stu-id="630d8-107">In addition to the three attributes shared with cosmetic pens (width, style, and color), geometric pens possess the following four attributes: pattern, optional hatch, end style, and join style.</span></span> <span data-ttu-id="630d8-108">Para obtener más información sobre estos atributos, vea [Pen Attributes](pen-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="630d8-108">For more information about these attributes, see [Pen Attributes](pen-attributes.md).</span></span>

<span data-ttu-id="630d8-109">Para crear un lápiz geométrico, una aplicación utiliza la función [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) .</span><span class="sxs-lookup"><span data-stu-id="630d8-109">To create a geometric pen, an application uses the [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) function.</span></span> <span data-ttu-id="630d8-110">Al igual que con los lápices estéticos, la función [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) selecciona una plumilla geométrica en el controlador de dominio de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="630d8-110">As with cosmetic pens, the [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) function selects a geometric pen into the application's DC.</span></span>

 

 



