---
title: Método ModifyAuditPermissions de la clase Win32_TSAccount
description: Prepara para establecer un conjunto más granular de permisos de auditoría en la cuenta especificada.
ms.assetid: 7df44a37-257d-49c6-8193-f1e1c5ebbb57
ms.tgt_platform: multiple
keywords:
- Método ModifyAuditPermissions Servicios de Escritorio remoto
- Método ModifyAuditPermissions Servicios de Escritorio remoto, clase Win32_TSAccount
- Win32_TSAccount de clase Servicios de Escritorio remoto, método ModifyAuditPermissions
topic_type:
- apiref
api_name:
- Win32_TSAccount.ModifyAuditPermissions
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f19337cc6110a15b206fc437fb6ec594ded60640
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905564"
---
# <a name="modifyauditpermissions-method-of-the-win32_tsaccount-class"></a><span data-ttu-id="a8308-106">Método ModifyAuditPermissions de la \_ clase TSAccount de Win32</span><span class="sxs-lookup"><span data-stu-id="a8308-106">ModifyAuditPermissions method of the Win32\_TSAccount class</span></span>

<span data-ttu-id="a8308-107">El método **ModifyAuditPermissions** se prepara para establecer un conjunto más granular de permisos de auditoría en la cuenta especificada.</span><span class="sxs-lookup"><span data-stu-id="a8308-107">The **ModifyAuditPermissions** method prepares to set a more granular set of audit permissions to the specified account.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8308-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a8308-108">Syntax</span></span>


```mof
uint32 ModifyAuditPermissions(
  [in] uint32  PermissionMask,
  [in] boolean Success
);
```



## <a name="parameters"></a><span data-ttu-id="a8308-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a8308-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8308-110">*PermissionMask* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a8308-110">*PermissionMask* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8308-111">Conjunto de [permisos de host de sesión escritorio remoto](terminal-services-permissions.md) que se van a asociar a la cuenta especificada.</span><span class="sxs-lookup"><span data-stu-id="a8308-111">The set of [Remote Desktop Session Host Permissions](terminal-services-permissions.md) to associate with the specified account.</span></span> <span data-ttu-id="a8308-112">El valor de este parámetro es un mapa de bits y se puede seleccionar uno o todos los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="a8308-112">The value of this parameter is a bitmap, and any or all of the following values may be selected.</span></span>

<dt>

<span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>

<span data-ttu-id="a8308-113"><span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>**Estación \_ de CONSULTA** (0)</span><span class="sxs-lookup"><span data-stu-id="a8308-113"><span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>**WINSTATION\_QUERY** (0)</span></span>


</dt> <dd>

<span data-ttu-id="a8308-114">Permiso para consultar información acerca de una sesión.</span><span class="sxs-lookup"><span data-stu-id="a8308-114">Permission to query information about a session.</span></span>

</dd> <dt>

<span id="WINSTATION_SET"></span><span id="winstation_set"></span>

<span data-ttu-id="a8308-115"><span id="WINSTATION_SET"></span><span id="winstation_set"></span>**Estación \_ de CONJUNTO** (1)</span><span class="sxs-lookup"><span data-stu-id="a8308-115"><span id="WINSTATION_SET"></span><span id="winstation_set"></span>**WINSTATION\_SET** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a8308-116">Permiso para modificar los parámetros de conexión.</span><span class="sxs-lookup"><span data-stu-id="a8308-116">Permission to modify connection parameters.</span></span>

</dd> <dt>

<span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>

<span data-ttu-id="a8308-117"><span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**Estación \_ de RESTABLECER** (6)</span><span class="sxs-lookup"><span data-stu-id="a8308-117"><span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**WINSTATION\_RESET** (6)</span></span>


</dt> <dd>

<span data-ttu-id="a8308-118">Permiso para restablecer o finalizar una sesión o una conexión.</span><span class="sxs-lookup"><span data-stu-id="a8308-118">Permission to reset or end a session or connection.</span></span>

</dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>

<span data-ttu-id="a8308-119"><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**Estación \_ de Se \| \_ \_ requieren derechos de estándar virtual** (3)</span><span class="sxs-lookup"><span data-stu-id="a8308-119"><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**WINSTATION\_VIRTUAL \| STANDARD\_RIGHTS\_REQUIRED** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a8308-120">Permiso para usar canales virtuales.</span><span class="sxs-lookup"><span data-stu-id="a8308-120">Permission to use virtual channels.</span></span> <span data-ttu-id="a8308-121">Los canales virtuales proporcionan acceso desde un programa de servidor a los dispositivos cliente.</span><span class="sxs-lookup"><span data-stu-id="a8308-121">Virtual channels provide access from a server program to client devices.</span></span>

</dd> <dt>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>

<span data-ttu-id="a8308-122"><span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**Estación \_ de SOMBRA** (4)</span><span class="sxs-lookup"><span data-stu-id="a8308-122"><span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**WINSTATION\_SHADOW** (4)</span></span>


