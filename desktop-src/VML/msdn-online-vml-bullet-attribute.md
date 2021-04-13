---
title: Atributo de viñeta VML
description: Atributo de viñeta VML
ms.assetid: 17c24b97-191b-4170-8a2d-9284f500e728
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4edcf1194a234284a70f928adad198ca77f597a9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420936"
---
# <a name="vml-bullet-attribute"></a><span data-ttu-id="81fe3-103">Atributo de viñeta VML</span><span class="sxs-lookup"><span data-stu-id="81fe3-103">VML Bullet Attribute</span></span>

<span data-ttu-id="81fe3-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="81fe3-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="81fe3-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="81fe3-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="81fe3-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="81fe3-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="81fe3-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="81fe3-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="81fe3-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="81fe3-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="81fe3-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="81fe3-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="81fe3-110">Determina si una forma es una viñeta gráfica.</span><span class="sxs-lookup"><span data-stu-id="81fe3-110">Determines whether a shape is a graphical bullet.</span></span> <span data-ttu-id="81fe3-111">**VgTriState** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="81fe3-111">Read/write **VgTriState**.</span></span>

<span data-ttu-id="81fe3-112">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="81fe3-112">**Applies To**</span></span>

[<span data-ttu-id="81fe3-113">Forma</span><span class="sxs-lookup"><span data-stu-id="81fe3-113">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="81fe3-114">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="81fe3-114">**Tag Syntax**</span></span>

<span data-ttu-id="81fe3-115"><v: *Element* o:Bullet = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="81fe3-115"><v: *element* o:bullet=" *expression* "></span></span>

<span data-ttu-id="81fe3-116">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="81fe3-116">**Remarks**</span></span>

<span data-ttu-id="81fe3-117">El valor predeterminado es **False**.</span><span class="sxs-lookup"><span data-stu-id="81fe3-117">The default is **False**.</span></span> <span data-ttu-id="81fe3-118">Si es **true**, la forma es una viñeta gráfica.</span><span class="sxs-lookup"><span data-stu-id="81fe3-118">If **True**, the shape is a graphical bullet.</span></span>

<span data-ttu-id="81fe3-119">*Microsoft Office atributo Extensions*</span><span class="sxs-lookup"><span data-stu-id="81fe3-119">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="81fe3-120">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="81fe3-120">**Example**</span></span>

<span data-ttu-id="81fe3-121">La forma es una viñeta.</span><span class="sxs-lookup"><span data-stu-id="81fe3-121">The shape is a bullet.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:bullet="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 