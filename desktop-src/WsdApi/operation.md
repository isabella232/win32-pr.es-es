---
description: Especifica una operación para la que se va a generar código.
ms.assetid: d198197e-d146-4f1b-99df-944822e83357
title: elemento operation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c0e4562241f5f437554d0af28dc8bca482512ea
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994321"
---
# <a name="operation-element"></a><span data-ttu-id="64aee-103">elemento operation</span><span class="sxs-lookup"><span data-stu-id="64aee-103">operation element</span></span>

<span data-ttu-id="64aee-104">Especifica una operación para la que se va a generar código.</span><span class="sxs-lookup"><span data-stu-id="64aee-104">Specifies an operation for which code is to be generated.</span></span>

## <a name="usage"></a><span data-ttu-id="64aee-105">Uso</span><span class="sxs-lookup"><span data-stu-id="64aee-105">Usage</span></span>

``` syntax
<operation/>
```

## <a name="attributes"></a><span data-ttu-id="64aee-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="64aee-106">Attributes</span></span>

<span data-ttu-id="64aee-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="64aee-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="64aee-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="64aee-108">Child elements</span></span>

<span data-ttu-id="64aee-109">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="64aee-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="64aee-110">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="64aee-110">Parent elements</span></span>



| <span data-ttu-id="64aee-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="64aee-111">Element</span></span>                                                                                                 | <span data-ttu-id="64aee-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="64aee-112">Description</span></span>                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="64aee-113">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="64aee-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                                         | <span data-ttu-id="64aee-114">Genera declaraciones de implementación para las funciones de proxy para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="64aee-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/>                                    |
| [<span data-ttu-id="64aee-115">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="64aee-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>                                   | <span data-ttu-id="64aee-116">Genera declaraciones IDL para las funciones de proxy para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="64aee-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>                                               |
| [<span data-ttu-id="64aee-117">**messageStructureDefinitions**</span><span class="sxs-lookup"><span data-stu-id="64aee-117">**messageStructureDefinitions**</span></span>](messagestructuredefinitions.md)<br/>                           | <span data-ttu-id="64aee-118">Genera definiciones de estructura de C para tipos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="64aee-118">Generates C structure definitions for message types.</span></span><br/> <br/>                                                                   |
| [<span data-ttu-id="64aee-119">**messageTypeDeclarations**</span><span class="sxs-lookup"><span data-stu-id="64aee-119">**messageTypeDeclarations**</span></span>](messagetypedeclarations.md)<br/>                                   | <span data-ttu-id="64aee-120">Genera declaraciones constantes de C para tablas de esquema XML para tipos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="64aee-120">Generates C constant declarations for XML schema tables for message types.</span></span><br/> <br/>                                             |
| [<span data-ttu-id="64aee-121">**messageTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="64aee-121">**messageTypeDefinitions**</span></span>](messagetypedefinitions.md)<br/>                                     | <span data-ttu-id="64aee-122">Genera constantes de C para tablas de esquema XML para tipos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="64aee-122">Generates C constants for XML schema tables for message types.</span></span><br/> <br/>                                                         |
| [<span data-ttu-id="64aee-123">**portTypeDeclarations**</span><span class="sxs-lookup"><span data-stu-id="64aee-123">**portTypeDeclarations**</span></span>](porttypedeclarations.md)<br/>                                         | <span data-ttu-id="64aee-124">Genera declaraciones constantes de C para tipos de puerto.</span><span class="sxs-lookup"><span data-stu-id="64aee-124">Generates C constant declarations for port types.</span></span><br/> <br/>                                                                      |
| [<span data-ttu-id="64aee-125">**portTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="64aee-125">**portTypeDefinitions**</span></span>](porttypedefinitions.md)<br/>                                           | <span data-ttu-id="64aee-126">Genera constantes de C para tipos de puerto.</span><span class="sxs-lookup"><span data-stu-id="64aee-126">Generates C constants for port types.</span></span><br/> <br/>                                                                                  |
| [<span data-ttu-id="64aee-127">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="64aee-127">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/>                         | <span data-ttu-id="64aee-128">Genera implementaciones para las funciones de proxy para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="64aee-128">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>                                                |
| [<span data-ttu-id="64aee-129">**stubDeclarations**</span><span class="sxs-lookup"><span data-stu-id="64aee-129">**stubDeclarations**</span></span>](stubdeclarations.md)<br/>                                                 | <span data-ttu-id="64aee-130">Genera declaraciones para las funciones de código auxiliar para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="64aee-130">Generates declarations for stub functions for port type operations.</span></span><br/> <br/>                                                    |
| [<span data-ttu-id="64aee-131">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="64aee-131">**stubDefinitions**</span></span>](stubdefinitions.md)<br/>                                                   | <span data-ttu-id="64aee-132">Genera implementaciones para las funciones de código auxiliar para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="64aee-132">Generates implementations for stub functions for port type operations.</span></span><br/> <br/>                                                 |
| [<span data-ttu-id="64aee-133">**subscriptionFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="64aee-133">**subscriptionFunctionDeclarations**</span></span>](subscriptionfunctiondeclarations.md)<br/>                 | <span data-ttu-id="64aee-134">Genera declaraciones de implementación para las funciones de proxy de suscripción o cancelación de suscripción para las operaciones de notificación de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="64aee-134">Generates implementation declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/> |
| [<span data-ttu-id="64aee-135">**subscriptionIdlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="64aee-135">**subscriptionIdlFunctionDeclarations**</span></span>](subscriptionidlfunctiondeclarations.md)<br/>           | <span data-ttu-id="64aee-136">Genera declaraciones IDL para las funciones de proxy de suscripción o cancelación de suscripción para las operaciones de notificación de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="64aee-136">Generates IDL declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="64aee-137">**subscriptionProxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="64aee-137">**subscriptionProxyFunctionImplementations**</span></span>](subscriptionproxyfunctionimplementations.md)<br/> | <span data-ttu-id="64aee-138">Genera implementaciones para las funciones de proxy de suscripción o cancelación de suscripción para las operaciones de notificación de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="64aee-138">Generates implementations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/>             |



## <a name="remarks"></a><span data-ttu-id="64aee-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="64aee-139">Remarks</span></span>

<span data-ttu-id="64aee-140">Se puede especificar cualquier número de operaciones.</span><span class="sxs-lookup"><span data-stu-id="64aee-140">Any number of operations may be specified.</span></span> <span data-ttu-id="64aee-141">Si no se especifica ninguna operación, se genera código para todas las operaciones en todos los tipos de puerto pertinentes.</span><span class="sxs-lookup"><span data-stu-id="64aee-141">If no operations are specified, code is generated for all operations in all the relevant port types.</span></span> <span data-ttu-id="64aee-142">El uso **del elemento** operation limitará los métodos generados a los contenidos en la operación.</span><span class="sxs-lookup"><span data-stu-id="64aee-142">Using the **operation** element will limit the methods generated to those contained in the operation.</span></span>

<span data-ttu-id="64aee-143">Por ejemplo, una impresora admite estas operaciones, entre otras:</span><span class="sxs-lookup"><span data-stu-id="64aee-143">For example, a printer supports these operations among others:</span></span>

-   <span data-ttu-id="64aee-144">**PrintJobByPost**</span><span class="sxs-lookup"><span data-stu-id="64aee-144">**PrintJobByPost**</span></span>
-   <span data-ttu-id="64aee-145">**PrintJobByReference**</span><span class="sxs-lookup"><span data-stu-id="64aee-145">**PrintJobByReference**</span></span>
-   <span data-ttu-id="64aee-146">**CancelJob**</span><span class="sxs-lookup"><span data-stu-id="64aee-146">**CancelJob**</span></span>
-   <span data-ttu-id="64aee-147">**GetJobElements**</span><span class="sxs-lookup"><span data-stu-id="64aee-147">**GetJobElements**</span></span>
-   <span data-ttu-id="64aee-148">**GetActiveJobs**</span><span class="sxs-lookup"><span data-stu-id="64aee-148">**GetActiveJobs**</span></span>
-   <span data-ttu-id="64aee-149">**GetJobHistory**</span><span class="sxs-lookup"><span data-stu-id="64aee-149">**GetJobHistory**</span></span>
-   <span data-ttu-id="64aee-150">**SubscribeToPrinterConfigChange**</span><span class="sxs-lookup"><span data-stu-id="64aee-150">**SubscribeToPrinterConfigChange**</span></span>
-   <span data-ttu-id="64aee-151">**UnsubscribeToPrinterConfigChange**</span><span class="sxs-lookup"><span data-stu-id="64aee-151">**UnsubscribeToPrinterConfigChange**</span></span>

<span data-ttu-id="64aee-152">Sin embargo, para incluir solo los métodos relacionados con las operaciones **PrintJobByPost** y **GetJobElements,** el script de generación de código usaría los elementos [**idlFunctionDeclarations**](idlfunctiondeclarations.md) como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="64aee-152">However, to include only the methods related to the **PrintJobByPost** and **GetJobElements** operations, the code generation script would use the [**idlFunctionDeclarations**](idlfunctiondeclarations.md) elements as follows:</span></span>

``` syntax
<idlFunctionDeclarations>
    <operation>PrintJobByPost</operation>
    <operation>GetJobElements></operation>
</idlFunctionDeclarations>
```

<span data-ttu-id="64aee-153">Esto genera declaraciones de función idl para todos los métodos asociados a las dos operaciones (por ejemplo, **BeginPrintJobByPost,** **EndPrintJobByPost,** **BeginGetJobElements** y **EndGetJobElements).**</span><span class="sxs-lookup"><span data-stu-id="64aee-153">This generates idl function declarations for all methods associated with the two operations (for example, **BeginPrintJobByPost**, **EndPrintJobByPost**, **BeginGetJobElements** and **EndGetJobElements**).</span></span>

## <a name="element-information"></a><span data-ttu-id="64aee-154">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="64aee-154">Element information</span></span>



| <span data-ttu-id="64aee-155">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="64aee-155">Label</span></span> | <span data-ttu-id="64aee-156">Value</span><span class="sxs-lookup"><span data-stu-id="64aee-156">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="64aee-157">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64aee-157">Minimum supported system</span></span><br/> | <span data-ttu-id="64aee-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="64aee-158">Windows Vista</span></span> |
| <span data-ttu-id="64aee-159">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="64aee-159">Can be empty</span></span>                        | <span data-ttu-id="64aee-160">Sí</span><span class="sxs-lookup"><span data-stu-id="64aee-160">Yes</span></span>           |



 

 




