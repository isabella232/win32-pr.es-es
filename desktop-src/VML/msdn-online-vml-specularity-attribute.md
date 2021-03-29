---
title: Atributo de especulación VML
description: Atributo de especulación VML
ms.assetid: df04c15c-cfad-4172-81fa-a28e13f205fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5b4e8814a9bd0cd897ae018cf8b37aa67d732aa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904689"
---
# <a name="vml-specularity-attribute"></a><span data-ttu-id="42938-103">Atributo de especulación VML</span><span class="sxs-lookup"><span data-stu-id="42938-103">VML Specularity Attribute</span></span>

<span data-ttu-id="42938-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="42938-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="42938-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="42938-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="42938-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="42938-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="42938-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="42938-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="42938-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="42938-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="42938-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="42938-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="42938-110">Define la especulación de una forma extruida.</span><span class="sxs-lookup"><span data-stu-id="42938-110">Defines the specularity of an extruded shape.</span></span> <span data-ttu-id="42938-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="42938-111">Read/write.</span></span> <span data-ttu-id="42938-112">**VgNumber**.</span><span class="sxs-lookup"><span data-stu-id="42938-112">**VgNumber**.</span></span>

<span data-ttu-id="42938-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="42938-113">**Applies To**</span></span>

[<span data-ttu-id="42938-114">Trusión</span><span class="sxs-lookup"><span data-stu-id="42938-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="42938-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="42938-115">**Tag Syntax**</span></span>

<span data-ttu-id="42938-116"><o: especular de *elemento* = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="42938-116"><o: *element* specularity=" *expression* "></span></span>

<span data-ttu-id="42938-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="42938-117">**Script Syntax**</span></span>

<span data-ttu-id="42938-118">*Element* . especulate = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="42938-118">*element* .specularity="*expression*"</span></span>

<span data-ttu-id="42938-119">*expresión* = de *elemento*. especulate</span><span class="sxs-lookup"><span data-stu-id="42938-119">*expression*=*element*.specularity</span></span>

<span data-ttu-id="42938-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="42938-120">**Remarks**</span></span>

<span data-ttu-id="42938-121">Este valor define la relación de la luz de incidente con la luz reflejada especular.</span><span class="sxs-lookup"><span data-stu-id="42938-121">This value defines the ratio of incident light to specularly reflected light.</span></span> <span data-ttu-id="42938-122">Los valores normales oscilan entre 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="42938-122">Normal values range from 0 to 1.</span></span> <span data-ttu-id="42938-123">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="42938-123">The default value is 0.</span></span>

<span data-ttu-id="42938-124">Si se especifican valores mayores que 1, se pueden producir efectos inusuales.</span><span class="sxs-lookup"><span data-stu-id="42938-124">If values greater than 1 are specified, unusual effects can result.</span></span>

<span data-ttu-id="42938-125">Microsoft Office atributo Extensions</span><span class="sxs-lookup"><span data-stu-id="42938-125">Microsoft Office Extensions Attribute</span></span>

 

 