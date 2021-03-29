---
title: Atributo de ángulo (relleno) (VML)
description: Atributo de ángulo (relleno) (VML)
ms.assetid: 97203e73-4dae-40c5-bb3d-127110525cff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4167c52d82fabc5804143966b13f9d24ff7b39d6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078280"
---
# <a name="angle-attribute-fillvml"></a><span data-ttu-id="6ce99-103">Atributo de ángulo (relleno) (VML)</span><span class="sxs-lookup"><span data-stu-id="6ce99-103">Angle Attribute (Fill)(VML)</span></span>

<span data-ttu-id="6ce99-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="6ce99-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="6ce99-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="6ce99-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="6ce99-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="6ce99-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="6ce99-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="6ce99-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="6ce99-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="6ce99-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="6ce99-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="6ce99-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="6ce99-110">Define el ángulo de un relleno de degradado.</span><span class="sxs-lookup"><span data-stu-id="6ce99-110">Defines the angle of a gradient fill.</span></span> <span data-ttu-id="6ce99-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6ce99-111">Read/write.</span></span> <span data-ttu-id="6ce99-112">[VgAngle](msdn-online-vml-vgangleindegrees-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="6ce99-112">[VgAngle](msdn-online-vml-vgangleindegrees-data-type.md) .</span></span>

<span data-ttu-id="6ce99-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="6ce99-113">**Applies To**</span></span>

[<span data-ttu-id="6ce99-114">Fill</span><span class="sxs-lookup"><span data-stu-id="6ce99-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="6ce99-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="6ce99-115">**Tag Syntax**</span></span>

<span data-ttu-id="6ce99-116"><v: *elemento* Angle = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="6ce99-116"><v: *element* angle=" *expression* "></span></span>

<span data-ttu-id="6ce99-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="6ce99-117">**Script Syntax**</span></span>

<span data-ttu-id="6ce99-118">*Element* . Angle = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="6ce99-118">*element* .angle="*expression*"</span></span>

<span data-ttu-id="6ce99-119">*expresión* = de *elemento*. Angle</span><span class="sxs-lookup"><span data-stu-id="6ce99-119">*expression*=*element*.angle</span></span>

<span data-ttu-id="6ce99-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="6ce99-120">**Remarks**</span></span>

<span data-ttu-id="6ce99-121">El vector de un degradado es perpendicular al vector de la dirección de combinación de un color a otro.</span><span class="sxs-lookup"><span data-stu-id="6ce99-121">The vector of a gradient is perpendicular to the vector of the blend direction from one color to another.</span></span> <span data-ttu-id="6ce99-122">El valor predeterminado es 0 (cero) grados, que es un vector horizontal de izquierda a derecha.</span><span class="sxs-lookup"><span data-stu-id="6ce99-122">The default value is 0 (zero) degrees, which is a horizontal vector from left to right.</span></span> <span data-ttu-id="6ce99-123">Los ángulos positivos giran el degradado en sentido contrario a las agujas del reloj.</span><span class="sxs-lookup"><span data-stu-id="6ce99-123">Positive angles rotate the gradient in a counter-clockwise direction.</span></span>

<span data-ttu-id="6ce99-124">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="6ce99-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="6ce99-125">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="6ce99-125">**Example**</span></span>

<span data-ttu-id="6ce99-126">El relleno de la forma se compone de un degradado de dos colores, que se ejecuta de azul a rojo a un ángulo de 45 grados.</span><span class="sxs-lookup"><span data-stu-id="6ce99-126">The fill of the shape is composed of a gradient of two colors, running from blue to red at an angle of 45 degrees.</span></span> <span data-ttu-id="6ce99-127">El color rojo estará en la esquina superior izquierda y el azul estará en la esquina inferior derecha.</span><span class="sxs-lookup"><span data-stu-id="6ce99-127">Red will be in the top left corner and blue will be in the bottom right corner.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="blue" color2="red" angle="45"/>
   </v:shape>
```



 

 