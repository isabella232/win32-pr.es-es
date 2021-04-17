---
description: Genera implementaciones para las funciones de código auxiliar para las operaciones de tipo de puerto.
ms.assetid: 69899302-db54-493b-90de-596750be566f
title: elemento stubDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6676cfc6cf55aa9c9961bd614506500d847def0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697248"
---
# <a name="stubdefinitions-element"></a><span data-ttu-id="fa17d-103">elemento stubDefinitions</span><span class="sxs-lookup"><span data-stu-id="fa17d-103">stubDefinitions element</span></span>

<span data-ttu-id="fa17d-104">Genera implementaciones para las funciones de código auxiliar para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="fa17d-104">Generates implementations for stub functions for port-type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="fa17d-105">Uso</span><span class="sxs-lookup"><span data-stu-id="fa17d-105">Usage</span></span>

``` syntax
<stubDefinitions>
  child elements
</stubDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="fa17d-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="fa17d-106">Attributes</span></span>

<span data-ttu-id="fa17d-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="fa17d-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="fa17d-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fa17d-108">Child elements</span></span>



| <span data-ttu-id="fa17d-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="fa17d-109">Element</span></span>                                                         | <span data-ttu-id="fa17d-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="fa17d-110">Description</span></span>                                                                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa17d-111">**desasignador**</span><span class="sxs-lookup"><span data-stu-id="fa17d-111">**deallocator**</span></span>](deallocator.md)<br/>                   | <span data-ttu-id="fa17d-112">Especifica el tipo de desasignador que va a usar una función de código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="fa17d-112">Specifies the type of deallocator to be used by a stub function.</span></span><br/> <br/>                                 |
| [<span data-ttu-id="fa17d-113">**eventArg**</span><span class="sxs-lookup"><span data-stu-id="fa17d-113">**eventArg**</span></span>](eventarg.md)<br/>                         | <span data-ttu-id="fa17d-114">Especifica si los argumentos de evento relacionados se incluyen en las funciones generadas.</span><span class="sxs-lookup"><span data-stu-id="fa17d-114">Specifies whether related event arguments are included in the generated functions.</span></span><br/> <br/>               |
| [<span data-ttu-id="fa17d-115">**ceso**</span><span class="sxs-lookup"><span data-stu-id="fa17d-115">**events**</span></span>](events.md)<br/>                             | <span data-ttu-id="fa17d-116">Especifica si los eventos relacionados se incluyen en las funciones generadas.</span><span class="sxs-lookup"><span data-stu-id="fa17d-116">Specifies whether related events are included in the generated functions.</span></span><br/> <br/>                        |
| [<span data-ttu-id="fa17d-117">**faultInfo**</span><span class="sxs-lookup"><span data-stu-id="fa17d-117">**faultInfo**</span></span>](faultinfo.md)<br/>                       | <span data-ttu-id="fa17d-118">Especifica si los parámetros usados para pasar información de error se incluyen en las funciones generadas.</span><span class="sxs-lookup"><span data-stu-id="fa17d-118">Specifies whether parameters used to pass fault information are included in generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="fa17d-119">**sesión**</span><span class="sxs-lookup"><span data-stu-id="fa17d-119">**operation**</span></span>](operation.md)<br/>                       | <span data-ttu-id="fa17d-120">Especifica una operación para la que se va a generar código.</span><span class="sxs-lookup"><span data-stu-id="fa17d-120">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                        |
| [<span data-ttu-id="fa17d-121">**operationDeallocator**</span><span class="sxs-lookup"><span data-stu-id="fa17d-121">**operationDeallocator**</span></span>](operationdeallocator.md)<br/> | <span data-ttu-id="fa17d-122">Especifica el tipo de desasignador que va a usar la función de código auxiliar de una operación.</span><span class="sxs-lookup"><span data-stu-id="fa17d-122">Specifies the type of deallocator to be used by an operation's stub function.</span></span><br/> <br/>                    |
| [<span data-ttu-id="fa17d-123">**portType**</span><span class="sxs-lookup"><span data-stu-id="fa17d-123">**portType**</span></span>](porttype.md)<br/>                         | <span data-ttu-id="fa17d-124">Especifica el tipo de puerto para el que se generará el código.</span><span class="sxs-lookup"><span data-stu-id="fa17d-124">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                       |
| [<span data-ttu-id="fa17d-125">**serverClass**</span><span class="sxs-lookup"><span data-stu-id="fa17d-125">**serverClass**</span></span>](serverclass.md)<br/>                   | <span data-ttu-id="fa17d-126">Especifica el nombre de la clase de servidor del host.</span><span class="sxs-lookup"><span data-stu-id="fa17d-126">Specifies the name of the host-side server class.</span></span><br/> <br/>                                                |



### <a name="child-element-sequence"></a><span data-ttu-id="fa17d-127">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fa17d-127">Child element sequence</span></span>

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

## <a name="parent-elements"></a><span data-ttu-id="fa17d-128">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="fa17d-128">Parent elements</span></span>



| <span data-ttu-id="fa17d-129">Elemento</span><span class="sxs-lookup"><span data-stu-id="fa17d-129">Element</span></span>                         | <span data-ttu-id="fa17d-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="fa17d-130">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="fa17d-131">**archivo**</span><span class="sxs-lookup"><span data-stu-id="fa17d-131">**file**</span></span>](file.md)<br/> | <span data-ttu-id="fa17d-132">Genera un archivo desde el generador de código.</span><span class="sxs-lookup"><span data-stu-id="fa17d-132">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="fa17d-133">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="fa17d-133">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="fa17d-134">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fa17d-134">Minimum supported system</span></span><br/> | <span data-ttu-id="fa17d-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fa17d-135">Windows Vista</span></span> |
| <span data-ttu-id="fa17d-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="fa17d-136">Can be empty</span></span>                        | <span data-ttu-id="fa17d-137">No</span><span class="sxs-lookup"><span data-stu-id="fa17d-137">No</span></span>            |



 

 




