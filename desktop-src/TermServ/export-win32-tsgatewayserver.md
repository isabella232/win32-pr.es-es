---
title: Método Export de la clase Win32_TSGatewayServer
description: Devuelve la configuración del servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto) como una cadena XML.
ms.assetid: abf3a616-2b86-4cfe-934f-f1f17ce3ce31
ms.tgt_platform: multiple
keywords:
- Método de exportación Servicios de Escritorio remoto
- Método de exportación Servicios de Escritorio remoto, Win32_TSGatewayServer clase)
- Win32_TSGatewayServer de clase Servicios de Escritorio remoto, método Export
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer.Export
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429e27cb93c319e977d37926ac43488008d62714
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997154"
---
# <a name="export-method-of-the-win32_tsgatewayserver-class"></a><span data-ttu-id="4bbc1-106">Método Export de la \_ clase Win32 TSGatewayServer</span><span class="sxs-lookup"><span data-stu-id="4bbc1-106">Export method of the Win32\_TSGatewayServer class</span></span>

<span data-ttu-id="4bbc1-107">Devuelve la configuración del servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto) como una cadena XML.</span><span class="sxs-lookup"><span data-stu-id="4bbc1-107">Returns the Remote Desktop Gateway (RD Gateway) server configuration as an XML string.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bbc1-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4bbc1-108">Syntax</span></span>


```mof
uint32 Export(
  [in]  uint32 ExportType,
  [out] string XmlString
);
```



## <a name="parameters"></a><span data-ttu-id="4bbc1-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4bbc1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bbc1-110">*ExportType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4bbc1-110">*ExportType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bbc1-111">Contenido que se va a exportar.</span><span class="sxs-lookup"><span data-stu-id="4bbc1-111">The content to export.</span></span> <span data-ttu-id="4bbc1-112">Establezca el tipo de exportación mediante el establecimiento de los bits correspondientes en el parámetro *ExportType* .</span><span class="sxs-lookup"><span data-stu-id="4bbc1-112">Set the export type by setting the corresponding bits in the *ExportType* parameter.</span></span> <span data-ttu-id="4bbc1-113">Puede establecer varios tipos de exportación.</span><span class="sxs-lookup"><span data-stu-id="4bbc1-113">You can set multiple export types.</span></span> <span data-ttu-id="4bbc1-114">Por ejemplo, si se establece el bit 0, se exportarán Servicios de Escritorio remoto las directivas de autorización de conexión (Cap de RD).</span><span class="sxs-lookup"><span data-stu-id="4bbc1-114">For example, if the 0 bit is set, Remote Desktop Services connection authorization policies (RD CAPs) will be exported.</span></span> <span data-ttu-id="4bbc1-115">Si se establece el 0 y el segundo bit, se exportarán tanto las Cap de RD como las directivas de autorización de recursos de Servicios de Escritorio remoto (RAP de RD).</span><span class="sxs-lookup"><span data-stu-id="4bbc1-115">If both the 0 and the 2nd bit is set, both RD CAPs and Remote Desktop Services resource authorization policies (RD RAPs) will be exported.</span></span>

<dt>

<span id="Export_all_CAPs"></span><span id="export_all_caps"></span><span id="EXPORT_ALL_CAPS"></span>

<span data-ttu-id="4bbc1-116"><span id="Export_all_CAPs"></span><span id="export_all_caps"></span><span id="EXPORT_ALL_CAPS"></span>**Exportar todos los Cap** (1)</span><span class="sxs-lookup"><span data-stu-id="4bbc1-116"><span id="Export_all_CAPs"></span><span id="export_all_caps"></span><span id="EXPORT_ALL_CAPS"></span>**Export all CAPs** (1)</span></span>


</dt> <dd>

<span data-ttu-id="4bbc1-117">Exportar todas las Cap de RD.</span><span class="sxs-lookup"><span data-stu-id="4bbc1-117">Export all RD CAPs.</span></span>

