---
title: Atributo de color (sombra) (VML)
description: Atributo de color (sombra) (VML)
ms.assetid: 677615b7-b4a4-411f-b04e-3ed0399f4c05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73df77e65a3ae0f74c6e79b9c179c31da27698f9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695620"
---
# <a name="color-attribute-shadowvml"></a><span data-ttu-id="4cdf5-103">Atributo de color (sombra) (VML)</span><span class="sxs-lookup"><span data-stu-id="4cdf5-103">Color Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="4cdf5-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="4cdf5-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="4cdf5-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="4cdf5-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="4cdf5-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="4cdf5-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="4cdf5-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="4cdf5-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="4cdf5-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="4cdf5-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="4cdf5-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="4cdf5-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="4cdf5-110">Define el color de la sombra.</span><span class="sxs-lookup"><span data-stu-id="4cdf5-110">Defines the color of the shadow.</span></span> <span data-ttu-id="4cdf5-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4cdf5-111">Read/write.</span></span> <span data-ttu-id="4cdf5-112">**VgColor**.</span><span class="sxs-lookup"><span data-stu-id="4cdf5-112">**VgColor**.</span></span>

<span data-ttu-id="4cdf5-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="4cdf5-113">**Applies To**</span></span>

[<span data-ttu-id="4cdf5-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="4cdf5-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="4cdf5-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="4cdf5-115">**Tag Syntax**</span></span>

<span data-ttu-id="4cdf5-116"><v: *elemento* color = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="4cdf5-116"><v: *element* color=" *expression* "></span></span>

<span data-ttu-id="4cdf5-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="4cdf5-117">**Script Syntax**</span></span>

<span data-ttu-id="4cdf5-118">*Element* . color = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="4cdf5-118">*element* .color="*expression*"</span></span>

<span data-ttu-id="4cdf5-119">*expresión* = de *elemento*. color</span><span class="sxs-lookup"><span data-stu-id="4cdf5-119">*expression*=*element*.color</span></span>

<span data-ttu-id="4cdf5-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="4cdf5-120">**Remarks**</span></span>

<span data-ttu-id="4cdf5-121">Use el atributo color para establecer u obtener el color de una sombra.</span><span class="sxs-lookup"><span data-stu-id="4cdf5-121">Use the color attribute to set or get the color of a shadow.</span></span>

<span data-ttu-id="4cdf5-122">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="4cdf5-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="4cdf5-123">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="4cdf5-123">**Example**</span></span>

<span data-ttu-id="4cdf5-124">La sombra es verde.</span><span class="sxs-lookup"><span data-stu-id="4cdf5-124">The shadow is green.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" color="green"/>
   </v:shape>
```



 

 