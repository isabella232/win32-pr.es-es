---
title: HRef (atributo, forma) (VML)
description: HRef (atributo, forma) (VML)
ms.assetid: c44b3099-df3f-42e5-ad0c-10400630e884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ecbc0f97ca2fb9c1565b712d3677d007a62b035
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078278"
---
# <a name="href-attribute-shapevml"></a><span data-ttu-id="bbc05-103">HRef (atributo, forma) (VML)</span><span class="sxs-lookup"><span data-stu-id="bbc05-103">HRef Attribute (Shape)(VML)</span></span>

<span data-ttu-id="bbc05-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="bbc05-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="bbc05-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="bbc05-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="bbc05-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="bbc05-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="bbc05-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="bbc05-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="bbc05-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="bbc05-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="bbc05-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="bbc05-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="bbc05-110">Define una dirección URL para una forma.</span><span class="sxs-lookup"><span data-stu-id="bbc05-110">Defines a URL for a shape.</span></span> <span data-ttu-id="bbc05-111">Al hacer clic en la forma, el explorador cargará la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="bbc05-111">When the shape is clicked, the browser will load the URL.</span></span> <span data-ttu-id="bbc05-112">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bbc05-112">Read/write.</span></span> <span data-ttu-id="bbc05-113">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="bbc05-113">**String**.</span></span>

<span data-ttu-id="bbc05-114">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="bbc05-114">**Applies To**</span></span>

[<span data-ttu-id="bbc05-115">Forma</span><span class="sxs-lookup"><span data-stu-id="bbc05-115">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="bbc05-116">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="bbc05-116">**Tag Syntax**</span></span>

<span data-ttu-id="bbc05-117"><v: *Element* href = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="bbc05-117"><v: *element* href=" *expression* "></span></span>

<span data-ttu-id="bbc05-118">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="bbc05-118">**Script Syntax**</span></span>

<span data-ttu-id="bbc05-119">*Element* . href = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="bbc05-119">*element* .href="*expression*"</span></span>

<span data-ttu-id="bbc05-120">*expresión* = de *elemento*. href</span><span class="sxs-lookup"><span data-stu-id="bbc05-120">*expression*=*element*.href</span></span>

<span data-ttu-id="bbc05-121">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="bbc05-121">**Remarks**</span></span>

<span data-ttu-id="bbc05-122">El atributo **href** es similar al atributo **href** de HTML estándar de los delimitadores.</span><span class="sxs-lookup"><span data-stu-id="bbc05-122">The **HRef** attribute is similar to the standard HTML **HRef** attribute of anchors.</span></span>

<span data-ttu-id="bbc05-123">El uso de **href** facilita la creación de botones interesantes en una página web.</span><span class="sxs-lookup"><span data-stu-id="bbc05-123">Using **HRef** makes it easy to create interesting buttons on a Web page.</span></span>

<span data-ttu-id="bbc05-124">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="bbc05-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="bbc05-125">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="bbc05-125">**Example**</span></span>

<span data-ttu-id="bbc05-126">Cuando se hace clic en el rectángulo, el explorador carga la Página principal de Microsoft Corporation.</span><span class="sxs-lookup"><span data-stu-id="bbc05-126">When the rectangle is clicked, the browser will load the Microsoft Corporation home page.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   href="https://www.microsoft.com"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
   
```



<span data-ttu-id="bbc05-127">[Ejemplo del atributo href](/previous-versions/bb229672(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bbc05-127">[HRef Attribute Example](/previous-versions/bb229672(v=vs.85)).</span></span> <span data-ttu-id="bbc05-128">(Requiere Microsoft Internet Explorer 5 o posterior).</span><span class="sxs-lookup"><span data-stu-id="bbc05-128">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 