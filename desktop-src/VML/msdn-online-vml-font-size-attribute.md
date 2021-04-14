---
title: Atributo de Font-Size VML
description: Atributo de Font-Size VML
ms.assetid: 49394cd5-3009-424a-97d3-28c85d874bc4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c02b2df8fb0076ed6df6342e40b980ed8aa248e5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488251"
---
# <a name="vml-font-size-attribute"></a><span data-ttu-id="c2b65-103">Atributo de Font-Size VML</span><span class="sxs-lookup"><span data-stu-id="c2b65-103">VML Font-Size Attribute</span></span>

<span data-ttu-id="c2b65-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c2b65-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c2b65-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="c2b65-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c2b65-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="c2b65-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c2b65-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="c2b65-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c2b65-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c2b65-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c2b65-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c2b65-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c2b65-110">Define el tamaño de la fuente.</span><span class="sxs-lookup"><span data-stu-id="c2b65-110">Defines the size of the font.</span></span> <span data-ttu-id="c2b65-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c2b65-111">Read/write.</span></span> <span data-ttu-id="c2b65-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="c2b65-112">**String**.</span></span>

<span data-ttu-id="c2b65-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="c2b65-113">**Applies To**</span></span>

[<span data-ttu-id="c2b65-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="c2b65-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="c2b65-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="c2b65-115">**Tag Syntax**</span></span>

<span data-ttu-id="c2b65-116"><v: *Element* style = "font-size: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="c2b65-116"><v: *element* style="font-size: *expression* "></span></span>

<span data-ttu-id="c2b65-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="c2b65-117">**Script Syntax**</span></span>

<span data-ttu-id="c2b65-118">*Element* . Style. FontSize = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="c2b65-118">*element* .style.fontsize="*expression*"</span></span>

<span data-ttu-id="c2b65-119">*expresión* = de *Element*. Style. FontSize</span><span class="sxs-lookup"><span data-stu-id="c2b65-119">*expression*=*element*.style.fontsize</span></span>

<span data-ttu-id="c2b65-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="c2b65-120">**Remarks**</span></span>

<span data-ttu-id="c2b65-121">El tamaño de fuente se define en puntos.</span><span class="sxs-lookup"><span data-stu-id="c2b65-121">The font size is defined in points.</span></span> <span data-ttu-id="c2b65-122">Los valores son los mismos que los atributos de estilo HTML estándar.</span><span class="sxs-lookup"><span data-stu-id="c2b65-122">The values are the same as the standard HTML style attributes.</span></span>

<span data-ttu-id="c2b65-123">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="c2b65-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="c2b65-124">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="c2b65-124">**Example**</span></span>

<span data-ttu-id="c2b65-125">El tamaño de fuente es de 36 puntos.</span><span class="sxs-lookup"><span data-stu-id="c2b65-125">The font size is 36 points.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 