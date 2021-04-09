---
title: Atributo V-Rotate-Letters VML
description: Atributo V-Rotate-Letters VML
ms.assetid: f9bd5c04-7479-4dc0-83d7-4a0bd5e2d41d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9397fe8a819e9f4c8b517e1ac92e0094ad8e4458
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149308"
---
# <a name="vml-v-rotate-letters-attribute"></a><span data-ttu-id="f3b78-103">Atributo V-Rotate-Letters VML</span><span class="sxs-lookup"><span data-stu-id="f3b78-103">VML V-Rotate-Letters Attribute</span></span>

<span data-ttu-id="f3b78-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="f3b78-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="f3b78-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="f3b78-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="f3b78-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="f3b78-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="f3b78-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="f3b78-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="f3b78-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="f3b78-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="f3b78-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="f3b78-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="f3b78-110">Determina si las letras del texto se giran.</span><span class="sxs-lookup"><span data-stu-id="f3b78-110">Determines whether the letters of the text are rotated.</span></span> <span data-ttu-id="f3b78-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f3b78-111">Read/write.</span></span> <span data-ttu-id="f3b78-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="f3b78-112">**VgTriState**.</span></span>

<span data-ttu-id="f3b78-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="f3b78-113">**Applies To**</span></span>

[<span data-ttu-id="f3b78-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="f3b78-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="f3b78-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="f3b78-115">**Tag Syntax**</span></span>

<span data-ttu-id="f3b78-116"><v: *Element* style = "v-Rotate-Letters: *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="f3b78-116"><v: *element* style="v-rotate-letters: *expression* "></span></span>

<span data-ttu-id="f3b78-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="f3b78-117">**Script Syntax**</span></span>

<span data-ttu-id="f3b78-118">*Element* . Style. v-Rotate-Letters = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="f3b78-118">*element* .style.v-rotate-letters="*expression*"</span></span>

<span data-ttu-id="f3b78-119">*expresión* = de *Element*. Style. v-Rotate-Letters</span><span class="sxs-lookup"><span data-stu-id="f3b78-119">*expression*=*element*.style.v-rotate-letters</span></span>

<span data-ttu-id="f3b78-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="f3b78-120">**Remarks**</span></span>

<span data-ttu-id="f3b78-121">Si **es true**, las letras del texto se giran 90 grados.</span><span class="sxs-lookup"><span data-stu-id="f3b78-121">If **True**, the letters of the text are rotated 90 degrees.</span></span> <span data-ttu-id="f3b78-122">El valor predeterminado es **False**.</span><span class="sxs-lookup"><span data-stu-id="f3b78-122">The default value is **False**.</span></span>

<span data-ttu-id="f3b78-123">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="f3b78-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="f3b78-124">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="f3b78-124">**Example**</span></span>

<span data-ttu-id="f3b78-125">Las letras se giran 90 grados.</span><span class="sxs-lookup"><span data-stu-id="f3b78-125">The letters are rotated 90 degrees.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-rotate-letters:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 