</dt> <dd>

<span data-ttu-id="a8308-123">Permiso para sombra o control remoto de la sesión de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="a8308-123">Permission to shadow or remotely control another user's session.</span></span>

</dd> <dt>

<span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>

<span data-ttu-id="a8308-124"><span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**Estación \_ de Inicio de sesión** (5)</span><span class="sxs-lookup"><span data-stu-id="a8308-124"><span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**WINSTATION\_LOGON** (5)</span></span>


</dt> <dd>

<span data-ttu-id="a8308-125">Permiso para iniciar sesión en una sesión en el servidor.</span><span class="sxs-lookup"><span data-stu-id="a8308-125">Permission to log on to a session on the server.</span></span>

</dd> <dt>

<span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>

<span data-ttu-id="a8308-126"><span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**Estación \_ de CERRAR sesión** (2)</span><span class="sxs-lookup"><span data-stu-id="a8308-126"><span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**WINSTATION\_LOGOFF** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a8308-127">Permiso para cerrar la sesión de un usuario.</span><span class="sxs-lookup"><span data-stu-id="a8308-127">Permission to log off a user from a session.</span></span>

</dd> <dt>

<span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>

<span data-ttu-id="a8308-128"><span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**Estación \_ de MENSAJE** (7)</span><span class="sxs-lookup"><span data-stu-id="a8308-128"><span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**WINSTATION\_MSG** (7)</span></span>


</dt> <dd>

<span data-ttu-id="a8308-129">Permiso para enviar un mensaje a la sesión de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="a8308-129">Permission to send a message to another user's session.</span></span>

</dd> <dt>

<span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>

<span data-ttu-id="a8308-130"><span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**Estación \_ de CONECTAR** (8)</span><span class="sxs-lookup"><span data-stu-id="a8308-130"><span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**WINSTATION\_CONNECT** (8)</span></span>


</dt> <dd>

<span data-ttu-id="a8308-131">Permiso para conectarse a otra sesión.</span><span class="sxs-lookup"><span data-stu-id="a8308-131">Permission to connect to another session.</span></span>

</dd> <dt>

<span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>

<span data-ttu-id="a8308-132"><span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**Estación \_ de DESCONECTAR** (9)</span><span class="sxs-lookup"><span data-stu-id="a8308-132"><span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**WINSTATION\_DISCONNECT** (9)</span></span>


</dt> <dd>

<span data-ttu-id="a8308-133">Permiso para desconectar una sesión.</span><span class="sxs-lookup"><span data-stu-id="a8308-133">Permission to disconnect a session.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a8308-134">*Correcto* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a8308-134">*Success* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8308-135">Especifica si se permite o se deniega el conjunto de permisos especificado por el valor del parámetro *PermissionMask* .</span><span class="sxs-lookup"><span data-stu-id="a8308-135">Specifies if the permission set specified by the value of the *PermissionMask* parameter is allowed or denied.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="a8308-136"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="a8308-136"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="a8308-137">Se permite el conjunto de permisos especificado.</span><span class="sxs-lookup"><span data-stu-id="a8308-137">The specified permission set is allowed.</span></span>

</dd> <dt>

<span id="0"></span>

<span data-ttu-id="a8308-138"><span id="0"></span>**0,1**</span><span class="sxs-lookup"><span data-stu-id="a8308-138"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="a8308-139">Se denegó el conjunto de permisos especificado.</span><span class="sxs-lookup"><span data-stu-id="a8308-139">The specified permission set is denied.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8308-140">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a8308-140">Return value</span></span>

<span data-ttu-id="a8308-141">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="a8308-141">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="a8308-142">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="a8308-142">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8308-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a8308-143">Remarks</span></span>

<span data-ttu-id="a8308-144">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="a8308-144">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a8308-145">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="a8308-145">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a8308-146">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="a8308-146">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a8308-147">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="a8308-147">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a8308-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8308-148">Requirements</span></span>



| <span data-ttu-id="a8308-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8308-149">Requirement</span></span> | <span data-ttu-id="a8308-150">Value</span><span class="sxs-lookup"><span data-stu-id="a8308-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8308-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8308-151">Minimum supported client</span></span><br/> | <span data-ttu-id="a8308-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a8308-152">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a8308-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8308-153">Minimum supported server</span></span><br/> | <span data-ttu-id="a8308-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a8308-154">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a8308-155">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a8308-155">Namespace</span></span><br/>                | <span data-ttu-id="a8308-156">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="a8308-156">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="a8308-157">MOF</span><span class="sxs-lookup"><span data-stu-id="a8308-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a8308-158"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a8308-158"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="a8308-159">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a8308-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8308-160"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8308-160"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8308-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8308-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8308-162">**Win32 \_ TSAccount**</span><span class="sxs-lookup"><span data-stu-id="a8308-162">**Win32\_TSAccount**</span></span>](win32-tsaccount.md)
</dt> </dl>

 

