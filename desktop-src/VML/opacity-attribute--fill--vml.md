---
title: Opacity (atributo, Fill) (VML)
description: Opacity (atributo, Fill) (VML)
ms.assetid: abd2fe4d-6391-4413-80f0-549bcc74f42e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b913498705e65fa7211db4b4cef039894d573a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793750"
---
# <a name="opacity-attribute-fillvml"></a><span data-ttu-id="7cba1-103">Opacity (atributo, Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="7cba1-103">Opacity Attribute (Fill)(VML)</span></span>

<span data-ttu-id="7cba1-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="7cba1-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="7cba1-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="7cba1-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="7cba1-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="7cba1-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="7cba1-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="7cba1-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="7cba1-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="7cba1-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="7cba1-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="7cba1-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="7cba1-110">Define la transparencia de un relleno.</span><span class="sxs-lookup"><span data-stu-id="7cba1-110">Defines the transparency of a fill.</span></span> <span data-ttu-id="7cba1-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7cba1-111">Read/write.</span></span> <span data-ttu-id="7cba1-112">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="7cba1-112">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span>

<span data-ttu-id="7cba1-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="7cba1-113">**Applies To**</span></span>

[<span data-ttu-id="7cba1-114">Fill</span><span class="sxs-lookup"><span data-stu-id="7cba1-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="7cba1-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="7cba1-115">**Tag Syntax**</span></span>

<span data-ttu-id="7cba1-116"><v: *elemento* Opacity = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="7cba1-116"><v: *element* opacity=" *expression* "></span></span>

<span data-ttu-id="7cba1-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="7cba1-117">**Script Syntax**</span></span>

<span data-ttu-id="7cba1-118">*elemento* . Opacity = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="7cba1-118">*element* .opacity="*expression*"</span></span>

<span data-ttu-id="7cba1-119">*expresión* = de *elemento*. Opacity</span><span class="sxs-lookup"><span data-stu-id="7cba1-119">*expression*=*element*.opacity</span></span>

<span data-ttu-id="7cba1-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="7cba1-120">**Remarks**</span></span>

<span data-ttu-id="7cba1-121">El valor predeterminado es 1,0.</span><span class="sxs-lookup"><span data-stu-id="7cba1-121">The default value is 1.0.</span></span>

<span data-ttu-id="7cba1-122">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="7cba1-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="7cba1-123">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="7cba1-123">**Example**</span></span>

<span data-ttu-id="7cba1-124">El relleno de la forma será 50% transparente.</span><span class="sxs-lookup"><span data-stu-id="7cba1-124">The fill of the shape will be 50% transparent.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill opacity="50%" color="red"/>
   </v:shape>
```



 

 