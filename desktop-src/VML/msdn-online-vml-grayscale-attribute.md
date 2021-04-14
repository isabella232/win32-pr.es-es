---
title: Atributo de escala de grises VML
description: Atributo de escala de grises VML
ms.assetid: 0715b78c-f529-422e-9064-7b99324e60de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1c4b5da616ec5f96eeb226ecb2ba18202874f67
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420926"
---
# <a name="vml-grayscale-attribute"></a><span data-ttu-id="0a142-103">Atributo de escala de grises VML</span><span class="sxs-lookup"><span data-stu-id="0a142-103">VML GrayScale Attribute</span></span>

<span data-ttu-id="0a142-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="0a142-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="0a142-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="0a142-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="0a142-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="0a142-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="0a142-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="0a142-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="0a142-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="0a142-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="0a142-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="0a142-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="0a142-110">Determina si una imagen se mostrará en el modo de escala de grises.</span><span class="sxs-lookup"><span data-stu-id="0a142-110">Determines whether a picture will be displayed in grayscale mode.</span></span> <span data-ttu-id="0a142-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0a142-111">Read/write.</span></span> <span data-ttu-id="0a142-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="0a142-112">**VgTriState**.</span></span>

<span data-ttu-id="0a142-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="0a142-113">**Applies To**</span></span>

[<span data-ttu-id="0a142-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="0a142-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="0a142-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="0a142-115">**Tag Syntax**</span></span>

<span data-ttu-id="0a142-116"><v: *elemento* de escala de grises = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="0a142-116"><v: *element* grayscale=" *expression* "></span></span>

<span data-ttu-id="0a142-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="0a142-117">**Script Syntax**</span></span>

<span data-ttu-id="0a142-118">*Element* . = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="0a142-118">*element* .grayscale="*expression*"</span></span>

<span data-ttu-id="0a142-119">*expresión* = de *elemento*. escala de grises</span><span class="sxs-lookup"><span data-stu-id="0a142-119">*expression*=*element*.grayscale</span></span>

<span data-ttu-id="0a142-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="0a142-120">**Remarks**</span></span>

<span data-ttu-id="0a142-121">Si **es true**, la imagen se mostrará en escala de grises en lugar de en color.</span><span class="sxs-lookup"><span data-stu-id="0a142-121">If **True**, the picture will be displayed in grayscale instead of color.</span></span> <span data-ttu-id="0a142-122">El valor predeterminado es **False**.</span><span class="sxs-lookup"><span data-stu-id="0a142-122">The default is **False**.</span></span>

<span data-ttu-id="0a142-123">El valor se basa en la recomendación de CCIR 709, que favorece un mayor peso verde y produce resultados más agradables para el color natural.</span><span class="sxs-lookup"><span data-stu-id="0a142-123">The value is based according to CCIR recommendation 709, which favors more green weight and produces more pleasing results for natural color.</span></span>

<span data-ttu-id="0a142-124">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="0a142-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="0a142-125">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="0a142-125">**Example**</span></span>

<span data-ttu-id="0a142-126">La imagen se mostrará en escala de grises en lugar de en color.</span><span class="sxs-lookup"><span data-stu-id="0a142-126">The image will be displayed in grayscale instead of color.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata grayscale="True" src="kids.jpg"/>
   </v:shape>
```



 

 