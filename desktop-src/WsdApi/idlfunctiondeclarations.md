---
description: Genera declaraciones IDL para las funciones de proxy para las operaciones de tipo de puerto.
ms.assetid: e56fdd68-b72d-4167-9e4c-b5bbf103880b
title: elemento idlFunctionDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1afa43676898231f739804185b8bf5d6e2b4faf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715805"
---
# <a name="idlfunctiondeclarations-element"></a><span data-ttu-id="f7964-103">elemento idlFunctionDeclarations</span><span class="sxs-lookup"><span data-stu-id="f7964-103">idlFunctionDeclarations element</span></span>

<span data-ttu-id="f7964-104">Genera declaraciones IDL para las funciones de proxy para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="f7964-104">Generates IDL declarations for proxy functions for port type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="f7964-105">Uso</span><span class="sxs-lookup"><span data-stu-id="f7964-105">Usage</span></span>

``` syntax
<idlFunctionDeclarations>
  child elements
</idlFunctionDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="f7964-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="f7964-106">Attributes</span></span>

<span data-ttu-id="f7964-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="f7964-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="f7964-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f7964-108">Child elements</span></span>



| <span data-ttu-id="f7964-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="f7964-109">Element</span></span>                                   | <span data-ttu-id="f7964-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f7964-110">Description</span></span>                                                                                                             |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f7964-111">**async**</span><span class="sxs-lookup"><span data-stu-id="f7964-111">**async**</span></span>](async.md)<br/>         | <span data-ttu-id="f7964-112">Especifica si las operaciones asincrónicas se incluyen en las funciones de proxy generadas.</span><span class="sxs-lookup"><span data-stu-id="f7964-112">Specifies whether asynchronous operations are included in the generated proxy functions.</span></span><br/> <br/>         |
| [<span data-ttu-id="f7964-113">**eventArg**</span><span class="sxs-lookup"><span data-stu-id="f7964-113">**eventArg**</span></span>](eventarg.md)<br/>   | <span data-ttu-id="f7964-114">Especifica si los argumentos de evento relacionados se incluyen en las funciones generadas.</span><span class="sxs-lookup"><span data-stu-id="f7964-114">Specifies whether related event arguments are included in the generated functions.</span></span><br/> <br/>               |
| [<span data-ttu-id="f7964-115">**ceso**</span><span class="sxs-lookup"><span data-stu-id="f7964-115">**events**</span></span>](events.md)<br/>       | <span data-ttu-id="f7964-116">Especifica si los eventos relacionados se incluyen en las funciones generadas.</span><span class="sxs-lookup"><span data-stu-id="f7964-116">Specifies whether related events are included in the generated functions.</span></span><br/> <br/>                        |
| [<span data-ttu-id="f7964-117">**faultInfo**</span><span class="sxs-lookup"><span data-stu-id="f7964-117">**faultInfo**</span></span>](faultinfo.md)<br/> | <span data-ttu-id="f7964-118">Especifica si los parámetros usados para pasar información de error se incluyen en las funciones generadas.</span><span class="sxs-lookup"><span data-stu-id="f7964-118">Specifies whether parameters used to pass fault information are included in generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="f7964-119">**sesión**</span><span class="sxs-lookup"><span data-stu-id="f7964-119">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="f7964-120">Especifica una operación para la que se va a generar código.</span><span class="sxs-lookup"><span data-stu-id="f7964-120">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                        |
| [<span data-ttu-id="f7964-121">**portType**</span><span class="sxs-lookup"><span data-stu-id="f7964-121">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="f7964-122">Especifica el tipo de puerto para el que se generará el código.</span><span class="sxs-lookup"><span data-stu-id="f7964-122">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                       |



### <a name="child-element-sequence"></a><span data-ttu-id="f7964-123">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f7964-123">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  eventArg?, 
  events?, 
  async?, 
  faultInfo?
)
```

## <a name="parent-elements"></a><span data-ttu-id="f7964-124">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="f7964-124">Parent elements</span></span>



| <span data-ttu-id="f7964-125">Elemento</span><span class="sxs-lookup"><span data-stu-id="f7964-125">Element</span></span>                         | <span data-ttu-id="f7964-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="f7964-126">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="f7964-127">**archivo**</span><span class="sxs-lookup"><span data-stu-id="f7964-127">**file**</span></span>](file.md)<br/> | <span data-ttu-id="f7964-128">Genera un archivo desde el generador de código.</span><span class="sxs-lookup"><span data-stu-id="f7964-128">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="f7964-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f7964-129">Remarks</span></span>

<span data-ttu-id="f7964-130">Este elemento genera declaraciones de funciones miembro correspondientes a las operaciones a las que el contrato llama.</span><span class="sxs-lookup"><span data-stu-id="f7964-130">This element generates declarations of member functions corresponding to operations called out by the contract.</span></span> <span data-ttu-id="f7964-131">Estas declaraciones tienen un formato adecuado para su uso por el compilador de MIDL y se suelen usar en archivos. idl.</span><span class="sxs-lookup"><span data-stu-id="f7964-131">These declarations are in a form appropriate for consumption by the MIDL compiler and are generally used in .idl files.</span></span>

<span data-ttu-id="f7964-132">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="f7964-132">Example:</span></span>

``` syntax
<idlFunctionDeclarations events = "true"/>
```

## <a name="element-information"></a><span data-ttu-id="f7964-133">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="f7964-133">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="f7964-134">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f7964-134">Minimum supported system</span></span><br/> | <span data-ttu-id="f7964-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f7964-135">Windows Vista</span></span> |
| <span data-ttu-id="f7964-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f7964-136">Can be empty</span></span>                        | <span data-ttu-id="f7964-137">Sí</span><span class="sxs-lookup"><span data-stu-id="f7964-137">Yes</span></span>           |



 

 




