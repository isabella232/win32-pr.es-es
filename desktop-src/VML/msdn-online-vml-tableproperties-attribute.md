---
title: Atributo TableProperties de VML
description: Atributo TableProperties de VML
ms.assetid: 10355742-13b9-4c08-bff7-f7f7501762e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f0f010f673b2663764814150f7a38fc06f23e11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695610"
---
# <a name="vml-tableproperties-attribute"></a><span data-ttu-id="9e47f-103">Atributo TableProperties de VML</span><span class="sxs-lookup"><span data-stu-id="9e47f-103">VML TableProperties Attribute</span></span>

<span data-ttu-id="9e47f-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="9e47f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="9e47f-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="9e47f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="9e47f-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="9e47f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="9e47f-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="9e47f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="9e47f-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="9e47f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="9e47f-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="9e47f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="9e47f-110">Determina las propiedades de la tabla.</span><span class="sxs-lookup"><span data-stu-id="9e47f-110">Determines table properties.</span></span> <span data-ttu-id="9e47f-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="9e47f-111">Read/write.</span></span> <span data-ttu-id="9e47f-112">**Entero**.</span><span class="sxs-lookup"><span data-stu-id="9e47f-112">**Integer**.</span></span>

<span data-ttu-id="9e47f-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="9e47f-113">**Applies To**</span></span>

[<span data-ttu-id="9e47f-114">Forma</span><span class="sxs-lookup"><span data-stu-id="9e47f-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="9e47f-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="9e47f-115">**Tag Syntax**</span></span>

<span data-ttu-id="9e47f-116"><v: *Element* o:TableProperties = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="9e47f-116"><v: *element* o:tableproperties=" *expression* "></span></span>

<span data-ttu-id="9e47f-117">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="9e47f-117">**Remarks**</span></span>

<span data-ttu-id="9e47f-118">Usado por Microsoft PowerPoint para tablas nativas.</span><span class="sxs-lookup"><span data-stu-id="9e47f-118">Used by Microsoft PowerPoint for native tables.</span></span> <span data-ttu-id="9e47f-119">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="9e47f-119">Default value is 0.</span></span> <span data-ttu-id="9e47f-120">Solo se utilizan los tres primeros bits de este entero.</span><span class="sxs-lookup"><span data-stu-id="9e47f-120">Only the first three bits of this integer are used.</span></span>

<span data-ttu-id="9e47f-121">Aunque el valor se almacena en una forma, el atributo solo es útil cuando la tabla está formada por formas agrupadas. Se pueden combinar bits.</span><span class="sxs-lookup"><span data-stu-id="9e47f-121">Even though the value is stored in a shape, the attribute is only useful when the table is made up of shapes that are grouped.Bits may be combined.</span></span>

<span data-ttu-id="9e47f-122">Se incluyen los siguientes valores de bit.</span><span class="sxs-lookup"><span data-stu-id="9e47f-122">The following bit values are included.</span></span>



| <span data-ttu-id="9e47f-123">bit</span><span class="sxs-lookup"><span data-stu-id="9e47f-123">Bit</span></span> | <span data-ttu-id="9e47f-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="9e47f-124">Description</span></span>                              |
|-----|------------------------------------------|
| <span data-ttu-id="9e47f-125">1</span><span class="sxs-lookup"><span data-stu-id="9e47f-125">1</span></span>   | <span data-ttu-id="9e47f-126">Se establece si el grupo de formas es una tabla.</span><span class="sxs-lookup"><span data-stu-id="9e47f-126">Set if the group of shapes is a table.</span></span>   |
| <span data-ttu-id="9e47f-127">2</span><span class="sxs-lookup"><span data-stu-id="9e47f-127">2</span></span>   | <span data-ttu-id="9e47f-128">Se establece si la forma es un marcador de posición.</span><span class="sxs-lookup"><span data-stu-id="9e47f-128">Set if the shape is a placeholder.</span></span>       |
| <span data-ttu-id="9e47f-129">3</span><span class="sxs-lookup"><span data-stu-id="9e47f-129">3</span></span>   | <span data-ttu-id="9e47f-130">Se establece si el texto de la tabla es bidireccional.</span><span class="sxs-lookup"><span data-stu-id="9e47f-130">Set if the table text is bi-directional.</span></span> |



 

<span data-ttu-id="9e47f-131">*Microsoft Office atributo Extensions*</span><span class="sxs-lookup"><span data-stu-id="9e47f-131">*Microsoft Office Extensions Attribute*</span></span>

 

 