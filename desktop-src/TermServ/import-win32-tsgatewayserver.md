---
title: Método Import de la clase Win32_TSGatewayServer
description: Importa una configuración determinada en el servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).
ms.assetid: d849afb9-f6cb-41e6-aab5-e47b30a5581f
ms.tgt_platform: multiple
keywords:
- Método de importación Servicios de Escritorio remoto
- Método de importación Servicios de Escritorio remoto, clase Win32_TSGatewayServer
- Servicios de Escritorio remoto de clase Win32_TSGatewayServer, método Import
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer.Import
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b35395342be7c13f2a96f73f914eda103e1ef4c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996602"
---
# <a name="import-method-of-the-win32_tsgatewayserver-class"></a><span data-ttu-id="f9abc-106">Método Import de la \_ clase Win32 TSGatewayServer</span><span class="sxs-lookup"><span data-stu-id="f9abc-106">Import method of the Win32\_TSGatewayServer class</span></span>

<span data-ttu-id="f9abc-107">Importa una configuración determinada en el servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="f9abc-107">Imports a given configuration to the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9abc-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f9abc-108">Syntax</span></span>


```mof
uint32 Import(
  [in]  uint32 ImportType,
  [in]  string XmlString,
  [in]  uint32 MergeOrReplace,
  [out] string LogString
);
```



## <a name="parameters"></a><span data-ttu-id="f9abc-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f9abc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9abc-110">*ImportType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f9abc-110">*ImportType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9abc-111">Contenido que se va a importar.</span><span class="sxs-lookup"><span data-stu-id="f9abc-111">The content to import.</span></span> <span data-ttu-id="f9abc-112">Establezca el tipo de importación mediante el establecimiento de los bits correspondientes en el parámetro *ImportType* .</span><span class="sxs-lookup"><span data-stu-id="f9abc-112">Set the import type by setting the corresponding bits in the *ImportType* parameter.</span></span> <span data-ttu-id="f9abc-113">Puede establecer varios tipos de importación.</span><span class="sxs-lookup"><span data-stu-id="f9abc-113">You can set multiple import types.</span></span> <span data-ttu-id="f9abc-114">Por ejemplo, si se establece el bit 0, se importarán Servicios de Escritorio remoto las directivas de autorización de conexión (Cap de RD).</span><span class="sxs-lookup"><span data-stu-id="f9abc-114">For example, if the 0 bit is set, Remote Desktop Services connection authorization policies (RD CAPs) will be imported.</span></span> <span data-ttu-id="f9abc-115">Si se establece el 0 y el segundo bit, se importarán tanto las Cap de RD como las directivas de autorización de recursos de Servicios de Escritorio remoto (RAP de RD).</span><span class="sxs-lookup"><span data-stu-id="f9abc-115">If both the 0 and the 2nd bit is set, both RD CAPs and Remote Desktop Services resource authorization policies (RD RAPs) will be imported.</span></span>

<dt>

<span id="Import_all_CAPs"></span><span id="import_all_caps"></span><span id="IMPORT_ALL_CAPS"></span>

<span data-ttu-id="f9abc-116"><span id="Import_all_CAPs"></span><span id="import_all_caps"></span><span id="IMPORT_ALL_CAPS"></span>**Importar todos los Cap** (1)</span><span class="sxs-lookup"><span data-stu-id="f9abc-116"><span id="Import_all_CAPs"></span><span id="import_all_caps"></span><span id="IMPORT_ALL_CAPS"></span>**Import all CAPs** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f9abc-117">Importe todas las Cap de RD.</span><span class="sxs-lookup"><span data-stu-id="f9abc-117">Import all RD CAPs.</span></span>

</dd> <dt>

<span id="Import_all_Radius_Servers"></span><span id="import_all_radius_servers"></span><span id="IMPORT_ALL_RADIUS_SERVERS"></span>

