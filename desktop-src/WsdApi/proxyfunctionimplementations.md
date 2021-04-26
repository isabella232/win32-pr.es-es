---
description: Genera implementaciones para las funciones de proxy para las operaciones de tipo de puerto.
ms.assetid: 9505ee5f-fdb9-41b8-9537-0c5d29f90168
title: elemento proxyFunctionImplementations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e9f03834ca59ede41f2f3c3dff00d7dacdd54db
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995762"
---
# <a name="proxyfunctionimplementations-element"></a><span data-ttu-id="e2976-103">elemento proxyFunctionImplementations</span><span class="sxs-lookup"><span data-stu-id="e2976-103">proxyFunctionImplementations element</span></span>

<span data-ttu-id="e2976-104">Genera implementaciones para las funciones de proxy para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="e2976-104">Generates implementations for proxy functions for port type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="e2976-105">Uso</span><span class="sxs-lookup"><span data-stu-id="e2976-105">Usage</span></span>

``` syntax
<proxyFunctionImplementations>
  child elements
</proxyFunctionImplementations>
```

## <a name="attributes"></a><span data-ttu-id="e2976-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="e2976-106">Attributes</span></span>

<span data-ttu-id="e2976-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="e2976-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="e2976-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e2976-108">Child elements</span></span>



| <span data-ttu-id="e2976-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="e2976-109">Element</span></span>                                     | <span data-ttu-id="e2976-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e2976-110">Description</span></span>                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e2976-111">**async**</span><span class="sxs-lookup"><span data-stu-id="e2976-111">**async**</span></span>](async.md)<br/>           | <span data-ttu-id="e2976-112">Especifica si las operaciones asincrónicas se incluyen en las funciones de proxy generadas.</span><span class="sxs-lookup"><span data-stu-id="e2976-112">Specifies whether asynchronous operations are included in the generated proxy functions.</span></span><br/> <br/>         |
| [<span data-ttu-id="e2976-113">**Eventos**</span><span class="sxs-lookup"><span data-stu-id="e2976-113">**events**</span></span>](events.md)<br/>         | <span data-ttu-id="e2976-114">Especifica si los eventos relacionados se incluyen en las funciones generadas.</span><span class="sxs-lookup"><span data-stu-id="e2976-114">Specifies whether related events are included in the generated functions.</span></span><br/> <br/>                        |
| [<span data-ttu-id="e2976-115">**faultInfo**</span><span class="sxs-lookup"><span data-stu-id="e2976-115">**faultInfo**</span></span>](faultinfo.md)<br/>   | <span data-ttu-id="e2976-116">Especifica si los parámetros usados para pasar información de error se incluyen en las funciones generadas.</span><span class="sxs-lookup"><span data-stu-id="e2976-116">Specifies whether parameters used to pass fault information are included in generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="e2976-117">**Operación**</span><span class="sxs-lookup"><span data-stu-id="e2976-117">**operation**</span></span>](operation.md)<br/>   | <span data-ttu-id="e2976-118">Especifica una operación para la que se va a generar código.</span><span class="sxs-lookup"><span data-stu-id="e2976-118">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                        |
| [<span data-ttu-id="e2976-119">**portType**</span><span class="sxs-lookup"><span data-stu-id="e2976-119">**portType**</span></span>](porttype.md)<br/>     | <span data-ttu-id="e2976-120">Especifica el tipo de puerto para el que se va a generar el código.</span><span class="sxs-lookup"><span data-stu-id="e2976-120">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                       |
| [<span data-ttu-id="e2976-121">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="e2976-121">**proxyClass**</span></span>](proxyclass.md)<br/> | <span data-ttu-id="e2976-122">Especifica el nombre de la clase de proxy del lado cliente.</span><span class="sxs-lookup"><span data-stu-id="e2976-122">Specifies the name of the client-side proxy class.</span></span><br/> <br/>                                               |



### <a name="child-element-sequence"></a><span data-ttu-id="e2976-123">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e2976-123">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  proxyClass?, 
  events?, 
  async?, 
  faultInfo?
)
```

## <a name="parent-elements"></a><span data-ttu-id="e2976-124">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="e2976-124">Parent elements</span></span>



| <span data-ttu-id="e2976-125">Elemento</span><span class="sxs-lookup"><span data-stu-id="e2976-125">Element</span></span>                         | <span data-ttu-id="e2976-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="e2976-126">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="e2976-127">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="e2976-127">**file**</span></span>](file.md)<br/> | <span data-ttu-id="e2976-128">Genera un archivo del generador de código.</span><span class="sxs-lookup"><span data-stu-id="e2976-128">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="e2976-129">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="e2976-129">Element information</span></span>



| <span data-ttu-id="e2976-130">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="e2976-130">Label</span></span> | <span data-ttu-id="e2976-131">Value</span><span class="sxs-lookup"><span data-stu-id="e2976-131">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="e2976-132">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2976-132">Minimum supported system</span></span><br/> | <span data-ttu-id="e2976-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e2976-133">Windows Vista</span></span> |
| <span data-ttu-id="e2976-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e2976-134">Can be empty</span></span>                        | <span data-ttu-id="e2976-135">Sí</span><span class="sxs-lookup"><span data-stu-id="e2976-135">Yes</span></span>           |



 

 




