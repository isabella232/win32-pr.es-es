---
title: Atributo de método VML
description: Atributo de método VML
ms.assetid: 42ab9d78-f004-4571-a566-03edd8341d19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2f7440e1e793e7ad34860524f63a3bfc38456f1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695698"
---
# <a name="vml-method-attribute"></a><span data-ttu-id="12aca-103">Atributo de método VML</span><span class="sxs-lookup"><span data-stu-id="12aca-103">VML Method Attribute</span></span>

<span data-ttu-id="12aca-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="12aca-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="12aca-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="12aca-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="12aca-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="12aca-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="12aca-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="12aca-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="12aca-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="12aca-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="12aca-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="12aca-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="12aca-110">Define el método utilizado para generar un relleno de degradado.</span><span class="sxs-lookup"><span data-stu-id="12aca-110">Defines the method used to generate a gradient fill.</span></span> <span data-ttu-id="12aca-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="12aca-111">Read/write.</span></span> <span data-ttu-id="12aca-112">**VgSigmaType**.</span><span class="sxs-lookup"><span data-stu-id="12aca-112">**VgSigmaType**.</span></span>

<span data-ttu-id="12aca-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="12aca-113">**Applies To**</span></span>

[<span data-ttu-id="12aca-114">Fill</span><span class="sxs-lookup"><span data-stu-id="12aca-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="12aca-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="12aca-115">**Tag Syntax**</span></span>

<span data-ttu-id="12aca-116"><v: *Element* Method = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="12aca-116"><v: *element* method=" *expression* "></span></span>

<span data-ttu-id="12aca-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="12aca-117">**Script Syntax**</span></span>

<span data-ttu-id="12aca-118">*Element* . Method = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="12aca-118">*element* .method="*expression*"</span></span>

<span data-ttu-id="12aca-119">*expresión* = de *Element*. Method</span><span class="sxs-lookup"><span data-stu-id="12aca-119">*expression*=*element*.method</span></span>

<span data-ttu-id="12aca-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="12aca-120">**Remarks**</span></span>

<span data-ttu-id="12aca-121">Estos valores incluyen:</span><span class="sxs-lookup"><span data-stu-id="12aca-121">Values include:</span></span>



| <span data-ttu-id="12aca-122">Value</span><span class="sxs-lookup"><span data-stu-id="12aca-122">Value</span></span>  | <span data-ttu-id="12aca-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="12aca-123">Description</span></span>          |
|--------|----------------------|
| <span data-ttu-id="12aca-124">None</span><span class="sxs-lookup"><span data-stu-id="12aca-124">None</span></span>   | <span data-ttu-id="12aca-125">Sin relleno de Sigma.</span><span class="sxs-lookup"><span data-stu-id="12aca-125">No sigma fill.</span></span>       |
| <span data-ttu-id="12aca-126">Lineal</span><span class="sxs-lookup"><span data-stu-id="12aca-126">Linear</span></span> | <span data-ttu-id="12aca-127">Relleno de Sigma lineal.</span><span class="sxs-lookup"><span data-stu-id="12aca-127">Linear sigma fill.</span></span>   |
| <span data-ttu-id="12aca-128">Sigma</span><span class="sxs-lookup"><span data-stu-id="12aca-128">Sigma</span></span>  | <span data-ttu-id="12aca-129">Relleno de Sigma.</span><span class="sxs-lookup"><span data-stu-id="12aca-129">Sigma fill.</span></span> <span data-ttu-id="12aca-130">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="12aca-130">Default.</span></span> |
| <span data-ttu-id="12aca-131">Any</span><span class="sxs-lookup"><span data-stu-id="12aca-131">Any</span></span>    | <span data-ttu-id="12aca-132">Cualquier relleno de Sigma.</span><span class="sxs-lookup"><span data-stu-id="12aca-132">Any sigma fill.</span></span>      |



 

<span data-ttu-id="12aca-133">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="12aca-133">*VML Standard Attribute*</span></span>

<span data-ttu-id="12aca-134">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="12aca-134">**Example**</span></span>

<span data-ttu-id="12aca-135">La forma tendrá un relleno de degradado lineal rojo.</span><span class="sxs-lookup"><span data-stu-id="12aca-135">The shape will have a red linear gradient fill.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="red" type="gradient" method="linear"/>
   </v:shape>
```



 

 