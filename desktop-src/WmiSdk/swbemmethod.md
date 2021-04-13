---
description: Puede utilizar las propiedades del objeto SWbemMethod para inspeccionar una definición de un solo método de un objeto WMI. Este objeto no se puede crear mediante la llamada CreateObject de VBScript.
ms.assetid: 461d5c41-4930-40cf-96e2-bc8cae335b60
ms.tgt_platform: multiple
title: Objeto SWbemMethod (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethod
- ISWbemMethod
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 055957bf2774fc1e5c2e1f0149b00ece7b0a1bea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544675"
---
# <a name="swbemmethod-object"></a><span data-ttu-id="42ce2-104">Objeto SWbemMethod</span><span class="sxs-lookup"><span data-stu-id="42ce2-104">SWbemMethod object</span></span>

<span data-ttu-id="42ce2-105">Puede utilizar las propiedades del objeto **SWbemMethod** para inspeccionar una definición de un solo método de un objeto WMI.</span><span class="sxs-lookup"><span data-stu-id="42ce2-105">You can use the properties of the **SWbemMethod** object to inspect a single method definition of a WMI object.</span></span> <span data-ttu-id="42ce2-106">Este objeto no se puede crear mediante la llamada **CreateObject** de VBScript.</span><span class="sxs-lookup"><span data-stu-id="42ce2-106">This object cannot be created by the VBScript **CreateObject** call.</span></span>

<span data-ttu-id="42ce2-107">Este objeto se puede utilizar para inspeccionar las definiciones de los métodos.</span><span class="sxs-lookup"><span data-stu-id="42ce2-107">This object can be used to inspect the definitions of methods.</span></span> <span data-ttu-id="42ce2-108">Para invocar los métodos, debe usar el acceso directo (vea [manipular la información de clase e instancia](manipulating-class-and-instance-information.md)) en un objeto [**SWbemObject**](swbemobject.md) (que es el mecanismo recomendado) o la llamada a [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) .</span><span class="sxs-lookup"><span data-stu-id="42ce2-108">To invoke the methods, you should use either direct access (see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md)) on an [**SWbemObject**](swbemobject.md) (which is the recommended mechanism) object, or the [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) call.</span></span>

