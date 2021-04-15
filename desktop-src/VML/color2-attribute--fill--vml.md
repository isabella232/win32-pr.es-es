---
title: Color2 (atributo, Fill) (VML)
description: Color2 (atributo, Fill) (VML)
ms.assetid: 971c8783-8c7b-43c7-8b94-01159336eef6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5689bba52277b4056f57a171f3ffc1e197aa4c8b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676449"
---
# <a name="color2-attribute-fillvml"></a><span data-ttu-id="2fefc-103">Color2 (atributo, Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="2fefc-103">Color2 Attribute (Fill)(VML)</span></span>

<span data-ttu-id="2fefc-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="2fefc-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="2fefc-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="2fefc-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="2fefc-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="2fefc-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="2fefc-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="2fefc-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="2fefc-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="2fefc-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="2fefc-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="2fefc-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="2fefc-110">Define un segundo color para los rellenos.</span><span class="sxs-lookup"><span data-stu-id="2fefc-110">Defines a second color for fills.</span></span> <span data-ttu-id="2fefc-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2fefc-111">Read/write.</span></span> <span data-ttu-id="2fefc-112">[VgColor](msdn-online-vml-ivgcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="2fefc-112">[VgColor](msdn-online-vml-ivgcolor.md) .</span></span>

<span data-ttu-id="2fefc-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="2fefc-113">**Applies To**</span></span>

[<span data-ttu-id="2fefc-114">Fill</span><span class="sxs-lookup"><span data-stu-id="2fefc-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="2fefc-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="2fefc-115">**Tag Syntax**</span></span>

<span data-ttu-id="2fefc-116"><v: *elemento* color2 = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="2fefc-116"><v: *element* color2=" *expression* "></span></span>

<span data-ttu-id="2fefc-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="2fefc-117">**Script Syntax**</span></span>

<span data-ttu-id="2fefc-118">*Element* . color2 = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="2fefc-118">*element* .color2="*expression*"</span></span>

<span data-ttu-id="2fefc-119">*expresión* = de *elemento*. color2</span><span class="sxs-lookup"><span data-stu-id="2fefc-119">*expression*=*element*.color2</span></span>

<span data-ttu-id="2fefc-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="2fefc-120">**Remarks**</span></span>

<span data-ttu-id="2fefc-121">Se utiliza un segundo color cuando un tipo de relleno es un patrón o un degradado.</span><span class="sxs-lookup"><span data-stu-id="2fefc-121">A second color is used when a fill type is a pattern or a gradient.</span></span> <span data-ttu-id="2fefc-122">El valor predeterminado es **blanco**.</span><span class="sxs-lookup"><span data-stu-id="2fefc-122">The default value is **White**.</span></span>

<span data-ttu-id="2fefc-123">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="2fefc-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="2fefc-124">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="2fefc-124">**Example**</span></span>

<span data-ttu-id="2fefc-125">El tipo de relleno de la forma es un patrón en el que la imagen de origen define el relleno de primer plano, pero el segundo color define el fondo transparente.</span><span class="sxs-lookup"><span data-stu-id="2fefc-125">The shape's fill type is a pattern where the foreground fill is defined by the source image but the transparent background is defined by the second color.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" color2="green" src="myimage.gif"/>
   </v:shape>
```



 

 