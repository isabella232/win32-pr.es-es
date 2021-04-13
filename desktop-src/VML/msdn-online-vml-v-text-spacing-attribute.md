---
title: Atributo de espaciado de texto V de VML
description: Atributo de espaciado de texto V de VML
ms.assetid: c0d83854-4009-4d1d-aa8a-37f660dd0ef7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab31d1f0b0b1d41b7e99451c422028fe54498483
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421064"
---
# <a name="vml-v-text-spacing-attribute"></a><span data-ttu-id="e79b8-103">Atributo de espaciado de texto V de VML</span><span class="sxs-lookup"><span data-stu-id="e79b8-103">VML V-Text-Spacing Attribute</span></span>

<span data-ttu-id="e79b8-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="e79b8-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e79b8-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="e79b8-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e79b8-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="e79b8-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e79b8-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="e79b8-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e79b8-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e79b8-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e79b8-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e79b8-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e79b8-110">Define la cantidad de espaciado del texto.</span><span class="sxs-lookup"><span data-stu-id="e79b8-110">Defines the amount of spacing for text.</span></span> <span data-ttu-id="e79b8-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e79b8-111">Read/write.</span></span> <span data-ttu-id="e79b8-112">**VgNumber**.</span><span class="sxs-lookup"><span data-stu-id="e79b8-112">**VgNumber**.</span></span>

<span data-ttu-id="e79b8-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="e79b8-113">**Applies To**</span></span>

[<span data-ttu-id="e79b8-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="e79b8-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="e79b8-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="e79b8-115">**Tag Syntax**</span></span>

<span data-ttu-id="e79b8-116"><v: *Element* style = "v-Text-spacing: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="e79b8-116"><v: *element* style="v-text-spacing: *expression* "></span></span>

<span data-ttu-id="e79b8-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="e79b8-117">**Script Syntax**</span></span>

<span data-ttu-id="e79b8-118">*Element* . Style. v-Text-spacing = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="e79b8-118">*element* .style.v-text-spacing="*expression*"</span></span>

<span data-ttu-id="e79b8-119">*expresión* = de *Element*. Style. v: espaciado de texto</span><span class="sxs-lookup"><span data-stu-id="e79b8-119">*expression*=*element*.style.v-text-spacing</span></span>

<span data-ttu-id="e79b8-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="e79b8-120">**Remarks**</span></span>

<span data-ttu-id="e79b8-121">El valor predeterminado es 100.</span><span class="sxs-lookup"><span data-stu-id="e79b8-121">The default value is 100.</span></span> <span data-ttu-id="e79b8-122">Vea el atributo de [modo de espaciado de texto V](msdn-online-vml-v-text-spacing-mode-attribute.md) para obtener más información sobre el espaciado de texto.</span><span class="sxs-lookup"><span data-stu-id="e79b8-122">See the [V-Text-Spacing-Mode](msdn-online-vml-v-text-spacing-mode-attribute.md) attribute for more information about text spacing.</span></span>

<span data-ttu-id="e79b8-123">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="e79b8-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="e79b8-124">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="e79b8-124">**Example**</span></span>

<span data-ttu-id="e79b8-125">El espaciado entre letras se ajusta en 200 unidades.</span><span class="sxs-lookup"><span data-stu-id="e79b8-125">The letterspacing between each letter is tightened by 200 units.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-spacing:200;v-text-spacing-mode:tightening;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 