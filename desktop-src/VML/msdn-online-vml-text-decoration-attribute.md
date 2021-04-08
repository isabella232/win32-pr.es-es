---
title: Atributo de Text-Decoration VML
description: Atributo de Text-Decoration VML
ms.assetid: a64985bd-d025-4e9c-bb4b-bf0450d5143a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24ee85007db2dbca04221604cafd79c5d7052c91
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995324"
---
# <a name="vml-text-decoration-attribute"></a><span data-ttu-id="20ccf-103">Atributo de Text-Decoration VML</span><span class="sxs-lookup"><span data-stu-id="20ccf-103">VML Text-Decoration Attribute</span></span>

<span data-ttu-id="20ccf-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="20ccf-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="20ccf-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="20ccf-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="20ccf-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="20ccf-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="20ccf-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="20ccf-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="20ccf-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="20ccf-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="20ccf-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="20ccf-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="20ccf-110">Define el estilo de decoración de texto.</span><span class="sxs-lookup"><span data-stu-id="20ccf-110">Defines the style of text decoration.</span></span> <span data-ttu-id="20ccf-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="20ccf-111">Read/write.</span></span> <span data-ttu-id="20ccf-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="20ccf-112">**String**.</span></span>

<span data-ttu-id="20ccf-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="20ccf-113">**Applies To**</span></span>

[<span data-ttu-id="20ccf-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="20ccf-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="20ccf-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="20ccf-115">**Tag Syntax**</span></span>

<span data-ttu-id="20ccf-116"><v: *Element* style = "text-decoration: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="20ccf-116"><v: *element* style="text-decoration: *expression* "></span></span>

<span data-ttu-id="20ccf-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="20ccf-117">**Script Syntax**</span></span>

<span data-ttu-id="20ccf-118">*Element* . Style. TextDecoration = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="20ccf-118">*element* .style.textdecoration="*expression*"</span></span>

<span data-ttu-id="20ccf-119">*expresión* = de *Element*. Style. TextDecoration</span><span class="sxs-lookup"><span data-stu-id="20ccf-119">*expression*=*element*.style.textdecoration</span></span>

<span data-ttu-id="20ccf-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="20ccf-120">**Remarks**</span></span>

<span data-ttu-id="20ccf-121">Estos valores incluyen:</span><span class="sxs-lookup"><span data-stu-id="20ccf-121">Values include:</span></span>

-   <span data-ttu-id="20ccf-122">ninguno (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="20ccf-122">none (default)</span></span>
-   <span data-ttu-id="20ccf-123">subrayado</span><span class="sxs-lookup"><span data-stu-id="20ccf-123">underline</span></span>
-   <span data-ttu-id="20ccf-124">línea alta</span><span class="sxs-lookup"><span data-stu-id="20ccf-124">overline</span></span>
-   <span data-ttu-id="20ccf-125">línea a través</span><span class="sxs-lookup"><span data-stu-id="20ccf-125">line-through</span></span>
-   <span data-ttu-id="20ccf-126">blink</span><span class="sxs-lookup"><span data-stu-id="20ccf-126">blink</span></span>

<span data-ttu-id="20ccf-127">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="20ccf-127">*VML Standard Attribute*</span></span>

<span data-ttu-id="20ccf-128">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="20ccf-128">**Example**</span></span>

<span data-ttu-id="20ccf-129">El texto estará subrayado.</span><span class="sxs-lookup"><span data-stu-id="20ccf-129">The text will be underlined.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="text-decoration:underline;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 