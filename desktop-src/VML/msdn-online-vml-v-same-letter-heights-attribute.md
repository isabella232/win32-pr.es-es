---
title: VML V-Same-Letter-alto atributo
description: VML V-Same-Letter-alto atributo
ms.assetid: f06c0a50-1de1-47d8-8b94-01fe0599ed59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6d155c3c72eb67718edd33ae601d22f8e5d074a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791973"
---
# <a name="vml-v-same-letter-heights-attribute"></a><span data-ttu-id="f8e37-103">VML V-Same-Letter-alto atributo</span><span class="sxs-lookup"><span data-stu-id="f8e37-103">VML V-Same-Letter-Heights Attribute</span></span>

<span data-ttu-id="f8e37-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="f8e37-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="f8e37-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="f8e37-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="f8e37-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="f8e37-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="f8e37-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="f8e37-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="f8e37-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="f8e37-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="f8e37-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="f8e37-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="f8e37-110">Determina si todas las letras serán el mismo alto independientemente del caso inicial.</span><span class="sxs-lookup"><span data-stu-id="f8e37-110">Determines whether all letters will be the same height regardless of initial case.</span></span> <span data-ttu-id="f8e37-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f8e37-111">Read/write.</span></span> <span data-ttu-id="f8e37-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="f8e37-112">**VgTriState**.</span></span>

<span data-ttu-id="f8e37-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="f8e37-113">**Applies To**</span></span>

[<span data-ttu-id="f8e37-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="f8e37-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="f8e37-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="f8e37-115">**Tag Syntax**</span></span>

<span data-ttu-id="f8e37-116"><v: *Element* style = "v-Same-Letter-alturas: *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="f8e37-116"><v: *element* style="v-same-letter-heights: *expression* "></span></span>

<span data-ttu-id="f8e37-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="f8e37-117">**Script Syntax**</span></span>

<span data-ttu-id="f8e37-118">*Element* . Style. v-Same-Letter-alto = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="f8e37-118">*element* .style.v-same-letter-heights="*expression*"</span></span>

<span data-ttu-id="f8e37-119">*expresión* = de *Element*. Style. v-Same-Letter-alto</span><span class="sxs-lookup"><span data-stu-id="f8e37-119">*expression*=*element*.style.v-same-letter-heights</span></span>

<span data-ttu-id="f8e37-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="f8e37-120">**Remarks**</span></span>

<span data-ttu-id="f8e37-121">Si **es true**, las letras minúsculas se ajustan al alto de las letras mayúsculas.</span><span class="sxs-lookup"><span data-stu-id="f8e37-121">If **True**, the lowercase letters are stretched to the height of the uppercase letters.</span></span> <span data-ttu-id="f8e37-122">El valor predeterminado es **False**.</span><span class="sxs-lookup"><span data-stu-id="f8e37-122">The default value is **False**.</span></span>

<span data-ttu-id="f8e37-123">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="f8e37-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="f8e37-124">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="f8e37-124">**Example**</span></span>

<span data-ttu-id="f8e37-125">Todas las letras tendrán el mismo alto, independientemente del uso de mayúsculas o minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f8e37-125">All letters will be the same height, regardless of case.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-same-letter-heights:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 