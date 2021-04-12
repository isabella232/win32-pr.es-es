---
title: EXT (atributo) (sesgo) (VML)
description: EXT (atributo) (sesgo) (VML)
ms.assetid: ff1dfb2f-9098-4418-a2f7-c7159328bd09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 153273f613d188ae9e6fe733b2d0337c5010295d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104271296"
---
# <a name="ext-attribute-skewvml"></a><span data-ttu-id="e530b-103">EXT (atributo) (sesgo) (VML)</span><span class="sxs-lookup"><span data-stu-id="e530b-103">Ext Attribute (Skew)(VML)</span></span>

<span data-ttu-id="e530b-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="e530b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e530b-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="e530b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e530b-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="e530b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e530b-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="e530b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e530b-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e530b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e530b-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e530b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e530b-110">Define la forma en que se muestra un sesgo.</span><span class="sxs-lookup"><span data-stu-id="e530b-110">Defines the way a skew is displayed.</span></span> <span data-ttu-id="e530b-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e530b-111">Read/write.</span></span> <span data-ttu-id="e530b-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="e530b-112">**String**.</span></span>

<span data-ttu-id="e530b-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="e530b-113">**Applies To**</span></span>

[<span data-ttu-id="e530b-114">Sesgar</span><span class="sxs-lookup"><span data-stu-id="e530b-114">Skew</span></span>](msdn-online-vml-skew-element.md)

<span data-ttu-id="e530b-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="e530b-115">**Tag Syntax**</span></span>

<span data-ttu-id="e530b-116"><o: *elemento* v:EXT = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="e530b-116"><o: *element* v:ext=" *expression* "></span></span>

<span data-ttu-id="e530b-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="e530b-117">**Script Syntax**</span></span>

<span data-ttu-id="e530b-118">*Element* . ext = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="e530b-118">*element* .ext="*expression*"</span></span>

<span data-ttu-id="e530b-119">*expresión* = de *elemento*. ext</span><span class="sxs-lookup"><span data-stu-id="e530b-119">*expression*=*element*.ext</span></span>

<span data-ttu-id="e530b-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="e530b-120">**Remarks**</span></span>

<span data-ttu-id="e530b-121">Este atributo se utiliza para indicar a los Editores gráficos cómo procesar el elemento de **sesgo** .</span><span class="sxs-lookup"><span data-stu-id="e530b-121">This attribute is used to tell graphical editors how to process the **Skew** element.</span></span> <span data-ttu-id="e530b-122">Estos valores incluyen:</span><span class="sxs-lookup"><span data-stu-id="e530b-122">Values include:</span></span>

-   <span data-ttu-id="e530b-123">**edit**</span><span class="sxs-lookup"><span data-stu-id="e530b-123">**edit**</span></span>
-   <span data-ttu-id="e530b-124">**vista** (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="e530b-124">**view** (default)</span></span>
-   <span data-ttu-id="e530b-125">**backwardCompatible**</span><span class="sxs-lookup"><span data-stu-id="e530b-125">**backwardCompatible**</span></span>

<span data-ttu-id="e530b-126">Si una extensión está establecida en **Editar**, puede ser omitida por un visor de software.</span><span class="sxs-lookup"><span data-stu-id="e530b-126">If an extension is set to **edit**, it can be ignored by a software viewer.</span></span> <span data-ttu-id="e530b-127">Si se establece en **Ver**, el visor debe representar la representación del mapa de bits en su lugar.</span><span class="sxs-lookup"><span data-stu-id="e530b-127">If set to **view**, the viewer must render the bitmap representation instead.</span></span>

<span data-ttu-id="e530b-128">*Microsoft Office atributo Extensions*</span><span class="sxs-lookup"><span data-stu-id="e530b-128">*Microsoft Office Extensions Attribute*</span></span>

 

 