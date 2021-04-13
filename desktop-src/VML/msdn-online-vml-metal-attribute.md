---
title: Atributo de metal de VML
description: Atributo de metal de VML
ms.assetid: 4d2efaed-d391-494f-9f0c-d57ad019f71d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d318724f0a8f3c5fbce1ee9045ed5d6e0d49686
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420753"
---
# <a name="vml-metal-attribute"></a><span data-ttu-id="cb974-103">Atributo de metal de VML</span><span class="sxs-lookup"><span data-stu-id="cb974-103">VML Metal Attribute</span></span>

<span data-ttu-id="cb974-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="cb974-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="cb974-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="cb974-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="cb974-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="cb974-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="cb974-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="cb974-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="cb974-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="cb974-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="cb974-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="cb974-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="cb974-110">Determina si la superficie de la forma extruida se parecerá a metal.</span><span class="sxs-lookup"><span data-stu-id="cb974-110">Determines whether the surface of the extruded shape will resemble metal.</span></span> <span data-ttu-id="cb974-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="cb974-111">Read/write.</span></span> <span data-ttu-id="cb974-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="cb974-112">**VgTriState**.</span></span>

<span data-ttu-id="cb974-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="cb974-113">**Applies To**</span></span>

[<span data-ttu-id="cb974-114">Trusión</span><span class="sxs-lookup"><span data-stu-id="cb974-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="cb974-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="cb974-115">**Tag Syntax**</span></span>

<span data-ttu-id="cb974-116"><o: *elemento* metal = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="cb974-116"><o: *element* metal=" *expression* "></span></span>

<span data-ttu-id="cb974-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="cb974-117">**Script Syntax**</span></span>

<span data-ttu-id="cb974-118">*Element* . metal = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="cb974-118">*element* .metal="*expression*"</span></span>

<span data-ttu-id="cb974-119">*expresión* = de *elemento*. metal</span><span class="sxs-lookup"><span data-stu-id="cb974-119">*expression*=*element*.metal</span></span>

<span data-ttu-id="cb974-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="cb974-120">**Remarks**</span></span>

<span data-ttu-id="cb974-121">Si se establece en **true**, este atributo hace que la luz reflejada especular sea el color del material en lugar del color de la fuente de luz, lo que hace que el objeto parezca más metálico. Para aproximarse más a un material metálico, es necesario que la especulación sea relativamente alta (aproximadamente 1,2) y que la difusión sea relativamente baja (aproximadamente 0,6).</span><span class="sxs-lookup"><span data-stu-id="cb974-121">If set to **True**, this attribute causes the specularly reflected light to be the material color instead of the light source color, making the object seem more metallic.To further approximate a metallic material requires that specularity be relatively high (about 1.2) and diffusity be relatively low (about 0.6).</span></span> <span data-ttu-id="cb974-122">El valor predeterminado es **False**.</span><span class="sxs-lookup"><span data-stu-id="cb974-122">The default value is **False**.</span></span>

<span data-ttu-id="cb974-123">*Microsoft Office atributo Extensions*</span><span class="sxs-lookup"><span data-stu-id="cb974-123">*Microsoft Office Extensions Attribute*</span></span>

 

 