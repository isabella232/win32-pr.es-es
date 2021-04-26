---
description: Especifica si los eventos relacionados se incluyen en las funciones generadas.
ms.assetid: 23ca463c-b305-496b-a1e3-58dbb793f17e
title: elemento events
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6883f1bcca9b62c3d8b60ca86f47b0e688d513c2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995941"
---
# <a name="events-element"></a><span data-ttu-id="7e85c-103">elemento events</span><span class="sxs-lookup"><span data-stu-id="7e85c-103">events element</span></span>

<span data-ttu-id="7e85c-104">Especifica si los eventos relacionados se incluyen en las funciones generadas.</span><span class="sxs-lookup"><span data-stu-id="7e85c-104">Specifies whether related events are included in the generated functions.</span></span>

## <a name="usage"></a><span data-ttu-id="7e85c-105">Uso</span><span class="sxs-lookup"><span data-stu-id="7e85c-105">Usage</span></span>

``` syntax
<events/>
```

## <a name="attributes"></a><span data-ttu-id="7e85c-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="7e85c-106">Attributes</span></span>

<span data-ttu-id="7e85c-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="7e85c-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="7e85c-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7e85c-108">Child elements</span></span>

<span data-ttu-id="7e85c-109">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="7e85c-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="7e85c-110">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="7e85c-110">Parent elements</span></span>



| <span data-ttu-id="7e85c-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="7e85c-111">Element</span></span>                                                                         | <span data-ttu-id="7e85c-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e85c-112">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7e85c-113">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="7e85c-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                 | <span data-ttu-id="7e85c-114">Genera declaraciones de implementación para las funciones de proxy para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="7e85c-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/> |
| [<span data-ttu-id="7e85c-115">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="7e85c-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>           | <span data-ttu-id="7e85c-116">Genera declaraciones IDL para las funciones de proxy para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="7e85c-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="7e85c-117">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="7e85c-117">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/> | <span data-ttu-id="7e85c-118">Genera implementaciones para las funciones de proxy para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="7e85c-118">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>             |
| [<span data-ttu-id="7e85c-119">**stubDeclarations**</span><span class="sxs-lookup"><span data-stu-id="7e85c-119">**stubDeclarations**</span></span>](stubdeclarations.md)<br/>                         | <span data-ttu-id="7e85c-120">Genera declaraciones para las funciones de código auxiliar para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="7e85c-120">Generates declarations for stub functions for port type operations.</span></span><br/> <br/>                 |
| [<span data-ttu-id="7e85c-121">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="7e85c-121">**stubDefinitions**</span></span>](stubdefinitions.md)<br/>                           | <span data-ttu-id="7e85c-122">Genera implementaciones para las funciones de código auxiliar para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="7e85c-122">Generates implementations for stub functions for port type operations.</span></span><br/> <br/>              |



## <a name="remarks"></a><span data-ttu-id="7e85c-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7e85c-123">Remarks</span></span>

<span data-ttu-id="7e85c-124">Los valores posibles son 1 (eventos incluidos) y 0 (valor predeterminado, eventos excluidos).</span><span class="sxs-lookup"><span data-stu-id="7e85c-124">Possible values are 1 (events included) and 0 (default, events excluded).</span></span>

## <a name="element-information"></a><span data-ttu-id="7e85c-125">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="7e85c-125">Element information</span></span>



| <span data-ttu-id="7e85c-126">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="7e85c-126">Label</span></span> | <span data-ttu-id="7e85c-127">Value</span><span class="sxs-lookup"><span data-stu-id="7e85c-127">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="7e85c-128">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e85c-128">Minimum supported system</span></span><br/> | <span data-ttu-id="7e85c-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7e85c-129">Windows Vista</span></span> |
| <span data-ttu-id="7e85c-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7e85c-130">Can be empty</span></span>                        | <span data-ttu-id="7e85c-131">Sí</span><span class="sxs-lookup"><span data-stu-id="7e85c-131">Yes</span></span>           |



 

 




