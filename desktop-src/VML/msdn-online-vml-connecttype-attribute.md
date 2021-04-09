---
title: Atributo ConnectType de VML
description: Atributo ConnectType de VML
ms.assetid: 907803c8-687b-4823-8252-b59acbbd9aa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a54135dcb4ffe0a86f781d68b8babe1259029be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149285"
---
# <a name="vml-connecttype-attribute"></a><span data-ttu-id="bf289-103">Atributo ConnectType de VML</span><span class="sxs-lookup"><span data-stu-id="bf289-103">VML ConnectType Attribute</span></span>

<span data-ttu-id="bf289-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="bf289-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="bf289-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="bf289-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="bf289-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="bf289-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="bf289-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="bf289-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="bf289-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="bf289-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="bf289-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="bf289-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="bf289-110">Define el tipo de puntos de conexión que se utiliza para adjuntar formas a otras formas.</span><span class="sxs-lookup"><span data-stu-id="bf289-110">Defines the type of connection points used for attaching shapes to other shapes.</span></span> <span data-ttu-id="bf289-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bf289-111">Read/write.</span></span> <span data-ttu-id="bf289-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="bf289-112">**String**.</span></span>

<span data-ttu-id="bf289-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="bf289-113">**Applies To**</span></span>

[<span data-ttu-id="bf289-114">Ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="bf289-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="bf289-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="bf289-115">**Tag Syntax**</span></span>

<span data-ttu-id="bf289-116"><v: *Element* o:connecttype = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="bf289-116"><v: *element* o:connecttype=" *expression* "></span></span>

<span data-ttu-id="bf289-117">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="bf289-117">**Remarks**</span></span>

<span data-ttu-id="bf289-118">Estos valores incluyen:</span><span class="sxs-lookup"><span data-stu-id="bf289-118">Values include:</span></span>



| <span data-ttu-id="bf289-119">Value</span><span class="sxs-lookup"><span data-stu-id="bf289-119">Value</span></span>    | <span data-ttu-id="bf289-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="bf289-120">Description</span></span>                                                                                                                           |
|----------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf289-121">ninguno</span><span class="sxs-lookup"><span data-stu-id="bf289-121">none</span></span>     | <span data-ttu-id="bf289-122">No hay sitios de conexión.</span><span class="sxs-lookup"><span data-stu-id="bf289-122">No connection sites.</span></span> <span data-ttu-id="bf289-123">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="bf289-123">Default.</span></span>                                                                                                         |
| <span data-ttu-id="bf289-124">rect</span><span class="sxs-lookup"><span data-stu-id="bf289-124">rect</span></span>     | <span data-ttu-id="bf289-125">Cuatro puntos de conexión estándar en los puntos medio de los lados superior, inferior, izquierdo y derecho.</span><span class="sxs-lookup"><span data-stu-id="bf289-125">Standard four connection points at midpoints of top, bottom, left, and right sides.</span></span>                                                   |
| <span data-ttu-id="bf289-126">segmentos</span><span class="sxs-lookup"><span data-stu-id="bf289-126">segments</span></span> | <span data-ttu-id="bf289-127">Se usan los puntos de edición de la forma.</span><span class="sxs-lookup"><span data-stu-id="bf289-127">The edit points of the shape are used.</span></span> <span data-ttu-id="bf289-128">Los puntos de edición son los puntos negros de un editor gráfico que se usan para seleccionar partes de una forma.</span><span class="sxs-lookup"><span data-stu-id="bf289-128">Edit points are the black dots in a graphical editor that are used to select parts of a shape.</span></span> |
| <span data-ttu-id="bf289-129">custom</span><span class="sxs-lookup"><span data-stu-id="bf289-129">custom</span></span>   | <span data-ttu-id="bf289-130">Una matriz de ubicaciones de conexión personalizadas.</span><span class="sxs-lookup"><span data-stu-id="bf289-130">A custom array of connection locations.</span></span>                                                                                               |



 

<span data-ttu-id="bf289-131">*Microsoft Office atributo Extensions*</span><span class="sxs-lookup"><span data-stu-id="bf289-131">*Microsoft Office Extensions Attribute*</span></span>

 

 