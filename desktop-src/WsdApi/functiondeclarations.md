---
description: Genera declaraciones de implementación para las funciones de proxy para las operaciones de tipo de puerto.
ms.assetid: 6ba7dbb6-6598-4569-97e1-d703e4b896c7
title: elemento functionDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b82aca30f94fc8fcec80701a74b56e83ab674c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104276974"
---
# <a name="functiondeclarations-element"></a><span data-ttu-id="7ab6f-103">elemento functionDeclarations</span><span class="sxs-lookup"><span data-stu-id="7ab6f-103">functionDeclarations element</span></span>

<span data-ttu-id="7ab6f-104">Genera declaraciones de implementación para las funciones de proxy para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="7ab6f-104">Generates implementation declarations for proxy functions for port type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="7ab6f-105">Uso</span><span class="sxs-lookup"><span data-stu-id="7ab6f-105">Usage</span></span>

``` syntax
<functionDeclarations>
  child elements
</functionDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="7ab6f-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="7ab6f-106">Attributes</span></span>

<span data-ttu-id="7ab6f-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="7ab6f-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="7ab6f-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7ab6f-108">Child elements</span></span>



| <span data-ttu-id="7ab6f-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="7ab6f-109">Element</span></span>                                   | <span data-ttu-id="7ab6f-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="7ab6f-110">Description</span></span>                                                                                                             |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7ab6f-111">**async**</span><span class="sxs-lookup"><span data-stu-id="7ab6f-111">**async**</span></span>](async.md)<br/>         | <span data-ttu-id="7ab6f-112">Especifica si las operaciones asincrónicas se incluyen en las funciones de proxy generadas.</span><span class="sxs-lookup"><span data-stu-id="7ab6f-112">Specifies whether asynchronous operations are included in the generated proxy functions.</span></span><br/> <br/>         |
| [<span data-ttu-id="7ab6f-113">**ceso**</span><span class="sxs-lookup"><span data-stu-id="7ab6f-113">**events**</span></span>](events.md)<br/>       | <span data-ttu-id="7ab6f-114">Especifica si los eventos relacionados se incluyen en las funciones generadas.</span><span class="sxs-lookup"><span data-stu-id="7ab6f-114">Specifies whether related events are included in the generated functions.</span></span><br/> <br/>                        |
| [<span data-ttu-id="7ab6f-115">**faultInfo**</span><span class="sxs-lookup"><span data-stu-id="7ab6f-115">**faultInfo**</span></span>](faultinfo.md)<br/> | <span data-ttu-id="7ab6f-116">Especifica si los parámetros usados para pasar información de error se incluyen en las funciones generadas.</span><span class="sxs-lookup"><span data-stu-id="7ab6f-116">Specifies whether parameters used to pass fault information are included in generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="7ab6f-117">**sesión**</span><span class="sxs-lookup"><span data-stu-id="7ab6f-117">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="7ab6f-118">Especifica una operación para la que se va a generar código.</span><span class="sxs-lookup"><span data-stu-id="7ab6f-118">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                        |
| [<span data-ttu-id="7ab6f-119">**portType**</span><span class="sxs-lookup"><span data-stu-id="7ab6f-119">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="7ab6f-120">Especifica el tipo de puerto para el que se generará el código.</span><span class="sxs-lookup"><span data-stu-id="7ab6f-120">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                       |



### <a name="child-element-sequence"></a><span data-ttu-id="7ab6f-121">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7ab6f-121">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  events?, 
  async?, 
  faultInfo?
)
```

## <a name="parent-elements"></a><span data-ttu-id="7ab6f-122">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="7ab6f-122">Parent elements</span></span>



| <span data-ttu-id="7ab6f-123">Elemento</span><span class="sxs-lookup"><span data-stu-id="7ab6f-123">Element</span></span>                         | <span data-ttu-id="7ab6f-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="7ab6f-124">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="7ab6f-125">**archivo**</span><span class="sxs-lookup"><span data-stu-id="7ab6f-125">**file**</span></span>](file.md)<br/> | <span data-ttu-id="7ab6f-126">Genera un archivo desde el generador de código.</span><span class="sxs-lookup"><span data-stu-id="7ab6f-126">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="7ab6f-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7ab6f-127">Remarks</span></span>

<span data-ttu-id="7ab6f-128">Este elemento genera declaraciones de funciones miembro correspondientes a las operaciones a las que el contrato llama.</span><span class="sxs-lookup"><span data-stu-id="7ab6f-128">This element generates declarations of member functions corresponding to operations called out by the contract.</span></span> <span data-ttu-id="7ab6f-129">Estas declaraciones tienen un formato adecuado para su uso por parte de un compilador de C++ y se suelen usar en los archivos. cpp.</span><span class="sxs-lookup"><span data-stu-id="7ab6f-129">These declarations are in a form appropriate for consumption by a C++ compiler and are generally used in .cpp files.</span></span>

<span data-ttu-id="7ab6f-130">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="7ab6f-130">Example:</span></span>

``` syntax
<functionDeclarations events = "true"/>
```

## <a name="element-information"></a><span data-ttu-id="7ab6f-131">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="7ab6f-131">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="7ab6f-132">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ab6f-132">Minimum supported system</span></span><br/> | <span data-ttu-id="7ab6f-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7ab6f-133">Windows Vista</span></span> |
| <span data-ttu-id="7ab6f-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7ab6f-134">Can be empty</span></span>                        | <span data-ttu-id="7ab6f-135">Sí</span><span class="sxs-lookup"><span data-stu-id="7ab6f-135">Yes</span></span>           |



 

 