<span data-ttu-id="f9abc-118"><span id="Import_all_Radius_Servers"></span><span id="import_all_radius_servers"></span><span id="IMPORT_ALL_RADIUS_SERVERS"></span>**Importar todos los servidores RADIUS** (2)</span><span class="sxs-lookup"><span data-stu-id="f9abc-118"><span id="Import_all_Radius_Servers"></span><span id="import_all_radius_servers"></span><span id="IMPORT_ALL_RADIUS_SERVERS"></span>**Import all Radius Servers** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f9abc-119">Importe una lista de todos los servidores NPS (servidor de directivas de redes).</span><span class="sxs-lookup"><span data-stu-id="f9abc-119">Import a list of all Network Policy Server (NPS) servers.</span></span>

</dd> <dt>

<span id="Import_all_RAPs"></span><span id="import_all_raps"></span><span id="IMPORT_ALL_RAPS"></span>

<span data-ttu-id="f9abc-120"><span id="Import_all_RAPs"></span><span id="import_all_raps"></span><span id="IMPORT_ALL_RAPS"></span>**Importar todas las rap** (4)</span><span class="sxs-lookup"><span data-stu-id="f9abc-120"><span id="Import_all_RAPs"></span><span id="import_all_raps"></span><span id="IMPORT_ALL_RAPS"></span>**Import all RAPs** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f9abc-121">Importe todas las rap de RD.</span><span class="sxs-lookup"><span data-stu-id="f9abc-121">Import all RD RAPs.</span></span>

</dd> <dt>

<span id="Import_all_RGs"></span><span id="import_all_rgs"></span><span id="IMPORT_ALL_RGS"></span>

<span data-ttu-id="f9abc-122"><span id="Import_all_RGs"></span><span id="import_all_rgs"></span><span id="IMPORT_ALL_RGS"></span>**Importar todos los RGs** (8)</span><span class="sxs-lookup"><span data-stu-id="f9abc-122"><span id="Import_all_RGs"></span><span id="import_all_rgs"></span><span id="IMPORT_ALL_RGS"></span>**Import all RGs** (8)</span></span>


</dt> <dd>

<span data-ttu-id="f9abc-123">Importe todos los grupos de recursos.</span><span class="sxs-lookup"><span data-stu-id="f9abc-123">Import all resource groups.</span></span>

</dd> <dt>

<span id="Import_all_LoadBalancing_Servers"></span><span id="import_all_loadbalancing_servers"></span><span id="IMPORT_ALL_LOADBALANCING_SERVERS"></span>

<span data-ttu-id="f9abc-124"><span id="Import_all_LoadBalancing_Servers"></span><span id="import_all_loadbalancing_servers"></span><span id="IMPORT_ALL_LOADBALANCING_SERVERS"></span>**Importar todos los servidores de equilibrio** (16)</span><span class="sxs-lookup"><span data-stu-id="f9abc-124"><span id="Import_all_LoadBalancing_Servers"></span><span id="import_all_loadbalancing_servers"></span><span id="IMPORT_ALL_LOADBALANCING_SERVERS"></span>**Import all LoadBalancing Servers** (16)</span></span>


</dt> <dd>

<span data-ttu-id="f9abc-125">Importe una lista de todos los servidores de equilibrio de carga.</span><span class="sxs-lookup"><span data-stu-id="f9abc-125">Import a list of all load-balancing servers.</span></span>

</dd> <dt>

<span id="Import_all_Server_Settings"></span><span id="import_all_server_settings"></span><span id="IMPORT_ALL_SERVER_SETTINGS"></span>

<span data-ttu-id="f9abc-126"><span id="Import_all_Server_Settings"></span><span id="import_all_server_settings"></span><span id="IMPORT_ALL_SERVER_SETTINGS"></span>**Importar la configuración de todos los servidores** (32)</span><span class="sxs-lookup"><span data-stu-id="f9abc-126"><span id="Import_all_Server_Settings"></span><span id="import_all_server_settings"></span><span id="IMPORT_ALL_SERVER_SETTINGS"></span>**Import all Server Settings** (32)</span></span>


</dt> <dd>

<span data-ttu-id="f9abc-127">Importe la configuración de todos los servidores relacionados con la puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="f9abc-127">Import all RD Gateway-related server settings.</span></span>

