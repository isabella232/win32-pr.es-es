---
title: Método GetTStoLSConnectivityStatus de la clase Win32_TerminalServiceSetting
description: Determina el estado de conectividad entre Servicios de Escritorio remoto y un servidor de licencias.
ms.assetid: 11fc5865-47e8-4be8-a526-53e29f72d0a4
ms.tgt_platform: multiple
keywords:
- Método GetTStoLSConnectivityStatus Servicios de Escritorio remoto
- Método GetTStoLSConnectivityStatus Servicios de Escritorio remoto, clase Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de clase Servicios de Escritorio remoto, método GetTStoLSConnectivityStatus
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetTStoLSConnectivityStatus
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fb73cd62c5ab5c343f44f24bbbd8de7f6343a21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491339"
---
# <a name="gettstolsconnectivitystatus-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="aa1e8-106">Método GetTStoLSConnectivityStatus de la \_ clase TerminalServiceSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="aa1e8-106">GetTStoLSConnectivityStatus method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="aa1e8-107">Determina el estado de conectividad entre Servicios de Escritorio remoto y un servidor de licencias.</span><span class="sxs-lookup"><span data-stu-id="aa1e8-107">Determines the connectivity status between Remote Desktop Services and a license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa1e8-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aa1e8-108">Syntax</span></span>


```mof
uint32 GetTStoLSConnectivityStatus(
  [in]  string ServerName,
  [out] uint32 TStoLSConnectivityStatus
);
```



## <a name="parameters"></a><span data-ttu-id="aa1e8-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aa1e8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa1e8-110">*NombreDeServidor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="aa1e8-110">*ServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa1e8-111">Nombre del servidor de licencias para comprobar el estado de conectividad.</span><span class="sxs-lookup"><span data-stu-id="aa1e8-111">The name of the license server to check the connectivity status of.</span></span>

</dd> <dt>

<span data-ttu-id="aa1e8-112">*TStoLSConnectivityStatus* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="aa1e8-112">*TStoLSConnectivityStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa1e8-113">Valor que indica el estado de Conectividad del servidor de licencias.</span><span class="sxs-lookup"><span data-stu-id="aa1e8-113">A value that indicates the connectivity status of the license server.</span></span> <span data-ttu-id="aa1e8-114">Puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="aa1e8-114">This can be one of the following values.</span></span>

<dt>

<span id="LS_CONNECTABLE_UNKNOWN"></span><span id="ls_connectable_unknown"></span>

<span data-ttu-id="aa1e8-115"><span id="LS_CONNECTABLE_UNKNOWN"></span><span id="ls_connectable_unknown"></span>**LS \_ CONNECTable \_ Unknown** (0)</span><span class="sxs-lookup"><span data-stu-id="aa1e8-115"><span id="LS_CONNECTABLE_UNKNOWN"></span><span id="ls_connectable_unknown"></span>**LS\_CONNECTABLE\_UNKNOWN** (0)</span></span>


</dt> <dd>

<span data-ttu-id="aa1e8-116">No se puede determinar el estado de conectividad.</span><span class="sxs-lookup"><span data-stu-id="aa1e8-116">The connectivity status cannot be determined.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08R2"></span><span id="ls_connectable_valid_ws08r2"></span>

<span data-ttu-id="aa1e8-117"><span id="LS_CONNECTABLE_VALID_WS08R2"></span><span id="ls_connectable_valid_ws08r2"></span>**LS \_ \_ \_ WS08R2 válido y conectable** (1)</span><span class="sxs-lookup"><span data-stu-id="aa1e8-117"><span id="LS_CONNECTABLE_VALID_WS08R2"></span><span id="ls_connectable_valid_ws08r2"></span>**LS\_CONNECTABLE\_VALID\_WS08R2** (1)</span></span>


</dt> <dd>

<span data-ttu-id="aa1e8-118">Servicios de Escritorio remoto puede conectarse al servidor de licencias de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="aa1e8-118">Remote Desktop Services can connect to the Windows Server 2008 R2 license server.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08"></span><span id="ls_connectable_valid_ws08"></span>

<span data-ttu-id="aa1e8-119"><span id="LS_CONNECTABLE_VALID_WS08"></span><span id="ls_connectable_valid_ws08"></span>**LS \_ \_ \_ WS08 válido y conectable** (2)</span><span class="sxs-lookup"><span data-stu-id="aa1e8-119"><span id="LS_CONNECTABLE_VALID_WS08"></span><span id="ls_connectable_valid_ws08"></span>**LS\_CONNECTABLE\_VALID\_WS08** (2)</span></span>


</dt> <dd>

<span data-ttu-id="aa1e8-120">Servicios de Escritorio remoto puede conectarse al servidor de licencias de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="aa1e8-120">Remote Desktop Services can connect to the Windows Server 2008 license server.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_BETA_RTM_MISMATCH"></span><span id="ls_connectable_beta_rtm_mismatch"></span>

