---
title: Atributo Origin (sesgo) (VML)
description: Atributo Origin (sesgo) (VML)
ms.assetid: 36f77073-7438-41b3-9107-95e27b01b776
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbf0c134ad8e7000e71a4237a6b5aac80e874c12
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421365"
---
# <a name="origin-attribute-skewvml"></a><span data-ttu-id="0e441-103">Atributo Origin (sesgo) (VML)</span><span class="sxs-lookup"><span data-stu-id="0e441-103">Origin Attribute (Skew)(VML)</span></span>

<span data-ttu-id="0e441-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="0e441-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="0e441-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="0e441-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="0e441-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="0e441-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="0e441-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="0e441-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="0e441-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="0e441-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="0e441-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="0e441-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="0e441-110">Define el origen del sesgo.</span><span class="sxs-lookup"><span data-stu-id="0e441-110">Defines the origin of the skew.</span></span> <span data-ttu-id="0e441-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0e441-111">Read/write.</span></span> <span data-ttu-id="0e441-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="0e441-112">**VgVector2D**.</span></span>

<span data-ttu-id="0e441-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="0e441-113">**Applies To**</span></span>

[<span data-ttu-id="0e441-114">Sesgar</span><span class="sxs-lookup"><span data-stu-id="0e441-114">Skew</span></span>](msdn-online-vml-skew-element.md)

<span data-ttu-id="0e441-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="0e441-115">**Tag Syntax**</span></span>

<span data-ttu-id="0e441-116"><o: *elemento* Origin = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="0e441-116"><o: *element* origin=" *expression* "></span></span>

<span data-ttu-id="0e441-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="0e441-117">**Script Syntax**</span></span>

<span data-ttu-id="0e441-118">*Element* . Origin = "*expresión \* *"**</span><span class="sxs-lookup"><span data-stu-id="0e441-118">*element* .origin="*expression\*\*\*"*\*</span></span>

<span data-ttu-id="0e441-119">*expresión* = de *elemento*. Origin</span><span class="sxs-lookup"><span data-stu-id="0e441-119">*expression*=*element*.origin</span></span>

<span data-ttu-id="0e441-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="0e441-120">**Remarks**</span></span>

<span data-ttu-id="0e441-121">Los valores suelen ser un porcentaje del tamaño de la forma y el intervalo de-0,5 a + 0,5.</span><span class="sxs-lookup"><span data-stu-id="0e441-121">Values are typically a percentage of the shape's size and range from -0.5 to +0.5.</span></span> <span data-ttu-id="0e441-122">Se permiten valores mayores que proporcionan desplazamientos como múltiplos del tamaño de la forma.</span><span class="sxs-lookup"><span data-stu-id="0e441-122">Larger values are allowed that give offsets as multiples of the shape's size.</span></span> <span data-ttu-id="0e441-123">El valor predeterminado es 0, 0.</span><span class="sxs-lookup"><span data-stu-id="0e441-123">The default is 0,0.</span></span>

<span data-ttu-id="0e441-124">*Microsoft Office atributo Extensions*</span><span class="sxs-lookup"><span data-stu-id="0e441-124">*Microsoft Office Extensions Attribute*</span></span>

 

 