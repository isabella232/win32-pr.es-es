---
title: Atributo FitShape de VML
description: Atributo FitShape de VML
ms.assetid: a6e5a198-1478-4256-a4f2-b9ae6db6d7fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2b05d7bc31afc52c664217ff21d14b40fd0c27
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676505"
---
# <a name="vml-fitshape-attribute"></a><span data-ttu-id="4fe42-103">Atributo FitShape de VML</span><span class="sxs-lookup"><span data-stu-id="4fe42-103">VML FitShape Attribute</span></span>

<span data-ttu-id="4fe42-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="4fe42-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="4fe42-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="4fe42-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="4fe42-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="4fe42-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="4fe42-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="4fe42-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="4fe42-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="4fe42-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="4fe42-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="4fe42-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="4fe42-110">Define si el texto se ajusta al rectángulo de selección de una forma.</span><span class="sxs-lookup"><span data-stu-id="4fe42-110">Defines whether the text fits bounding box of a shape.</span></span> <span data-ttu-id="4fe42-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4fe42-111">Read/write.</span></span> <span data-ttu-id="4fe42-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="4fe42-112">**VgTriState**.</span></span>

<span data-ttu-id="4fe42-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="4fe42-113">**Applies To**</span></span>

[<span data-ttu-id="4fe42-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="4fe42-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="4fe42-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="4fe42-115">**Tag Syntax**</span></span>

<span data-ttu-id="4fe42-116"><v: *Element* fitshape = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="4fe42-116"><v: *element* fitshape=" *expression* "></span></span>

<span data-ttu-id="4fe42-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="4fe42-117">**Script Syntax**</span></span>

<span data-ttu-id="4fe42-118">*Element* . fitshape = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="4fe42-118">*element* .fitshape="*expression*"</span></span>

<span data-ttu-id="4fe42-119">*expresión* = de *elemento*. fitshape</span><span class="sxs-lookup"><span data-stu-id="4fe42-119">*expression*=*element*.fitshape</span></span>

<span data-ttu-id="4fe42-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="4fe42-120">**Remarks**</span></span>

<span data-ttu-id="4fe42-121">Si **es true**, ajusta el texto a los bordes del cuadro que define la forma completa.</span><span class="sxs-lookup"><span data-stu-id="4fe42-121">If **True**, stretches the text out to the edges of the box that defines the entire shape.</span></span> <span data-ttu-id="4fe42-122">El valor predeterminado es **False**.</span><span class="sxs-lookup"><span data-stu-id="4fe42-122">The default is **False**.</span></span>

<span data-ttu-id="4fe42-123">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="4fe42-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="4fe42-124">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="4fe42-124">**Example**</span></span>

<span data-ttu-id="4fe42-125">El texto se ajustará para ajustarse a la forma.</span><span class="sxs-lookup"><span data-stu-id="4fe42-125">The text will stretch to fit the shape.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text" fitshape="True"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 