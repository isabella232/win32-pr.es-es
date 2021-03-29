---
title: VML V-Text-inverso (atributo)
description: VML V-Text-inverso (atributo)
ms.assetid: ad302b0f-5d93-457d-a8df-c9fce184475e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d2625439d4b7a767a21de3578a7b15d3115a8f5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078057"
---
# <a name="vml-v-text-reverse-attribute"></a><span data-ttu-id="4c3f5-103">VML V-Text-inverso (atributo)</span><span class="sxs-lookup"><span data-stu-id="4c3f5-103">VML V-Text-Reverse Attribute</span></span>

<span data-ttu-id="4c3f5-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="4c3f5-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="4c3f5-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="4c3f5-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="4c3f5-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="4c3f5-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="4c3f5-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="4c3f5-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="4c3f5-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="4c3f5-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="4c3f5-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="4c3f5-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="4c3f5-110">Determina si se invierte el orden de diseño de las filas.</span><span class="sxs-lookup"><span data-stu-id="4c3f5-110">Determines whether the layout order of rows is reversed.</span></span> <span data-ttu-id="4c3f5-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4c3f5-111">Read/write.</span></span> <span data-ttu-id="4c3f5-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="4c3f5-112">**VgTriState**.</span></span>

<span data-ttu-id="4c3f5-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="4c3f5-113">**Applies To**</span></span>

[<span data-ttu-id="4c3f5-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="4c3f5-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="4c3f5-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="4c3f5-115">**Tag Syntax**</span></span>

<span data-ttu-id="4c3f5-116"><v: *Element* style = "v-Text-Reverse: *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="4c3f5-116"><v: *element* style="v-text-reverse: *expression* "></span></span>

<span data-ttu-id="4c3f5-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="4c3f5-117">**Script Syntax**</span></span>

<span data-ttu-id="4c3f5-118">*Element* . Style. v-Text-REVERSE = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="4c3f5-118">*element* .style.v-text-reverse="*expression*"</span></span>

<span data-ttu-id="4c3f5-119">*expresión* = de *Element*. Style. v-Text-Reverse</span><span class="sxs-lookup"><span data-stu-id="4c3f5-119">*expression*=*element*.style.v-text-reverse</span></span>

<span data-ttu-id="4c3f5-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="4c3f5-120">**Remarks**</span></span>

<span data-ttu-id="4c3f5-121">Si es **true**, se invierte el orden de diseño de las filas.</span><span class="sxs-lookup"><span data-stu-id="4c3f5-121">If **True**, the layout order of rows is reversed.</span></span> <span data-ttu-id="4c3f5-122">Este atributo se usa para el diseño de texto vertical.</span><span class="sxs-lookup"><span data-stu-id="4c3f5-122">This attribute is used for vertical text layout.</span></span> <span data-ttu-id="4c3f5-123">El valor predeterminado es **False**.</span><span class="sxs-lookup"><span data-stu-id="4c3f5-123">The default value is **False**.</span></span>

<span data-ttu-id="4c3f5-124">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="4c3f5-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="4c3f5-125">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="4c3f5-125">**Example**</span></span>

<span data-ttu-id="4c3f5-126">Se invierte el orden de diseño.</span><span class="sxs-lookup"><span data-stu-id="4c3f5-126">The layout order is reversed.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-reverse:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 