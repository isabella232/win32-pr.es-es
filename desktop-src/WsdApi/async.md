---
description: Especifica si las operaciones asincrónicas se incluyen en las funciones de proxy generadas.
ms.assetid: 7b57d5c6-589b-4e03-bfcf-1faa671ebd77
title: Async (elemento)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea04eaa66fbdadfc784650c1a451cebf171f6372
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083249"
---
# <a name="async-element"></a><span data-ttu-id="b33d7-103">Async (elemento)</span><span class="sxs-lookup"><span data-stu-id="b33d7-103">async element</span></span>

<span data-ttu-id="b33d7-104">Especifica si las operaciones asincrónicas se incluyen en las funciones de proxy generadas.</span><span class="sxs-lookup"><span data-stu-id="b33d7-104">Specifies whether asynchronous operations are included in the generated proxy functions.</span></span>

## <a name="usage"></a><span data-ttu-id="b33d7-105">Uso</span><span class="sxs-lookup"><span data-stu-id="b33d7-105">Usage</span></span>

``` syntax
<async/>
```

## <a name="attributes"></a><span data-ttu-id="b33d7-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="b33d7-106">Attributes</span></span>

<span data-ttu-id="b33d7-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="b33d7-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="b33d7-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b33d7-108">Child elements</span></span>

<span data-ttu-id="b33d7-109">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="b33d7-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="b33d7-110">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="b33d7-110">Parent elements</span></span>



| <span data-ttu-id="b33d7-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="b33d7-111">Element</span></span>                                                                         | <span data-ttu-id="b33d7-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="b33d7-112">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b33d7-113">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="b33d7-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                 | <span data-ttu-id="b33d7-114">Genera declaraciones de implementación para las funciones de proxy para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="b33d7-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/> |
| [<span data-ttu-id="b33d7-115">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="b33d7-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>           | <span data-ttu-id="b33d7-116">Genera declaraciones IDL para las funciones de proxy para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="b33d7-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="b33d7-117">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="b33d7-117">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/> | <span data-ttu-id="b33d7-118">Genera implementaciones para las funciones de proxy para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="b33d7-118">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>             |



## <a name="remarks"></a><span data-ttu-id="b33d7-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b33d7-119">Remarks</span></span>

<span data-ttu-id="b33d7-120">Los valores posibles son 1 (operaciones asincrónicas incluidas) y 0 (valor predeterminado, se excluyen las operaciones asincrónicas).</span><span class="sxs-lookup"><span data-stu-id="b33d7-120">Possible values are 1 (asynchronous operations included) and 0 (default, asynchronous operations excluded).</span></span>

<span data-ttu-id="b33d7-121">Un proxy puede tener tanto versiones asincrónicas como sincrónicas de las mismas operaciones.</span><span class="sxs-lookup"><span data-stu-id="b33d7-121">A proxy can have both asynchronous and synchronous versions of the same operations.</span></span>

## <a name="element-information"></a><span data-ttu-id="b33d7-122">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="b33d7-122">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="b33d7-123">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b33d7-123">Minimum supported system</span></span><br/> | <span data-ttu-id="b33d7-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b33d7-124">Windows Vista</span></span> |
| <span data-ttu-id="b33d7-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b33d7-125">Can be empty</span></span>                        | <span data-ttu-id="b33d7-126">Sí</span><span class="sxs-lookup"><span data-stu-id="b33d7-126">Yes</span></span>           |



 

 




