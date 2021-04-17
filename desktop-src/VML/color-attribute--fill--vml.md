---
title: Atributo de color (relleno) (VML)
description: Atributo de color (relleno) (VML)
ms.assetid: 38e75bf5-4da9-4c58-af86-3554d03a6b7b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8480b3a013add36533a82b31338fba301e8353db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487774"
---
# <a name="color-attribute-fillvml"></a><span data-ttu-id="c93ed-103">Atributo de color (relleno) (VML)</span><span class="sxs-lookup"><span data-stu-id="c93ed-103">Color Attribute (Fill)(VML)</span></span>

<span data-ttu-id="c93ed-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c93ed-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c93ed-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="c93ed-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c93ed-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="c93ed-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c93ed-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="c93ed-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c93ed-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c93ed-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c93ed-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c93ed-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c93ed-110">Define el color de un relleno.</span><span class="sxs-lookup"><span data-stu-id="c93ed-110">Defines the color of a fill.</span></span> <span data-ttu-id="c93ed-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c93ed-111">Read/write.</span></span> <span data-ttu-id="c93ed-112">**VgColor**.</span><span class="sxs-lookup"><span data-stu-id="c93ed-112">**VgColor**.</span></span>

<span data-ttu-id="c93ed-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="c93ed-113">**Applies To**</span></span>

[<span data-ttu-id="c93ed-114">Fill</span><span class="sxs-lookup"><span data-stu-id="c93ed-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="c93ed-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="c93ed-115">**Tag Syntax**</span></span>

<span data-ttu-id="c93ed-116"><v: *elemento* color = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="c93ed-116"><v: *element* color=" *expression* "></span></span>

<span data-ttu-id="c93ed-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="c93ed-117">**Script Syntax**</span></span>

<span data-ttu-id="c93ed-118">*Element* . color = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="c93ed-118">*element* .color="*expression*"</span></span>

<span data-ttu-id="c93ed-119">*expresión* = de *elemento*. color</span><span class="sxs-lookup"><span data-stu-id="c93ed-119">*expression*=*element*.color</span></span>

<span data-ttu-id="c93ed-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="c93ed-120">**Remarks**</span></span>

<span data-ttu-id="c93ed-121">Invalida el atributo **fillColor** de una forma.</span><span class="sxs-lookup"><span data-stu-id="c93ed-121">Overrides the **FillColor** attribute of a shape.</span></span> <span data-ttu-id="c93ed-122">El valor predeterminado es **blanco**.</span><span class="sxs-lookup"><span data-stu-id="c93ed-122">The default value is **White**.</span></span>

<span data-ttu-id="c93ed-123">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="c93ed-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="c93ed-124">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="c93ed-124">**Example**</span></span>

<span data-ttu-id="c93ed-125">El color de relleno de la forma es verde.</span><span class="sxs-lookup"><span data-stu-id="c93ed-125">The fill color of the shape is green.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="green"/>
   </v:shape>
```



 

 