---
description: Genera implementaciones para las funciones de código auxiliar para las operaciones de tipo de puerto.
ms.assetid: 69899302-db54-493b-90de-596750be566f
title: elemento stubDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42c60b071c901538122751f6e92cfd7049f7be88
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994693"
---
# <a name="stubdefinitions-element"></a><span data-ttu-id="6d1a4-103">elemento stubDefinitions</span><span class="sxs-lookup"><span data-stu-id="6d1a4-103">stubDefinitions element</span></span>

<span data-ttu-id="6d1a4-104">Genera implementaciones para las funciones de código auxiliar para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="6d1a4-104">Generates implementations for stub functions for port-type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="6d1a4-105">Uso</span><span class="sxs-lookup"><span data-stu-id="6d1a4-105">Usage</span></span>

``` syntax
<stubDefinitions>
  child elements
</stubDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="6d1a4-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="6d1a4-106">Attributes</span></span>

<span data-ttu-id="6d1a4-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="6d1a4-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="6d1a4-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6d1a4-108">Child elements</span></span>



| <span data-ttu-id="6d1a4-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="6d1a4-109">Element</span></span>                                                         | <span data-ttu-id="6d1a4-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="6d1a4-110">Description</span></span>                                                                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6d1a4-111">**deallocator**</span><span class="sxs-lookup"><span data-stu-id="6d1a4-111">**deallocator**</span></span>](deallocator.md)<br/>                   | <span data-ttu-id="6d1a4-112">Especifica el tipo de desasignador que va a usar una función de código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="6d1a4-112">Specifies the type of deallocator to be used by a stub function.</span></span><br/> <br/>                                 |
| [<span data-ttu-id="6d1a4-113">**eventArg**</span><span class="sxs-lookup"><span data-stu-id="6d1a4-113">**eventArg**</span></span>](eventarg.md)<br/>                         | <span data-ttu-id="6d1a4-114">Especifica si los argumentos de evento relacionados se incluyen en las funciones generadas.</span><span class="sxs-lookup"><span data-stu-id="6d1a4-114">Specifies whether related event arguments are included in the generated functions.</span></span><br/> <br/>               |
| [<span data-ttu-id="6d1a4-115">**Eventos**</span><span class="sxs-lookup"><span data-stu-id="6d1a4-115">**events**</span></span>](events.md)<br/>                             | <span data-ttu-id="6d1a4-116">Especifica si los eventos relacionados se incluyen en las funciones generadas.</span><span class="sxs-lookup"><span data-stu-id="6d1a4-116">Specifies whether related events are included in the generated functions.</span></span><br/> <br/>                        |
| [<span data-ttu-id="6d1a4-117">**faultInfo**</span><span class="sxs-lookup"><span data-stu-id="6d1a4-117">**faultInfo**</span></span>](faultinfo.md)<br/>                       | <span data-ttu-id="6d1a4-118">Especifica si los parámetros usados para pasar información de error se incluyen en las funciones generadas.</span><span class="sxs-lookup"><span data-stu-id="6d1a4-118">Specifies whether parameters used to pass fault information are included in generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="6d1a4-119">**Operación**</span><span class="sxs-lookup"><span data-stu-id="6d1a4-119">**operation**</span></span>](operation.md)<br/>                       | <span data-ttu-id="6d1a4-120">Especifica una operación para la que se va a generar código.</span><span class="sxs-lookup"><span data-stu-id="6d1a4-120">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                        |
| [<span data-ttu-id="6d1a4-121">**operationDeallocator**</span><span class="sxs-lookup"><span data-stu-id="6d1a4-121">**operationDeallocator**</span></span>](operationdeallocator.md)<br/> | <span data-ttu-id="6d1a4-122">Especifica el tipo de desasignador que va a usar la función de código auxiliar de una operación.</span><span class="sxs-lookup"><span data-stu-id="6d1a4-122">Specifies the type of deallocator to be used by an operation's stub function.</span></span><br/> <br/>                    |
| [<span data-ttu-id="6d1a4-123">**portType**</span><span class="sxs-lookup"><span data-stu-id="6d1a4-123">**portType**</span></span>](porttype.md)<br/>                         | <span data-ttu-id="6d1a4-124">Especifica el tipo de puerto para el que se va a generar el código.</span><span class="sxs-lookup"><span data-stu-id="6d1a4-124">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                       |
| [<span data-ttu-id="6d1a4-125">**serverClass**</span><span class="sxs-lookup"><span data-stu-id="6d1a4-125">**serverClass**</span></span>](serverclass.md)<br/>                   | <span data-ttu-id="6d1a4-126">Especifica el nombre de la clase de servidor del lado host.</span><span class="sxs-lookup"><span data-stu-id="6d1a4-126">Specifies the name of the host-side server class.</span></span><br/> <br/>                                                |



### <a name="child-element-sequence"></a><span data-ttu-id="6d1a4-127">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6d1a4-127">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  serverClass, 
  eventArg?, 
  events?, 
  operationDeallocator*, 
  deallocator?, 
  faultInfo?
)
```

## <a name="parent-elements"></a><span data-ttu-id="6d1a4-128">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="6d1a4-128">Parent elements</span></span>



| <span data-ttu-id="6d1a4-129">Elemento</span><span class="sxs-lookup"><span data-stu-id="6d1a4-129">Element</span></span>                         | <span data-ttu-id="6d1a4-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="6d1a4-130">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="6d1a4-131">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="6d1a4-131">**file**</span></span>](file.md)<br/> | <span data-ttu-id="6d1a4-132">Genera un archivo del generador de código.</span><span class="sxs-lookup"><span data-stu-id="6d1a4-132">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="6d1a4-133">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="6d1a4-133">Element information</span></span>



| <span data-ttu-id="6d1a4-134">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="6d1a4-134">Label</span></span> | <span data-ttu-id="6d1a4-135">Value</span><span class="sxs-lookup"><span data-stu-id="6d1a4-135">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="6d1a4-136">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6d1a4-136">Minimum supported system</span></span><br/> | <span data-ttu-id="6d1a4-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6d1a4-137">Windows Vista</span></span> |
| <span data-ttu-id="6d1a4-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6d1a4-138">Can be empty</span></span>                        | <span data-ttu-id="6d1a4-139">No</span><span class="sxs-lookup"><span data-stu-id="6d1a4-139">No</span></span>            |



 

 




