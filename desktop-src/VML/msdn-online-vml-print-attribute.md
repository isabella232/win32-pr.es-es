---
title: Atributo de impresión VML
description: Atributo de impresión VML
ms.assetid: ef9f9f11-782a-40db-986c-946d9ee03071
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55925621ab56f011c998f3feac21a892a4d7ea66
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676393"
---
# <a name="vml-print-attribute"></a><span data-ttu-id="9bed3-103">Atributo de impresión VML</span><span class="sxs-lookup"><span data-stu-id="9bed3-103">VML Print Attribute</span></span>

<span data-ttu-id="9bed3-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="9bed3-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="9bed3-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="9bed3-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="9bed3-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="9bed3-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="9bed3-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="9bed3-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="9bed3-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="9bed3-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="9bed3-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="9bed3-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="9bed3-110">Determina si la forma se va a imprimir.</span><span class="sxs-lookup"><span data-stu-id="9bed3-110">Determines whether the shape will be printed.</span></span> <span data-ttu-id="9bed3-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="9bed3-111">Read/write.</span></span> <span data-ttu-id="9bed3-112">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="9bed3-112">[VgTriState](msdn-online-vml-vgtristate.md).</span></span>

<span data-ttu-id="9bed3-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="9bed3-113">**Applies To**</span></span>

[<span data-ttu-id="9bed3-114">Forma</span><span class="sxs-lookup"><span data-stu-id="9bed3-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="9bed3-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="9bed3-115">**Tag Syntax**</span></span>

<span data-ttu-id="9bed3-116"><v: *Element* Print = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="9bed3-116"><v: *element* print=" *expression* "></span></span>

<span data-ttu-id="9bed3-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="9bed3-117">**Script Syntax**</span></span>

<span data-ttu-id="9bed3-118">*Element* . Print = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="9bed3-118">*element* .print="*expression*"</span></span>

<span data-ttu-id="9bed3-119">*expresión* = de *elemento*. Print</span><span class="sxs-lookup"><span data-stu-id="9bed3-119">*expression*=*element*.print</span></span>

<span data-ttu-id="9bed3-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="9bed3-120">**Remarks**</span></span>

<span data-ttu-id="9bed3-121">Se proporciona como una manera de especificar si se van a imprimir las formas.</span><span class="sxs-lookup"><span data-stu-id="9bed3-121">Provided as a way to specify whether shapes will be printed.</span></span> <span data-ttu-id="9bed3-122">Tenga en cuenta que todavía se puede mostrar una forma en la pantalla, aunque no se imprima como resultado de que este atributo sea **falso**.</span><span class="sxs-lookup"><span data-stu-id="9bed3-122">Note that a shape can still be displayed on the screen, even if it is not printed as a result of this attribute being **False**.</span></span> <span data-ttu-id="9bed3-123">El valor predeterminado es **True**.</span><span class="sxs-lookup"><span data-stu-id="9bed3-123">The default value is **True**.</span></span>

<span data-ttu-id="9bed3-124">Este atributo lo usa Microsoft Office pero Microsoft Internet Explorer no lo usa.</span><span class="sxs-lookup"><span data-stu-id="9bed3-124">This attribute is used by Microsoft Office but is not used by Microsoft Internet Explorer.</span></span>

<span data-ttu-id="9bed3-125">*Microsoft Office atributo Extensions*</span><span class="sxs-lookup"><span data-stu-id="9bed3-125">*Microsoft Office Extensions Attribute*</span></span>

 

 