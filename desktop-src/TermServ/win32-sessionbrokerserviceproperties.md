---
title: Win32_SessionBrokerServiceProperties (clase)
description: Define la consulta para un servicio agente de sesiones.
ms.assetid: fe7a0317-8b52-4685-9d0d-2f81058b4561
ms.tgt_platform: multiple
keywords:
- Win32_SessionBrokerServiceProperties clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_SessionBrokerServiceProperties de clase, se describe
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties
- Win32_SessionBrokerServiceProperties.SBNetworkName
- Win32_SessionBrokerServiceProperties.SBDbConnectionString
- Win32_SessionBrokerServiceProperties.SBDbSecondaryConnectionString
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 507c4211b9506e0635966e9541167d24495735ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535367"
---
# <a name="win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="eeff5-105">\_Clase Win32 SessionBrokerServiceProperties</span><span class="sxs-lookup"><span data-stu-id="eeff5-105">Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="eeff5-106">Define la consulta para un servicio agente de sesiones.</span><span class="sxs-lookup"><span data-stu-id="eeff5-106">Defines the query for a session broker service.</span></span>

<span data-ttu-id="eeff5-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="eeff5-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="eeff5-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eeff5-108">Syntax</span></span>

``` syntax
[dynamic, singleton, provider("Win32_WIN32_SESSIONBROKERSERVICEPROPERTIES_Prov"), AMENDMENT]
class Win32_SessionBrokerServiceProperties
{
  string SBNetworkName;
  string SBDbConnectionString;
  string SBDbSecondaryConnectionString;
};
```

## <a name="members"></a><span data-ttu-id="eeff5-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="eeff5-109">Members</span></span>

<span data-ttu-id="eeff5-110">La **clase \_ SessionBrokerServiceProperties de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="eeff5-110">The **Win32\_SessionBrokerServiceProperties** class has these types of members:</span></span>

-   [<span data-ttu-id="eeff5-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="eeff5-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="eeff5-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="eeff5-112">Properties</span></span>](/windows)

### <a name="methods"></a><span data-ttu-id="eeff5-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="eeff5-113">Methods</span></span>

<span data-ttu-id="eeff5-114">La clase **Win32 \_ SessionBrokerServiceProperties** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="eeff5-114">The **Win32\_SessionBrokerServiceProperties** class has these methods.</span></span>



| <span data-ttu-id="eeff5-115">Método</span><span class="sxs-lookup"><span data-stu-id="eeff5-115">Method</span></span>                                                                                                | <span data-ttu-id="eeff5-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="eeff5-116">Description</span></span>                                                                                                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eeff5-117">**DeleteSBDbConnectionString**</span><span class="sxs-lookup"><span data-stu-id="eeff5-117">**DeleteSBDbConnectionString**</span></span>](win32-sessionbrokerserviceproperties-deletesbdbconnectionstring.md) | <span data-ttu-id="eeff5-118">Elimina las cadenas de conexión de base de datos (principal y secundaria) del registro.</span><span class="sxs-lookup"><span data-stu-id="eeff5-118">Deletes DB connection strings (primary and secondary) from the registry.</span></span><br/> <span data-ttu-id="eeff5-119">**Windows server 2012 R2, Windows server 2012 y Windows server 2008 R2:** Este método no está disponible antes de Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="eeff5-119">**Windows Server 2012 R2, Windows Server 2012 and Windows Server 2008 R2:** This method is not available prior to Windows Server 2016</span></span><br/> |
| [<span data-ttu-id="eeff5-120">**InstallBrokerDatabase**</span><span class="sxs-lookup"><span data-stu-id="eeff5-120">**InstallBrokerDatabase**</span></span>](win32-sessionbrokerserviceproperties-installbrokerdatabase.md)           | <span data-ttu-id="eeff5-121">Instala la base de de agente de conexión a escritorio remoto en el centro de SQL Server</span><span class="sxs-lookup"><span data-stu-id="eeff5-121">Installs RD Connection Broker DB on central SQL Server</span></span><br/>                                                                                                                                                                    |
| [<span data-ttu-id="eeff5-122">**IsDbReachable**</span><span class="sxs-lookup"><span data-stu-id="eeff5-122">**IsDbReachable**</span></span>](win32-sessionbrokerserviceproperties-isdbreachable.md)                           | <span data-ttu-id="eeff5-123">Comprueba si se puede obtener acceso a la base de BD</span><span class="sxs-lookup"><span data-stu-id="eeff5-123">Checks if DB is reachable</span></span><br/>                                                                                                                                                                                                 |
| [<span data-ttu-id="eeff5-124">**SetBrokerHAMode**</span><span class="sxs-lookup"><span data-stu-id="eeff5-124">**SetBrokerHAMode**</span></span>](win32-sessionbrokerserviceproperties-setbrokerhamode.md)                       | <span data-ttu-id="eeff5-125">Migra datos de la base de datos WID local a la nueva base de datos basada en el SQL Server.</span><span class="sxs-lookup"><span data-stu-id="eeff5-125">Migrates data from local WID DB to the new SQL Server based DB.</span></span> <span data-ttu-id="eeff5-126">También configura el servidor de agente para usar el SQL Server central</span><span class="sxs-lookup"><span data-stu-id="eeff5-126">It also configures the broker server to use the central SQL Server</span></span><br/>                                                                                        |
| [<span data-ttu-id="eeff5-127">**SetBrokerNonHAMode**</span><span class="sxs-lookup"><span data-stu-id="eeff5-127">**SetBrokerNonHAMode**</span></span>](win32-sessionbrokerserviceproperties-setbrokernonhamode.md)                 | <span data-ttu-id="eeff5-128">Migra datos de la SQL Server central a la base de datos local.</span><span class="sxs-lookup"><span data-stu-id="eeff5-128">Migrates data from central SQL Server to local DB.</span></span> <span data-ttu-id="eeff5-129">También configura el servidor de agente para usar la base de BD local.</span><span class="sxs-lookup"><span data-stu-id="eeff5-129">It also configures the broker server to use the local DB.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="eeff5-130">**SetSBDbConnectionStrings**</span><span class="sxs-lookup"><span data-stu-id="eeff5-130">**SetSBDbConnectionStrings**</span></span>](win32-sessionbrokerserviceproperties-setsbdbconnectionstrings.md)     | <span data-ttu-id="eeff5-131">Guarda las cadenas de conexión de base de datos (principal y secundaria) en el registro.</span><span class="sxs-lookup"><span data-stu-id="eeff5-131">Saves DB connection strings (primary and secondary) in the registry.</span></span><br/> <span data-ttu-id="eeff5-132">**Windows server 2012 R2, Windows server 2012 y Windows server 2008 R2:** Este método no está disponible antes de Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="eeff5-132">**Windows Server 2012 R2, Windows Server 2012 and Windows Server 2008 R2:** This method is not available prior to Windows Server 2016</span></span><br/>     |



 

