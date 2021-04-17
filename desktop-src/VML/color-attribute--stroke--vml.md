---
title: Atributo de color (Stroke) (VML)
description: Atributo de color (Stroke) (VML)
ms.assetid: 8fa19789-0bd6-4e9f-8af4-566155eafc6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faa91522adcba5fa854d4749dc257f5489969270
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695708"
---
# <a name="color-attribute-strokevml"></a><span data-ttu-id="1ddf1-103">Atributo de color (Stroke) (VML)</span><span class="sxs-lookup"><span data-stu-id="1ddf1-103">Color Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="1ddf1-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="1ddf1-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="1ddf1-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="1ddf1-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="1ddf1-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="1ddf1-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="1ddf1-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="1ddf1-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="1ddf1-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="1ddf1-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="1ddf1-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="1ddf1-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="1ddf1-110">Define el color de un trazo.</span><span class="sxs-lookup"><span data-stu-id="1ddf1-110">Defines the color of a stroke.</span></span> <span data-ttu-id="1ddf1-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1ddf1-111">Read/write.</span></span> <span data-ttu-id="1ddf1-112">**VgColor**.</span><span class="sxs-lookup"><span data-stu-id="1ddf1-112">**VgColor**.</span></span>

<span data-ttu-id="1ddf1-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="1ddf1-113">**Applies To**</span></span>

[<span data-ttu-id="1ddf1-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="1ddf1-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="1ddf1-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="1ddf1-115">**Tag Syntax**</span></span>

<span data-ttu-id="1ddf1-116"><v: *elemento* color = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="1ddf1-116"><v: *element* color=" *expression* "></span></span>

<span data-ttu-id="1ddf1-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="1ddf1-117">**Script Syntax**</span></span>

<span data-ttu-id="1ddf1-118">*Element* . color = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="1ddf1-118">*element* .color="*expression*"</span></span>

<span data-ttu-id="1ddf1-119">*expresión* = de *elemento*. color</span><span class="sxs-lookup"><span data-stu-id="1ddf1-119">*expression*=*element*.color</span></span>

<span data-ttu-id="1ddf1-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="1ddf1-120">**Remarks**</span></span>

<span data-ttu-id="1ddf1-121">Invalida el atributo **StrokeColor** de una forma.</span><span class="sxs-lookup"><span data-stu-id="1ddf1-121">Overrides the **StrokeColor** attribute of a shape.</span></span> <span data-ttu-id="1ddf1-122">El valor predeterminado es **negro**.</span><span class="sxs-lookup"><span data-stu-id="1ddf1-122">The default value is **black**.</span></span>

<span data-ttu-id="1ddf1-123">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="1ddf1-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="1ddf1-124">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="1ddf1-124">**Example**</span></span>

<span data-ttu-id="1ddf1-125">La forma tiene un color de trazo **verde**, no **rojo**.</span><span class="sxs-lookup"><span data-stu-id="1ddf1-125">The shape has a stroke color of **green**, not **red**.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke color="green"/>
   </v:shape>
```



 

 