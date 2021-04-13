---
title: Elemento sesgado de VML
description: Elemento sesgado de VML
ms.assetid: ab58bbd9-5fb2-434f-adea-9b3d2d170804
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e317d03fc0bbef361df56282bec55ea2a9e708f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487739"
---
# <a name="vml-skew-element"></a><span data-ttu-id="395ab-103">Elemento sesgado de VML</span><span class="sxs-lookup"><span data-stu-id="395ab-103">VML Skew Element</span></span>

<span data-ttu-id="395ab-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="395ab-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="395ab-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="395ab-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="395ab-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="395ab-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="395ab-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="395ab-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="395ab-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="395ab-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="395ab-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="395ab-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="395ab-110">Define un sesgo para una forma.</span><span class="sxs-lookup"><span data-stu-id="395ab-110">Defines a skew for a shape.</span></span>

<span data-ttu-id="395ab-111">Los atributos siguientes modifican un sesgo.</span><span class="sxs-lookup"><span data-stu-id="395ab-111">The following attributes modify a skew.</span></span>



| <span data-ttu-id="395ab-112">Atributo</span><span class="sxs-lookup"><span data-stu-id="395ab-112">Attribute</span></span>                                 | <span data-ttu-id="395ab-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="395ab-113">Description</span></span>                                    |
|-------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="395ab-114">Total</span><span class="sxs-lookup"><span data-stu-id="395ab-114">Ext</span></span>](ext-attribute--skew--vml.md)       | <span data-ttu-id="395ab-115">Define la forma en que se muestra un sesgo.</span><span class="sxs-lookup"><span data-stu-id="395ab-115">Defines the way a skew is displayed.</span></span>           |
| [<span data-ttu-id="395ab-116">Id</span><span class="sxs-lookup"><span data-stu-id="395ab-116">ID</span></span>](id-attribute--skew--vml.md)         | <span data-ttu-id="395ab-117">Define un identificador único para un sesgo.</span><span class="sxs-lookup"><span data-stu-id="395ab-117">Defines a unique identifier for a skew.</span></span>        |
| [<span data-ttu-id="395ab-118">Matriz</span><span class="sxs-lookup"><span data-stu-id="395ab-118">Matrix</span></span>](matrix-attribute--skew--vml.md) | <span data-ttu-id="395ab-119">Define una transformación de perspectiva para un sesgo.</span><span class="sxs-lookup"><span data-stu-id="395ab-119">Defines a perspective transform for a skew.</span></span>    |
| [<span data-ttu-id="395ab-120">Offset</span><span class="sxs-lookup"><span data-stu-id="395ab-120">Offset</span></span>](offset-attribute--skew--vml.md) | <span data-ttu-id="395ab-121">Define el desplazamiento de un sesgo.</span><span class="sxs-lookup"><span data-stu-id="395ab-121">Defines the offset of a skew.</span></span>                  |
| [<span data-ttu-id="395ab-122">Activado</span><span class="sxs-lookup"><span data-stu-id="395ab-122">On</span></span>](on-attribute--skew--vml.md)         | <span data-ttu-id="395ab-123">Determina si se mostrará el sesgo.</span><span class="sxs-lookup"><span data-stu-id="395ab-123">Determines whether the skew will be displayed.</span></span> |
| [<span data-ttu-id="395ab-124">Origen</span><span class="sxs-lookup"><span data-stu-id="395ab-124">Origin</span></span>](origin-attribute--skew--vml.md) | <span data-ttu-id="395ab-125">Determina el origen de un sesgo.</span><span class="sxs-lookup"><span data-stu-id="395ab-125">Determines the origin of a skew.</span></span>               |



 

<span data-ttu-id="395ab-126">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="395ab-126">**Remarks**</span></span>

<span data-ttu-id="395ab-127">Este elemento debe definirse dentro de un elemento de [forma](shape-element--vml.md) .</span><span class="sxs-lookup"><span data-stu-id="395ab-127">This element must be defined within a [Shape](shape-element--vml.md) element.</span></span>

<span data-ttu-id="395ab-128">Además, la [matriz](matrix-attribute--skew--vml.md) [y los](on-attribute--skew--vml.md) atributos deben establecerse en **true**.</span><span class="sxs-lookup"><span data-stu-id="395ab-128">In addition, the [Matrix](matrix-attribute--skew--vml.md) and [On](on-attribute--skew--vml.md) attributes must be set to **True**.</span></span>

<span data-ttu-id="395ab-129">A continuación se encuentra el código mínimo necesario para producir un sesgo.</span><span class="sxs-lookup"><span data-stu-id="395ab-129">The following is the minimum code needed to produce a skew.</span></span>


```HTML
   <v:rect
   fillcolor="green"
   style="position:relative;top:1;left:1;width:50;height:50">
   <o:skew on="t" matrix="1,-0.5,0,0.75,0,0"/>
   </v:rect>
```



<span data-ttu-id="395ab-130">El elemento **skew** es una extensión Microsoft Office a VML.</span><span class="sxs-lookup"><span data-stu-id="395ab-130">The **Skew** element is a Microsoft Office Extension to VML.</span></span>

<span data-ttu-id="395ab-131">**Ejemplos**</span><span class="sxs-lookup"><span data-stu-id="395ab-131">**Examples**</span></span>

-   <span data-ttu-id="395ab-132">[Ejemplo de sesgo simple](/previous-versions/bb229482(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="395ab-132">[Simple Skew Example](/previous-versions/bb229482(v=vs.85))</span></span>
-   [<span data-ttu-id="395ab-133">Ejemplo de sesgo dinámico</span><span class="sxs-lookup"><span data-stu-id="395ab-133">Dynamic Skew Example</span></span>](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/skew/x_skew.md)

 

 