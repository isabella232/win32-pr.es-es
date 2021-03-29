---
title: Atributo InvX de VML
description: Atributo InvX de VML
ms.assetid: 59fbd4c0-ae31-4198-a9e7-be12cd50288f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37d244b5feff319112959d3093927f11d1e92164
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792207"
---
# <a name="vml-invx-attribute"></a><span data-ttu-id="8e7b2-103">Atributo InvX de VML</span><span class="sxs-lookup"><span data-stu-id="8e7b2-103">VML InvX Attribute</span></span>

<span data-ttu-id="8e7b2-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="8e7b2-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8e7b2-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="8e7b2-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8e7b2-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="8e7b2-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8e7b2-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="8e7b2-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8e7b2-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="8e7b2-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8e7b2-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="8e7b2-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8e7b2-110">Determina si se invierte la posición x del identificador.</span><span class="sxs-lookup"><span data-stu-id="8e7b2-110">Determines whether the x position of the handle is inverted.</span></span> <span data-ttu-id="8e7b2-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="8e7b2-111">Read/write.</span></span> <span data-ttu-id="8e7b2-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="8e7b2-112">**VgTriState**.</span></span>

<span data-ttu-id="8e7b2-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="8e7b2-113">**Applies To**</span></span>

<span data-ttu-id="8e7b2-114">[H](msdn-online-vml-h-element.md) (subelemento de [Handles](msdn-online-vml-handles-element.md))</span><span class="sxs-lookup"><span data-stu-id="8e7b2-114">[H](msdn-online-vml-h-element.md) (subelement of [Handles](msdn-online-vml-handles-element.md))</span></span>

<span data-ttu-id="8e7b2-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="8e7b2-115">**Tag Syntax**</span></span>

<span data-ttu-id="8e7b2-116"><v: *Element* INVX = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="8e7b2-116"><v: *element* invx=" *expression* "></span></span>

<span data-ttu-id="8e7b2-117">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="8e7b2-117">**Remarks**</span></span>

<span data-ttu-id="8e7b2-118">Si es **true**, la posición x del identificador se invierte restando el valor x del valor x de **CoordOrigin** agregado al valor x de **CoordSize**.</span><span class="sxs-lookup"><span data-stu-id="8e7b2-118">If **True**, the x position of the handle is inverted by subtracting the x value from the x value of **CoordOrigin** added to the x value of **CoordSize**.</span></span> <span data-ttu-id="8e7b2-119">El valor predeterminado es **False**.</span><span class="sxs-lookup"><span data-stu-id="8e7b2-119">The default value is **False**.</span></span>

<span data-ttu-id="8e7b2-120">Este atributo es el equivalente de</span><span class="sxs-lookup"><span data-stu-id="8e7b2-120">This attribute is the equivalent of</span></span>

<span data-ttu-id="8e7b2-121">coordorigin. x + coordsize. x-h. position. x</span><span class="sxs-lookup"><span data-stu-id="8e7b2-121">coordorigin.x + coordsize.x - h.position.x</span></span>

<span data-ttu-id="8e7b2-122">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="8e7b2-122">*VML Standard Attribute*</span></span>

 

 