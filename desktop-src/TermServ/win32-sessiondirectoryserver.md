---
title: Win32_SessionDirectoryServer (clase)
description: Proporciona propiedades para ver las propiedades de un servidor de Conexión a Escritorio remoto Broker (agente de conexión a escritorio remoto).
ms.assetid: 73017b71-eff9-4ef6-aba0-71ddb969491f
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectoryServer clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_SessionDirectoryServer de clase, se describe
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryServer
- Win32_SessionDirectoryServer.ServerName
- Win32_SessionDirectoryServer.ServerIPAddress
- Win32_SessionDirectoryServer.ClusterName
- Win32_SessionDirectoryServer.NumberOfSessions
- Win32_SessionDirectoryServer.SingleSessionMode
- Win32_SessionDirectoryServer.ServerWeight
- Win32_SessionDirectoryServer.NumPendRedir
- Win32_SessionDirectoryServer.LoadIndicator
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9e96efb19e4db56e582cd44d05f3e9865e5282c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996249"
---
# <a name="win32_sessiondirectoryserver-class"></a><span data-ttu-id="5e3c8-105">\_Clase Win32 SessionDirectoryServer</span><span class="sxs-lookup"><span data-stu-id="5e3c8-105">Win32\_SessionDirectoryServer class</span></span>

