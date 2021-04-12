---
title: Atributo de estilo VML
description: Atributo de estilo VML
ms.assetid: 1695d2b2-cf60-48f1-b47e-f0f43696b5b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f291fad75bf14e06f40ad0a1446bd0418bba46b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487766"
---
# <a name="vml-style-attribute"></a><span data-ttu-id="be250-103">Atributo de estilo VML</span><span class="sxs-lookup"><span data-stu-id="be250-103">VML Style Attribute</span></span>

<span data-ttu-id="be250-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="be250-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="be250-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="be250-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="be250-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="be250-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="be250-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="be250-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="be250-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="be250-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="be250-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="be250-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="be250-110">Define el estilo del marco.</span><span class="sxs-lookup"><span data-stu-id="be250-110">Defines the style of the frame.</span></span> <span data-ttu-id="be250-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="be250-111">Read/write.</span></span> <span data-ttu-id="be250-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="be250-112">**String**.</span></span>

<span data-ttu-id="be250-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="be250-113">**Applies To**</span></span>

[<span data-ttu-id="be250-114">VMLFrame</span><span class="sxs-lookup"><span data-stu-id="be250-114">VMLFrame</span></span>](msdn-online-vml-vmlframe-element.md)

<span data-ttu-id="be250-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="be250-115">**Tag Syntax**</span></span>

<span data-ttu-id="be250-116"><v: *Element* style = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="be250-116"><v: *element* style=" *expression* "></span></span>

<span data-ttu-id="be250-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="be250-117">**Script Syntax**</span></span>

<span data-ttu-id="be250-118">*Element* . Style = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="be250-118">*element* .style="*expression*"</span></span>

<span data-ttu-id="be250-119">*expresión* = de *elemento*. Style</span><span class="sxs-lookup"><span data-stu-id="be250-119">*expression*=*element*.style</span></span>

<span data-ttu-id="be250-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="be250-120">**Remarks**</span></span>

<span data-ttu-id="be250-121">Este atributo utiliza los atributos de estilo CSS normales para la posición.</span><span class="sxs-lookup"><span data-stu-id="be250-121">This attribute uses the normal CSS style attributes for positioning.</span></span>

<span data-ttu-id="be250-122">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="be250-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="be250-123">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="be250-123">**Example**</span></span>

<span data-ttu-id="be250-124">El estilo define la posición real del marco.</span><span class="sxs-lookup"><span data-stu-id="be250-124">The style defines the actual position of the frame.</span></span>


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 