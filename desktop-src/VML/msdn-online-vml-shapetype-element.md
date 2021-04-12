---
title: Elemento TipoForma de VML
description: Elemento TipoForma de VML
ms.assetid: 4e0288c9-ab0f-4399-982a-97dcf16f4ec4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebbb35eef0a3c987fe1e6ec35d15701236ae0af1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104271270"
---
# <a name="vml-shapetype-element"></a><span data-ttu-id="b45bc-103">Elemento TipoForma de VML</span><span class="sxs-lookup"><span data-stu-id="b45bc-103">VML ShapeType Element</span></span>

<span data-ttu-id="b45bc-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="b45bc-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b45bc-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="b45bc-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b45bc-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="b45bc-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b45bc-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="b45bc-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b45bc-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b45bc-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b45bc-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b45bc-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b45bc-110">Define una forma que se puede utilizar para crear otras formas.</span><span class="sxs-lookup"><span data-stu-id="b45bc-110">Defines a shape that can be used to create other shapes.</span></span>

<span data-ttu-id="b45bc-111">El atributo siguiente modifica un **TipoForma**.</span><span class="sxs-lookup"><span data-stu-id="b45bc-111">The following attribute modifies a **ShapeType**.</span></span>



| <span data-ttu-id="b45bc-112">Atributo</span><span class="sxs-lookup"><span data-stu-id="b45bc-112">Attribute</span></span>                                      | <span data-ttu-id="b45bc-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="b45bc-113">Description</span></span>                                             |
|------------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="b45bc-114">Maestra</span><span class="sxs-lookup"><span data-stu-id="b45bc-114">Master</span></span>](msdn-online-vml-master-attribute.md) | <span data-ttu-id="b45bc-115">Determina si **TipoForma** es un elemento principal.</span><span class="sxs-lookup"><span data-stu-id="b45bc-115">Determines whether a **ShapeType** is a master element.</span></span> |



 

<span data-ttu-id="b45bc-116">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="b45bc-116">**Remarks**</span></span>

<span data-ttu-id="b45bc-117">**TipoForma** es idéntico al elemento **Shape** , pero no puede hacer referencia a otro elemento **TipoForma** .</span><span class="sxs-lookup"><span data-stu-id="b45bc-117">**ShapeType** is identical to the **Shape** element except it cannot reference another **ShapeType** element.</span></span>

<span data-ttu-id="b45bc-118">Cuando un elemento de **forma** hace referencia a un **TipoForma**, la **forma** puede duplicar algunas de las propiedades que ya se han especificado en el **TipoForma**.</span><span class="sxs-lookup"><span data-stu-id="b45bc-118">When a **Shape** element makes reference to a **ShapeType**, the **Shape** may duplicate some of the properties that have already been specified in the **ShapeType**.</span></span> <span data-ttu-id="b45bc-119">En estos casos, los atributos de la **forma** invalidan los del **TipoForma**.</span><span class="sxs-lookup"><span data-stu-id="b45bc-119">In these cases, the attributes in the **Shape** override those of the **ShapeType**.</span></span>

<span data-ttu-id="b45bc-120">El atributo de **tipo** no se puede usar con **TipoForma**.</span><span class="sxs-lookup"><span data-stu-id="b45bc-120">The **Type** attribute may not be used with **ShapeType**.</span></span>

<span data-ttu-id="b45bc-121">Los atributos de colocación de CSS (como **Top**, **left**, etc.) no se pasan a una **forma** de **TipoForma**.</span><span class="sxs-lookup"><span data-stu-id="b45bc-121">CSS positioning attributes (such as **Top**, **Left**, etc.) are not passed to a **Shape** from a **ShapeType**.</span></span>

<span data-ttu-id="b45bc-122">Para usar este elemento, cree un **TipoForma** con un atributo de [identificador](id-attribute--vml.md) específico.</span><span class="sxs-lookup"><span data-stu-id="b45bc-122">To use this element, create a **ShapeType** with a specific [ID](id-attribute--vml.md) attribute.</span></span> <span data-ttu-id="b45bc-123">A continuación, cree una **forma** y haga referencia al **TipoForma** con el atributo **Type** .</span><span class="sxs-lookup"><span data-stu-id="b45bc-123">Then create a **Shape** and reference the **ShapeType** with the **Type** attribute.</span></span> <span data-ttu-id="b45bc-124">Vea el atributo [Type](type-attribute--shape--vml.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="b45bc-124">See the [Type](type-attribute--shape--vml.md) attribute for more information.</span></span>

 

 