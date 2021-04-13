---
title: Atributo alternativo VML
description: Atributo alternativo VML
ms.assetid: 6b7e778c-d8e2-432e-b69a-5d80fa62d105
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b420d556e69ed2f987a3a3b10a5709f926dc5c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104271353"
---
# <a name="vml-alt-attribute"></a><span data-ttu-id="396af-103">Atributo alternativo VML</span><span class="sxs-lookup"><span data-stu-id="396af-103">VML Alt Attribute</span></span>

<span data-ttu-id="396af-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="396af-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="396af-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="396af-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="396af-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="396af-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="396af-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="396af-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="396af-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="396af-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="396af-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="396af-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="396af-110">Define el texto alternativo que se va a mostrar en lugar de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="396af-110">Defines alternative text to be displayed instead of a graphic.</span></span> <span data-ttu-id="396af-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="396af-111">Read/write.</span></span> <span data-ttu-id="396af-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="396af-112">**String**.</span></span>

<span data-ttu-id="396af-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="396af-113">**Applies To**</span></span>

[<span data-ttu-id="396af-114">Forma</span><span class="sxs-lookup"><span data-stu-id="396af-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="396af-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="396af-115">**Tag Syntax**</span></span>

<span data-ttu-id="396af-116"><v: *elemento* Alt = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="396af-116"><v: *element* alt=" *expression* "></span></span>

<span data-ttu-id="396af-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="396af-117">**Script Syntax**</span></span>

<span data-ttu-id="396af-118">*Element* . Alt = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="396af-118">*element* .alt="*expression*"</span></span>

<span data-ttu-id="396af-119">*expresión* = de *elemento*. Alt</span><span class="sxs-lookup"><span data-stu-id="396af-119">*expression*=*element*.alt</span></span>

<span data-ttu-id="396af-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="396af-120">**Remarks**</span></span>

<span data-ttu-id="396af-121">El atributo **Alt** es similar al atributo **Alt** de HTML estándar.</span><span class="sxs-lookup"><span data-stu-id="396af-121">The **Alt** attribute is similar to the standard HTML **Alt** attribute.</span></span> <span data-ttu-id="396af-122">Este atributo proporciona una manera para que los exploradores que convierten texto en voz describan los elementos gráficos de una página.</span><span class="sxs-lookup"><span data-stu-id="396af-122">This attribute provides a way for browsers that convert text to speech to describe graphical elements on a page.</span></span>

<span data-ttu-id="396af-123">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="396af-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="396af-124">**Vea también**</span><span class="sxs-lookup"><span data-stu-id="396af-124">**See Also**</span></span>

[<span data-ttu-id="396af-125">Forma</span><span class="sxs-lookup"><span data-stu-id="396af-125">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="396af-126">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="396af-126">**Example**</span></span>

<span data-ttu-id="396af-127">En el elemento **Alt** siguiente se mostrará la frase "rectángulo rojo" en los exploradores que convierten las páginas web en frases habladas.</span><span class="sxs-lookup"><span data-stu-id="396af-127">The **Alt** element below will display the phrase "Red rectangle" in browsers that convert Web pages to spoken phrases.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" alt="Red rectangle"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="396af-128">[Ejemplo del atributo ALT](/previous-versions/bb229663(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="396af-128">[Alt Attribute Example](/previous-versions/bb229663(v=vs.85)).</span></span> <span data-ttu-id="396af-129">(Requiere Microsoft Internet Explorer 5 o posterior).</span><span class="sxs-lookup"><span data-stu-id="396af-129">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 