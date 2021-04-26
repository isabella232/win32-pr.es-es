---
description: Genera declaraciones IDL para las funciones de proxy para las operaciones de tipo de puerto.
ms.assetid: e56fdd68-b72d-4167-9e4c-b5bbf103880b
title: Elemento idlFunctionDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf4d1648ac6d9c3ac6900826ebe90a64418822b6
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994742"
---
# <a name="idlfunctiondeclarations-element"></a><span data-ttu-id="b88b5-103">Elemento idlFunctionDeclarations</span><span class="sxs-lookup"><span data-stu-id="b88b5-103">idlFunctionDeclarations element</span></span>

<span data-ttu-id="b88b5-104">Genera declaraciones IDL para las funciones de proxy para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="b88b5-104">Generates IDL declarations for proxy functions for port type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="b88b5-105">Uso</span><span class="sxs-lookup"><span data-stu-id="b88b5-105">Usage</span></span>

``` syntax
<idlFunctionDeclarations>
  child elements
</idlFunctionDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="b88b5-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="b88b5-106">Attributes</span></span>

<span data-ttu-id="b88b5-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="b88b5-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="b88b5-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b88b5-108">Child elements</span></span>



| <span data-ttu-id="b88b5-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="b88b5-109">Element</span></span>                                   | <span data-ttu-id="b88b5-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="b88b5-110">Description</span></span>                                                                                                             |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b88b5-111">**async**</span><span class="sxs-lookup"><span data-stu-id="b88b5-111">**async**</span></span>](async.md)<br/>         | <span data-ttu-id="b88b5-112">Especifica si las operaciones asincrónicas se incluyen en las funciones de proxy generadas.</span><span class="sxs-lookup"><span data-stu-id="b88b5-112">Specifies whether asynchronous operations are included in the generated proxy functions.</span></span><br/> <br/>         |
| [<span data-ttu-id="b88b5-113">**eventArg**</span><span class="sxs-lookup"><span data-stu-id="b88b5-113">**eventArg**</span></span>](eventarg.md)<br/>   | <span data-ttu-id="b88b5-114">Especifica si los argumentos de evento relacionados se incluyen en las funciones generadas.</span><span class="sxs-lookup"><span data-stu-id="b88b5-114">Specifies whether related event arguments are included in the generated functions.</span></span><br/> <br/>               |
| [<span data-ttu-id="b88b5-115">**Eventos**</span><span class="sxs-lookup"><span data-stu-id="b88b5-115">**events**</span></span>](events.md)<br/>       | <span data-ttu-id="b88b5-116">Especifica si los eventos relacionados se incluyen en las funciones generadas.</span><span class="sxs-lookup"><span data-stu-id="b88b5-116">Specifies whether related events are included in the generated functions.</span></span><br/> <br/>                        |
| [<span data-ttu-id="b88b5-117">**faultInfo**</span><span class="sxs-lookup"><span data-stu-id="b88b5-117">**faultInfo**</span></span>](faultinfo.md)<br/> | <span data-ttu-id="b88b5-118">Especifica si los parámetros usados para pasar información de error se incluyen en las funciones generadas.</span><span class="sxs-lookup"><span data-stu-id="b88b5-118">Specifies whether parameters used to pass fault information are included in generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="b88b5-119">**Operación**</span><span class="sxs-lookup"><span data-stu-id="b88b5-119">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="b88b5-120">Especifica una operación para la que se va a generar código.</span><span class="sxs-lookup"><span data-stu-id="b88b5-120">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                        |
| [<span data-ttu-id="b88b5-121">**portType**</span><span class="sxs-lookup"><span data-stu-id="b88b5-121">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="b88b5-122">Especifica el tipo de puerto para el que se va a generar el código.</span><span class="sxs-lookup"><span data-stu-id="b88b5-122">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                       |



### <a name="child-element-sequence"></a><span data-ttu-id="b88b5-123">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b88b5-123">Child element sequence</span></span>

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

## <a name="parent-elements"></a><span data-ttu-id="b88b5-124">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="b88b5-124">Parent elements</span></span>



| <span data-ttu-id="b88b5-125">Elemento</span><span class="sxs-lookup"><span data-stu-id="b88b5-125">Element</span></span>                         | <span data-ttu-id="b88b5-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="b88b5-126">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="b88b5-127">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="b88b5-127">**file**</span></span>](file.md)<br/> | <span data-ttu-id="b88b5-128">Genera un archivo desde el generador de código.</span><span class="sxs-lookup"><span data-stu-id="b88b5-128">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="b88b5-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b88b5-129">Remarks</span></span>

<span data-ttu-id="b88b5-130">Este elemento genera declaraciones de funciones miembro correspondientes a las operaciones a las que llama el contrato.</span><span class="sxs-lookup"><span data-stu-id="b88b5-130">This element generates declarations of member functions corresponding to operations called out by the contract.</span></span> <span data-ttu-id="b88b5-131">Estas declaraciones tienen un formato adecuado para el consumo por parte del compilador MIDL y se usan generalmente en archivos .idl.</span><span class="sxs-lookup"><span data-stu-id="b88b5-131">These declarations are in a form appropriate for consumption by the MIDL compiler and are generally used in .idl files.</span></span>

<span data-ttu-id="b88b5-132">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="b88b5-132">Example:</span></span>

``` syntax
<idlFunctionDeclarations events = "true"/>
```

## <a name="element-information"></a><span data-ttu-id="b88b5-133">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="b88b5-133">Element information</span></span>



| <span data-ttu-id="b88b5-134">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="b88b5-134">Label</span></span> | <span data-ttu-id="b88b5-135">Value</span><span class="sxs-lookup"><span data-stu-id="b88b5-135">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="b88b5-136">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b88b5-136">Minimum supported system</span></span><br/> | <span data-ttu-id="b88b5-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b88b5-137">Windows Vista</span></span> |
| <span data-ttu-id="b88b5-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b88b5-138">Can be empty</span></span>                        | <span data-ttu-id="b88b5-139">Sí</span><span class="sxs-lookup"><span data-stu-id="b88b5-139">Yes</span></span>           |



 

 




