---
description: Especifica el tipo de desasignador que va a usar una función de código auxiliar.
ms.assetid: 58228dfd-1d4b-41e5-b423-a54525021c22
title: elemento desasignador
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3604f0efb366c3f88e2e0828c02344ee75606079
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276240"
---
# <a name="deallocator-element"></a><span data-ttu-id="0f3b8-103">elemento desasignador</span><span class="sxs-lookup"><span data-stu-id="0f3b8-103">deallocator element</span></span>

<span data-ttu-id="0f3b8-104">Especifica el tipo de desasignador que va a usar una función de código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="0f3b8-104">Specifies the type of deallocator to be used by a stub function.</span></span>

## <a name="usage"></a><span data-ttu-id="0f3b8-105">Uso</span><span class="sxs-lookup"><span data-stu-id="0f3b8-105">Usage</span></span>

``` syntax
<deallocator/>
```

## <a name="attributes"></a><span data-ttu-id="0f3b8-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="0f3b8-106">Attributes</span></span>

<span data-ttu-id="0f3b8-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="0f3b8-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="0f3b8-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0f3b8-108">Child elements</span></span>

<span data-ttu-id="0f3b8-109">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="0f3b8-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="0f3b8-110">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="0f3b8-110">Parent elements</span></span>



| <span data-ttu-id="0f3b8-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="0f3b8-111">Element</span></span>                                               | <span data-ttu-id="0f3b8-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="0f3b8-112">Description</span></span>                                                                                   |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0f3b8-113">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="0f3b8-113">**stubDefinitions**</span></span>](stubdefinitions.md)<br/> | <span data-ttu-id="0f3b8-114">Genera implementaciones para las funciones de código auxiliar para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="0f3b8-114">Generates implementations for stub functions for port-type operations.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="0f3b8-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0f3b8-115">Remarks</span></span>

<span data-ttu-id="0f3b8-116">El tipo desasignador debe estar incluido en un par de <deallocator></deallocator> etiquetas.</span><span class="sxs-lookup"><span data-stu-id="0f3b8-116">The deallocator type should be enclosed in a pair of <deallocator></deallocator> tags.</span></span> <span data-ttu-id="0f3b8-117">Las siguientes cadenas son valores de desasignador válidos:</span><span class="sxs-lookup"><span data-stu-id="0f3b8-117">The following strings are valid deallocator values:</span></span>

-   <span data-ttu-id="0f3b8-118">ninguno</span><span class="sxs-lookup"><span data-stu-id="0f3b8-118">none</span></span>
-   <span data-ttu-id="0f3b8-119">WSDFreeLinkedMemory</span><span class="sxs-lookup"><span data-stu-id="0f3b8-119">WSDFreeLinkedMemory</span></span>
-   <span data-ttu-id="0f3b8-120">CoTaskMemFree</span><span class="sxs-lookup"><span data-stu-id="0f3b8-120">CoTaskMemFree</span></span>
-   <span data-ttu-id="0f3b8-121">free</span><span class="sxs-lookup"><span data-stu-id="0f3b8-121">free</span></span>
-   <span data-ttu-id="0f3b8-122">delete</span><span class="sxs-lookup"><span data-stu-id="0f3b8-122">delete</span></span>
-   <span data-ttu-id="0f3b8-123">deleteArray</span><span class="sxs-lookup"><span data-stu-id="0f3b8-123">deleteArray</span></span>
-   <span data-ttu-id="0f3b8-124">Release</span><span class="sxs-lookup"><span data-stu-id="0f3b8-124">Release</span></span>

## <a name="element-information"></a><span data-ttu-id="0f3b8-125">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="0f3b8-125">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="0f3b8-126">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f3b8-126">Minimum supported system</span></span><br/> | <span data-ttu-id="0f3b8-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0f3b8-127">Windows Vista</span></span> |
| <span data-ttu-id="0f3b8-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0f3b8-128">Can be empty</span></span>                        | <span data-ttu-id="0f3b8-129">Sí</span><span class="sxs-lookup"><span data-stu-id="0f3b8-129">Yes</span></span>           |



 

 




