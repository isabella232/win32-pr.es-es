---
title: Atributo de peso en VML
description: Atributo de peso en VML
ms.assetid: 40164818-6b04-4afe-91cc-9fb8b12cb718
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba7a1a4d5dca91da6b3750f0d901d4e278a80dd7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695653"
---
# <a name="vml-weight-attribute"></a><span data-ttu-id="919ab-103">Atributo de peso en VML</span><span class="sxs-lookup"><span data-stu-id="919ab-103">VML Weight Attribute</span></span>

<span data-ttu-id="919ab-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="919ab-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="919ab-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="919ab-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="919ab-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="919ab-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="919ab-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="919ab-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="919ab-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="919ab-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="919ab-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="919ab-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="919ab-110">Define el grosor de un trazo.</span><span class="sxs-lookup"><span data-stu-id="919ab-110">Defines the thickness of a stroke.</span></span> <span data-ttu-id="919ab-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="919ab-111">Read/write.</span></span> <span data-ttu-id="919ab-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="919ab-112">**String**.</span></span>

<span data-ttu-id="919ab-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="919ab-113">**Applies To**</span></span>

[<span data-ttu-id="919ab-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="919ab-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="919ab-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="919ab-115">**Tag Syntax**</span></span>

<span data-ttu-id="919ab-116"><v: *elemento* Weight = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="919ab-116"><v: *element* weight=" *expression* "></span></span>

<span data-ttu-id="919ab-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="919ab-117">**Script Syntax**</span></span>

<span data-ttu-id="919ab-118">*Element* . Weight = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="919ab-118">*element* .weight="*expression*"</span></span>

<span data-ttu-id="919ab-119">*expresión* = de *elemento*. Weight</span><span class="sxs-lookup"><span data-stu-id="919ab-119">*expression*=*element*.weight</span></span>

<span data-ttu-id="919ab-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="919ab-120">**Remarks**</span></span>

<span data-ttu-id="919ab-121">Este atributo es igual que el atributo **StrokeWeight** de **Shape** y lo reemplaza.</span><span class="sxs-lookup"><span data-stu-id="919ab-121">This attribute is the same as the **StrokeWeight** attribute of **Shape** and overrides it.</span></span> <span data-ttu-id="919ab-122">El valor predeterminado es 1 punto.</span><span class="sxs-lookup"><span data-stu-id="919ab-122">The default value is 1 point.</span></span>

<span data-ttu-id="919ab-123">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="919ab-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="919ab-124">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="919ab-124">**Example**</span></span>

<span data-ttu-id="919ab-125">El trazo tiene un grosor de 5 puntos, no 2 puntos.</span><span class="sxs-lookup"><span data-stu-id="919ab-125">The stroke has a thickness of 5 points, not 2 points.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red" strokeweight="2pt"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke weight="5pt"/>
   </v:shape>
```



 

 