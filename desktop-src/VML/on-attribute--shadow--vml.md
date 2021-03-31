---
title: En atributo (sombra) (VML)
description: En atributo (sombra) (VML)
ms.assetid: 234fe63e-8a4a-4067-9d05-a8990d1cee5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83df69d8c90c99839f55836941746717a205d07a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995463"
---
# <a name="on-attribute-shadowvml"></a><span data-ttu-id="b439d-103">En atributo (sombra) (VML)</span><span class="sxs-lookup"><span data-stu-id="b439d-103">On Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="b439d-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="b439d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b439d-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="b439d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b439d-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="b439d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b439d-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="b439d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b439d-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b439d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b439d-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b439d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b439d-110">Determina si se mostrará una sombra.</span><span class="sxs-lookup"><span data-stu-id="b439d-110">Determines whether a shadow will be displayed.</span></span> <span data-ttu-id="b439d-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b439d-111">Read/write.</span></span> <span data-ttu-id="b439d-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="b439d-112">**VgTriState**.</span></span>

<span data-ttu-id="b439d-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="b439d-113">**Applies To**</span></span>

[<span data-ttu-id="b439d-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="b439d-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="b439d-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="b439d-115">**Tag Syntax**</span></span>

<span data-ttu-id="b439d-116"><v: *Element* on = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="b439d-116"><v: *element* on=" *expression* "></span></span>

<span data-ttu-id="b439d-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="b439d-117">**Script Syntax**</span></span>

<span data-ttu-id="b439d-118">*Element* . on = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="b439d-118">*element* .on="*expression*"</span></span>

<span data-ttu-id="b439d-119">*expresión* = de *elemento*. on</span><span class="sxs-lookup"><span data-stu-id="b439d-119">*expression*=*element*.on</span></span>

<span data-ttu-id="b439d-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="b439d-120">**Remarks**</span></span>

<span data-ttu-id="b439d-121">Si **es true**, se mostrará la sombra.</span><span class="sxs-lookup"><span data-stu-id="b439d-121">If **True**, the shadow will be displayed.</span></span> <span data-ttu-id="b439d-122">El valor predeterminado es **False**.</span><span class="sxs-lookup"><span data-stu-id="b439d-122">The default value is **False**.</span></span>

<span data-ttu-id="b439d-123">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="b439d-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="b439d-124">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="b439d-124">**Example**</span></span>

<span data-ttu-id="b439d-125">Se mostrará la sombra.</span><span class="sxs-lookup"><span data-stu-id="b439d-125">The shadow will be displayed.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True"/>
   </v:shape>
```





 

 