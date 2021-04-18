---
title: Atributo InvY de VML
description: Atributo InvY de VML
ms.assetid: 6c8c51ab-88ce-40b2-add7-1152e125ad8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a728d804d771f79b892ee6616cca527dba42bfa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359107"
---
# <a name="vml-invy-attribute"></a><span data-ttu-id="fd7e6-103">Atributo InvY de VML</span><span class="sxs-lookup"><span data-stu-id="fd7e6-103">VML InvY Attribute</span></span>

<span data-ttu-id="fd7e6-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="fd7e6-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="fd7e6-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="fd7e6-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="fd7e6-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="fd7e6-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="fd7e6-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="fd7e6-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="fd7e6-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="fd7e6-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="fd7e6-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="fd7e6-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="fd7e6-110">Determina si se invierte la posición y del identificador.</span><span class="sxs-lookup"><span data-stu-id="fd7e6-110">Determines whether the y position of the handle is inverted.</span></span> <span data-ttu-id="fd7e6-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="fd7e6-111">Read/write.</span></span> <span data-ttu-id="fd7e6-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="fd7e6-112">**VgTriState**.</span></span>

<span data-ttu-id="fd7e6-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="fd7e6-113">**Applies To**</span></span>

<span data-ttu-id="fd7e6-114">[H](msdn-online-vml-h-element.md) (subelemento de [Handles](msdn-online-vml-handles-element.md))</span><span class="sxs-lookup"><span data-stu-id="fd7e6-114">[H](msdn-online-vml-h-element.md) (subelement of [Handles](msdn-online-vml-handles-element.md))</span></span>

<span data-ttu-id="fd7e6-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="fd7e6-115">**Tag Syntax**</span></span>

<span data-ttu-id="fd7e6-116"><v: *Element* invy = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="fd7e6-116"><v: *element* invy=" *expression* "></span></span>

<span data-ttu-id="fd7e6-117">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="fd7e6-117">**Remarks**</span></span>

<span data-ttu-id="fd7e6-118">Si es **true**, la posición y del identificador se invierte restando el valor y del valor y de **CoordOrigin** agregado al valor y de **CoordSize**.</span><span class="sxs-lookup"><span data-stu-id="fd7e6-118">If **True**, the y position of the handle is inverted by subtracting the y value from the y value of **CoordOrigin** added to the y value of **CoordSize**.</span></span> <span data-ttu-id="fd7e6-119">El valor predeterminado es **False**.</span><span class="sxs-lookup"><span data-stu-id="fd7e6-119">The default value is **False**.</span></span>

<span data-ttu-id="fd7e6-120">Este atributo es el equivalente de</span><span class="sxs-lookup"><span data-stu-id="fd7e6-120">This attribute is the equivalent of</span></span>


```HTML
coordorigin.y + coordsize.y - h.position.y
```



<span data-ttu-id="fd7e6-121">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="fd7e6-121">*VML Standard Attribute*</span></span>

 

 