> [!Note]  
> <span data-ttu-id="42ce2-109">En esta versión de la API, no se admite el acceso de escritura a la información del método.</span><span class="sxs-lookup"><span data-stu-id="42ce2-109">In this version of the API, write access to method information is not supported.</span></span> <span data-ttu-id="42ce2-110">Si desea definir métodos o modificar las definiciones de método existentes, puede definir los cambios del método en un archivo MOF y enviar los cambios mediante el [compilador MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="42ce2-110">If you want to define methods or modify existing method definitions, you can define the method changes in a MOF file and submit the changes using the [MOF Compiler](compiling-mof-files.md).</span></span> <span data-ttu-id="42ce2-111">También puede usar la [API com para WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="42ce2-111">Alternatively, use the [COM API for WMI](com-api-for-wmi.md).</span></span>

 

## <a name="members"></a><span data-ttu-id="42ce2-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="42ce2-112">Members</span></span>

<span data-ttu-id="42ce2-113">El objeto **SWbemMethod** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="42ce2-113">The **SWbemMethod** object has these types of members:</span></span>

-   [<span data-ttu-id="42ce2-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="42ce2-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="42ce2-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="42ce2-115">Properties</span></span>

<span data-ttu-id="42ce2-116">El objeto **SWbemMethod** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="42ce2-116">The **SWbemMethod** object has these properties.</span></span>



| <span data-ttu-id="42ce2-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="42ce2-117">Property</span></span>                                                      | <span data-ttu-id="42ce2-118">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="42ce2-118">Access type</span></span>          | <span data-ttu-id="42ce2-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="42ce2-119">Description</span></span>                                                                                                                        |
|:--------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="42ce2-120">**Parameters**</span><span class="sxs-lookup"><span data-stu-id="42ce2-120">**InParameters**</span></span>](swbemmethod-inparameters.md)<br/>   | <span data-ttu-id="42ce2-121">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="42ce2-121">Read-only</span></span><br/> | <span data-ttu-id="42ce2-122">Objeto [**SWbemObject**](swbemobject.md) cuyas propiedades definen los parámetros de entrada para este método.</span><span class="sxs-lookup"><span data-stu-id="42ce2-122">An [**SWbemObject**](swbemobject.md) object whose properties define the input parameters for this method.</span></span><br/>              |
| [<span data-ttu-id="42ce2-123">**Name**</span><span class="sxs-lookup"><span data-stu-id="42ce2-123">**Name**</span></span>](swbemmethod-name.md)<br/>                   | <span data-ttu-id="42ce2-124">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="42ce2-124">Read-only</span></span><br/> | <span data-ttu-id="42ce2-125">Nombre del método.</span><span class="sxs-lookup"><span data-stu-id="42ce2-125">Name of the method.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="42ce2-126">**Origen**</span><span class="sxs-lookup"><span data-stu-id="42ce2-126">**Origin**</span></span>](swbemmethod-origin.md)<br/>               | <span data-ttu-id="42ce2-127">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="42ce2-127">Read-only</span></span><br/> | <span data-ttu-id="42ce2-128">Clase de origen del método.</span><span class="sxs-lookup"><span data-stu-id="42ce2-128">Originating class of the method.</span></span><br/>                                                                                        |
| [<span data-ttu-id="42ce2-129">**Parameters**</span><span class="sxs-lookup"><span data-stu-id="42ce2-129">**OutParameters**</span></span>](swbemmethod-outparameters.md)<br/> | <span data-ttu-id="42ce2-130">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="42ce2-130">Read-only</span></span><br/> | <span data-ttu-id="42ce2-131">Objeto [**SWbemObject**](swbemobject.md) cuyas propiedades definen los parámetros out y el tipo de valor devuelto de este método.</span><span class="sxs-lookup"><span data-stu-id="42ce2-131">An [**SWbemObject**](swbemobject.md) object whose properties define the out parameters and return type of this method.</span></span><br/> |
| [<span data-ttu-id="42ce2-132">**Calificadores\_**</span><span class="sxs-lookup"><span data-stu-id="42ce2-132">**Qualifiers\_**</span></span>](swbemmethod-qualifiers-.md)<br/>    | <span data-ttu-id="42ce2-133">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="42ce2-133">Read-only</span></span><br/> | <span data-ttu-id="42ce2-134">Un objeto [**SWbemQualifierSet**](swbemqualifierset.md) que contiene los calificadores de este método.</span><span class="sxs-lookup"><span data-stu-id="42ce2-134">An [**SWbemQualifierSet**](swbemqualifierset.md) object that contains the qualifiers for this method.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="42ce2-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42ce2-135">Requirements</span></span>



| <span data-ttu-id="42ce2-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="42ce2-136">Requirement</span></span> | <span data-ttu-id="42ce2-137">Value</span><span class="sxs-lookup"><span data-stu-id="42ce2-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="42ce2-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42ce2-138">Minimum supported client</span></span><br/> | <span data-ttu-id="42ce2-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="42ce2-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="42ce2-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42ce2-140">Minimum supported server</span></span><br/> | <span data-ttu-id="42ce2-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="42ce2-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="42ce2-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="42ce2-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="42ce2-143"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="42ce2-143"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="42ce2-144">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="42ce2-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="42ce2-145"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="42ce2-145"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="42ce2-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="42ce2-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42ce2-147"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42ce2-147"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="42ce2-148">CLSID</span><span class="sxs-lookup"><span data-stu-id="42ce2-148">CLSID</span></span><br/>                    | <span data-ttu-id="42ce2-149">CLSID \_ SWbemMethod</span><span class="sxs-lookup"><span data-stu-id="42ce2-149">CLSID\_SWbemMethod</span></span><br/>                                                           |
| <span data-ttu-id="42ce2-150">IID</span><span class="sxs-lookup"><span data-stu-id="42ce2-150">IID</span></span><br/>                      | <span data-ttu-id="42ce2-151">\_ISWBEMMETHOD IID</span><span class="sxs-lookup"><span data-stu-id="42ce2-151">IID\_ISWbemMethod</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="42ce2-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="42ce2-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42ce2-153">Scripting de objetos de API</span><span class="sxs-lookup"><span data-stu-id="42ce2-153">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




