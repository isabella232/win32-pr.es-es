---
description: Especifica si las referencias de funciones de código auxiliar deben incluirse en las estructuras de operación en las definiciones de tipo de puerto para las operaciones de notificación.
ms.assetid: 8a2fd7b2-e37b-465a-ba83-a68877a2e0c3
title: elemento eventStubFunction
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fe353f43d02eec68f29f3075cc445c1314c9762
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697305"
---
# <a name="eventstubfunction-element"></a><span data-ttu-id="a0a86-103">elemento eventStubFunction</span><span class="sxs-lookup"><span data-stu-id="a0a86-103">eventStubFunction element</span></span>

<span data-ttu-id="a0a86-104">Especifica si las referencias de funciones de código auxiliar deben incluirse en las estructuras de operación en las definiciones de tipo de puerto para las operaciones de notificación.</span><span class="sxs-lookup"><span data-stu-id="a0a86-104">Specifies whether stub function references should be included in the operation structures in the port type definitions for notification operations.</span></span>

## <a name="usage"></a><span data-ttu-id="a0a86-105">Uso</span><span class="sxs-lookup"><span data-stu-id="a0a86-105">Usage</span></span>

``` syntax
<eventStubFunction/>
```

## <a name="attributes"></a><span data-ttu-id="a0a86-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="a0a86-106">Attributes</span></span>

<span data-ttu-id="a0a86-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="a0a86-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="a0a86-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a0a86-108">Child elements</span></span>

<span data-ttu-id="a0a86-109">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="a0a86-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="a0a86-110">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="a0a86-110">Parent elements</span></span>



| <span data-ttu-id="a0a86-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="a0a86-111">Element</span></span>                                                       | <span data-ttu-id="a0a86-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0a86-112">Description</span></span>                                                  |
|---------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="a0a86-113">**portTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="a0a86-113">**portTypeDefinitions**</span></span>](porttypedefinitions.md)<br/> | <span data-ttu-id="a0a86-114">Genera constantes de C para los tipos de puerto.</span><span class="sxs-lookup"><span data-stu-id="a0a86-114">Generates C constants for port types.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="a0a86-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a0a86-115">Remarks</span></span>

<span data-ttu-id="a0a86-116">Las referencias de funciones de código auxiliar se encuentran en escenarios de cliente para las operaciones de notificación (eventos).</span><span class="sxs-lookup"><span data-stu-id="a0a86-116">Stub function references are in client scenarios for notification operations (events).</span></span>

<span data-ttu-id="a0a86-117">Los valores válidos para este elemento son 1 (se incluyen las referencias de funciones TRUE/stub) y 0 (FALSE/no se incluyen las referencias de funciones de código auxiliar).</span><span class="sxs-lookup"><span data-stu-id="a0a86-117">Valid values for this element are 1 (TRUE/stub function references included) and 0 (FALSE/no stub function references included).</span></span>

## <a name="element-information"></a><span data-ttu-id="a0a86-118">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="a0a86-118">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="a0a86-119">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a0a86-119">Minimum supported system</span></span><br/> | <span data-ttu-id="a0a86-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a0a86-120">Windows Vista</span></span> |
| <span data-ttu-id="a0a86-121">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a0a86-121">Can be empty</span></span>                        | <span data-ttu-id="a0a86-122">Sí</span><span class="sxs-lookup"><span data-stu-id="a0a86-122">Yes</span></span>           |



 

 