<span data-ttu-id="aa1e8-121"><span id="LS_CONNECTABLE_BETA_RTM_MISMATCH"></span><span id="ls_connectable_beta_rtm_mismatch"></span>**LS \_ \_ \_ \_ No coincide la versión RTM de beta conectable** (3)</span><span class="sxs-lookup"><span data-stu-id="aa1e8-121"><span id="LS_CONNECTABLE_BETA_RTM_MISMATCH"></span><span id="ls_connectable_beta_rtm_mismatch"></span>**LS\_CONNECTABLE\_BETA\_RTM\_MISMATCH** (3)</span></span>


</dt> <dd>

<span data-ttu-id="aa1e8-122">Servicios de Escritorio remoto puede conectarse al servidor de licencias, pero uno de los servidores está ejecutando una versión beta del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="aa1e8-122">Remote Desktop Services can connect to the license server, but one of the servers is running a beta version of the operating system.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_LOWER_VERSION"></span><span id="ls_connectable_lower_version"></span>

<span data-ttu-id="aa1e8-123"><span id="LS_CONNECTABLE_LOWER_VERSION"></span><span id="ls_connectable_lower_version"></span>**LS \_ \_ \_ Versión más antigua conectable** (4)</span><span class="sxs-lookup"><span data-stu-id="aa1e8-123"><span id="LS_CONNECTABLE_LOWER_VERSION"></span><span id="ls_connectable_lower_version"></span>**LS\_CONNECTABLE\_LOWER\_VERSION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="aa1e8-124">Servicios de Escritorio remoto puede conectarse al servidor de licencias, pero hay una incompatibilidad entre el servidor de licencias y el servidor host de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="aa1e8-124">Remote Desktop Services can connect to the license server, but there is an incompatibility between the license server and the Remote Desktop Services host server.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_NOT_IN_TSCGROUP"></span><span id="ls_connectable_not_in_tscgroup"></span>

<span data-ttu-id="aa1e8-125"><span id="LS_CONNECTABLE_NOT_IN_TSCGROUP"></span><span id="ls_connectable_not_in_tscgroup"></span>**LS \_ CONNECTable \_ no está \_ en \_ TSCGROUP** (5)</span><span class="sxs-lookup"><span data-stu-id="aa1e8-125"><span id="LS_CONNECTABLE_NOT_IN_TSCGROUP"></span><span id="ls_connectable_not_in_tscgroup"></span>**LS\_CONNECTABLE\_NOT\_IN\_TSCGROUP** (5)</span></span>


</dt> <dd>

<span data-ttu-id="aa1e8-126">La Directiva de grupo de seguridad está habilitada en el servidor de licencias, pero Servicios de Escritorio remoto no es parte de la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="aa1e8-126">Security group policy is enabled in license server, but Remote Desktop Services is not a part of the group policy.</span></span>

</dd> <dt>

<span id="LS_NOT_CONNECTABLE"></span><span id="ls_not_connectable"></span>

<span data-ttu-id="aa1e8-127"><span id="LS_NOT_CONNECTABLE"></span><span id="ls_not_connectable"></span>**LS \_ NO \_ conectable** (6)</span><span class="sxs-lookup"><span data-stu-id="aa1e8-127"><span id="LS_NOT_CONNECTABLE"></span><span id="ls_not_connectable"></span>**LS\_NOT\_CONNECTABLE** (6)</span></span>


</dt> <dd>

<span data-ttu-id="aa1e8-128">Servicios de Escritorio remoto no se puede conectar al servidor de licencias.</span><span class="sxs-lookup"><span data-stu-id="aa1e8-128">Remote Desktop Services cannot connect to the license server.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_UNKNOWN_VALIDITY"></span><span id="ls_connectable_unknown_validity"></span>

<span data-ttu-id="aa1e8-129"><span id="LS_CONNECTABLE_UNKNOWN_VALIDITY"></span><span id="ls_connectable_unknown_validity"></span>**LS \_ \_ \_ Validez desconocida conectable** (7)</span><span class="sxs-lookup"><span data-stu-id="aa1e8-129"><span id="LS_CONNECTABLE_UNKNOWN_VALIDITY"></span><span id="ls_connectable_unknown_validity"></span>**LS\_CONNECTABLE\_UNKNOWN\_VALIDITY** (7)</span></span>


</dt> <dd>

<span data-ttu-id="aa1e8-130">El servidor de licencias puede conectarse a, pero no se puede determinar la validez de la conexión.</span><span class="sxs-lookup"><span data-stu-id="aa1e8-130">The license server can be connected to, but the validity of the connection cannot be determined.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_BUT_ACCESS_DENIED"></span><span id="ls_connectable_but_access_denied"></span>

<span data-ttu-id="aa1e8-131"><span id="LS_CONNECTABLE_BUT_ACCESS_DENIED"></span><span id="ls_connectable_but_access_denied"></span>**LS \_ CONNECTable \_ pero \_ acceso \_ denegado** (8)</span><span class="sxs-lookup"><span data-stu-id="aa1e8-131"><span id="LS_CONNECTABLE_BUT_ACCESS_DENIED"></span><span id="ls_connectable_but_access_denied"></span>**LS\_CONNECTABLE\_BUT\_ACCESS\_DENIED** (8)</span></span>


</dt> <dd>

