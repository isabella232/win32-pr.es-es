---
title: Atributo UserHidden de VML
description: Atributo UserHidden de VML
ms.assetid: 0e4616c7-a456-4157-b77a-56cd289e913c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 519857d53cbec985afae31a5e7dea8811773dc43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695636"
---
# <a name="vml-userhidden-attribute"></a><span data-ttu-id="b1bb4-103">Atributo UserHidden de VML</span><span class="sxs-lookup"><span data-stu-id="b1bb4-103">VML UserHidden Attribute</span></span>

<span data-ttu-id="b1bb4-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="b1bb4-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b1bb4-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="b1bb4-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b1bb4-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="b1bb4-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b1bb4-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="b1bb4-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b1bb4-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b1bb4-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b1bb4-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b1bb4-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b1bb4-110">Determina si un delimitador de script está oculto.</span><span class="sxs-lookup"><span data-stu-id="b1bb4-110">Determines whether a script anchor is hidden.</span></span> <span data-ttu-id="b1bb4-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b1bb4-111">Read/write.</span></span> <span data-ttu-id="b1bb4-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="b1bb4-112">**VgTriState**.</span></span>

<span data-ttu-id="b1bb4-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="b1bb4-113">**Applies To**</span></span>

[<span data-ttu-id="b1bb4-114">Forma</span><span class="sxs-lookup"><span data-stu-id="b1bb4-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="b1bb4-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="b1bb4-115">**Tag Syntax**</span></span>

<span data-ttu-id="b1bb4-116"><v: *Element* o:userhidden = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="b1bb4-116"><v: *element* o:userhidden=" *expression* "></span></span>

<span data-ttu-id="b1bb4-117">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="b1bb4-117">**Remarks**</span></span>

<span data-ttu-id="b1bb4-118">El valor predeterminado es **False**.</span><span class="sxs-lookup"><span data-stu-id="b1bb4-118">The default is **False**.</span></span> <span data-ttu-id="b1bb4-119">Si **es true**, los delimitadores de script permanecen ocultos aunque la forma esté visible de otro modo.</span><span class="sxs-lookup"><span data-stu-id="b1bb4-119">If **True**, script anchors stay hidden even if the shape is otherwise visible.</span></span>

<span data-ttu-id="b1bb4-120">*Microsoft Office atributo Extensions*</span><span class="sxs-lookup"><span data-stu-id="b1bb4-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="b1bb4-121">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="b1bb4-121">**Example**</span></span>

<span data-ttu-id="b1bb4-122">El delimitador de script de la forma está oculto.</span><span class="sxs-lookup"><span data-stu-id="b1bb4-122">The script anchor of the shape is hidden.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" userhidden="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 