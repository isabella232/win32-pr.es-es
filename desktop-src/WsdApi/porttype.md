---
description: Especifica el tipo de puerto para el que se va a generar el código.
ms.assetid: 8a7762ae-2e39-46e1-b49f-09cae1af9b0d
title: elemento portType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a98f02fc5a18e330bb5617b52563adc79a039831
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996542"
---
# <a name="porttype-element"></a><span data-ttu-id="b023b-103">elemento portType</span><span class="sxs-lookup"><span data-stu-id="b023b-103">portType element</span></span>

<span data-ttu-id="b023b-104">Especifica el tipo de puerto para el que se va a generar el código.</span><span class="sxs-lookup"><span data-stu-id="b023b-104">Specifies the port type for which code is to be generated.</span></span>

## <a name="usage"></a><span data-ttu-id="b023b-105">Uso</span><span class="sxs-lookup"><span data-stu-id="b023b-105">Usage</span></span>

``` syntax
<portType/>
```

## <a name="attributes"></a><span data-ttu-id="b023b-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="b023b-106">Attributes</span></span>

<span data-ttu-id="b023b-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="b023b-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="b023b-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b023b-108">Child elements</span></span>

<span data-ttu-id="b023b-109">No hay elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="b023b-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="b023b-110">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="b023b-110">Parent elements</span></span>



| <span data-ttu-id="b023b-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="b023b-111">Element</span></span>                                                                                                 | <span data-ttu-id="b023b-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="b023b-112">Description</span></span>                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b023b-113">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="b023b-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                                         | <span data-ttu-id="b023b-114">Genera declaraciones de implementación para las funciones de proxy para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="b023b-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/>                                    |
| [<span data-ttu-id="b023b-115">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="b023b-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>                                   | <span data-ttu-id="b023b-116">Genera declaraciones IDL para las funciones de proxy para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="b023b-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>                                               |
| [<span data-ttu-id="b023b-117">**messageStructureDefinitions**</span><span class="sxs-lookup"><span data-stu-id="b023b-117">**messageStructureDefinitions**</span></span>](messagestructuredefinitions.md)<br/>                           | <span data-ttu-id="b023b-118">Genera definiciones de estructura de C para tipos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="b023b-118">Generates C structure definitions for message types.</span></span><br/> <br/>                                                                   |
| [<span data-ttu-id="b023b-119">**messageTypeDeclarations**</span><span class="sxs-lookup"><span data-stu-id="b023b-119">**messageTypeDeclarations**</span></span>](messagetypedeclarations.md)<br/>                                   | <span data-ttu-id="b023b-120">Genera declaraciones constantes de C para tablas de esquema XML para tipos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="b023b-120">Generates C constant declarations for XML schema tables for message types.</span></span><br/> <br/>                                             |
| [<span data-ttu-id="b023b-121">**messageTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="b023b-121">**messageTypeDefinitions**</span></span>](messagetypedefinitions.md)<br/>                                     | <span data-ttu-id="b023b-122">Genera constantes de C para tablas de esquema XML para tipos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="b023b-122">Generates C constants for XML schema tables for message types.</span></span><br/> <br/>                                                         |
| [<span data-ttu-id="b023b-123">**portTypeDeclarations**</span><span class="sxs-lookup"><span data-stu-id="b023b-123">**portTypeDeclarations**</span></span>](porttypedeclarations.md)<br/>                                         | <span data-ttu-id="b023b-124">Genera declaraciones constantes de C para tipos de puerto.</span><span class="sxs-lookup"><span data-stu-id="b023b-124">Generates C constant declarations for port types.</span></span><br/> <br/>                                                                      |
| [<span data-ttu-id="b023b-125">**portTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="b023b-125">**portTypeDefinitions**</span></span>](porttypedefinitions.md)<br/>                                           | <span data-ttu-id="b023b-126">Genera constantes de C para los tipos de puerto.</span><span class="sxs-lookup"><span data-stu-id="b023b-126">Generates C constants for port types.</span></span><br/> <br/>                                                                                  |
| [<span data-ttu-id="b023b-127">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="b023b-127">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/>                         | <span data-ttu-id="b023b-128">Genera implementaciones para las funciones de proxy para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="b023b-128">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>                                                |
| [<span data-ttu-id="b023b-129">**stubDeclarations**</span><span class="sxs-lookup"><span data-stu-id="b023b-129">**stubDeclarations**</span></span>](stubdeclarations.md)<br/>                                                 | <span data-ttu-id="b023b-130">Genera declaraciones para las funciones de código auxiliar para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="b023b-130">Generates declarations for stub functions for port type operations.</span></span><br/> <br/>                                                    |
| [<span data-ttu-id="b023b-131">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="b023b-131">**stubDefinitions**</span></span>](stubdefinitions.md)<br/>                                                   | <span data-ttu-id="b023b-132">Genera implementaciones para las funciones de código auxiliar para las operaciones de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="b023b-132">Generates implementations for stub functions for port type operations.</span></span><br/> <br/>                                                 |
| [<span data-ttu-id="b023b-133">**subscriptionFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="b023b-133">**subscriptionFunctionDeclarations**</span></span>](subscriptionfunctiondeclarations.md)<br/>                 | <span data-ttu-id="b023b-134">Genera declaraciones de implementación para las funciones de proxy de suscripción o cancelación de suscripción para las operaciones de notificación de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="b023b-134">Generates implementation declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/> |
| [<span data-ttu-id="b023b-135">**subscriptionIdlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="b023b-135">**subscriptionIdlFunctionDeclarations**</span></span>](subscriptionidlfunctiondeclarations.md)<br/>           | <span data-ttu-id="b023b-136">Genera declaraciones IDL para las funciones de proxy de suscripción o cancelación de suscripción para las operaciones de notificación de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="b023b-136">Generates IDL declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="b023b-137">**subscriptionProxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="b023b-137">**subscriptionProxyFunctionImplementations**</span></span>](subscriptionproxyfunctionimplementations.md)<br/> | <span data-ttu-id="b023b-138">Genera implementaciones para las funciones de proxy de suscripción o cancelación de suscripción para las operaciones de notificación de tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="b023b-138">Generates implementations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/>             |



## <a name="remarks"></a><span data-ttu-id="b023b-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b023b-139">Remarks</span></span>

<span data-ttu-id="b023b-140">De forma predeterminada, se genera código para todos los tipos de puerto en los archivos de entrada WSDL.</span><span class="sxs-lookup"><span data-stu-id="b023b-140">By default, code is generated for all port types in WSDL input files.</span></span>

## <a name="element-information"></a><span data-ttu-id="b023b-141">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="b023b-141">Element information</span></span>



| <span data-ttu-id="b023b-142">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="b023b-142">Label</span></span> | <span data-ttu-id="b023b-143">Value</span><span class="sxs-lookup"><span data-stu-id="b023b-143">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="b023b-144">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b023b-144">Minimum supported system</span></span><br/> | <span data-ttu-id="b023b-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b023b-145">Windows Vista</span></span> |
| <span data-ttu-id="b023b-146">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b023b-146">Can be empty</span></span>                        | <span data-ttu-id="b023b-147">Sí</span><span class="sxs-lookup"><span data-stu-id="b023b-147">Yes</span></span>           |



 

 




