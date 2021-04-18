---
title: Atributo de Font-Variant VML
description: Atributo de Font-Variant VML
ms.assetid: f58bf3e0-e285-474c-83b1-203fce4f3c3a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 243f8b36d36d8bb9b210a916cef239cda6061e0f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420781"
---
# <a name="vml-font-variant-attribute"></a><span data-ttu-id="74361-103">Atributo de Font-Variant VML</span><span class="sxs-lookup"><span data-stu-id="74361-103">VML Font-Variant Attribute</span></span>

<span data-ttu-id="74361-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="74361-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="74361-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="74361-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="74361-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="74361-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="74361-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="74361-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="74361-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="74361-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="74361-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="74361-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="74361-110">Define el estilo variante de una fuente.</span><span class="sxs-lookup"><span data-stu-id="74361-110">Defines the variant style of a font.</span></span> <span data-ttu-id="74361-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="74361-111">Read/write.</span></span> <span data-ttu-id="74361-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="74361-112">**String**.</span></span>

<span data-ttu-id="74361-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="74361-113">**Applies To**</span></span>

[<span data-ttu-id="74361-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="74361-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="74361-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="74361-115">**Tag Syntax**</span></span>

<span data-ttu-id="74361-116"><v: *Element* style = "font-variant: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="74361-116"><v: *element* style="font-variant: *expression* "></span></span>

<span data-ttu-id="74361-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="74361-117">**Script Syntax**</span></span>

<span data-ttu-id="74361-118">*Element* . Style. fontVariant = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="74361-118">*element* .style.fontvariant="*expression*"</span></span>

<span data-ttu-id="74361-119">*expresión* = de *Element*. Style. fontVariant</span><span class="sxs-lookup"><span data-stu-id="74361-119">*expression*=*element*.style.fontvariant</span></span>

<span data-ttu-id="74361-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="74361-120">**Remarks**</span></span>

<span data-ttu-id="74361-121">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="74361-121">The values are:</span></span>

-   <span data-ttu-id="74361-122">normal (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="74361-122">normal (default)</span></span>
-   <span data-ttu-id="74361-123">versalitas</span><span class="sxs-lookup"><span data-stu-id="74361-123">small-caps</span></span>

<span data-ttu-id="74361-124">Los valores son los mismos que los atributos de estilo HTML estándar.</span><span class="sxs-lookup"><span data-stu-id="74361-124">The values are the same as the standard HTML style attributes.</span></span>

<span data-ttu-id="74361-125">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="74361-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="74361-126">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="74361-126">**Example**</span></span>

<span data-ttu-id="74361-127">La fuente se representa como pequeña letra mayúscula.</span><span class="sxs-lookup"><span data-stu-id="74361-127">The font is rendered as small capital letters.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal small-caps normal 36pt Arial"/>
   </v:line>
```



 

 