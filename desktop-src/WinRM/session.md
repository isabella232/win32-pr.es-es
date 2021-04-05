---
title: Objeto de sesión (WSManDisp. h)
description: Define las operaciones y la configuración de la sesión.
ms.assetid: b98ca759-71cb-492e-8645-8766b202eb36
ms.tgt_platform: multiple
keywords:
- Administración remota de Windows de objeto de sesión
- Administración remota de Windows de objeto de sesión, descrito
topic_type:
- apiref
api_name:
- Session
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2e47658ad8a89af5adb2135b86cc2ad9b6ef438
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997144"
---
# <a name="session-object-wsmandisph"></a><span data-ttu-id="55df5-105">Objeto de sesión (WSManDisp. h)</span><span class="sxs-lookup"><span data-stu-id="55df5-105">Session object (WSManDisp.h)</span></span>

<span data-ttu-id="55df5-106">Define las operaciones y la configuración de la sesión.</span><span class="sxs-lookup"><span data-stu-id="55df5-106">Defines operations and session settings.</span></span> <span data-ttu-id="55df5-107">Cualquier operación de Administración remota de Windows requiere la creación de una **sesión** que se conecta a un equipo remoto, un [*controlador de administración de base*](windows-remote-management-glossary.md) (BMC) o el equipo local.</span><span class="sxs-lookup"><span data-stu-id="55df5-107">Any Windows Remote Management operations require creation of a **Session** that connects to a remote computer, [*base management controller*](windows-remote-management-glossary.md) (BMC), or the local computer.</span></span> <span data-ttu-id="55df5-108">Las operaciones de red de WinRM incluyen la obtención, escritura o enumeración de datos, o la invocación de métodos.</span><span class="sxs-lookup"><span data-stu-id="55df5-108">WinRM network operations include getting, writing, or enumerating data, or invoking methods.</span></span> <span data-ttu-id="55df5-109">Los métodos del objeto de **sesión** reflejan las operaciones básicas definidas en el protocolo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="55df5-109">The methods of the **Session** object mirror the basic operations defined in the WS-Management protocol.</span></span>

## <a name="members"></a><span data-ttu-id="55df5-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="55df5-110">Members</span></span>

<span data-ttu-id="55df5-111">El objeto de **sesión** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="55df5-111">The **Session** object has these types of members:</span></span>

