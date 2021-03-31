---
title: Atributo Offset2 de VML
description: Atributo Offset2 de VML
ms.assetid: a2792992-71a1-4932-8180-82ca38bd6dd2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4b5253e1a27ce8292ee5fc4ce49259db9512a5d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533436"
---
# <a name="vml-offset2-attribute"></a><span data-ttu-id="29b3f-103">Atributo Offset2 de VML</span><span class="sxs-lookup"><span data-stu-id="29b3f-103">VML Offset2 Attribute</span></span>

<span data-ttu-id="29b3f-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="29b3f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="29b3f-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="29b3f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="29b3f-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="29b3f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="29b3f-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="29b3f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="29b3f-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="29b3f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="29b3f-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="29b3f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="29b3f-110">Determina un segundo desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="29b3f-110">Determines a second offset.</span></span> <span data-ttu-id="29b3f-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="29b3f-111">Read/write.</span></span> <span data-ttu-id="29b3f-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="29b3f-112">**VgVector2D**.</span></span>

<span data-ttu-id="29b3f-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="29b3f-113">**Applies To**</span></span>

[<span data-ttu-id="29b3f-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="29b3f-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="29b3f-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="29b3f-115">**Tag Syntax**</span></span>

<span data-ttu-id="29b3f-116"><v: *Element* offset2 = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="29b3f-116"><v: *element* offset2=" *expression* "></span></span>

<span data-ttu-id="29b3f-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="29b3f-117">**Script Syntax**</span></span>

<span data-ttu-id="29b3f-118">*Element* . offset2 = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="29b3f-118">*element* .offset2="*expression*"</span></span>

<span data-ttu-id="29b3f-119">*expresión* = de *elemento*. offset2</span><span class="sxs-lookup"><span data-stu-id="29b3f-119">*expression*=*element*.offset2</span></span>

<span data-ttu-id="29b3f-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="29b3f-120">**Remarks**</span></span>

<span data-ttu-id="29b3f-121">El valor predeterminado para un segundo desplazamiento para el valor x es 0 y el valor predeterminado para el valor y es 0.</span><span class="sxs-lookup"><span data-stu-id="29b3f-121">The default for a second offset for the x value is 0 and the default for the y value is 0.</span></span> <span data-ttu-id="29b3f-122">Los valores son una medida absoluta o un valor fraccionario de forma.</span><span class="sxs-lookup"><span data-stu-id="29b3f-122">Values are either an absolute measurement, or a fractional value of shape.</span></span> <span data-ttu-id="29b3f-123">Si es fraccionario, los valores van de 50% a-50%.</span><span class="sxs-lookup"><span data-stu-id="29b3f-123">If fractional, the values range from 50% to -50%.</span></span>

<span data-ttu-id="29b3f-124">Use un segundo desplazamiento para crear efectos de sombra especiales.</span><span class="sxs-lookup"><span data-stu-id="29b3f-124">Use a second offset to create special shadow effects.</span></span> <span data-ttu-id="29b3f-125">Vea el atributo [Type](type-attribute--shadow--vml.md) para obtener más información sobre los dos desplazamientos.</span><span class="sxs-lookup"><span data-stu-id="29b3f-125">See the [Type](type-attribute--shadow--vml.md) attribute for more information about second offsets.</span></span>

<span data-ttu-id="29b3f-126">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="29b3f-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="29b3f-127">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="29b3f-127">**Example**</span></span>

<span data-ttu-id="29b3f-128">Se crea una sombra doble para la forma.</span><span class="sxs-lookup"><span data-stu-id="29b3f-128">A double shadow is created for the shape.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" color="red" color2="blue"
   offset="50%" offset2="-20%" type="double"/>
   </v:shape>
```



 

 