---
title: Atributo VML V-Text-Kern
description: Atributo VML V-Text-Kern
ms.assetid: cece49c3-8e62-4327-8949-684a1d073293
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b20eab11cc24cd7580b68de8acf86468fb1d16a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995464"
---
# <a name="vml-v-text-kern-attribute"></a><span data-ttu-id="64e44-103">Atributo VML V-Text-Kern</span><span class="sxs-lookup"><span data-stu-id="64e44-103">VML V-Text-Kern Attribute</span></span>

<span data-ttu-id="64e44-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="64e44-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="64e44-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="64e44-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="64e44-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="64e44-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="64e44-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="64e44-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="64e44-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="64e44-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="64e44-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="64e44-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="64e44-110">Determina si el kerning está activado.</span><span class="sxs-lookup"><span data-stu-id="64e44-110">Determines whether kerning is turned on.</span></span> <span data-ttu-id="64e44-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="64e44-111">Read/write.</span></span> <span data-ttu-id="64e44-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="64e44-112">**VgTriState**.</span></span>

<span data-ttu-id="64e44-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="64e44-113">**Applies To**</span></span>

[<span data-ttu-id="64e44-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="64e44-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="64e44-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="64e44-115">**Tag Syntax**</span></span>

<span data-ttu-id="64e44-116"><v: *Element* style = "v-Text-Kern: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="64e44-116"><v: *element* style="v-text-kern: *expression* "></span></span>

<span data-ttu-id="64e44-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="64e44-117">**Script Syntax**</span></span>

<span data-ttu-id="64e44-118">*Element* . Style. v-Text-kerning = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="64e44-118">*element* .style.v-text-kern="*expression*"</span></span>

<span data-ttu-id="64e44-119">*expresión* = de *elemento*. Style. v-texto-kerning</span><span class="sxs-lookup"><span data-stu-id="64e44-119">*expression*=*element*.style.v-text-kern</span></span>

<span data-ttu-id="64e44-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="64e44-120">**Remarks**</span></span>

<span data-ttu-id="64e44-121">Si es **true**, el kerning está activado.</span><span class="sxs-lookup"><span data-stu-id="64e44-121">If **True**, the kerning is turned on.</span></span> <span data-ttu-id="64e44-122">El valor predeterminado es **False**.</span><span class="sxs-lookup"><span data-stu-id="64e44-122">The default is **False**.</span></span> <span data-ttu-id="64e44-123">El interletraje es la eliminación de espacio entre determinados pares de letras para compensar una letterforms desigual.</span><span class="sxs-lookup"><span data-stu-id="64e44-123">Kerning is the removal of space between certain letter pairs to compensate for uneven letterforms.</span></span> <span data-ttu-id="64e44-124">Por ejemplo, si está activado el interletraje, se quitará el espacio adicional entre una "T" mayúscula y una "i" minúscula.</span><span class="sxs-lookup"><span data-stu-id="64e44-124">For example, if kerning is turned on, extra space between a capital "T" and a lowercase "i" would be removed.</span></span>

<span data-ttu-id="64e44-125">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="64e44-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="64e44-126">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="64e44-126">**Example**</span></span>

<span data-ttu-id="64e44-127">El kerning está activado.</span><span class="sxs-lookup"><span data-stu-id="64e44-127">Kerning is turned on.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-kern:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 