---
title: Win32_RDSHServer (clase)
description: Administra un servidor de host de sesión Escritorio remoto (RDSH).
ms.assetid: 2c2840d2-16aa-484a-979b-6dbb1a08bbcf
ms.tgt_platform: multiple
keywords:
- Win32_RDSHServer clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_RDSHServer de clase, se describe
topic_type:
- apiref
api_name:
- Win32_RDSHServer
- Win32_RDSHServer.Name
- Win32_RDSHServer.ConnectionBroker
- Win32_RDSHServer.CollectionAlias
- Win32_RDSHServer.ServerState
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6434a4dfe6bc1a79fdaf4576a89ef552cebd5e1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359742"
---
# <a name="win32_rdshserver-class"></a><span data-ttu-id="80d1f-105">\_Clase Win32 RDSHServer</span><span class="sxs-lookup"><span data-stu-id="80d1f-105">Win32\_RDSHServer class</span></span>

<span data-ttu-id="80d1f-106">Administra un servidor de host de sesión Escritorio remoto (RDSH).</span><span class="sxs-lookup"><span data-stu-id="80d1f-106">Manages a Remote Desktop Session Host (RDSH) server.</span></span>

<span data-ttu-id="80d1f-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="80d1f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="80d1f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="80d1f-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDSHServer
{
  string Name;
  string ConnectionBroker;
  string CollectionAlias;
  uint32 ServerState;
};
```

## <a name="members"></a><span data-ttu-id="80d1f-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="80d1f-109">Members</span></span>

<span data-ttu-id="80d1f-110">La **clase \_ RDSHServer de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="80d1f-110">The **Win32\_RDSHServer** class has these types of members:</span></span>

-   [<span data-ttu-id="80d1f-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="80d1f-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="80d1f-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="80d1f-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="80d1f-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="80d1f-113">Methods</span></span>

<span data-ttu-id="80d1f-114">La clase **Win32 \_ RDSHServer** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="80d1f-114">The **Win32\_RDSHServer** class has these methods.</span></span>



| <span data-ttu-id="80d1f-115">Método</span><span class="sxs-lookup"><span data-stu-id="80d1f-115">Method</span></span>                                                                          | <span data-ttu-id="80d1f-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="80d1f-116">Description</span></span>                                                                                                                                                                       |
|:--------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="80d1f-117">**GetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="80d1f-117">**GetInt32Property**</span></span>](getint32property-win32-rdshserver.md)                   | <span data-ttu-id="80d1f-118">Recupera un valor de propiedad de entero de un **objeto \_ RDSHServer de Win32** .</span><span class="sxs-lookup"><span data-stu-id="80d1f-118">Retrieves an integer property value of a **Win32\_RDSHServer** object.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="80d1f-119">**GetPendingStartServerList**</span><span class="sxs-lookup"><span data-stu-id="80d1f-119">**GetPendingStartServerList**</span></span>](win32-rdshserver-getpendingstartserverlist.md) | <span data-ttu-id="80d1f-120">Recupera una lista de servidores en espera de inicio.</span><span class="sxs-lookup"><span data-stu-id="80d1f-120">Retrieves a list of server waiting to start.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="80d1f-121">**GetStringProperty**</span><span class="sxs-lookup"><span data-stu-id="80d1f-121">**GetStringProperty**</span></span>](getstringproperty-win32-rdshserver.md)                 | <span data-ttu-id="80d1f-122">Recupera un valor de propiedad de cadena de un objeto **\_ RDSHServer de Win32** .</span><span class="sxs-lookup"><span data-stu-id="80d1f-122">Retrieves a string property value of a **Win32\_RDSHServer** object.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="80d1f-123">**SetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="80d1f-123">**SetInt32Property**</span></span>](setint32property-win32-rdshserver.md)                   | <span data-ttu-id="80d1f-124">Actualiza un valor de propiedad de entero de un objeto **\_ RDSHServer de Win32** .</span><span class="sxs-lookup"><span data-stu-id="80d1f-124">Updates an integer property value of a **Win32\_RDSHServer** object.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="80d1f-125">**SetStringProperty**</span><span class="sxs-lookup"><span data-stu-id="80d1f-125">**SetStringProperty**</span></span>](setstringproperty-win32-rdshserver.md)                 | <span data-ttu-id="80d1f-126">Actualiza un valor de propiedad de cadena de un objeto **\_ RDSHServer de Win32** .</span><span class="sxs-lookup"><span data-stu-id="80d1f-126">Updates a string property value of a **Win32\_RDSHServer** object.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="80d1f-127">**TestAndSetState**</span><span class="sxs-lookup"><span data-stu-id="80d1f-127">**TestAndSetState**</span></span>](win32-rdshserver-testandsetstate.md)                     | <span data-ttu-id="80d1f-128">Compara el estado actual con el especificado. Si los dos coinciden, el estado se establece en un nuevo valor.</span><span class="sxs-lookup"><span data-stu-id="80d1f-128">Compares the current state to the specified comparand; if the two match, the state is set to a new value.</span></span> <span data-ttu-id="80d1f-129">Independientemente de la coincidencia, también se devuelve el estado actual.</span><span class="sxs-lookup"><span data-stu-id="80d1f-129">Regardless of the match, the current state is also returned.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="80d1f-130">Propiedades</span><span class="sxs-lookup"><span data-stu-id="80d1f-130">Properties</span></span>

<span data-ttu-id="80d1f-131">La **clase \_ RDSHServer de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="80d1f-131">The **Win32\_RDSHServer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="80d1f-132">**CollectionAlias**</span><span class="sxs-lookup"><span data-stu-id="80d1f-132">**CollectionAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80d1f-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="80d1f-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80d1f-134">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="80d1f-134">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="80d1f-135">Calificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="80d1f-135">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="80d1f-136">Obtiene y establece el alias de la colección RDSH a la que se asigna el servidor RDSH.</span><span class="sxs-lookup"><span data-stu-id="80d1f-136">Gets and sets the alias to the RDSH collection to which the RDSH server is assigned.</span></span>

</dd> <dt>

<span data-ttu-id="80d1f-137">**ConnectionBroker**</span><span class="sxs-lookup"><span data-stu-id="80d1f-137">**ConnectionBroker**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80d1f-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="80d1f-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80d1f-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="80d1f-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="80d1f-140">Obtiene y establece el nombre del agente de Conexión a Escritorio remoto (RDCB) que administra el acceso del usuario al servidor RDSH.</span><span class="sxs-lookup"><span data-stu-id="80d1f-140">Gets and sets the name of the Remote Desktop Connection Broker (RDCB) that manages user access to the RDSH server.</span></span>

</dd> <dt>

<span data-ttu-id="80d1f-141">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="80d1f-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80d1f-142">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="80d1f-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80d1f-143">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="80d1f-143">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="80d1f-144">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="80d1f-144">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="80d1f-145">Obtiene y establece el nombre del servidor RDSH.</span><span class="sxs-lookup"><span data-stu-id="80d1f-145">Gets and sets the name of the RDSH server.</span></span>

</dd> <dt>

<span data-ttu-id="80d1f-146">**ServerState**</span><span class="sxs-lookup"><span data-stu-id="80d1f-146">**ServerState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80d1f-147">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="80d1f-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="80d1f-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="80d1f-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80d1f-149">Calificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="80d1f-149">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="80d1f-150">Describe el estado del servidor.</span><span class="sxs-lookup"><span data-stu-id="80d1f-150">Describes the state of the server.</span></span> <span data-ttu-id="80d1f-151">Cualquier valor distinto del **destino \_ que se ejecuta** (3) está reservado y debe tener en cuenta un estado no válido.</span><span class="sxs-lookup"><span data-stu-id="80d1f-151">Any value other than **TARGET\_RUNNING** (3) is reserved and should be consider an invalid state.</span></span>

<span data-ttu-id="80d1f-152">Los valores posibles son.</span><span class="sxs-lookup"><span data-stu-id="80d1f-152">The possible values are.</span></span>

<dt>

<span id="TARGET_UNKNOWN"></span><span id="target_unknown"></span>

<span data-ttu-id="80d1f-153">**Destino \_ de DESCONOCIDO** (1)</span><span class="sxs-lookup"><span data-stu-id="80d1f-153">**TARGET\_UNKNOWN** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="TARGET_RUNNING"></span><span id="target_running"></span>

<span data-ttu-id="80d1f-154">**Destino \_ de En ejecución** (3)</span><span class="sxs-lookup"><span data-stu-id="80d1f-154">**TARGET\_RUNNING** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="TARGET_INVALID"></span><span id="target_invalid"></span>

<span data-ttu-id="80d1f-155">**Destino \_ de NO válido** (8)</span><span class="sxs-lookup"><span data-stu-id="80d1f-155">**TARGET\_INVALID** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="TARGET_STARTING"></span><span id="target_starting"></span>

<span data-ttu-id="80d1f-156">**Destino \_ de Inicio** (9)</span><span class="sxs-lookup"><span data-stu-id="80d1f-156">**TARGET\_STARTING** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="TARGET_STOPPING"></span><span id="target_stopping"></span>

<span data-ttu-id="80d1f-157">**Destino \_ de DETENCIÓN** (10)</span><span class="sxs-lookup"><span data-stu-id="80d1f-157">**TARGET\_STOPPING** (10)</span></span>


<span data-ttu-id="80d1f-158"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="80d1f-158"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="80d1f-159">**Windows server 2012 R2 y Windows server 2012:** Esta propiedad no está disponible antes de Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="80d1f-159">**Windows Server 2012 R2 and Windows Server 2012:** This property is unavailable prior to Windows Server 2016.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="80d1f-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80d1f-160">Requirements</span></span>



| <span data-ttu-id="80d1f-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="80d1f-161">Requirement</span></span> | <span data-ttu-id="80d1f-162">Value</span><span class="sxs-lookup"><span data-stu-id="80d1f-162">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="80d1f-163">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80d1f-163">Minimum supported client</span></span><br/> | <span data-ttu-id="80d1f-164">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="80d1f-164">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="80d1f-165">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80d1f-165">Minimum supported server</span></span><br/> | <span data-ttu-id="80d1f-166">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="80d1f-166">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="80d1f-167">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="80d1f-167">Namespace</span></span><br/>                | <span data-ttu-id="80d1f-168">RDMs raíz de \\ cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="80d1f-168">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="80d1f-169">MOF</span><span class="sxs-lookup"><span data-stu-id="80d1f-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="80d1f-170"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="80d1f-170"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="80d1f-171">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="80d1f-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80d1f-172"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80d1f-172"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="80d1f-173">Vea también</span><span class="sxs-lookup"><span data-stu-id="80d1f-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80d1f-174">Proveedor de servicios de administración de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="80d1f-174">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

