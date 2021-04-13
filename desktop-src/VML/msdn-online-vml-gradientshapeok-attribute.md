---
title: Atributo GradientShapeOK de VML
description: Atributo GradientShapeOK de VML
ms.assetid: c26ac4cb-f7f0-4666-b32f-d9fcaf9044a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d1b7c215fbe0b98c11f7e4d33301e81798bd37f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421318"
---
# <a name="vml-gradientshapeok-attribute"></a><span data-ttu-id="af1bc-103">Atributo GradientShapeOK de VML</span><span class="sxs-lookup"><span data-stu-id="af1bc-103">VML GradientShapeOK Attribute</span></span>

<span data-ttu-id="af1bc-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="af1bc-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="af1bc-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="af1bc-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="af1bc-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="af1bc-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="af1bc-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="af1bc-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="af1bc-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="af1bc-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="af1bc-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="af1bc-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="af1bc-110">Determina si una ruta de acceso de degradado se compone de rutas de acceso concéntrica repetidas.</span><span class="sxs-lookup"><span data-stu-id="af1bc-110">Determines whether a gradient path will be made up of repeated concentric paths.</span></span> <span data-ttu-id="af1bc-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="af1bc-111">Read/write.</span></span> <span data-ttu-id="af1bc-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="af1bc-112">**VgTriState**.</span></span>

<span data-ttu-id="af1bc-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="af1bc-113">**Applies To**</span></span>

[<span data-ttu-id="af1bc-114">Ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="af1bc-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="af1bc-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="af1bc-115">**Tag Syntax**</span></span>

<span data-ttu-id="af1bc-116"><v: *Element* gradientshapeok = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="af1bc-116"><v: *element* gradientshapeok=" *expression* "></span></span>

<span data-ttu-id="af1bc-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="af1bc-117">**Script Syntax**</span></span>

<span data-ttu-id="af1bc-118">*Element* . gradientshapeok = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="af1bc-118">*element* .gradientshapeok="*expression*"</span></span>

<span data-ttu-id="af1bc-119">*expresión* = de *elemento*. gradientshapeok</span><span class="sxs-lookup"><span data-stu-id="af1bc-119">*expression*=*element*.gradientshapeok</span></span>

<span data-ttu-id="af1bc-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="af1bc-120">**Remarks**</span></span>

<span data-ttu-id="af1bc-121">Si **es true**, la ruta de acceso se rellenará con un relleno de degradado concéntrico utilizando la ruta de acceso como forma repetida del degradado. El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="af1bc-121">If **True**, the path will be filled with a concentric gradient fill using the path as the repeated shape of the gradient.The default is **False**.</span></span>

<span data-ttu-id="af1bc-122">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="af1bc-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="af1bc-123">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="af1bc-123">**Example**</span></span>

<span data-ttu-id="af1bc-124">La ruta de acceso se rellenará con un relleno de degradado concéntrico compuesto por rectángulos repetidos.</span><span class="sxs-lookup"><span data-stu-id="af1bc-124">The path will be filled with a concentric gradient fill made up of repeated rectangles.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:path gradientshapeok="True"/>
   </v:shape>
```



 

 