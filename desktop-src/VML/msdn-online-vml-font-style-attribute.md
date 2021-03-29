---
title: Atributo de Font-Style VML
description: Atributo de Font-Style VML
ms.assetid: 3dfea8d0-d03b-46c0-b972-a529bc12b62c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f4fc2f299d78c3ccd8b194b8506cfce07abceb7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077826"
---
# <a name="vml-font-style-attribute"></a><span data-ttu-id="5fba4-103">Atributo de Font-Style VML</span><span class="sxs-lookup"><span data-stu-id="5fba4-103">VML Font-Style Attribute</span></span>

<span data-ttu-id="5fba4-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="5fba4-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="5fba4-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="5fba4-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="5fba4-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="5fba4-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="5fba4-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="5fba4-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="5fba4-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="5fba4-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="5fba4-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="5fba4-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="5fba4-110">Define la cantidad de inclinación de una fuente.</span><span class="sxs-lookup"><span data-stu-id="5fba4-110">Defines the amount of slant for a font.</span></span> <span data-ttu-id="5fba4-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5fba4-111">Read/write.</span></span> <span data-ttu-id="5fba4-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="5fba4-112">**String**.</span></span>

<span data-ttu-id="5fba4-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="5fba4-113">**Applies To**</span></span>

[<span data-ttu-id="5fba4-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="5fba4-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="5fba4-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="5fba4-115">**Tag Syntax**</span></span>

<span data-ttu-id="5fba4-116"><v: *Element* style = "font-style: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="5fba4-116"><v: *element* style="font-style: *expression* "></span></span>

<span data-ttu-id="5fba4-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="5fba4-117">**Script Syntax**</span></span>

<span data-ttu-id="5fba4-118">*Element* . Style. FontStyle = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="5fba4-118">*element* .style.fontstyle="*expression*"</span></span>

<span data-ttu-id="5fba4-119">*expresión* = de *Element*. Style. FontStyle</span><span class="sxs-lookup"><span data-stu-id="5fba4-119">*expression*=*element*.style.fontstyle</span></span>

<span data-ttu-id="5fba4-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="5fba4-120">**Remarks**</span></span>

<span data-ttu-id="5fba4-121">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="5fba4-121">The values are:</span></span>

-   <span data-ttu-id="5fba4-122">normal (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="5fba4-122">normal (default)</span></span>
-   <span data-ttu-id="5fba4-123">oblicuo</span><span class="sxs-lookup"><span data-stu-id="5fba4-123">oblique</span></span>
-   <span data-ttu-id="5fba4-124">cursiva</span><span class="sxs-lookup"><span data-stu-id="5fba4-124">italic</span></span>

<span data-ttu-id="5fba4-125">La mayoría de los exploradores representan oblicuo como cursiva.</span><span class="sxs-lookup"><span data-stu-id="5fba4-125">Most browsers render oblique as italic.</span></span> <span data-ttu-id="5fba4-126">Los valores son los mismos que los atributos de estilo HTML estándar.</span><span class="sxs-lookup"><span data-stu-id="5fba4-126">The values are the same as the standard HTML style attributes.</span></span>

<span data-ttu-id="5fba4-127">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="5fba4-127">*VML Standard Attribute*</span></span>

<span data-ttu-id="5fba4-128">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="5fba4-128">**Example**</span></span>

<span data-ttu-id="5fba4-129">La fuente está en cursiva (inclinada).</span><span class="sxs-lookup"><span data-stu-id="5fba4-129">The font is italic (slanted).</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:italic normal normal 36pt Arial"/>
   </v:line>
```



 

 