<span data-ttu-id="5e3c8-106">Proporciona propiedades para ver las propiedades de un servidor de Conexión a Escritorio remoto Broker (agente de conexión a escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="5e3c8-106">Provides properties for viewing the properties of a Remote Desktop Connection Broker (RD Connection Broker) server.</span></span>

> [!Note]  
> <span data-ttu-id="5e3c8-107">En Windows Server 2008 R2, el nombre de Terminal Services agente de sesión (agente de sesiones de TS) se cambió al agente de conexión a escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="5e3c8-107">In Windows Server 2008 R2, the name of Terminal Services Session Broker (TS Session Broker) was changed to RD Connection Broker.</span></span> <span data-ttu-id="5e3c8-108">Estas propiedades se aplican a todos los sistemas operativos compatibles a menos que se indique lo contrario.</span><span class="sxs-lookup"><span data-stu-id="5e3c8-108">These properties apply to all supported operating systems unless otherwise noted.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="5e3c8-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5e3c8-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYSERVER_Prov"), AMENDMENT]
class Win32_SessionDirectoryServer
{
  string ServerName;
  string ServerIPAddress;
  string ClusterName;
  uint32 NumberOfSessions;
  uint32 SingleSessionMode;
  uint32 ServerWeight;
  uint32 NumPendRedir;
  uint32 LoadIndicator;
};
```

## <a name="members"></a><span data-ttu-id="5e3c8-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="5e3c8-110">Members</span></span>

<span data-ttu-id="5e3c8-111">La **clase \_ SessionDirectoryServer de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5e3c8-111">The **Win32\_SessionDirectoryServer** class has these types of members:</span></span>

-   [<span data-ttu-id="5e3c8-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5e3c8-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5e3c8-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5e3c8-113">Properties</span></span>

<span data-ttu-id="5e3c8-114">La **clase \_ SessionDirectoryServer de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="5e3c8-114">The **Win32\_SessionDirectoryServer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5e3c8-115">**NombreDeClúster**</span><span class="sxs-lookup"><span data-stu-id="5e3c8-115">**ClusterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e3c8-116">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5e3c8-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e3c8-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e3c8-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e3c8-118">Nombre de la granja de servidores que incluye el servidor.</span><span class="sxs-lookup"><span data-stu-id="5e3c8-118">Name of the farm that includes the server.</span></span>

</dd> <dt>

<span data-ttu-id="5e3c8-119">**LoadIndicator**</span><span class="sxs-lookup"><span data-stu-id="5e3c8-119">**LoadIndicator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e3c8-120">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e3c8-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e3c8-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e3c8-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e3c8-122">Número relativo que representa el servidor host de sesión de escritorio remoto que se carga cuando se usa el algoritmo de equilibrio de carga predeterminado.</span><span class="sxs-lookup"><span data-stu-id="5e3c8-122">A relative number that represents the RD Session Host server load when the default load-balancing algorithm is used.</span></span> <span data-ttu-id="5e3c8-123">El valor de la propiedad *LoadIndicator* se basa en el número de sesiones, el número de solicitudes de redirección pendientes y el valor de peso del servidor.</span><span class="sxs-lookup"><span data-stu-id="5e3c8-123">The *LoadIndicator* property value is based on the number of sessions, the number of pending redirection requests, and the server weight value.</span></span>

</dd> <dt>

<span data-ttu-id="5e3c8-124">**NumberOfSessions**</span><span class="sxs-lookup"><span data-stu-id="5e3c8-124">**NumberOfSessions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e3c8-125">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e3c8-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e3c8-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e3c8-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e3c8-127">Número de sesiones en el servidor de agente de conexión a escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="5e3c8-127">Number of sessions in the RD Connection Broker server.</span></span>

</dd> <dt>

<span data-ttu-id="5e3c8-128">**NumPendRedir**</span><span class="sxs-lookup"><span data-stu-id="5e3c8-128">**NumPendRedir**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e3c8-129">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e3c8-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e3c8-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e3c8-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e3c8-131">Número de solicitudes de redirección pendientes.</span><span class="sxs-lookup"><span data-stu-id="5e3c8-131">Number of pending redirection requests.</span></span>

</dd> <dt>

<span data-ttu-id="5e3c8-132">**ServerIPAddress**</span><span class="sxs-lookup"><span data-stu-id="5e3c8-132">**ServerIPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e3c8-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5e3c8-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e3c8-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e3c8-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e3c8-135">Dirección IP del servidor de agente de conexión a escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="5e3c8-135">IP address of the RD Connection Broker server.</span></span> <span data-ttu-id="5e3c8-136">Si el servidor está configurado para direcciones IPv4 e IPv6, este contendrá la dirección IPv4.</span><span class="sxs-lookup"><span data-stu-id="5e3c8-136">If the server is configured for both IPv4 and IPv6 addresses, this will contain the IPv4 address.</span></span>

</dd> <dt>

<span data-ttu-id="5e3c8-137">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="5e3c8-137">**ServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e3c8-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5e3c8-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e3c8-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e3c8-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e3c8-140">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5e3c8-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5e3c8-141">Nombre del servidor de agente de conexión a escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="5e3c8-141">Name of the RD Connection Broker server.</span></span>

</dd> <dt>

<span data-ttu-id="5e3c8-142">**ServerWeight**</span><span class="sxs-lookup"><span data-stu-id="5e3c8-142">**ServerWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e3c8-143">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e3c8-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e3c8-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e3c8-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e3c8-145">Valor de peso del servidor, que se usa en el equilibrio de carga.</span><span class="sxs-lookup"><span data-stu-id="5e3c8-145">Server weight value, used in load balancing.</span></span>

</dd> <dt>

<span data-ttu-id="5e3c8-146">**SingleSessionMode**</span><span class="sxs-lookup"><span data-stu-id="5e3c8-146">**SingleSessionMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e3c8-147">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e3c8-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e3c8-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e3c8-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e3c8-149">Configuración del modo de sesión única del servidor de agente de conexión a escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="5e3c8-149">Single session mode setting of the RD Connection Broker server.</span></span>

<dt>

<span data-ttu-id="5e3c8-150">0</span><span class="sxs-lookup"><span data-stu-id="5e3c8-150">0</span></span>
</dt> <dd>

<span data-ttu-id="5e3c8-151">La granja de servidores no está en modo de sesión única.</span><span class="sxs-lookup"><span data-stu-id="5e3c8-151">The farm is not in single session mode.</span></span>

</dd> <dt>

<span data-ttu-id="5e3c8-152">1</span><span class="sxs-lookup"><span data-stu-id="5e3c8-152">1</span></span>
</dt> <dd>

<span data-ttu-id="5e3c8-153">La granja de servidores de está en modo de sesión única.</span><span class="sxs-lookup"><span data-stu-id="5e3c8-153">The farm in is in single session mode.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5e3c8-154">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5e3c8-154">Remarks</span></span>

<span data-ttu-id="5e3c8-155">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="5e3c8-155">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5e3c8-156">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="5e3c8-156">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5e3c8-157">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="5e3c8-157">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5e3c8-158">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="5e3c8-158">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5e3c8-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e3c8-159">Requirements</span></span>



| <span data-ttu-id="5e3c8-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e3c8-160">Requirement</span></span> | <span data-ttu-id="5e3c8-161">Value</span><span class="sxs-lookup"><span data-stu-id="5e3c8-161">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e3c8-162">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e3c8-162">Minimum supported client</span></span><br/> | <span data-ttu-id="5e3c8-163">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5e3c8-163">None supported</span></span><br/>                                                              |
| <span data-ttu-id="5e3c8-164">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e3c8-164">Minimum supported server</span></span><br/> | <span data-ttu-id="5e3c8-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5e3c8-165">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="5e3c8-166">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5e3c8-166">Namespace</span></span><br/>                | <span data-ttu-id="5e3c8-167">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="5e3c8-167">Root\\CIMv2</span></span><br/>                                                                 |
| <span data-ttu-id="5e3c8-168">MOF</span><span class="sxs-lookup"><span data-stu-id="5e3c8-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5e3c8-169"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5e3c8-169"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="5e3c8-170">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5e3c8-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e3c8-171"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e3c8-171"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e3c8-172">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e3c8-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e3c8-173">**Win32 \_ SessionDirectoryCluster**</span><span class="sxs-lookup"><span data-stu-id="5e3c8-173">**Win32\_SessionDirectoryCluster**</span></span>](win32-sessiondirectorycluster.md)
</dt> <dt>

[<span data-ttu-id="5e3c8-174">**Win32 \_ SessionDirectorySession**</span><span class="sxs-lookup"><span data-stu-id="5e3c8-174">**Win32\_SessionDirectorySession**</span></span>](win32-sessiondirectorysession.md)
</dt> </dl>

 

