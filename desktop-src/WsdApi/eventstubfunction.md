---
description: Especifica si las referencias de función de código auxiliar deben incluirse en las estructuras de operación en las definiciones de tipo de puerto para las operaciones de notificación.
ms.assetid: 8a2fd7b2-e37b-465a-ba83-a68877a2e0c3
title: Elemento eventStubFunction
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80777a53d37e7651559a09b8e8445d4314aaca63
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995892"
---
# <a name="eventstubfunction-element"></a><span data-ttu-id="d457a-103">Elemento eventStubFunction</span><span class="sxs-lookup"><span data-stu-id="d457a-103">eventStubFunction element</span></span>

<span data-ttu-id="d457a-104">Especifica si las referencias de función de código auxiliar deben incluirse en las estructuras de operación en las definiciones de tipo de puerto para las operaciones de notificación.</span><span class="sxs-lookup"><span data-stu-id="d457a-104">Specifies whether stub function references should be included in the operation structures in the port type definitions for notification operations.</span></span>

## <a name="usage"></a><span data-ttu-id="d457a-105">Uso</span><span class="sxs-lookup"><span data-stu-id="d457a-105">Usage</span></span>

``` syntax
<eventStubFunction/>
```

## <a name="attributes"></a><span data-ttu-id="d457a-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="d457a-106">Attributes</span></span>

<span data-ttu-id="d457a-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="d457a-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="d457a-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d457a-108">Child elements</span></span>

<span data-ttu-id="d457a-109">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="d457a-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="d457a-110">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="d457a-110">Parent elements</span></span>



| <span data-ttu-id="d457a-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="d457a-111">Element</span></span>                                                       | <span data-ttu-id="d457a-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="d457a-112">Description</span></span>                                                  |
|---------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="d457a-113">**portTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="d457a-113">**portTypeDefinitions**</span></span>](porttypedefinitions.md)<br/> | <span data-ttu-id="d457a-114">Genera constantes de C para los tipos de puerto.</span><span class="sxs-lookup"><span data-stu-id="d457a-114">Generates C constants for port types.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="d457a-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d457a-115">Remarks</span></span>

<span data-ttu-id="d457a-116">Las referencias de función de código auxiliar se encuentran en escenarios de cliente para operaciones de notificación (eventos).</span><span class="sxs-lookup"><span data-stu-id="d457a-116">Stub function references are in client scenarios for notification operations (events).</span></span>

<span data-ttu-id="d457a-117">Los valores válidos para este elemento son 1 (referencias de función TRUE/stub incluidas) y 0 (se incluyen referencias de función FALSE/no stub).</span><span class="sxs-lookup"><span data-stu-id="d457a-117">Valid values for this element are 1 (TRUE/stub function references included) and 0 (FALSE/no stub function references included).</span></span>

## <a name="element-information"></a><span data-ttu-id="d457a-118">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="d457a-118">Element information</span></span>



| <span data-ttu-id="d457a-119">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="d457a-119">Label</span></span> | <span data-ttu-id="d457a-120">Value</span><span class="sxs-lookup"><span data-stu-id="d457a-120">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="d457a-121">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d457a-121">Minimum supported system</span></span><br/> | <span data-ttu-id="d457a-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d457a-122">Windows Vista</span></span> |
| <span data-ttu-id="d457a-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d457a-123">Can be empty</span></span>                        | <span data-ttu-id="d457a-124">Sí</span><span class="sxs-lookup"><span data-stu-id="d457a-124">Yes</span></span>           |



 

 




