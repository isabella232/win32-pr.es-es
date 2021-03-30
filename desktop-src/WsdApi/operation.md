---
description: Especifica una operación para la que se va a generar código.
ms.assetid: d198197e-d146-4f1b-99df-944822e83357
title: elemento Operation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bdd8324553e046000f467c103afd6ac0464cbc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082440"
---
# <a name="operation-element"></a><span data-ttu-id="8914d-103">elemento Operation</span><span class="sxs-lookup"><span data-stu-id="8914d-103">operation element</span></span>

<span data-ttu-id="8914d-104">Especifica una operación para la que se va a generar código.</span><span class="sxs-lookup"><span data-stu-id="8914d-104">Specifies an operation for which code is to be generated.</span></span>

## <a name="usage"></a><span data-ttu-id="8914d-105">Uso</span><span class="sxs-lookup"><span data-stu-id="8914d-105">Usage</span></span>

``` syntax
<operation/>
```

## <a name="attributes"></a><span data-ttu-id="8914d-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="8914d-106">Attributes</span></span>

<span data-ttu-id="8914d-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="8914d-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="8914d-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8914d-108">Child elements</span></span>

<span data-ttu-id="8914d-109">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="8914d-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="8914d-110">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="8914d-110">Parent elements</span></span>



| <span data-ttu-id="8914d-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="8914d-111">Element</span></span>                                                                                                 | <span data-ttu-id="8914d-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="8914d-112">Description</span></span>                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8914d-113">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="8914d-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                                         | <span data-ttu-id="8914d-114">Genera declaraciones de implementación para las funciones de proxy para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="8914d-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/>                                    |
| [<span data-ttu-id="8914d-115">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="8914d-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>                                   | <span data-ttu-id="8914d-116">Genera declaraciones IDL para las funciones de proxy para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="8914d-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>                                               |
| [<span data-ttu-id="8914d-117">**messageStructureDefinitions**</span><span class="sxs-lookup"><span data-stu-id="8914d-117">**messageStructureDefinitions**</span></span>](messagestructuredefinitions.md)<br/>                           | <span data-ttu-id="8914d-118">Genera definiciones de estructura de C para los tipos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="8914d-118">Generates C structure definitions for message types.</span></span><br/> <br/>                                                                   |
| [<span data-ttu-id="8914d-119">**messageTypeDeclarations**</span><span class="sxs-lookup"><span data-stu-id="8914d-119">**messageTypeDeclarations**</span></span>](messagetypedeclarations.md)<br/>                                   | <span data-ttu-id="8914d-120">Genera declaraciones de constantes de C para las tablas de esquemas XML para los tipos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="8914d-120">Generates C constant declarations for XML schema tables for message types.</span></span><br/> <br/>                                             |
| [<span data-ttu-id="8914d-121">**messageTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="8914d-121">**messageTypeDefinitions**</span></span>](messagetypedefinitions.md)<br/>                                     | <span data-ttu-id="8914d-122">Genera constantes de C para las tablas de esquemas XML para los tipos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="8914d-122">Generates C constants for XML schema tables for message types.</span></span><br/> <br/>                                                         |
| [<span data-ttu-id="8914d-123">**portTypeDeclarations**</span><span class="sxs-lookup"><span data-stu-id="8914d-123">**portTypeDeclarations**</span></span>](porttypedeclarations.md)<br/>                                         | <span data-ttu-id="8914d-124">Genera declaraciones de constantes de C para los tipos de puerto.</span><span class="sxs-lookup"><span data-stu-id="8914d-124">Generates C constant declarations for port types.</span></span><br/> <br/>                                                                      |
| [<span data-ttu-id="8914d-125">**portTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="8914d-125">**portTypeDefinitions**</span></span>](porttypedefinitions.md)<br/>                                           | <span data-ttu-id="8914d-126">Genera constantes de C para los tipos de puerto.</span><span class="sxs-lookup"><span data-stu-id="8914d-126">Generates C constants for port types.</span></span><br/> <br/>                                                                                  |
| [<span data-ttu-id="8914d-127">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="8914d-127">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/>                         | <span data-ttu-id="8914d-128">Genera implementaciones para las funciones de proxy para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="8914d-128">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>                                                |
| [<span data-ttu-id="8914d-129">**stubDeclarations**</span><span class="sxs-lookup"><span data-stu-id="8914d-129">**stubDeclarations**</span></span>](stubdeclarations.md)<br/>                                                 | <span data-ttu-id="8914d-130">Genera declaraciones para las funciones de código auxiliar para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="8914d-130">Generates declarations for stub functions for port type operations.</span></span><br/> <br/>                                                    |
| [<span data-ttu-id="8914d-131">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="8914d-131">**stubDefinitions**</span></span>](stubdefinitions.md)<br/>                                                   | <span data-ttu-id="8914d-132">Genera implementaciones para las funciones de código auxiliar para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="8914d-132">Generates implementations for stub functions for port type operations.</span></span><br/> <br/>                                                 |
| [<span data-ttu-id="8914d-133">**subscriptionFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="8914d-133">**subscriptionFunctionDeclarations**</span></span>](subscriptionfunctiondeclarations.md)<br/>                 | <span data-ttu-id="8914d-134">Genera declaraciones de implementación para las funciones de proxy de suscripción y cancelación de suscripción para las operaciones de notificación de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="8914d-134">Generates implementation declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/> |
| [<span data-ttu-id="8914d-135">**subscriptionIdlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="8914d-135">**subscriptionIdlFunctionDeclarations**</span></span>](subscriptionidlfunctiondeclarations.md)<br/>           | <span data-ttu-id="8914d-136">Genera declaraciones IDL para las funciones de proxy de suscripción y cancelación de suscripción para las operaciones de notificación de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="8914d-136">Generates IDL declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="8914d-137">**subscriptionProxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="8914d-137">**subscriptionProxyFunctionImplementations**</span></span>](subscriptionproxyfunctionimplementations.md)<br/> | <span data-ttu-id="8914d-138">Genera implementaciones para las funciones de proxy de suscripción y cancelación de suscripción para las operaciones de notificación de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="8914d-138">Generates implementations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/>             |



## <a name="remarks"></a><span data-ttu-id="8914d-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8914d-139">Remarks</span></span>

<span data-ttu-id="8914d-140">Se puede especificar cualquier número de operaciones.</span><span class="sxs-lookup"><span data-stu-id="8914d-140">Any number of operations may be specified.</span></span> <span data-ttu-id="8914d-141">Si no se especifica ninguna operación, se genera código para todas las operaciones en todos los tipos de Puerto pertinentes.</span><span class="sxs-lookup"><span data-stu-id="8914d-141">If no operations are specified, code is generated for all operations in all the relevant port types.</span></span> <span data-ttu-id="8914d-142">El uso del elemento **Operation** limitará los métodos generados a los que se incluyen en la operación.</span><span class="sxs-lookup"><span data-stu-id="8914d-142">Using the **operation** element will limit the methods generated to those contained in the operation.</span></span>

<span data-ttu-id="8914d-143">Por ejemplo, una impresora admite estas operaciones entre otras:</span><span class="sxs-lookup"><span data-stu-id="8914d-143">For example, a printer supports these operations among others:</span></span>

-   <span data-ttu-id="8914d-144">**PrintJobByPost**</span><span class="sxs-lookup"><span data-stu-id="8914d-144">**PrintJobByPost**</span></span>
-   <span data-ttu-id="8914d-145">**PrintJobByReference**</span><span class="sxs-lookup"><span data-stu-id="8914d-145">**PrintJobByReference**</span></span>
-   <span data-ttu-id="8914d-146">**CancelJob**</span><span class="sxs-lookup"><span data-stu-id="8914d-146">**CancelJob**</span></span>
-   <span data-ttu-id="8914d-147">**GetJobElements**</span><span class="sxs-lookup"><span data-stu-id="8914d-147">**GetJobElements**</span></span>
-   <span data-ttu-id="8914d-148">**GetActiveJobs**</span><span class="sxs-lookup"><span data-stu-id="8914d-148">**GetActiveJobs**</span></span>
-   <span data-ttu-id="8914d-149">**GetJobHistory**</span><span class="sxs-lookup"><span data-stu-id="8914d-149">**GetJobHistory**</span></span>
-   <span data-ttu-id="8914d-150">**SubscribeToPrinterConfigChange**</span><span class="sxs-lookup"><span data-stu-id="8914d-150">**SubscribeToPrinterConfigChange**</span></span>
-   <span data-ttu-id="8914d-151">**UnsubscribeToPrinterConfigChange**</span><span class="sxs-lookup"><span data-stu-id="8914d-151">**UnsubscribeToPrinterConfigChange**</span></span>

<span data-ttu-id="8914d-152">Sin embargo, para incluir solo los métodos relacionados con las operaciones **PrintJobByPost** y **GetJobElements** , el script de generación de código usaría los elementos [**idlFunctionDeclarations**](idlfunctiondeclarations.md) de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8914d-152">However, to include only the methods related to the **PrintJobByPost** and **GetJobElements** operations, the code generation script would use the [**idlFunctionDeclarations**](idlfunctiondeclarations.md) elements as follows:</span></span>

``` syntax
<idlFunctionDeclarations>
    <operation>PrintJobByPost</operation>
    <operation>GetJobElements></operation>
</idlFunctionDeclarations>
```

<span data-ttu-id="8914d-153">Esto genera declaraciones de función IDL para todos los métodos asociados a las dos operaciones (por ejemplo, **BeginPrintJobByPost**, **EndPrintJobByPost**, **BeginGetJobElements** y **EndGetJobElements**).</span><span class="sxs-lookup"><span data-stu-id="8914d-153">This generates idl function declarations for all methods associated with the two operations (for example, **BeginPrintJobByPost**, **EndPrintJobByPost**, **BeginGetJobElements** and **EndGetJobElements**).</span></span>

## <a name="element-information"></a><span data-ttu-id="8914d-154">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="8914d-154">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="8914d-155">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8914d-155">Minimum supported system</span></span><br/> | <span data-ttu-id="8914d-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8914d-156">Windows Vista</span></span> |
| <span data-ttu-id="8914d-157">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8914d-157">Can be empty</span></span>                        | <span data-ttu-id="8914d-158">Sí</span><span class="sxs-lookup"><span data-stu-id="8914d-158">Yes</span></span>           |



 

 




