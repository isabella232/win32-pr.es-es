---
title: Atributo de atribución VML
description: Atributo de atribución VML
ms.assetid: fc8276dc-8f61-42f4-b405-e92ca31e4637
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b22f157a1ccfc2337baa0bb5de747332bb78d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359382"
---
# <a name="vml-endangle-attribute"></a><span data-ttu-id="0c33a-103">Atributo de atribución VML</span><span class="sxs-lookup"><span data-stu-id="0c33a-103">VML EndAngle Attribute</span></span>

<span data-ttu-id="0c33a-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="0c33a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="0c33a-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="0c33a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="0c33a-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="0c33a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="0c33a-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="0c33a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="0c33a-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="0c33a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="0c33a-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="0c33a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="0c33a-110">Define el extremo del arco. Lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="0c33a-110">Defines the endpoint of the arc. Read/write.</span></span> <span data-ttu-id="0c33a-111">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="0c33a-111">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md) .</span></span>

<span data-ttu-id="0c33a-112">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="0c33a-112">**Applies To**</span></span>

[<span data-ttu-id="0c33a-113">Arc</span><span class="sxs-lookup"><span data-stu-id="0c33a-113">Arc</span></span>](msdn-online-vml-arc-element.md)

<span data-ttu-id="0c33a-114">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="0c33a-114">**Tag Syntax**</span></span>

<span data-ttu-id="0c33a-115"><v: *elemento* dependiente = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="0c33a-115"><v: *element* endangle=" *expression* "></span></span>

<span data-ttu-id="0c33a-116">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="0c33a-116">**Script Syntax**</span></span>

<span data-ttu-id="0c33a-117">*elemento* . impuesto = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="0c33a-117">*element* .endAngle="*expression*"</span></span>

<span data-ttu-id="0c33a-118">*expresión* = de *elemento*. impuesto</span><span class="sxs-lookup"><span data-stu-id="0c33a-118">*expression*=*element*.endAngle</span></span>

<span data-ttu-id="0c33a-119">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="0c33a-119">**Remarks**</span></span>

<span data-ttu-id="0c33a-120">El arco se define como un trazo dibujado a lo largo de un óvalo limitado por los atributos de **estilo** de una forma.</span><span class="sxs-lookup"><span data-stu-id="0c33a-120">The arc is defined as a stroke drawn along an oval bounded by the **Style** attributes of a shape.</span></span> <span data-ttu-id="0c33a-121">El final del trazo se define mediante un ángulo medido desde la derecha hacia arriba (12 en la izquierda).</span><span class="sxs-lookup"><span data-stu-id="0c33a-121">The end of the stroke is defined by an angle measured from straight up (12 o'clock) clockwise.</span></span> <span data-ttu-id="0c33a-122">El valor predeterminado es 90 grados.</span><span class="sxs-lookup"><span data-stu-id="0c33a-122">The default value is 90 degrees.</span></span>

<span data-ttu-id="0c33a-123">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="0c33a-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="0c33a-124">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="0c33a-124">**Example**</span></span>

<span data-ttu-id="0c33a-125">El arco es sonriente.</span><span class="sxs-lookup"><span data-stu-id="0c33a-125">The arc is smiling.</span></span> <span data-ttu-id="0c33a-126">El punto de inicio se encuentra en el punto de 90 de una elipse inscrita dentro del cuadro de límite de la forma.</span><span class="sxs-lookup"><span data-stu-id="0c33a-126">The start point is at the 90-degree point of an oval inscribed inside the shape bounding box.</span></span> <span data-ttu-id="0c33a-127">El punto final se encuentra en el punto de 270 grados del óvalo.</span><span class="sxs-lookup"><span data-stu-id="0c33a-127">The end point is at the 270-degree point of the oval.</span></span>


```HTML
   <v:arc id="myarc"
   style="position:relative;top:10;left:10;width:200;height:200"
   startangle="90" endangle="270">
   </v:arc>
```



 

 