---
title: Atributo ConnectorType de VML
description: Atributo ConnectorType de VML
ms.assetid: acb9050d-c9e4-4d87-96c2-0bd2a1cf6e6b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0be0309e478970b93324b98a5efaaae54964435
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676389"
---
# <a name="vml-connectortype-attribute"></a><span data-ttu-id="7765e-103">Atributo ConnectorType de VML</span><span class="sxs-lookup"><span data-stu-id="7765e-103">VML ConnectorType Attribute</span></span>

<span data-ttu-id="7765e-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="7765e-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="7765e-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="7765e-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="7765e-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="7765e-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="7765e-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="7765e-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="7765e-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="7765e-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="7765e-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="7765e-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="7765e-110">Indica el tipo de conector que se usa para combinar formas.</span><span class="sxs-lookup"><span data-stu-id="7765e-110">Indicates the type of connector used for joining shapes.</span></span> <span data-ttu-id="7765e-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7765e-111">Read/write.</span></span> <span data-ttu-id="7765e-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="7765e-112">**String**.</span></span>

<span data-ttu-id="7765e-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="7765e-113">**Applies To**</span></span>

[<span data-ttu-id="7765e-114">Forma</span><span class="sxs-lookup"><span data-stu-id="7765e-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="7765e-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="7765e-115">**Tag Syntax**</span></span>

<span data-ttu-id="7765e-116"><v: *Element* o:ConnectorType = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="7765e-116"><v: *element* o:connectortype=" *expression* "></span></span>

<span data-ttu-id="7765e-117">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="7765e-117">**Remarks**</span></span>

<span data-ttu-id="7765e-118">Estos valores incluyen:</span><span class="sxs-lookup"><span data-stu-id="7765e-118">Values include:</span></span>



| <span data-ttu-id="7765e-119">Value</span><span class="sxs-lookup"><span data-stu-id="7765e-119">Value</span></span>    | <span data-ttu-id="7765e-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="7765e-120">Description</span></span>                    |
|----------|--------------------------------|
| <span data-ttu-id="7765e-121">ninguno</span><span class="sxs-lookup"><span data-stu-id="7765e-121">none</span></span>     | <span data-ttu-id="7765e-122">Ningún conector.</span><span class="sxs-lookup"><span data-stu-id="7765e-122">No connector.</span></span>                  |
| <span data-ttu-id="7765e-123">normales</span><span class="sxs-lookup"><span data-stu-id="7765e-123">straight</span></span> | <span data-ttu-id="7765e-124">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="7765e-124">Default.</span></span> <span data-ttu-id="7765e-125">Conector recto.</span><span class="sxs-lookup"><span data-stu-id="7765e-125">A straight connector.</span></span> |
| <span data-ttu-id="7765e-126">del codo</span><span class="sxs-lookup"><span data-stu-id="7765e-126">elbow</span></span>    | <span data-ttu-id="7765e-127">Conector en forma de codo.</span><span class="sxs-lookup"><span data-stu-id="7765e-127">An elbow-shaped connector.</span></span>     |
| <span data-ttu-id="7765e-128">curva</span><span class="sxs-lookup"><span data-stu-id="7765e-128">curved</span></span>   | <span data-ttu-id="7765e-129">Conector curvo.</span><span class="sxs-lookup"><span data-stu-id="7765e-129">A curved connector.</span></span>            |



 

<span data-ttu-id="7765e-130">Este atributo también puede ser utilizado por un motor de reglas de un editor gráfico.</span><span class="sxs-lookup"><span data-stu-id="7765e-130">This attribute may also be used by a rules engine of a graphical editor.</span></span>

<span data-ttu-id="7765e-131">*Microsoft Office atributo Extensions*</span><span class="sxs-lookup"><span data-stu-id="7765e-131">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="7765e-132">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="7765e-132">**Example**</span></span>

<span data-ttu-id="7765e-133">La forma usa una línea recta como conector.</span><span class="sxs-lookup"><span data-stu-id="7765e-133">The shape uses a straight line as a connector.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:connectortype="straight"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 