### <a name="properties"></a><span data-ttu-id="eeff5-133">Propiedades</span><span class="sxs-lookup"><span data-stu-id="eeff5-133">Properties</span></span>

<span data-ttu-id="eeff5-134">La **clase \_ SessionBrokerServiceProperties de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="eeff5-134">The **Win32\_SessionBrokerServiceProperties** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eeff5-135">**SBDbConnectionString**</span><span class="sxs-lookup"><span data-stu-id="eeff5-135">**SBDbConnectionString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eeff5-136">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eeff5-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eeff5-137">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eeff5-137">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="eeff5-138">Cadena de conexión de base de datos usada por el servicio agente de sesiones.</span><span class="sxs-lookup"><span data-stu-id="eeff5-138">Database connection string used by Session Broker service.</span></span>

<span data-ttu-id="eeff5-139">**Windows Server 2008 R2:** Esta propiedad no está disponible antes de Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="eeff5-139">**Windows Server 2008 R2:** This property is not available prior to Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="eeff5-140">**SBDbSecondaryConnectionString**</span><span class="sxs-lookup"><span data-stu-id="eeff5-140">**SBDbSecondaryConnectionString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eeff5-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eeff5-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eeff5-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="eeff5-142">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="eeff5-143">Opcional.</span><span class="sxs-lookup"><span data-stu-id="eeff5-143">Optional.</span></span> <span data-ttu-id="eeff5-144">Cadena de conexión de base de datos secundaria, usada por el servicio agente de sesiones para admitir la expiración de contraseña.</span><span class="sxs-lookup"><span data-stu-id="eeff5-144">Secondary database connection string, used by Session Broker service to support password expiration.</span></span>

<span data-ttu-id="eeff5-145">**Windows server 2012 R2, Windows server 2012 y Windows server 2008 R2:** Esta propiedad no está disponible antes de Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="eeff5-145">**Windows Server 2012 R2, Windows Server 2012 and Windows Server 2008 R2:** This property is not available prior to Windows Server 2016</span></span>

</dd> <dt>

<span data-ttu-id="eeff5-146">**SBNetworkName**</span><span class="sxs-lookup"><span data-stu-id="eeff5-146">**SBNetworkName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eeff5-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eeff5-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eeff5-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eeff5-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eeff5-149">El nombre de red que usa el servicio agente de sesiones.</span><span class="sxs-lookup"><span data-stu-id="eeff5-149">The network name used by the session broker service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eeff5-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eeff5-150">Requirements</span></span>



| <span data-ttu-id="eeff5-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="eeff5-151">Requirement</span></span> | <span data-ttu-id="eeff5-152">Value</span><span class="sxs-lookup"><span data-stu-id="eeff5-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eeff5-153">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eeff5-153">Minimum supported client</span></span><br/> | <span data-ttu-id="eeff5-154">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="eeff5-154">None supported</span></span><br/>                                                              |
| <span data-ttu-id="eeff5-155">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eeff5-155">Minimum supported server</span></span><br/> | <span data-ttu-id="eeff5-156">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="eeff5-156">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="eeff5-157">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="eeff5-157">Namespace</span></span><br/>                | <span data-ttu-id="eeff5-158">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="eeff5-158">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="eeff5-159">MOF</span><span class="sxs-lookup"><span data-stu-id="eeff5-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eeff5-160"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eeff5-160"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="eeff5-161">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="eeff5-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eeff5-162"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eeff5-162"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

