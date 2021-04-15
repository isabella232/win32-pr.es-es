---
title: Atributo de modificador VML
description: Atributo de modificador VML
ms.assetid: fc099c0a-6789-41e8-ab08-36f4fd2d3bfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9d102d6af20e698d8ec281cb1be6fae9690de4e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676386"
---
# <a name="vml-switch-attribute"></a><span data-ttu-id="a7298-103">Atributo de modificador VML</span><span class="sxs-lookup"><span data-stu-id="a7298-103">VML Switch Attribute</span></span>

<span data-ttu-id="a7298-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="a7298-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a7298-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="a7298-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a7298-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="a7298-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a7298-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="a7298-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a7298-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a7298-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a7298-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a7298-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a7298-110">Determina si las direcciones de identificador se intercambian.</span><span class="sxs-lookup"><span data-stu-id="a7298-110">Determines whether the handle directions are swapped.</span></span> <span data-ttu-id="a7298-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a7298-111">Read/write.</span></span> <span data-ttu-id="a7298-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="a7298-112">**VgTriState**.</span></span>

<span data-ttu-id="a7298-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="a7298-113">**Applies To**</span></span>

<span data-ttu-id="a7298-114">[H](msdn-online-vml-h-element.md) (subelemento de [Handles](msdn-online-vml-handles-element.md))</span><span class="sxs-lookup"><span data-stu-id="a7298-114">[H](msdn-online-vml-h-element.md) (subelement of [Handles](msdn-online-vml-handles-element.md))</span></span>

<span data-ttu-id="a7298-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="a7298-115">**Tag Syntax**</span></span>

<span data-ttu-id="a7298-116"><v: *Element* switch = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="a7298-116"><v: *element* switch=" *expression* "></span></span>

<span data-ttu-id="a7298-117">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="a7298-117">**Remarks**</span></span>

<span data-ttu-id="a7298-118">Si es **true**, el identificador se cambia entre las direcciones x e y si la forma es más alta que ancha.</span><span class="sxs-lookup"><span data-stu-id="a7298-118">If **True**, the handle is switched between the x and y directions if the shape is taller than it is wide.</span></span> <span data-ttu-id="a7298-119">El valor predeterminado es **False**.</span><span class="sxs-lookup"><span data-stu-id="a7298-119">The default value is **False**.</span></span>

<span data-ttu-id="a7298-120">Este atributo se usa para las formas con el comportamiento de stretch de limo.</span><span class="sxs-lookup"><span data-stu-id="a7298-120">This attribute is used for shapes with limo stretch behavior.</span></span>

<span data-ttu-id="a7298-121">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="a7298-121">*VML Standard Attribute*</span></span>

 

 