</dd> <dt>

<span id="Export_all_Radius_Servers"></span><span id="export_all_radius_servers"></span><span id="EXPORT_ALL_RADIUS_SERVERS"></span>

<span data-ttu-id="4bbc1-118"><span id="Export_all_Radius_Servers"></span><span id="export_all_radius_servers"></span><span id="EXPORT_ALL_RADIUS_SERVERS"></span>**Exportar todos los servidores RADIUS** (2)</span><span class="sxs-lookup"><span data-stu-id="4bbc1-118"><span id="Export_all_Radius_Servers"></span><span id="export_all_radius_servers"></span><span id="EXPORT_ALL_RADIUS_SERVERS"></span>**Export all Radius Servers** (2)</span></span>


</dt> <dd>

<span data-ttu-id="4bbc1-119">Exporte una lista de todos los servidores NPS (servidor de directivas de redes).</span><span class="sxs-lookup"><span data-stu-id="4bbc1-119">Export a list of all Network Policy Server (NPS) servers.</span></span>

</dd> <dt>

<span id="Export_all_RAPs"></span><span id="export_all_raps"></span><span id="EXPORT_ALL_RAPS"></span>

<span data-ttu-id="4bbc1-120"><span id="Export_all_RAPs"></span><span id="export_all_raps"></span><span id="EXPORT_ALL_RAPS"></span>**Exportar todas las rap** (4)</span><span class="sxs-lookup"><span data-stu-id="4bbc1-120"><span id="Export_all_RAPs"></span><span id="export_all_raps"></span><span id="EXPORT_ALL_RAPS"></span>**Export all RAPs** (4)</span></span>


</dt> <dd>

<span data-ttu-id="4bbc1-121">Exportar todas las rap de RD.</span><span class="sxs-lookup"><span data-stu-id="4bbc1-121">Export all RD RAPs.</span></span>

</dd> <dt>

<span id="Export_all_RGs"></span><span id="export_all_rgs"></span><span id="EXPORT_ALL_RGS"></span>

<span data-ttu-id="4bbc1-122"><span id="Export_all_RGs"></span><span id="export_all_rgs"></span><span id="EXPORT_ALL_RGS"></span>**Exportar todos los RGs** (8)</span><span class="sxs-lookup"><span data-stu-id="4bbc1-122"><span id="Export_all_RGs"></span><span id="export_all_rgs"></span><span id="EXPORT_ALL_RGS"></span>**Export all RGs** (8)</span></span>


</dt> <dd>

<span data-ttu-id="4bbc1-123">Exporte todos los grupos de recursos.</span><span class="sxs-lookup"><span data-stu-id="4bbc1-123">Export all resource groups.</span></span>

</dd> <dt>

<span id="Export_all_LoadBalancing_Servers"></span><span id="export_all_loadbalancing_servers"></span><span id="EXPORT_ALL_LOADBALANCING_SERVERS"></span>

<span data-ttu-id="4bbc1-124"><span id="Export_all_LoadBalancing_Servers"></span><span id="export_all_loadbalancing_servers"></span><span id="EXPORT_ALL_LOADBALANCING_SERVERS"></span>**Exportar todos los servidores de equilibrio** (16)</span><span class="sxs-lookup"><span data-stu-id="4bbc1-124"><span id="Export_all_LoadBalancing_Servers"></span><span id="export_all_loadbalancing_servers"></span><span id="EXPORT_ALL_LOADBALANCING_SERVERS"></span>**Export all LoadBalancing Servers** (16)</span></span>


</dt> <dd>

<span data-ttu-id="4bbc1-125">Exporte una lista de todos los servidores de equilibrio de carga.</span><span class="sxs-lookup"><span data-stu-id="4bbc1-125">Export a list of all load-balancing servers.</span></span>

</dd> <dt>

<span id="Export_all_Server_Settings"></span><span id="export_all_server_settings"></span><span id="EXPORT_ALL_SERVER_SETTINGS"></span>

