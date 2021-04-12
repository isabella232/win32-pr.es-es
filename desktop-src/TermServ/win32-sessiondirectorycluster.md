---
title: Win32_SessionDirectoryCluster (clase)
description: Proporciona propiedades para ver las propiedades de una granja en Conexión a Escritorio remoto Broker (agente de conexión a escritorio remoto).
ms.assetid: a4a924fd-88ea-46db-968e-378c3dc46cfc
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectoryCluster clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_SessionDirectoryCluster de clase, se describe
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryCluster
- Win32_SessionDirectoryCluster.ClusterName
- Win32_SessionDirectoryCluster.NumberOfServers
- Win32_SessionDirectoryCluster.SingleSessionMode
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3979dbe5403ca8f18e941b01e95774dabefe3211
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490096"
---
# <a name="win32_sessiondirectorycluster-class"></a><span data-ttu-id="2a5e3-105">\_Clase Win32 SessionDirectoryCluster</span><span class="sxs-lookup"><span data-stu-id="2a5e3-105">Win32\_SessionDirectoryCluster class</span></span>

<span data-ttu-id="2a5e3-106">Proporciona propiedades para ver las propiedades de una granja en Conexión a Escritorio remoto Broker (agente de conexión a escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="2a5e3-106">Provides properties for viewing the properties of a farm in Remote Desktop Connection Broker (RD Connection Broker).</span></span>

> [!Note]  
> <span data-ttu-id="2a5e3-107">En Windows Server 2008 R2, el nombre de Terminal Services agente de sesión (agente de sesiones de TS) se cambió al agente de conexión a escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="2a5e3-107">In Windows Server 2008 R2, the name of Terminal Services Session Broker (TS Session Broker) was changed to RD Connection Broker.</span></span> <span data-ttu-id="2a5e3-108">Estas propiedades se aplican a todos los sistemas operativos compatibles a menos que se indique lo contrario.</span><span class="sxs-lookup"><span data-stu-id="2a5e3-108">These properties apply to all supported operating systems unless otherwise noted.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="2a5e3-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2a5e3-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYCLUSTER_Prov"), AMENDMENT]
class Win32_SessionDirectoryCluster
{
  string ClusterName;
  uint32 NumberOfServers;
  uint32 SingleSessionMode;
};
```

## <a name="members"></a><span data-ttu-id="2a5e3-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="2a5e3-110">Members</span></span>

<span data-ttu-id="2a5e3-111">La **clase \_ SessionDirectoryCluster de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2a5e3-111">The **Win32\_SessionDirectoryCluster** class has these types of members:</span></span>

-   [<span data-ttu-id="2a5e3-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2a5e3-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2a5e3-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2a5e3-113">Properties</span></span>

<span data-ttu-id="2a5e3-114">La **clase \_ SessionDirectoryCluster de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2a5e3-114">The **Win32\_SessionDirectoryCluster** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2a5e3-115">**NombreDeClúster**</span><span class="sxs-lookup"><span data-stu-id="2a5e3-115">**ClusterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a5e3-116">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2a5e3-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a5e3-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2a5e3-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a5e3-118">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2a5e3-118">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2a5e3-119">Nombre de la granja de servidores en el agente de conexión a escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="2a5e3-119">Name of the farm in RD Connection Broker.</span></span>

</dd> <dt>

<span data-ttu-id="2a5e3-120">**NumberOfServers**</span><span class="sxs-lookup"><span data-stu-id="2a5e3-120">**NumberOfServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a5e3-121">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2a5e3-121">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2a5e3-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2a5e3-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a5e3-123">Número de servidores de la granja en el agente de conexión a escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="2a5e3-123">Number of servers in the farm in RD Connection Broker.</span></span>

</dd> <dt>

<span data-ttu-id="2a5e3-124">**SingleSessionMode**</span><span class="sxs-lookup"><span data-stu-id="2a5e3-124">**SingleSessionMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a5e3-125">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2a5e3-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2a5e3-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2a5e3-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a5e3-127">Modo de sesión única de la granja de servidores en el agente de conexión a escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="2a5e3-127">Single session mode of the farm in RD Connection Broker.</span></span>

<dt>

<span data-ttu-id="2a5e3-128">0</span><span class="sxs-lookup"><span data-stu-id="2a5e3-128">0</span></span>
</dt> <dd>

<span data-ttu-id="2a5e3-129">La granja de servidores del agente de conexión a escritorio remoto no está en modo de sesión única.</span><span class="sxs-lookup"><span data-stu-id="2a5e3-129">The farm in RD Connection Broker is not in single session mode.</span></span>

</dd> <dt>

<span data-ttu-id="2a5e3-130">1</span><span class="sxs-lookup"><span data-stu-id="2a5e3-130">1</span></span>
</dt> <dd>

<span data-ttu-id="2a5e3-131">La granja de servidores del agente de conexión a escritorio remoto está en modo de sesión única.</span><span class="sxs-lookup"><span data-stu-id="2a5e3-131">The farm in RD Connection Broker is in single session mode.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2a5e3-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2a5e3-132">Remarks</span></span>

<span data-ttu-id="2a5e3-133">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="2a5e3-133">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2a5e3-134">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="2a5e3-134">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="2a5e3-135">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="2a5e3-135">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2a5e3-136">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="2a5e3-136">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="2a5e3-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a5e3-137">Requirements</span></span>



| <span data-ttu-id="2a5e3-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a5e3-138">Requirement</span></span> | <span data-ttu-id="2a5e3-139">Value</span><span class="sxs-lookup"><span data-stu-id="2a5e3-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a5e3-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a5e3-140">Minimum supported client</span></span><br/> | <span data-ttu-id="2a5e3-141">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2a5e3-141">None supported</span></span><br/>                                                              |
| <span data-ttu-id="2a5e3-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a5e3-142">Minimum supported server</span></span><br/> | <span data-ttu-id="2a5e3-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2a5e3-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="2a5e3-144">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2a5e3-144">Namespace</span></span><br/>                | <span data-ttu-id="2a5e3-145">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="2a5e3-145">Root\\CIMv2</span></span><br/>                                                                 |
| <span data-ttu-id="2a5e3-146">MOF</span><span class="sxs-lookup"><span data-stu-id="2a5e3-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2a5e3-147"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2a5e3-147"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="2a5e3-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2a5e3-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a5e3-149"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a5e3-149"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a5e3-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="2a5e3-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a5e3-151">**Win32 \_ SessionDirectoryServer**</span><span class="sxs-lookup"><span data-stu-id="2a5e3-151">**Win32\_SessionDirectoryServer**</span></span>](win32-sessiondirectoryserver.md)
</dt> <dt>

[<span data-ttu-id="2a5e3-152">**Win32 \_ SessionDirectorySession**</span><span class="sxs-lookup"><span data-stu-id="2a5e3-152">**Win32\_SessionDirectorySession**</span></span>](win32-sessiondirectorysession.md)
</dt> </dl>

 

