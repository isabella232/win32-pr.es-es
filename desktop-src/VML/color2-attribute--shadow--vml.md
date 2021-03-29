---
title: Atributo color2 (Shadow) (VML)
description: Atributo color2 (Shadow) (VML)
ms.assetid: 265d189a-1a11-4f57-9299-1bc1efd13595
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e735d7672457153881d384c7b625199cf4a202e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793047"
---
# <a name="color2-attribute-shadowvml"></a><span data-ttu-id="3454a-103">Atributo color2 (Shadow) (VML)</span><span class="sxs-lookup"><span data-stu-id="3454a-103">Color2 Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="3454a-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="3454a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3454a-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="3454a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3454a-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="3454a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3454a-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="3454a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3454a-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3454a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3454a-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3454a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3454a-110">Define el segundo color de una sombra.</span><span class="sxs-lookup"><span data-stu-id="3454a-110">Defines the second color of a shadow.</span></span> <span data-ttu-id="3454a-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3454a-111">Read/write.</span></span> <span data-ttu-id="3454a-112">**VgColor**.</span><span class="sxs-lookup"><span data-stu-id="3454a-112">**VgColor**.</span></span>

<span data-ttu-id="3454a-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="3454a-113">**Applies To**</span></span>

[<span data-ttu-id="3454a-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="3454a-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="3454a-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="3454a-115">**Tag Syntax**</span></span>

<span data-ttu-id="3454a-116"><v: *elemento* color2 = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="3454a-116"><v: *element* color2=" *expression* "></span></span>

<span data-ttu-id="3454a-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="3454a-117">**Script Syntax**</span></span>

<span data-ttu-id="3454a-118">*Element* . color2 = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="3454a-118">*element* .color2="*expression*"</span></span>

<span data-ttu-id="3454a-119">*expresión* = de *elemento*. color2</span><span class="sxs-lookup"><span data-stu-id="3454a-119">*expression*=*element*.color2</span></span>

<span data-ttu-id="3454a-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="3454a-120">**Remarks**</span></span>

<span data-ttu-id="3454a-121">Use un segundo color para crear efectos de sombra especiales.</span><span class="sxs-lookup"><span data-stu-id="3454a-121">Use a second color to create special shadow effects.</span></span> <span data-ttu-id="3454a-122">Vea el atributo [Type](type-attribute--shadow--vml.md) para obtener más información sobre los segundos colores.</span><span class="sxs-lookup"><span data-stu-id="3454a-122">See the [Type](type-attribute--shadow--vml.md) attribute for more information about second colors.</span></span>

<span data-ttu-id="3454a-123">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="3454a-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="3454a-124">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="3454a-124">**Example**</span></span>

<span data-ttu-id="3454a-125">La sombra tiene un azul para un segundo color.</span><span class="sxs-lookup"><span data-stu-id="3454a-125">The shadow has blue for a second color.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" color="green" color2="blue"/>
   </v:shape>
```



 

 