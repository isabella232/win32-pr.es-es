---
title: Atributo EndCap de VML
description: Atributo EndCap de VML
ms.assetid: d8669a34-0fec-461e-90de-d9d5f7749a15
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 726d2bba2128ebb1897f306ae608f4bebb48d63f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359401"
---
# <a name="vml-endcap-attribute"></a><span data-ttu-id="dba9d-103">Atributo EndCap de VML</span><span class="sxs-lookup"><span data-stu-id="dba9d-103">VML EndCap Attribute</span></span>

<span data-ttu-id="dba9d-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="dba9d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="dba9d-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="dba9d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="dba9d-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="dba9d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="dba9d-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="dba9d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="dba9d-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="dba9d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="dba9d-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="dba9d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="dba9d-110">Define el estilo de extremo para el final de un trazo.</span><span class="sxs-lookup"><span data-stu-id="dba9d-110">Defines the cap style for the end of a stroke.</span></span> <span data-ttu-id="dba9d-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dba9d-111">Read/write.</span></span> <span data-ttu-id="dba9d-112">**VgLineEndCapStyle**.</span><span class="sxs-lookup"><span data-stu-id="dba9d-112">**VgLineEndCapStyle**.</span></span>

<span data-ttu-id="dba9d-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="dba9d-113">**Applies To**</span></span>

[<span data-ttu-id="dba9d-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="dba9d-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="dba9d-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="dba9d-115">**Tag Syntax**</span></span>

<span data-ttu-id="dba9d-116"><v: *Element* Endcap = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="dba9d-116"><v: *element* endcap=" *expression* "></span></span>

<span data-ttu-id="dba9d-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="dba9d-117">**Script Syntax**</span></span>

<span data-ttu-id="dba9d-118">*Element* . Endcap = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="dba9d-118">*element* .endcap="*expression*"</span></span>

<span data-ttu-id="dba9d-119">*expresión* = de *elemento*. Endcap</span><span class="sxs-lookup"><span data-stu-id="dba9d-119">*expression*=*element*.endcap</span></span>

<span data-ttu-id="dba9d-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="dba9d-120">**Remarks**</span></span>

<span data-ttu-id="dba9d-121">Estos valores incluyen:</span><span class="sxs-lookup"><span data-stu-id="dba9d-121">Values include:</span></span>

-   <span data-ttu-id="dba9d-122">Plano (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="dba9d-122">Flat (default)</span></span>
-   <span data-ttu-id="dba9d-123">Square</span><span class="sxs-lookup"><span data-stu-id="dba9d-123">Square</span></span>
-   <span data-ttu-id="dba9d-124">Round</span><span class="sxs-lookup"><span data-stu-id="dba9d-124">Round</span></span>

<span data-ttu-id="dba9d-125">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="dba9d-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="dba9d-126">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="dba9d-126">**Example**</span></span>

<span data-ttu-id="dba9d-127">Una línea se dibuja con una punta plana al final del trazo.</span><span class="sxs-lookup"><span data-stu-id="dba9d-127">A line is drawn with a flat cap on the end of the stroke.</span></span>


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endcap="flat"/>
   </v:line>
```



 

 