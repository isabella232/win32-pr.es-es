---
title: Atributo de botón VML
description: Atributo de botón VML
ms.assetid: 273024ac-683f-48d2-b6a0-574824f4c05d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f2760fceaf52e3f9ee217d4c3d249fb670a845f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676417"
---
# <a name="vml-button-attribute"></a><span data-ttu-id="ead2a-103">Atributo de botón VML</span><span class="sxs-lookup"><span data-stu-id="ead2a-103">VML Button Attribute</span></span>

<span data-ttu-id="ead2a-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="ead2a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ead2a-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="ead2a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ead2a-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="ead2a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ead2a-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="ead2a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ead2a-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ead2a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ead2a-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ead2a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ead2a-110">Determina si una forma se procesará como un botón.</span><span class="sxs-lookup"><span data-stu-id="ead2a-110">Determines whether a shape will be processed as a button.</span></span> <span data-ttu-id="ead2a-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ead2a-111">Read/write.</span></span> <span data-ttu-id="ead2a-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="ead2a-112">**VgTriState**.</span></span>

<span data-ttu-id="ead2a-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="ead2a-113">**Applies To**</span></span>

[<span data-ttu-id="ead2a-114">Forma</span><span class="sxs-lookup"><span data-stu-id="ead2a-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="ead2a-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="ead2a-115">**Tag Syntax**</span></span>

<span data-ttu-id="ead2a-116"><v: *Element* o:Button = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="ead2a-116"><v: *element* o:button=" *expression* "></span></span>

<span data-ttu-id="ead2a-117">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="ead2a-117">**Remarks**</span></span>

<span data-ttu-id="ead2a-118">El valor predeterminado es **False**.</span><span class="sxs-lookup"><span data-stu-id="ead2a-118">The default is **False**.</span></span> <span data-ttu-id="ead2a-119">Si es **true**, la forma se procesa como un botón.</span><span class="sxs-lookup"><span data-stu-id="ead2a-119">If **True**, the shape is processed as a button.</span></span>

<span data-ttu-id="ead2a-120">*Microsoft Office atributo Extensions*</span><span class="sxs-lookup"><span data-stu-id="ead2a-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="ead2a-121">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="ead2a-121">**Example**</span></span>

<span data-ttu-id="ead2a-122">La forma es un botón.</span><span class="sxs-lookup"><span data-stu-id="ead2a-122">The shape is a button.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:button="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 