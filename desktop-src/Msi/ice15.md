---
description: ICE15 valida que el tipo de contenido y las referencias de extensión de MIME y las tablas de extensión sean recíprocos. La tabla MIME debe hacer referencia a un tipo de contenido a una extensión a la que la tabla de extensión hace referencia al mismo tipo de contenido.
ms.assetid: 8a38c8d2-324d-4de9-932b-d188ff5ccbaf
title: ICE15
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb39b3c617db41e9e58a226f1eeb92c3d733ebad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082929"
---
# <a name="ice15"></a><span data-ttu-id="a6e8a-104">ICE15</span><span class="sxs-lookup"><span data-stu-id="a6e8a-104">ICE15</span></span>

<span data-ttu-id="a6e8a-105">ICE15 valida que el tipo de contenido y las referencias de extensión de [MIME](mime-table.md) y las tablas de [extensión](extension-table.md) sean recíprocos.</span><span class="sxs-lookup"><span data-stu-id="a6e8a-105">ICE15 validates that content type and extension references in the [MIME](mime-table.md) and [Extension](extension-table.md) tables are reciprocal.</span></span> <span data-ttu-id="a6e8a-106">La tabla MIME debe hacer referencia a un tipo de contenido a una extensión a la que la tabla de extensión hace referencia al mismo tipo de contenido.</span><span class="sxs-lookup"><span data-stu-id="a6e8a-106">The MIME table must reference a content type to an extension that the Extension table references back to the same content type.</span></span>

<span data-ttu-id="a6e8a-107">Varias extensiones pueden hacer referencia al mismo tipo MIME, siempre que el tipo MIME haga referencia a una de las extensiones.</span><span class="sxs-lookup"><span data-stu-id="a6e8a-107">Multiple extensions can reference the same MIME type, as long as the MIME type references back to one of the extensions.</span></span> <span data-ttu-id="a6e8a-108">Varios tipos MIME pueden hacer referencia a la misma extensión, siempre y cuando la extensión haga referencia de nuevo a uno de los tipos MIME.</span><span class="sxs-lookup"><span data-stu-id="a6e8a-108">Multiple MIME types can reference the same extension, as long as the extension references back to one of the MIME types.</span></span>

<span data-ttu-id="a6e8a-109">Tenga en cuenta que cada vez que un MIME hace referencia a una extensión, esa extensión no puede tener la \_ columna MIME en la tabla de extensión establecida en NULL.</span><span class="sxs-lookup"><span data-stu-id="a6e8a-109">Note that whenever a MIME references an extension, that extension cannot have the MIME\_ column in the Extension table set to Null.</span></span>

## <a name="result"></a><span data-ttu-id="a6e8a-110">Resultado</span><span class="sxs-lookup"><span data-stu-id="a6e8a-110">Result</span></span>

<span data-ttu-id="a6e8a-111">ICE15 publica un error si el tipo de contenido y las referencias de extensión no son recíprocos.</span><span class="sxs-lookup"><span data-stu-id="a6e8a-111">ICE15 posts an error if the content type and extension references are not reciprocal.</span></span>

## <a name="example"></a><span data-ttu-id="a6e8a-112">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a6e8a-112">Example</span></span>

<span data-ttu-id="a6e8a-113">ICE15 envía dos mensajes de error para el ejemplo mostrado:</span><span class="sxs-lookup"><span data-stu-id="a6e8a-113">ICE15 posts two error messages for the example shown:</span></span>

-   <span data-ttu-id="a6e8a-114">El tipo de contenido test/solapas de la tabla MIME hace referencia a la extensión TST, pero la extensión TST en la tabla de la extensión hace referencia a las aletas/x-solapas.</span><span class="sxs-lookup"><span data-stu-id="a6e8a-114">The content type test/x-flaps in the MIME table references the extension tst, but the extension tst in the Extension table references flaps/x-flaps.</span></span> <span data-ttu-id="a6e8a-115">Esto no es recíproco.</span><span class="sxs-lookup"><span data-stu-id="a6e8a-115">This is not reciprocal.</span></span>
-   <span data-ttu-id="a6e8a-116">Las solapas de tipo de contenido/solapas hacen referencia a la extensión FLP, pero esa extensión tiene una entrada nula en la \_ columna MIME de la tabla de extensión.</span><span class="sxs-lookup"><span data-stu-id="a6e8a-116">The content type flaps/x-flaps references the extension flp, but that extension has a Null entry in the MIME\_ column of the Extension table.</span></span>

<span data-ttu-id="a6e8a-117">[Tabla MIME](mime-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="a6e8a-117">[MIME Table](mime-table.md) (partial)</span></span>



| <span data-ttu-id="a6e8a-118">ContentType</span><span class="sxs-lookup"><span data-stu-id="a6e8a-118">ContentType</span></span>   | <span data-ttu-id="a6e8a-119">Extensión\_</span><span class="sxs-lookup"><span data-stu-id="a6e8a-119">Extension\_</span></span> |
|---------------|-------------|
| <span data-ttu-id="a6e8a-120">prueba/x-prueba</span><span class="sxs-lookup"><span data-stu-id="a6e8a-120">test/x-test</span></span>   | <span data-ttu-id="a6e8a-121">TST</span><span class="sxs-lookup"><span data-stu-id="a6e8a-121">tst</span></span>         |
| <span data-ttu-id="a6e8a-122">solapas/solapas</span><span class="sxs-lookup"><span data-stu-id="a6e8a-122">flaps/x-flaps</span></span> | <span data-ttu-id="a6e8a-123">FLP</span><span class="sxs-lookup"><span data-stu-id="a6e8a-123">flp</span></span>         |



 

<span data-ttu-id="a6e8a-124">[Tabla de extensión](extension-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="a6e8a-124">[Extension Table](extension-table.md) (partial)</span></span>



| <span data-ttu-id="a6e8a-125">Extensión</span><span class="sxs-lookup"><span data-stu-id="a6e8a-125">Extension</span></span> | <span data-ttu-id="a6e8a-126">Mine\_</span><span class="sxs-lookup"><span data-stu-id="a6e8a-126">MIME\_</span></span>        |
|-----------|---------------|
| <span data-ttu-id="a6e8a-127">TST</span><span class="sxs-lookup"><span data-stu-id="a6e8a-127">tst</span></span>       | <span data-ttu-id="a6e8a-128">solapas/solapas</span><span class="sxs-lookup"><span data-stu-id="a6e8a-128">flaps/x-flaps</span></span> |
| <span data-ttu-id="a6e8a-129">FLP</span><span class="sxs-lookup"><span data-stu-id="a6e8a-129">flp</span></span>       | <span data-ttu-id="a6e8a-130">Null</span><span class="sxs-lookup"><span data-stu-id="a6e8a-130">Null</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="a6e8a-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a6e8a-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6e8a-132">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="a6e8a-132">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



