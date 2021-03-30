---
description: Describe las convenciones de documentos para leer los temas de la API de scripting de WMI.
ms.assetid: 889e6322-96f6-4a24-a084-e3b7bfa94a40
ms.tgt_platform: multiple
title: Convenciones de documentos para la API de scripting
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 33335982672472fa9924a6e250305a3630628b21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360947"
---
# <a name="document-conventions-for-the-scripting-api"></a><span data-ttu-id="ed2c7-103">Convenciones de documentos para la API de scripting</span><span class="sxs-lookup"><span data-stu-id="ed2c7-103">Document Conventions for the Scripting API</span></span>

<span data-ttu-id="ed2c7-104">La referencia [de la API de scripting para WMI](scripting-api-for-wmi.md) utiliza las siguientes convenciones de documento:</span><span class="sxs-lookup"><span data-stu-id="ed2c7-104">The [Scripting API for WMI](scripting-api-for-wmi.md) reference uses the following document conventions:</span></span>

-   <span data-ttu-id="ed2c7-105">Los tipos de parámetro se definen mediante un prefijo: b (booleano), STR (cadena), I (entero), OBJ (objeto de automatización), var (variante).</span><span class="sxs-lookup"><span data-stu-id="ed2c7-105">Parameter types are defined using a prefix: b (Boolean), str (string), I (integer), obj (Automation object), var (Variant).</span></span>
-   <span data-ttu-id="ed2c7-106">Los parámetros opcionales se colocan entre corchetes con sus valores predeterminados que se muestran por asignación.</span><span class="sxs-lookup"><span data-stu-id="ed2c7-106">Optional parameters are placed in square brackets with their default values shown by assignment.</span></span>
-   <span data-ttu-id="ed2c7-107">En el caso de los parámetros de objeto, los caracteres situados después del prefijo "obj" indican el tipo de objeto esperado.</span><span class="sxs-lookup"><span data-stu-id="ed2c7-107">In the case of object parameters, the characters after the "obj" prefix indicate the type of object expected.</span></span>