-   [<span data-ttu-id="55df5-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="55df5-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="55df5-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="55df5-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="55df5-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="55df5-114">Methods</span></span>

<span data-ttu-id="55df5-115">El objeto de **sesión** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="55df5-115">The **Session** object has these methods.</span></span>



| <span data-ttu-id="55df5-116">Método</span><span class="sxs-lookup"><span data-stu-id="55df5-116">Method</span></span>                                 | <span data-ttu-id="55df5-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="55df5-117">Description</span></span>                                                                                                                 |
|:---------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="55df5-118">**A**</span><span class="sxs-lookup"><span data-stu-id="55df5-118">**Create**</span></span>](session-create.md)       | <span data-ttu-id="55df5-119">Crea una nueva instancia de un recurso y devuelve el URI del nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="55df5-119">Creates a new instance of a resource and returns the URI of the new object.</span></span><br/>                                      |
| [<span data-ttu-id="55df5-120">**Elimínelos**</span><span class="sxs-lookup"><span data-stu-id="55df5-120">**Delete**</span></span>](session-delete.md)       | <span data-ttu-id="55df5-121">Elimina el recurso especificado en el URI del recurso.</span><span class="sxs-lookup"><span data-stu-id="55df5-121">Deletes the resource specified in the resource URI.</span></span><br/>                                                              |
| [<span data-ttu-id="55df5-122">**Enumerar**</span><span class="sxs-lookup"><span data-stu-id="55df5-122">**Enumerate**</span></span>](session-enumerate.md) | <span data-ttu-id="55df5-123">Enumera una colección, una tabla o un recurso de registro de mensajes.</span><span class="sxs-lookup"><span data-stu-id="55df5-123">Enumerates a collection, table, or message log resource.</span></span><br/>                                                         |
| [<span data-ttu-id="55df5-124">**Obtener**</span><span class="sxs-lookup"><span data-stu-id="55df5-124">**Get**</span></span>](session-get.md)             | <span data-ttu-id="55df5-125">Recupera un recurso del servicio y devuelve una representación XML de la instancia actual del recurso.</span><span class="sxs-lookup"><span data-stu-id="55df5-125">Retrieves a resource from the service and returns an XML representation of the current instance of the resource.</span></span><br/> |
| [<span data-ttu-id="55df5-126">**Identificar**</span><span class="sxs-lookup"><span data-stu-id="55df5-126">**Identify**</span></span>](session-identify.md)   | <span data-ttu-id="55df5-127">Consulta un equipo remoto para determinar si es compatible con el protocolo de WS-Management</span><span class="sxs-lookup"><span data-stu-id="55df5-127">Queries a remote computer to determine if it supports the WS-Management protocol</span></span><br/>                                 |
| [<span data-ttu-id="55df5-128">**Invocar**</span><span class="sxs-lookup"><span data-stu-id="55df5-128">**Invoke**</span></span>](session-invoke.md)       | <span data-ttu-id="55df5-129">Invoca un método que devuelve los resultados de la llamada al método.</span><span class="sxs-lookup"><span data-stu-id="55df5-129">Invokes a method that returns the results of the method call.</span></span><br/>                                                    |
| [<span data-ttu-id="55df5-130">**Pondrán**</span><span class="sxs-lookup"><span data-stu-id="55df5-130">**Put**</span></span>](session-put.md)             | <span data-ttu-id="55df5-131">Actualiza un recurso.</span><span class="sxs-lookup"><span data-stu-id="55df5-131">Updates a resource.</span></span><br/>                                                                                              |



 

### <a name="properties"></a><span data-ttu-id="55df5-132">Propiedades</span><span class="sxs-lookup"><span data-stu-id="55df5-132">Properties</span></span>

<span data-ttu-id="55df5-133">El objeto de **sesión** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="55df5-133">The **Session** object has these properties.</span></span>



| <span data-ttu-id="55df5-134">Propiedad</span><span class="sxs-lookup"><span data-stu-id="55df5-134">Property</span></span>                                            | <span data-ttu-id="55df5-135">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="55df5-135">Access type</span></span>           | <span data-ttu-id="55df5-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="55df5-136">Description</span></span>                                                                                                                                                                                                                 |
|:----------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="55df5-137">**BatchItems**</span><span class="sxs-lookup"><span data-stu-id="55df5-137">**BatchItems**</span></span>](session-batchitems.md)<br/> | <span data-ttu-id="55df5-138">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="55df5-138">Read/write</span></span><br/> | <span data-ttu-id="55df5-139">Establece y obtiene el número de elementos de cada lote de enumeración.</span><span class="sxs-lookup"><span data-stu-id="55df5-139">Sets and gets the number of items in each enumeration batch.</span></span> <span data-ttu-id="55df5-140">Este valor no se puede cambiar durante una enumeración.</span><span class="sxs-lookup"><span data-stu-id="55df5-140">This value cannot be changed during an enumeration.</span></span> <span data-ttu-id="55df5-141">De forma predeterminada, el valor predeterminado es un número ilimitado de elementos.</span><span class="sxs-lookup"><span data-stu-id="55df5-141">By default, the default is an unlimited number of items.</span></span> <span data-ttu-id="55df5-142">El proveedor de recursos puede establecer un límite.</span><span class="sxs-lookup"><span data-stu-id="55df5-142">The resource provider may set a limit.</span></span><br/> |
| [<span data-ttu-id="55df5-143">**Error**</span><span class="sxs-lookup"><span data-stu-id="55df5-143">**Error**</span></span>](session-error.md)<br/>           | <span data-ttu-id="55df5-144">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="55df5-144">Read-only</span></span><br/>  | <span data-ttu-id="55df5-145">Obtiene información de error adicional en una secuencia XML.</span><span class="sxs-lookup"><span data-stu-id="55df5-145">Gets additional error information in an XML stream.</span></span><br/>                                                                                                                                                              |
| [<span data-ttu-id="55df5-146">**Tiempo de espera**</span><span class="sxs-lookup"><span data-stu-id="55df5-146">**Timeout**</span></span>](session-timeout.md)<br/>       | <span data-ttu-id="55df5-147">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="55df5-147">Read/write</span></span><br/> | <span data-ttu-id="55df5-148">Establece y obtiene el tiempo máximo (en milisegundos) que la aplicación cliente debe esperar.</span><span class="sxs-lookup"><span data-stu-id="55df5-148">Sets and gets the maximum amount of time (in milliseconds) for the client application to wait.</span></span><br/>                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="55df5-149">Observaciones</span><span class="sxs-lookup"><span data-stu-id="55df5-149">Remarks</span></span>

