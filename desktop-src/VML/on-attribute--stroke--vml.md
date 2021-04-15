---
title: En atributo (Stroke) (VML)
description: En atributo (Stroke) (VML)
ms.assetid: 8a966dc2-826b-4202-9c5c-c6afb00cd501
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e418857db22ee1ac12a35e9b81840b89e06c00
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695695"
---
# <a name="on-attribute-strokevml"></a><span data-ttu-id="4bfed-103">En atributo (Stroke) (VML)</span><span class="sxs-lookup"><span data-stu-id="4bfed-103">On Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="4bfed-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="4bfed-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="4bfed-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="4bfed-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="4bfed-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="4bfed-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="4bfed-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="4bfed-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="4bfed-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="4bfed-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="4bfed-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="4bfed-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="4bfed-110">Determina si se mostrará el trazo.</span><span class="sxs-lookup"><span data-stu-id="4bfed-110">Determines whether the stroke will be displayed.</span></span> <span data-ttu-id="4bfed-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4bfed-111">Read/write.</span></span> <span data-ttu-id="4bfed-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="4bfed-112">**VgTriState**.</span></span>

<span data-ttu-id="4bfed-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="4bfed-113">**Applies To**</span></span>

[<span data-ttu-id="4bfed-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="4bfed-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="4bfed-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="4bfed-115">**Tag Syntax**</span></span>

<span data-ttu-id="4bfed-116"><v: *Element* on = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="4bfed-116"><v: *element* on=" *expression* "></span></span>

<span data-ttu-id="4bfed-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="4bfed-117">**Script Syntax**</span></span>

<span data-ttu-id="4bfed-118">*Element* . on = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="4bfed-118">*element* .on="*expression*"</span></span>

<span data-ttu-id="4bfed-119">*expresión* = de *elemento*. on</span><span class="sxs-lookup"><span data-stu-id="4bfed-119">*expression*=*element*.on</span></span>

<span data-ttu-id="4bfed-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="4bfed-120">**Remarks**</span></span>

<span data-ttu-id="4bfed-121">Si es **false**, no se muestra el trazo.</span><span class="sxs-lookup"><span data-stu-id="4bfed-121">If **False**, the stroke is not displayed.</span></span> <span data-ttu-id="4bfed-122">El valor predeterminado es **True**.</span><span class="sxs-lookup"><span data-stu-id="4bfed-122">The default is **True**.</span></span>

<span data-ttu-id="4bfed-123">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="4bfed-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="4bfed-124">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="4bfed-124">**Example**</span></span>

<span data-ttu-id="4bfed-125">No se mostrará el trazo.</span><span class="sxs-lookup"><span data-stu-id="4bfed-125">The stroke will not be displayed.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="blue"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke on="False"/>
   </v:shape>
```



 

 