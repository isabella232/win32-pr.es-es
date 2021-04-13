---
description: Especifica si las referencias de funciones de código auxiliar deben incluirse en las estructuras de operación en las definiciones de tipo de puerto para las operaciones unidireccionales y bidireccionales.
ms.assetid: 2547f71d-8a30-4df8-ba38-6707c415708e
title: elemento stubFunction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7282e7280c8d701710094b70b84a65756f7230ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278409"
---
# <a name="stubfunction-element"></a><span data-ttu-id="fb364-103">elemento stubFunction</span><span class="sxs-lookup"><span data-stu-id="fb364-103">stubFunction element</span></span>

<span data-ttu-id="fb364-104">Especifica si las referencias de funciones de código auxiliar deben incluirse en las estructuras de operación en las definiciones de tipo de puerto para las operaciones unidireccionales y bidireccionales.</span><span class="sxs-lookup"><span data-stu-id="fb364-104">Specifies whether stub function references should be included in the operation structures in the port type definitions for one-way and two-way operations.</span></span>

## <a name="usage"></a><span data-ttu-id="fb364-105">Uso</span><span class="sxs-lookup"><span data-stu-id="fb364-105">Usage</span></span>

``` syntax
<stubFunction/>
```

## <a name="attributes"></a><span data-ttu-id="fb364-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="fb364-106">Attributes</span></span>

<span data-ttu-id="fb364-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="fb364-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="fb364-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fb364-108">Child elements</span></span>

<span data-ttu-id="fb364-109">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="fb364-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="fb364-110">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="fb364-110">Parent elements</span></span>



| <span data-ttu-id="fb364-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="fb364-111">Element</span></span>                                                       | <span data-ttu-id="fb364-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb364-112">Description</span></span>                                                  |
|---------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="fb364-113">**portTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="fb364-113">**portTypeDefinitions**</span></span>](porttypedefinitions.md)<br/> | <span data-ttu-id="fb364-114">Genera constantes de C para los tipos de puerto.</span><span class="sxs-lookup"><span data-stu-id="fb364-114">Generates C constants for port types.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="fb364-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fb364-115">Remarks</span></span>

<span data-ttu-id="fb364-116">Las referencias de funciones de código auxiliar se usan en escenarios de hospedaje para las operaciones unidireccionales y bidireccionales.</span><span class="sxs-lookup"><span data-stu-id="fb364-116">Stub function references are used in hosting scenarios for one-way and two-way operations.</span></span>

<span data-ttu-id="fb364-117">Los valores válidos para este elemento son 1 (se incluyen las referencias de funciones TRUE/stub) y 0 (FALSE/no se incluyen las referencias de funciones de código auxiliar).</span><span class="sxs-lookup"><span data-stu-id="fb364-117">Valid values for this element are 1 (TRUE/stub function references included) and 0 (FALSE/no stub function references included).</span></span>

## <a name="element-information"></a><span data-ttu-id="fb364-118">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="fb364-118">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="fb364-119">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb364-119">Minimum supported system</span></span><br/> | <span data-ttu-id="fb364-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fb364-120">Windows Vista</span></span> |
| <span data-ttu-id="fb364-121">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="fb364-121">Can be empty</span></span>                        | <span data-ttu-id="fb364-122">Sí</span><span class="sxs-lookup"><span data-stu-id="fb364-122">Yes</span></span>           |



 

 