<span data-ttu-id="4bbc1-126"><span id="Export_all_Server_Settings"></span><span id="export_all_server_settings"></span><span id="EXPORT_ALL_SERVER_SETTINGS"></span>**Exportar toda la configuración del servidor** (32)</span><span class="sxs-lookup"><span data-stu-id="4bbc1-126"><span id="Export_all_Server_Settings"></span><span id="export_all_server_settings"></span><span id="EXPORT_ALL_SERVER_SETTINGS"></span>**Export all Server Settings** (32)</span></span>


</dt> <dd>

<span data-ttu-id="4bbc1-127">Exporte todas las opciones del servidor relacionadas con la puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="4bbc1-127">Export all RD Gateway-related server settings.</span></span>

</dd> <dt>

<span id="Export_all_Health_Policies"></span><span id="export_all_health_policies"></span><span id="EXPORT_ALL_HEALTH_POLICIES"></span>

<span data-ttu-id="4bbc1-128"><span id="Export_all_Health_Policies"></span><span id="export_all_health_policies"></span><span id="EXPORT_ALL_HEALTH_POLICIES"></span>**Exportar todas las directivas de mantenimiento** (64)</span><span class="sxs-lookup"><span data-stu-id="4bbc1-128"><span id="Export_all_Health_Policies"></span><span id="export_all_health_policies"></span><span id="EXPORT_ALL_HEALTH_POLICIES"></span>**Export all Health Policies** (64)</span></span>


</dt> <dd>

<span data-ttu-id="4bbc1-129">Exporte todas las directivas de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="4bbc1-129">Export all health policies.</span></span>

<span data-ttu-id="4bbc1-130">\* \* Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 y Windows Server 2008: \* \*</span><span class="sxs-lookup"><span data-stu-id="4bbc1-130">\*\*Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  \*\*</span></span>

<span data-ttu-id="4bbc1-131">Este valor no se admite antes de Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="4bbc1-131">This value is not supported before Windows Server 2016.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4bbc1-132">*XmlString* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4bbc1-132">*XmlString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4bbc1-133">Cadena XML.</span><span class="sxs-lookup"><span data-stu-id="4bbc1-133">The XML string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4bbc1-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4bbc1-134">Remarks</span></span>

<span data-ttu-id="4bbc1-135">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="4bbc1-135">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="4bbc1-136">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="4bbc1-136">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4bbc1-137">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="4bbc1-137">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="4bbc1-138">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="4bbc1-138">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4bbc1-139">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="4bbc1-139">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="4bbc1-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4bbc1-140">Requirements</span></span>



| <span data-ttu-id="4bbc1-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="4bbc1-141">Requirement</span></span> | <span data-ttu-id="4bbc1-142">Value</span><span class="sxs-lookup"><span data-stu-id="4bbc1-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bbc1-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4bbc1-143">Minimum supported client</span></span><br/> | <span data-ttu-id="4bbc1-144">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="4bbc1-144">None supported</span></span><br/>                                                                |
| <span data-ttu-id="4bbc1-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4bbc1-145">Minimum supported server</span></span><br/> | <span data-ttu-id="4bbc1-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4bbc1-146">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="4bbc1-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4bbc1-147">Namespace</span></span><br/>                | <span data-ttu-id="4bbc1-148">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="4bbc1-148">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="4bbc1-149">MOF</span><span class="sxs-lookup"><span data-stu-id="4bbc1-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4bbc1-150"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4bbc1-150"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="4bbc1-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4bbc1-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4bbc1-152"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4bbc1-152"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="4bbc1-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="4bbc1-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bbc1-154">**Win32 \_ TSGatewayServer**</span><span class="sxs-lookup"><span data-stu-id="4bbc1-154">**Win32\_TSGatewayServer**</span></span>](win32-tsgatewayserver.md)
</dt> </dl>

 

