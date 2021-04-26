---
description: Especifica si las operaciones asincrónicas se incluyen en las funciones de proxy generadas.
ms.assetid: 7b57d5c6-589b-4e03-bfcf-1faa671ebd77
title: async, elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6cbc68d0a5dea30f4b4d179a54539ac3f9516a4
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994962"
---
# <a name="async-element"></a><span data-ttu-id="91930-103">async, elemento</span><span class="sxs-lookup"><span data-stu-id="91930-103">async element</span></span>

<span data-ttu-id="91930-104">Especifica si las operaciones asincrónicas se incluyen en las funciones de proxy generadas.</span><span class="sxs-lookup"><span data-stu-id="91930-104">Specifies whether asynchronous operations are included in the generated proxy functions.</span></span>

## <a name="usage"></a><span data-ttu-id="91930-105">Uso</span><span class="sxs-lookup"><span data-stu-id="91930-105">Usage</span></span>

``` syntax
<async/>
```

## <a name="attributes"></a><span data-ttu-id="91930-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="91930-106">Attributes</span></span>

<span data-ttu-id="91930-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="91930-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="91930-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="91930-108">Child elements</span></span>

<span data-ttu-id="91930-109">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="91930-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="91930-110">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="91930-110">Parent elements</span></span>



| <span data-ttu-id="91930-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="91930-111">Element</span></span>                                                                         | <span data-ttu-id="91930-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="91930-112">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="91930-113">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="91930-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                 | <span data-ttu-id="91930-114">Genera declaraciones de implementación para las funciones de proxy para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="91930-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/> |
| [<span data-ttu-id="91930-115">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="91930-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>           | <span data-ttu-id="91930-116">Genera declaraciones IDL para las funciones de proxy para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="91930-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="91930-117">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="91930-117">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/> | <span data-ttu-id="91930-118">Genera implementaciones para las funciones de proxy para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="91930-118">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>             |



## <a name="remarks"></a><span data-ttu-id="91930-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="91930-119">Remarks</span></span>

<span data-ttu-id="91930-120">Los valores posibles son 1 (operaciones asincrónicas incluidas) y 0 (valor predeterminado, operaciones asincrónicas excluidas).</span><span class="sxs-lookup"><span data-stu-id="91930-120">Possible values are 1 (asynchronous operations included) and 0 (default, asynchronous operations excluded).</span></span>

<span data-ttu-id="91930-121">Un proxy puede tener versiones asincrónicas y sincrónicas de las mismas operaciones.</span><span class="sxs-lookup"><span data-stu-id="91930-121">A proxy can have both asynchronous and synchronous versions of the same operations.</span></span>

## <a name="element-information"></a><span data-ttu-id="91930-122">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="91930-122">Element information</span></span>



| <span data-ttu-id="91930-123">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="91930-123">Label</span></span> | <span data-ttu-id="91930-124">Value</span><span class="sxs-lookup"><span data-stu-id="91930-124">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="91930-125">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91930-125">Minimum supported system</span></span><br/> | <span data-ttu-id="91930-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="91930-126">Windows Vista</span></span> |
| <span data-ttu-id="91930-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="91930-127">Can be empty</span></span>                        | <span data-ttu-id="91930-128">Sí</span><span class="sxs-lookup"><span data-stu-id="91930-128">Yes</span></span>           |



 

 