<span data-ttu-id="aa1e8-132">Servicios de Escritorio remoto puede conectarse al servidor de licencias, pero la cuenta de usuario no tiene privilegios de administrador en el servidor de licencias.</span><span class="sxs-lookup"><span data-stu-id="aa1e8-132">Remote Desktop Services can connect to the license server, but the user account does not have administrator privileges on the license server.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08R2_VDI"></span><span id="ls_connectable_valid_ws08r2_vdi"></span>

<span data-ttu-id="aa1e8-133"><span id="LS_CONNECTABLE_VALID_WS08R2_VDI"></span><span id="ls_connectable_valid_ws08r2_vdi"></span>**LS \_ CONNECTable \_ \_ WS08R2 válido \_** (9)</span><span class="sxs-lookup"><span data-stu-id="aa1e8-133"><span id="LS_CONNECTABLE_VALID_WS08R2_VDI"></span><span id="ls_connectable_valid_ws08r2_vdi"></span>**LS\_CONNECTABLE\_VALID\_WS08R2\_VDI** (9)</span></span>


</dt> <dd>

<span data-ttu-id="aa1e8-134">Servicios de Escritorio remoto puede conectarse al servidor de infraestructura de escritorio virtual (VDI) de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="aa1e8-134">Remote Desktop Services can connect to the Windows Server 2008 R2 Virtual Desktop Infrastructure (VDI) server.</span></span>

<span data-ttu-id="aa1e8-135">**Windows Server 2008 R2:** Este valor no se admite antes de Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="aa1e8-135">**Windows Server 2008 R2:** This value is not supported before Windows Server 2012.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_FEATURE_NOT_SUPPORTED"></span><span id="ls_connectable_feature_not_supported"></span>

<span data-ttu-id="aa1e8-136"><span id="LS_CONNECTABLE_FEATURE_NOT_SUPPORTED"></span><span id="ls_connectable_feature_not_supported"></span>**LS \_ No se \_ \_ \_ admite la característica conectable** (10)</span><span class="sxs-lookup"><span data-stu-id="aa1e8-136"><span id="LS_CONNECTABLE_FEATURE_NOT_SUPPORTED"></span><span id="ls_connectable_feature_not_supported"></span>**LS\_CONNECTABLE\_FEATURE\_NOT\_SUPPORTED** (10)</span></span>


</dt> <dd>

<span data-ttu-id="aa1e8-137">No se admite la característica.</span><span class="sxs-lookup"><span data-stu-id="aa1e8-137">The feature is not supported.</span></span>

<span data-ttu-id="aa1e8-138">**Windows server 2008 R2 y Windows server 2008 R2 con SP1:** Este valor no se admite antes de Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="aa1e8-138">**Windows Server 2008 R2 and Windows Server 2008 R2 with SP1:** This value is not supported before Windows Server 2012.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_LS"></span><span id="ls_connectable_valid_ls"></span>

<span data-ttu-id="aa1e8-139"><span id="LS_CONNECTABLE_VALID_LS"></span><span id="ls_connectable_valid_ls"></span>**LS \_ CONNECTable \_ válido \_ LS** (11)</span><span class="sxs-lookup"><span data-stu-id="aa1e8-139"><span id="LS_CONNECTABLE_VALID_LS"></span><span id="ls_connectable_valid_ls"></span>**LS\_CONNECTABLE\_VALID\_LS** (11)</span></span>


</dt> <dd>

<span data-ttu-id="aa1e8-140">El servidor de licencias es válido.</span><span class="sxs-lookup"><span data-stu-id="aa1e8-140">The license server is valid.</span></span>

<span data-ttu-id="aa1e8-141">**Windows server 2008 R2 y Windows server 2008 R2 con SP1:** Este valor no se admite antes de Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="aa1e8-141">**Windows Server 2008 R2 and Windows Server 2008 R2 with SP1:** This value is not supported before Windows Server 2012.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa1e8-142">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aa1e8-142">Return value</span></span>

<span data-ttu-id="aa1e8-143">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="aa1e8-143">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="aa1e8-144">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="aa1e8-144">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa1e8-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa1e8-145">Requirements</span></span>



| <span data-ttu-id="aa1e8-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa1e8-146">Requirement</span></span> | <span data-ttu-id="aa1e8-147">Value</span><span class="sxs-lookup"><span data-stu-id="aa1e8-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa1e8-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa1e8-148">Minimum supported client</span></span><br/> | <span data-ttu-id="aa1e8-149">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="aa1e8-149">None supported</span></span><br/>                                                               |
| <span data-ttu-id="aa1e8-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa1e8-150">Minimum supported server</span></span><br/> | <span data-ttu-id="aa1e8-151">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="aa1e8-151">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="aa1e8-152">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="aa1e8-152">Namespace</span></span><br/>                | <span data-ttu-id="aa1e8-153">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="aa1e8-153">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="aa1e8-154">MOF</span><span class="sxs-lookup"><span data-stu-id="aa1e8-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aa1e8-155"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aa1e8-155"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="aa1e8-156">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="aa1e8-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa1e8-157"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa1e8-157"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa1e8-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="aa1e8-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa1e8-159">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="aa1e8-159">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

 





