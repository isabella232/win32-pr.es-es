---
title: Atributo BiLevel de VML
description: Atributo BiLevel de VML
ms.assetid: 5b87e928-6f0a-4b00-833a-3c2add2d5677
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 263a9d538a76ba0c9b203cbcf04f8413d4286c34
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792382"
---
# <a name="vml-bilevel-attribute"></a><span data-ttu-id="6f57a-103">Atributo BiLevel de VML</span><span class="sxs-lookup"><span data-stu-id="6f57a-103">VML Bilevel Attribute</span></span>

<span data-ttu-id="6f57a-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="6f57a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="6f57a-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="6f57a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="6f57a-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="6f57a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="6f57a-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="6f57a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="6f57a-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="6f57a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="6f57a-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="6f57a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="6f57a-110">Determina si una imagen se mostrará en blanco y negro.</span><span class="sxs-lookup"><span data-stu-id="6f57a-110">Determines whether an image will be displayed in black and white.</span></span> <span data-ttu-id="6f57a-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6f57a-111">Read/write.</span></span> <span data-ttu-id="6f57a-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="6f57a-112">**VgTriState**.</span></span>

<span data-ttu-id="6f57a-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="6f57a-113">**Applies To**</span></span>

[<span data-ttu-id="6f57a-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="6f57a-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="6f57a-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="6f57a-115">**Tag Syntax**</span></span>

<span data-ttu-id="6f57a-116"><v: *elemento* BiLevel = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="6f57a-116"><v: *element* bilevel=" *expression* "></span></span>

<span data-ttu-id="6f57a-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="6f57a-117">**Script Syntax**</span></span>

<span data-ttu-id="6f57a-118">*elemento* . BiLevel = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="6f57a-118">*element* .bilevel="*expression*"</span></span>

<span data-ttu-id="6f57a-119">*expresión* = de *elemento*. BiLevel</span><span class="sxs-lookup"><span data-stu-id="6f57a-119">*expression*=*element*.bilevel</span></span>

<span data-ttu-id="6f57a-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="6f57a-120">**Remarks**</span></span>

<span data-ttu-id="6f57a-121">Si **es true**, la imagen se mostrará con dos colores (blanco y negro).</span><span class="sxs-lookup"><span data-stu-id="6f57a-121">If **True**, the image will be displayed using two colors (black and white).</span></span> <span data-ttu-id="6f57a-122">El valor predeterminado es **False**.</span><span class="sxs-lookup"><span data-stu-id="6f57a-122">The default is **False**.</span></span> <span data-ttu-id="6f57a-123">Esto crea un efecto similar a la posterización.</span><span class="sxs-lookup"><span data-stu-id="6f57a-123">This creates an effect similar to posterization.</span></span>

<span data-ttu-id="6f57a-124">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="6f57a-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="6f57a-125">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="6f57a-125">**Example**</span></span>

<span data-ttu-id="6f57a-126">La imagen solo se mostrará en blanco y negro.</span><span class="sxs-lookup"><span data-stu-id="6f57a-126">The image will be displayed in black and white only.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata bilevel="True" src="kids.jpg"/>
   </v:shape>
```



 

 