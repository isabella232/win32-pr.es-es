---
title: Atributo Origin (VMLFrame) (VML)
description: Atributo Origin (VMLFrame) (VML)
ms.assetid: 317c027e-5054-4543-ad98-2c21d1cf7154
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae9341eecea9ec1eae8aaf1d7b1ad729986a8249
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793642"
---
# <a name="origin-attribute-vmlframevml"></a><span data-ttu-id="b16bd-103">Atributo Origin (VMLFrame) (VML)</span><span class="sxs-lookup"><span data-stu-id="b16bd-103">Origin Attribute (VMLFrame)(VML)</span></span>

<span data-ttu-id="b16bd-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="b16bd-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b16bd-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="b16bd-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b16bd-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="b16bd-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b16bd-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="b16bd-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b16bd-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b16bd-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b16bd-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b16bd-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b16bd-110">Define el origen de la región de recorte del marco.</span><span class="sxs-lookup"><span data-stu-id="b16bd-110">Defines the origin of the clipping region of the frame.</span></span> <span data-ttu-id="b16bd-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b16bd-111">Read/write.</span></span> <span data-ttu-id="b16bd-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="b16bd-112">**VgVector2D**.</span></span>

<span data-ttu-id="b16bd-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="b16bd-113">**Applies To**</span></span>

[<span data-ttu-id="b16bd-114">VMLFrame</span><span class="sxs-lookup"><span data-stu-id="b16bd-114">VMLFrame</span></span>](msdn-online-vml-vmlframe-element.md)

<span data-ttu-id="b16bd-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="b16bd-115">**Tag Syntax**</span></span>

<span data-ttu-id="b16bd-116"><v: *elemento* Origin = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="b16bd-116"><v: *element* origin=" *expression* "></span></span>

<span data-ttu-id="b16bd-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="b16bd-117">**Script Syntax**</span></span>

<span data-ttu-id="b16bd-118">*Element* . Origin = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="b16bd-118">*element* .origin="*expression*"</span></span>

<span data-ttu-id="b16bd-119">*expresión* = de *elemento*. Origin</span><span class="sxs-lookup"><span data-stu-id="b16bd-119">*expression*=*element*.origin</span></span>

<span data-ttu-id="b16bd-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="b16bd-120">**Remarks**</span></span>

<span data-ttu-id="b16bd-121">El valor predeterminado es 0,0.</span><span class="sxs-lookup"><span data-stu-id="b16bd-121">The default value is 0,0.</span></span> <span data-ttu-id="b16bd-122">Tenga en cuenta que **Origin** solo funciona si [clip](msdn-online-vml-clip-attribute.md) es **true**.</span><span class="sxs-lookup"><span data-stu-id="b16bd-122">Note that **Origin** only works if [Clip](msdn-online-vml-clip-attribute.md) is **True**.</span></span> <span data-ttu-id="b16bd-123">En este atributo, el origen se define como la esquina superior izquierda del marco.</span><span class="sxs-lookup"><span data-stu-id="b16bd-123">In this attribute, the origin is defined as the upper left corner of the frame.</span></span>

<span data-ttu-id="b16bd-124">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="b16bd-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="b16bd-125">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="b16bd-125">**Example**</span></span>

<span data-ttu-id="b16bd-126">El origen de la región de recorte es 100pt, 100pt.</span><span class="sxs-lookup"><span data-stu-id="b16bd-126">The origin of the clipping region is 100pt,100pt.</span></span>


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'
   </v:vmlframe>
```



 

 