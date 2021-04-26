---
description: Especifica si las referencias de función de código auxiliar deben incluirse en las estructuras de operación en las definiciones de tipo de puerto para las operaciones un sentido y dos.
ms.assetid: 2547f71d-8a30-4df8-ba38-6707c415708e
title: elemento stubFunction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a77f37aed20dae4f04eea087e3d1eac2d23369af
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994152"
---
# <a name="stubfunction-element"></a><span data-ttu-id="8727e-103">elemento stubFunction</span><span class="sxs-lookup"><span data-stu-id="8727e-103">stubFunction element</span></span>

<span data-ttu-id="8727e-104">Especifica si las referencias de función de código auxiliar deben incluirse en las estructuras de operación en las definiciones de tipo de puerto para las operaciones un sentido y dos.</span><span class="sxs-lookup"><span data-stu-id="8727e-104">Specifies whether stub function references should be included in the operation structures in the port type definitions for one-way and two-way operations.</span></span>

## <a name="usage"></a><span data-ttu-id="8727e-105">Uso</span><span class="sxs-lookup"><span data-stu-id="8727e-105">Usage</span></span>

``` syntax
<stubFunction/>
```

## <a name="attributes"></a><span data-ttu-id="8727e-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="8727e-106">Attributes</span></span>

<span data-ttu-id="8727e-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="8727e-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="8727e-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8727e-108">Child elements</span></span>

<span data-ttu-id="8727e-109">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="8727e-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="8727e-110">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="8727e-110">Parent elements</span></span>



| <span data-ttu-id="8727e-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="8727e-111">Element</span></span>                                                       | <span data-ttu-id="8727e-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="8727e-112">Description</span></span>                                                  |
|---------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="8727e-113">**portTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="8727e-113">**portTypeDefinitions**</span></span>](porttypedefinitions.md)<br/> | <span data-ttu-id="8727e-114">Genera constantes de C para los tipos de puerto.</span><span class="sxs-lookup"><span data-stu-id="8727e-114">Generates C constants for port types.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="8727e-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8727e-115">Remarks</span></span>

<span data-ttu-id="8727e-116">Las referencias de función de código auxiliar se usan en escenarios de hospedaje para operaciones un solo sentido y dos.</span><span class="sxs-lookup"><span data-stu-id="8727e-116">Stub function references are used in hosting scenarios for one-way and two-way operations.</span></span>

<span data-ttu-id="8727e-117">Los valores válidos para este elemento son 1 (referencias de función TRUE/stub incluidas) y 0 (se incluyen referencias de función FALSE/no stub).</span><span class="sxs-lookup"><span data-stu-id="8727e-117">Valid values for this element are 1 (TRUE/stub function references included) and 0 (FALSE/no stub function references included).</span></span>

## <a name="element-information"></a><span data-ttu-id="8727e-118">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="8727e-118">Element information</span></span>



| <span data-ttu-id="8727e-119">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="8727e-119">Label</span></span> | <span data-ttu-id="8727e-120">Value</span><span class="sxs-lookup"><span data-stu-id="8727e-120">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="8727e-121">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8727e-121">Minimum supported system</span></span><br/> | <span data-ttu-id="8727e-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8727e-122">Windows Vista</span></span> |
| <span data-ttu-id="8727e-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8727e-123">Can be empty</span></span>                        | <span data-ttu-id="8727e-124">Sí</span><span class="sxs-lookup"><span data-stu-id="8727e-124">Yes</span></span>           |



 

 




