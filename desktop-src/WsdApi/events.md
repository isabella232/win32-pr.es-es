---
description: Especifica si los eventos relacionados se incluyen en las funciones generadas.
ms.assetid: 23ca463c-b305-496b-a1e3-58dbb793f17e
title: elemento Events
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2571cc8e9820ca38beb649b3c227fb1c01f61c50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276239"
---
# <a name="events-element"></a><span data-ttu-id="4366d-103">elemento Events</span><span class="sxs-lookup"><span data-stu-id="4366d-103">events element</span></span>

<span data-ttu-id="4366d-104">Especifica si los eventos relacionados se incluyen en las funciones generadas.</span><span class="sxs-lookup"><span data-stu-id="4366d-104">Specifies whether related events are included in the generated functions.</span></span>

## <a name="usage"></a><span data-ttu-id="4366d-105">Uso</span><span class="sxs-lookup"><span data-stu-id="4366d-105">Usage</span></span>

``` syntax
<events/>
```

## <a name="attributes"></a><span data-ttu-id="4366d-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="4366d-106">Attributes</span></span>

<span data-ttu-id="4366d-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="4366d-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="4366d-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4366d-108">Child elements</span></span>

<span data-ttu-id="4366d-109">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="4366d-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="4366d-110">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="4366d-110">Parent elements</span></span>



| <span data-ttu-id="4366d-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="4366d-111">Element</span></span>                                                                         | <span data-ttu-id="4366d-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="4366d-112">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4366d-113">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="4366d-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                 | <span data-ttu-id="4366d-114">Genera declaraciones de implementación para las funciones de proxy para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="4366d-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/> |
| [<span data-ttu-id="4366d-115">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="4366d-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>           | <span data-ttu-id="4366d-116">Genera declaraciones IDL para las funciones de proxy para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="4366d-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="4366d-117">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="4366d-117">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/> | <span data-ttu-id="4366d-118">Genera implementaciones para las funciones de proxy para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="4366d-118">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>             |
| [<span data-ttu-id="4366d-119">**stubDeclarations**</span><span class="sxs-lookup"><span data-stu-id="4366d-119">**stubDeclarations**</span></span>](stubdeclarations.md)<br/>                         | <span data-ttu-id="4366d-120">Genera declaraciones para las funciones de código auxiliar para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="4366d-120">Generates declarations for stub functions for port type operations.</span></span><br/> <br/>                 |
| [<span data-ttu-id="4366d-121">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="4366d-121">**stubDefinitions**</span></span>](stubdefinitions.md)<br/>                           | <span data-ttu-id="4366d-122">Genera implementaciones para las funciones de código auxiliar para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="4366d-122">Generates implementations for stub functions for port type operations.</span></span><br/> <br/>              |



## <a name="remarks"></a><span data-ttu-id="4366d-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4366d-123">Remarks</span></span>

<span data-ttu-id="4366d-124">Los valores posibles son 1 (eventos incluidos) y 0 (predeterminado, eventos excluidos).</span><span class="sxs-lookup"><span data-stu-id="4366d-124">Possible values are 1 (events included) and 0 (default, events excluded).</span></span>

## <a name="element-information"></a><span data-ttu-id="4366d-125">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="4366d-125">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="4366d-126">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4366d-126">Minimum supported system</span></span><br/> | <span data-ttu-id="4366d-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4366d-127">Windows Vista</span></span> |
| <span data-ttu-id="4366d-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4366d-128">Can be empty</span></span>                        | <span data-ttu-id="4366d-129">Sí</span><span class="sxs-lookup"><span data-stu-id="4366d-129">Yes</span></span>           |



 

 




