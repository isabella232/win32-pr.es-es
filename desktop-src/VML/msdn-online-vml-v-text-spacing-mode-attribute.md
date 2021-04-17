---
title: Atributo de modo de espaciado-texto (V) de VML
description: Atributo de modo de espaciado-texto (V) de VML
ms.assetid: 2c20e9d7-cb6a-4da7-af7a-9a7b1baa8e1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a288f89a1405412ba8c582a5c52c7bfe56809c38
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488247"
---
# <a name="vml-v-text-spacing-mode-attribute"></a><span data-ttu-id="54eb6-103">Atributo de modo de espaciado-texto (V) de VML</span><span class="sxs-lookup"><span data-stu-id="54eb6-103">VML V-Text-Spacing-Mode Attribute</span></span>

<span data-ttu-id="54eb6-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="54eb6-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="54eb6-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="54eb6-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="54eb6-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="54eb6-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="54eb6-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="54eb6-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="54eb6-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="54eb6-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="54eb6-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="54eb6-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="54eb6-110">Define el modo de espaciado entre letras.</span><span class="sxs-lookup"><span data-stu-id="54eb6-110">Defines the mode for letterspacing.</span></span> <span data-ttu-id="54eb6-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="54eb6-111">Read/write.</span></span> <span data-ttu-id="54eb6-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="54eb6-112">**String**.</span></span>

<span data-ttu-id="54eb6-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="54eb6-113">**Applies To**</span></span>

[<span data-ttu-id="54eb6-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="54eb6-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="54eb6-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="54eb6-115">**Tag Syntax**</span></span>

<span data-ttu-id="54eb6-116"><v: *Element* style = "v-Text-spacing-Mode: *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="54eb6-116"><v: *element* style="v-text-spacing-mode: *expression* "></span></span>

<span data-ttu-id="54eb6-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="54eb6-117">**Script Syntax**</span></span>

<span data-ttu-id="54eb6-118">*Element* . Style. v-Text-spacing-Mode = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="54eb6-118">*element* .style.v-text-spacing-mode="*expression*"</span></span>

<span data-ttu-id="54eb6-119">*expresión* = de *Element*. Style. v: modo de espaciado de texto</span><span class="sxs-lookup"><span data-stu-id="54eb6-119">*expression*=*element*.style.v-text-spacing-mode</span></span>

<span data-ttu-id="54eb6-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="54eb6-120">**Remarks**</span></span>

<span data-ttu-id="54eb6-121">Los valores incluyen</span><span class="sxs-lookup"><span data-stu-id="54eb6-121">Values include</span></span>

-   <span data-ttu-id="54eb6-122">**apretar** (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="54eb6-122">**tightening** (default)</span></span>
-   <span data-ttu-id="54eb6-123">**llevar**</span><span class="sxs-lookup"><span data-stu-id="54eb6-123">**tracking**</span></span>

<span data-ttu-id="54eb6-124">Este atributo determina si se quitará el espacio entre cada letra (apriete) o se agregará entre cada letra (seguimiento).</span><span class="sxs-lookup"><span data-stu-id="54eb6-124">This attribute determines whether space will be removed between each letter (tightening) or added between each letter (tracking).</span></span> <span data-ttu-id="54eb6-125">La cantidad de cambio de letterSpacing se define mediante el atributo [de espaciado de texto V](msdn-online-vml-v-text-spacing-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="54eb6-125">The amount of letterspacing change is defined by the [V-Text-Spacing](msdn-online-vml-v-text-spacing-attribute.md) attribute.</span></span>

<span data-ttu-id="54eb6-126">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="54eb6-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="54eb6-127">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="54eb6-127">**Example**</span></span>

<span data-ttu-id="54eb6-128">El espaciado entre letras se incrementa en 200 unidades.</span><span class="sxs-lookup"><span data-stu-id="54eb6-128">The letterspacing between each letter is increased by 200 units.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-spacing:200;v-text-spacing-mode:tracking;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 