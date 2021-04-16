---
title: Atributo Position (H) (VML)
description: Atributo Position (H) (VML)
ms.assetid: 0bae708d-5409-4609-a102-7f799f2c1fbb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac310c0fad457beaf3b9aeb04671b7ffbb1dbd8d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695734"
---
# <a name="position-attribute-hvml"></a><span data-ttu-id="0a982-103">Atributo Position (H) (VML)</span><span class="sxs-lookup"><span data-stu-id="0a982-103">Position Attribute (H)(VML)</span></span>

<span data-ttu-id="0a982-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="0a982-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="0a982-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="0a982-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="0a982-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="0a982-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="0a982-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="0a982-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="0a982-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="0a982-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="0a982-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="0a982-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="0a982-110">Especifica los valores TheX e y del identificador.</span><span class="sxs-lookup"><span data-stu-id="0a982-110">Specifies thex and y values of the handle.</span></span> <span data-ttu-id="0a982-111">**VgVector2D** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="0a982-111">Read/write **VgVector2D**.</span></span>

<span data-ttu-id="0a982-112">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="0a982-112">**Applies To**</span></span>

<span data-ttu-id="0a982-113">[H](msdn-online-vml-h-element.md) (subelemento de [Handles](msdn-online-vml-handles-element.md))</span><span class="sxs-lookup"><span data-stu-id="0a982-113">[H](msdn-online-vml-h-element.md) (subelement of [Handles](msdn-online-vml-handles-element.md))</span></span>

<span data-ttu-id="0a982-114">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="0a982-114">**Tag Syntax**</span></span>

<span data-ttu-id="0a982-115"><v: *elemento* position = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="0a982-115"><v: *element* position=" *expression* "></span></span>

<span data-ttu-id="0a982-116">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="0a982-116">**Remarks**</span></span>

<span data-ttu-id="0a982-117">los valores x e y pueden ser de uno de los tipos siguientes:</span><span class="sxs-lookup"><span data-stu-id="0a982-117">x and y values can be one of the following types:</span></span>

-   <span data-ttu-id="0a982-118">constant</span><span class="sxs-lookup"><span data-stu-id="0a982-118">constant</span></span>
-   <span data-ttu-id="0a982-119">fórmula (por ejemplo, @2 )</span><span class="sxs-lookup"><span data-stu-id="0a982-119">formula (for example, @2)</span></span>
-   <span data-ttu-id="0a982-120">ajustar (por ejemplo, \# 3)</span><span class="sxs-lookup"><span data-stu-id="0a982-120">adjust (for example, \#3)</span></span>
-   <span data-ttu-id="0a982-121">centro</span><span class="sxs-lookup"><span data-stu-id="0a982-121">center</span></span>
-   <span data-ttu-id="0a982-122">a la izquierda</span><span class="sxs-lookup"><span data-stu-id="0a982-122">topleft</span></span>
-   <span data-ttu-id="0a982-123">PivotDetailRange</span><span class="sxs-lookup"><span data-stu-id="0a982-123">bottomright</span></span>

<span data-ttu-id="0a982-124">Si se especifica cualquiera de los tipos anteriores, excepto *ADJUST* , la posición del identificador se fija en esa dimensión.</span><span class="sxs-lookup"><span data-stu-id="0a982-124">If any of the above types except *adjust* are specified, the handle position is fixed in that dimension.</span></span> <span data-ttu-id="0a982-125">Si se especifica un identificador de ajuste, el identificador es libre de mover en esa dimensión y el valor de ajuste viene determinado por la posición del identificador.</span><span class="sxs-lookup"><span data-stu-id="0a982-125">If an adjust handle is specified, the handle is free to move in that dimension and the adjust value is determined by the position of the handle.</span></span>

<span data-ttu-id="0a982-126">Si se especifica un atributo [polar](msdn-online-vml-polar-attribute.md) , el atributo **Position** representa los valores de radio y ángulo del controlador en lugar de x e y.</span><span class="sxs-lookup"><span data-stu-id="0a982-126">If a [Polar](msdn-online-vml-polar-attribute.md) attribute is specified, the **Position** attribute represents the radius and angle values of the handle instead of x and y.</span></span>

<span data-ttu-id="0a982-127">El valor predeterminado es 0,0.</span><span class="sxs-lookup"><span data-stu-id="0a982-127">The default value is 0,0.</span></span>

<span data-ttu-id="0a982-128">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="0a982-128">*VML Standard Attribute*</span></span>

 

 