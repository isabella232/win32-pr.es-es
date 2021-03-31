---
title: Atributo oculto VML
description: Atributo oculto VML
ms.assetid: b8cdb066-e4fc-4dd6-a55a-7c2488f89e61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e383061d3210c9c52dc8c89322bd617257555e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077956"
---
# <a name="vml-obscured-attribute"></a><span data-ttu-id="30a97-103">Atributo oculto VML</span><span class="sxs-lookup"><span data-stu-id="30a97-103">VML Obscured Attribute</span></span>

<span data-ttu-id="30a97-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="30a97-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="30a97-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="30a97-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="30a97-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="30a97-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="30a97-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="30a97-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="30a97-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="30a97-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="30a97-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="30a97-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="30a97-110">Determina si una sombra es transparente.</span><span class="sxs-lookup"><span data-stu-id="30a97-110">Determines whether a shadow is transparent.</span></span> <span data-ttu-id="30a97-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="30a97-111">Read/write.</span></span> <span data-ttu-id="30a97-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="30a97-112">**VgTriState**.</span></span>

<span data-ttu-id="30a97-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="30a97-113">**Applies To**</span></span>

[<span data-ttu-id="30a97-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="30a97-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="30a97-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="30a97-115">**Tag Syntax**</span></span>

<span data-ttu-id="30a97-116"><v: *elemento* oculto = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="30a97-116"><v: *element* obscured=" *expression* "></span></span>

<span data-ttu-id="30a97-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="30a97-117">**Script Syntax**</span></span>

<span data-ttu-id="30a97-118">*Element* . Obscured = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="30a97-118">*element* .obscured="*expression*"</span></span>

<span data-ttu-id="30a97-119">*expresión* = de *Element*. Obscured</span><span class="sxs-lookup"><span data-stu-id="30a97-119">*expression*=*element*.obscured</span></span>

<span data-ttu-id="30a97-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="30a97-120">**Remarks**</span></span>

<span data-ttu-id="30a97-121">Si es **true**, le permite ver a través de la sombra si no hay ningún relleno en la forma.</span><span class="sxs-lookup"><span data-stu-id="30a97-121">If **True**, lets you see through the shadow if there is no fill on the shape.</span></span> <span data-ttu-id="30a97-122">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="30a97-122">Default is **False**.</span></span>

<span data-ttu-id="30a97-123">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="30a97-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="30a97-124">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="30a97-124">**Example**</span></span>

<span data-ttu-id="30a97-125">El fondo se muestra a través de la sombra.</span><span class="sxs-lookup"><span data-stu-id="30a97-125">The background shows through the shadow.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m1,1 l 1,200,200,200, 200,1 x e">
   <v:shadow on="True" obscured="True"/>
   </v:shape>
```



 

 