| <span data-ttu-id="ed2c7-108">Parámetro de objeto</span><span class="sxs-lookup"><span data-stu-id="ed2c7-108">Object parameter</span></span>      | <span data-ttu-id="ed2c7-109">Tipo de objeto</span><span class="sxs-lookup"><span data-stu-id="ed2c7-109">Object type</span></span>                                          |
|-----------------------|------------------------------------------------------|
| <span data-ttu-id="ed2c7-110">*WbemDatetime*</span><span class="sxs-lookup"><span data-stu-id="ed2c7-110">*WbemDatetime*</span></span>        | [<span data-ttu-id="ed2c7-111">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="ed2c7-111">**SWbemDateTime**</span></span>](swbemdatetime.md)               |
| <span data-ttu-id="ed2c7-112">*WbemEventSource*</span><span class="sxs-lookup"><span data-stu-id="ed2c7-112">*WbemEventSource*</span></span>     | [<span data-ttu-id="ed2c7-113">**SWbemEventSource**</span><span class="sxs-lookup"><span data-stu-id="ed2c7-113">**SWbemEventSource**</span></span>](swbemeventsource.md)         |
| <span data-ttu-id="ed2c7-114">*WbemLocator*</span><span class="sxs-lookup"><span data-stu-id="ed2c7-114">*WbemLocator*</span></span>         | [<span data-ttu-id="ed2c7-115">**SWbemLocator**</span><span class="sxs-lookup"><span data-stu-id="ed2c7-115">**SWbemLocator**</span></span>](swbemlocator.md)                 |
| <span data-ttu-id="ed2c7-116">*WbemMethod*</span><span class="sxs-lookup"><span data-stu-id="ed2c7-116">*WbemMethod*</span></span>          | [<span data-ttu-id="ed2c7-117">**SWbemMethod**</span><span class="sxs-lookup"><span data-stu-id="ed2c7-117">**SWbemMethod**</span></span>](swbemmethod.md)                   |
| <span data-ttu-id="ed2c7-118">*WbemMethodSet*</span><span class="sxs-lookup"><span data-stu-id="ed2c7-118">*WbemMethodSet*</span></span>       | [<span data-ttu-id="ed2c7-119">**SWbemMethodSet**</span><span class="sxs-lookup"><span data-stu-id="ed2c7-119">**SWbemMethodSet**</span></span>](swbemmethodset.md)             |
| <span data-ttu-id="ed2c7-120">*WbemNamedValueSet*</span><span class="sxs-lookup"><span data-stu-id="ed2c7-120">*WbemNamedValueSet*</span></span>   | [<span data-ttu-id="ed2c7-121">**SWbemNamedValueSet**</span><span class="sxs-lookup"><span data-stu-id="ed2c7-121">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md)     |
| <span data-ttu-id="ed2c7-122">*WbemObject*</span><span class="sxs-lookup"><span data-stu-id="ed2c7-122">*WbemObject*</span></span>          | [<span data-ttu-id="ed2c7-123">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="ed2c7-123">**SWbemObject**</span></span>](swbemobject.md)                   |
| <span data-ttu-id="ed2c7-124">*WbemObjectEx*</span><span class="sxs-lookup"><span data-stu-id="ed2c7-124">*WbemObjectEx*</span></span>        | [<span data-ttu-id="ed2c7-125">**SWbemObjectEx**</span><span class="sxs-lookup"><span data-stu-id="ed2c7-125">**SWbemObjectEx**</span></span>](swbemobjectex.md)               |
| <span data-ttu-id="ed2c7-126">*WbemObjectPath*</span><span class="sxs-lookup"><span data-stu-id="ed2c7-126">*WbemObjectPath*</span></span>      | [<span data-ttu-id="ed2c7-127">**SWbemObjectPath**</span><span class="sxs-lookup"><span data-stu-id="ed2c7-127">**SWbemObjectPath**</span></span>](swbemobjectpath.md)           |
| <span data-ttu-id="ed2c7-128">*WbemObjectSet*</span><span class="sxs-lookup"><span data-stu-id="ed2c7-128">*WbemObjectSet*</span></span>       | [<span data-ttu-id="ed2c7-129">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="ed2c7-129">**SWbemObjectSet**</span></span>](swbemobjectset.md)             |
| <span data-ttu-id="ed2c7-130">*WbemPrivilege*</span><span class="sxs-lookup"><span data-stu-id="ed2c7-130">*WbemPrivilege*</span></span>       | [<span data-ttu-id="ed2c7-131">**SWbemPrivilege**</span><span class="sxs-lookup"><span data-stu-id="ed2c7-131">**SWbemPrivilege**</span></span>](swbemprivilege.md)             |
| <span data-ttu-id="ed2c7-132">*WbemPrivilegeSet*</span><span class="sxs-lookup"><span data-stu-id="ed2c7-132">*WbemPrivilegeSet*</span></span>    | [<span data-ttu-id="ed2c7-133">**SWbemPrivilegeSet**</span><span class="sxs-lookup"><span data-stu-id="ed2c7-133">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)       |
| <span data-ttu-id="ed2c7-134">*WbemProperty*</span><span class="sxs-lookup"><span data-stu-id="ed2c7-134">*WbemProperty*</span></span>        | [<span data-ttu-id="ed2c7-135">**SWbemProperty**</span><span class="sxs-lookup"><span data-stu-id="ed2c7-135">**SWbemProperty**</span></span>](swbemproperty.md)               |
| <span data-ttu-id="ed2c7-136">*WbemPropertySet*</span><span class="sxs-lookup"><span data-stu-id="ed2c7-136">*WbemPropertySet*</span></span>     | [<span data-ttu-id="ed2c7-137">**SWbemPropertySet**</span><span class="sxs-lookup"><span data-stu-id="ed2c7-137">**SWbemPropertySet**</span></span>](swbempropertyset.md)         |
| <span data-ttu-id="ed2c7-138">*WbemQualifier*</span><span class="sxs-lookup"><span data-stu-id="ed2c7-138">*WbemQualifier*</span></span>       | [<span data-ttu-id="ed2c7-139">**SWbemQualifier**</span><span class="sxs-lookup"><span data-stu-id="ed2c7-139">**SWbemQualifier**</span></span>](swbemqualifier.md)             |
| <span data-ttu-id="ed2c7-140">*WbemQualifierSet*</span><span class="sxs-lookup"><span data-stu-id="ed2c7-140">*WbemQualifierSet*</span></span>    | [<span data-ttu-id="ed2c7-141">**SWbemQualifierSet**</span><span class="sxs-lookup"><span data-stu-id="ed2c7-141">**SWbemQualifierSet**</span></span>](swbemqualifierset.md)       |
| <span data-ttu-id="ed2c7-142">*WbemRefreshableItem*</span><span class="sxs-lookup"><span data-stu-id="ed2c7-142">*WbemRefreshableItem*</span></span> | [<span data-ttu-id="ed2c7-143">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="ed2c7-143">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md) |
| <span data-ttu-id="ed2c7-144">*WbemRefresher*</span><span class="sxs-lookup"><span data-stu-id="ed2c7-144">*WbemRefresher*</span></span>       | [<span data-ttu-id="ed2c7-145">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="ed2c7-145">**SWbemRefresher**</span></span>](swbemrefresher.md)             |
| <span data-ttu-id="ed2c7-146">*WbemServices*</span><span class="sxs-lookup"><span data-stu-id="ed2c7-146">*WbemServices*</span></span>        | [<span data-ttu-id="ed2c7-147">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="ed2c7-147">**SWbemServices**</span></span>](swbemservices.md)               |
| <span data-ttu-id="ed2c7-148">*WbemServicesEx*</span><span class="sxs-lookup"><span data-stu-id="ed2c7-148">*WbemServicesEx*</span></span>      | [<span data-ttu-id="ed2c7-149">**SWbemServicesEx**</span><span class="sxs-lookup"><span data-stu-id="ed2c7-149">**SWbemServicesEx**</span></span>](swbemservicesex.md)           |



 

<span data-ttu-id="ed2c7-150">Por ejemplo, el código siguiente muestra cómo asignar un nombre a las variables para distintos tipos de objetos:</span><span class="sxs-lookup"><span data-stu-id="ed2c7-150">For example, the following code shows how to name variables for different types of objects:</span></span>


```VB
strComputerName  ' a string value for a computer name
bStatusFlag  ' a boolean value used for a status
objServices  ' an object value used to store an SWbemServices value
```



 

 