</dd> <dt>

<span id="Import_all_Health_Policies"></span><span id="import_all_health_policies"></span><span id="IMPORT_ALL_HEALTH_POLICIES"></span>

<span data-ttu-id="f9abc-128"><span id="Import_all_Health_Policies"></span><span id="import_all_health_policies"></span><span id="IMPORT_ALL_HEALTH_POLICIES"></span>**Importar todas las directivas de mantenimiento** (64)</span><span class="sxs-lookup"><span data-stu-id="f9abc-128"><span id="Import_all_Health_Policies"></span><span id="import_all_health_policies"></span><span id="IMPORT_ALL_HEALTH_POLICIES"></span>**Import all Health Policies** (64)</span></span>


</dt> <dd>

<span data-ttu-id="f9abc-129">Importe todas las directivas de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="f9abc-129">Import all health policies.</span></span>

<span data-ttu-id="f9abc-130">\* \* Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 y Windows Server 2008: \* \*</span><span class="sxs-lookup"><span data-stu-id="f9abc-130">\*\*Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  \*\*</span></span>

<span data-ttu-id="f9abc-131">Este valor no se admite antes de Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="f9abc-131">This value is not supported before Windows Server 2016.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f9abc-132">*XmlString* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f9abc-132">*XmlString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9abc-133">La configuración como una cadena XML.</span><span class="sxs-lookup"><span data-stu-id="f9abc-133">The configuration as an XML string.</span></span>

</dd> <dt>

<span data-ttu-id="f9abc-134">*MergeOrReplace* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f9abc-134">*MergeOrReplace* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9abc-135">Indica si se deben combinar o reemplazar los datos cuando se produce un conflicto.</span><span class="sxs-lookup"><span data-stu-id="f9abc-135">Indicates whether to merge or replace data when a conflict occurs.</span></span>

> [!Note]  
> <span data-ttu-id="f9abc-136">La fusión mediante combinación no se ha implementado todavía.</span><span class="sxs-lookup"><span data-stu-id="f9abc-136">Merge is not yet implemented.</span></span> <span data-ttu-id="f9abc-137">Por lo tanto, se omite este valor de parámetro.</span><span class="sxs-lookup"><span data-stu-id="f9abc-137">Therefore, this parameter value is ignored.</span></span>

 

</dd> <dt>

<span data-ttu-id="f9abc-138">*LogString* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f9abc-138">*LogString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9abc-139">La información de registro que se genera durante la operación de importación.</span><span class="sxs-lookup"><span data-stu-id="f9abc-139">The log information that is generated during the import operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f9abc-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f9abc-140">Remarks</span></span>

<span data-ttu-id="f9abc-141">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="f9abc-141">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="f9abc-142">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="f9abc-142">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f9abc-143">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="f9abc-143">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f9abc-144">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="f9abc-144">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f9abc-145">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f9abc-145">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f9abc-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9abc-146">Requirements</span></span>



| <span data-ttu-id="f9abc-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9abc-147">Requirement</span></span> | <span data-ttu-id="f9abc-148">Value</span><span class="sxs-lookup"><span data-stu-id="f9abc-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9abc-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9abc-149">Minimum supported client</span></span><br/> | <span data-ttu-id="f9abc-150">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f9abc-150">None supported</span></span><br/>                                                                |
| <span data-ttu-id="f9abc-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9abc-151">Minimum supported server</span></span><br/> | <span data-ttu-id="f9abc-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f9abc-152">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="f9abc-153">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f9abc-153">Namespace</span></span><br/>                | <span data-ttu-id="f9abc-154">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="f9abc-154">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="f9abc-155">MOF</span><span class="sxs-lookup"><span data-stu-id="f9abc-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f9abc-156"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f9abc-156"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="f9abc-157">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f9abc-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9abc-158"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9abc-158"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="f9abc-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9abc-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9abc-160">**Win32 \_ TSGatewayServer**</span><span class="sxs-lookup"><span data-stu-id="f9abc-160">**Win32\_TSGatewayServer**</span></span>](win32-tsgatewayserver.md)
</dt> </dl>

 