<span data-ttu-id="55df5-150">El objeto de **sesión** corresponde a la interfaz [**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession) .</span><span class="sxs-lookup"><span data-stu-id="55df5-150">The **Session** object corresponds to the [**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="55df5-151">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="55df5-151">Examples</span></span>

<span data-ttu-id="55df5-152">En el ejemplo de código de VBScript siguiente se muestra cómo crear un objeto de **sesión** .</span><span class="sxs-lookup"><span data-stu-id="55df5-152">The following VBScript code example shows how to create a **Session** object.</span></span>


```VB
' Create a WSMan object.
Dim objWsman 
Set objWsman = CreateObject( "WSMAN.Automation" )

' Create Session object.
Dim objSession
Set objSession = objWsman.CreateSession
```



## <a name="requirements"></a><span data-ttu-id="55df5-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55df5-153">Requirements</span></span>



| <span data-ttu-id="55df5-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="55df5-154">Requirement</span></span> | <span data-ttu-id="55df5-155">Value</span><span class="sxs-lookup"><span data-stu-id="55df5-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="55df5-156">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55df5-156">Minimum supported client</span></span><br/> | <span data-ttu-id="55df5-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="55df5-157">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="55df5-158">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55df5-158">Minimum supported server</span></span><br/> | <span data-ttu-id="55df5-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="55df5-159">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="55df5-160">Encabezado</span><span class="sxs-lookup"><span data-stu-id="55df5-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="55df5-161"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="55df5-161"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="55df5-162">IDL</span><span class="sxs-lookup"><span data-stu-id="55df5-162">IDL</span></span><br/>                      | <dl> <span data-ttu-id="55df5-163"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="55df5-163"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="55df5-164">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="55df5-164">Library</span></span><br/>                  | <dl> <span data-ttu-id="55df5-165"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="55df5-165"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="55df5-166">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="55df5-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55df5-167"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55df5-167"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="55df5-168">Vea también</span><span class="sxs-lookup"><span data-stu-id="55df5-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55df5-169">API de scripting de WinRM</span><span class="sxs-lookup"><span data-stu-id="55df5-169">WinRM Scripting API</span></span>](winrm-scripting-api.md)
</dt> <dt>

[<span data-ttu-id="55df5-170">Acerca de Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="55df5-170">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="55df5-171">Usar Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="55df5-171">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="55df5-172">Scripting en Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="55df5-172">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="55df5-173">Obtención de datos del equipo local</span><span class="sxs-lookup"><span data-stu-id="55df5-173">Obtaining Data from the Local Computer</span></span>](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[<span data-ttu-id="55df5-174">Obtención de datos de un equipo remoto</span><span class="sxs-lookup"><span data-stu-id="55df5-174">Obtaining Data from a Remote Computer</span></span>](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

 





