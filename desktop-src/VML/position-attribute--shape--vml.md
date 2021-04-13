---
title: Posición (atributo, forma) (VML)
description: Posición (atributo, forma) (VML)
ms.assetid: 64ffe754-298b-4cf1-a236-6a4bdcd27123
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 866c14817ff6ac741b7fb41b1331f6d9ae32d069
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421363"
---
# <a name="position-attribute-shapevml"></a><span data-ttu-id="49678-103">Posición (atributo, forma) (VML)</span><span class="sxs-lookup"><span data-stu-id="49678-103">Position Attribute (Shape)(VML)</span></span>

<span data-ttu-id="49678-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="49678-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="49678-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="49678-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="49678-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="49678-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="49678-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="49678-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="49678-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="49678-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="49678-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="49678-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="49678-110">Define el tipo de posición utilizado para colocar un elemento.</span><span class="sxs-lookup"><span data-stu-id="49678-110">Defines the type of positioning used to place an element.</span></span> <span data-ttu-id="49678-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="49678-111">Read/write.</span></span> <span data-ttu-id="49678-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="49678-112">**String**.</span></span>

<span data-ttu-id="49678-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="49678-113">**Applies To**</span></span>

[<span data-ttu-id="49678-114">Forma</span><span class="sxs-lookup"><span data-stu-id="49678-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="49678-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="49678-115">**Tag Syntax**</span></span>

<span data-ttu-id="49678-116"><v: *Element* style = "Position: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="49678-116"><v: *element* style="position: *expression* "></span></span>

<span data-ttu-id="49678-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="49678-117">**Script Syntax**</span></span>

<span data-ttu-id="49678-118">*Element* . Style. position = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="49678-118">*element* .style.position="*expression*"</span></span>

<span data-ttu-id="49678-119">*expresión* = de *Element*. Style. Position</span><span class="sxs-lookup"><span data-stu-id="49678-119">*expression*=*element*.style.position</span></span>

<span data-ttu-id="49678-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="49678-120">**Remarks**</span></span>

<span data-ttu-id="49678-121">El atributo **Position** es similar al atributo **Position** HTML estándar que se usa con las hojas de estilos.</span><span class="sxs-lookup"><span data-stu-id="49678-121">The **Position** attribute is similar to the standard HTML **Position** attribute used with style sheets.</span></span>

<span data-ttu-id="49678-122">Estos valores incluyen:</span><span class="sxs-lookup"><span data-stu-id="49678-122">Values include:</span></span>



| <span data-ttu-id="49678-123">Value</span><span class="sxs-lookup"><span data-stu-id="49678-123">Value</span></span>    | <span data-ttu-id="49678-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="49678-124">Description</span></span>                                                                                                                                                                                                               |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49678-125">static</span><span class="sxs-lookup"><span data-stu-id="49678-125">static</span></span>   | <span data-ttu-id="49678-126">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="49678-126">Default.</span></span> <span data-ttu-id="49678-127">El elemento se coloca según el flujo normal de la página.</span><span class="sxs-lookup"><span data-stu-id="49678-127">The element is positioned according to the normal flow of the page.</span></span> <span data-ttu-id="49678-128">Se omiten los atributos **superior** e **izquierdo** .</span><span class="sxs-lookup"><span data-stu-id="49678-128">The **Top** and **Left** attributes are ignored.</span></span> <span data-ttu-id="49678-129">Si el objeto está delimitado en línea, que solo ocurre en Microsoft Word, se usa este valor.</span><span class="sxs-lookup"><span data-stu-id="49678-129">If the object is anchored inline, which only happens in Microsoft Word, this value is used.</span></span> |
| <span data-ttu-id="49678-130">absolute</span><span class="sxs-lookup"><span data-stu-id="49678-130">absolute</span></span> | <span data-ttu-id="49678-131">El elemento se coloca en relación con el elemento primario, utilizando los atributos **superior** e **izquierdo** .</span><span class="sxs-lookup"><span data-stu-id="49678-131">The element is positioned relative to the parent, using the **Top** and **Left** attributes.</span></span> <span data-ttu-id="49678-132">Este valor lo usan los objetos flotantes de Microsoft Word y Microsoft Excel, y las diapositivas de Microsoft PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="49678-132">This value is used by Microsoft Word and Microsoft Excel floating objects, and Microsoft PowerPoint slides.</span></span>                  |
| <span data-ttu-id="49678-133">relative</span><span class="sxs-lookup"><span data-stu-id="49678-133">relative</span></span> | <span data-ttu-id="49678-134">El elemento se coloca según el flujo normal de la página, pero se utilizan los atributos **superior** e **izquierdo** .</span><span class="sxs-lookup"><span data-stu-id="49678-134">The element is positioned according to the normal flow of the page, but the **Top** and **Left** attributes are used.</span></span> <span data-ttu-id="49678-135">La superposición de los elementos superpuestos se rige por el atributo **Z-index** .</span><span class="sxs-lookup"><span data-stu-id="49678-135">The overlap of overlapping elements is governed by the **Z-Index** attribute.</span></span>                       |



 

<span data-ttu-id="49678-136">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="49678-136">*VML Standard Attribute*</span></span>

<span data-ttu-id="49678-137">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="49678-137">**Example**</span></span>

<span data-ttu-id="49678-138">La posición del rectángulo se muestra utilizando el estilo *relativo* .</span><span class="sxs-lookup"><span data-stu-id="49678-138">The position of the rectangle is displayed using the *relative* style.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="49678-139">[Ejemplo de atributo de posición](/previous-versions/bb264090(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="49678-139">[Position Attribute Example](/previous-versions/bb264090(v=vs.85)).</span></span> <span data-ttu-id="49678-140">(Requiere Microsoft Internet Explorer 5 o posterior).</span><span class="sxs-lookup"><span data-stu-id="49678-140">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 