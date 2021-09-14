---
title: Método ModifyAuditPermissions de la Win32_TSAccount clase
description: Se prepara para establecer un conjunto más granular de permisos de auditoría en la cuenta especificada.
ms.assetid: 7df44a37-257d-49c6-8193-f1e1c5ebbb57
ms.tgt_platform: multiple
keywords:
- Método ModifyAuditPermissions Servicios de Escritorio remoto
- Método ModifyAuditPermissions Servicios de Escritorio remoto , Win32_TSAccount clase
- Win32_TSAccount clase Servicios de Escritorio remoto método , ModifyAuditPermissions
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967932"
---
# <a name="modifyauditpermissions-method-of-the-win32_tsaccount-class"></a>Método ModifyAuditPermissions de la clase TSAccount de Win32 \_

El **método ModifyAuditPermissions** se prepara para establecer un conjunto más granular de permisos de auditoría en la cuenta especificada.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ModifyAuditPermissions(
  [in] uint32  PermissionMask,
  [in] boolean Success
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PermissionMask* \[ En\]
</dt> <dd>

Conjunto de permisos [Escritorio remoto host de sesión que se](terminal-services-permissions.md) asocian a la cuenta especificada. El valor de este parámetro es un mapa de bits y se pueden seleccionar cualquiera o todos los valores siguientes.

<dt>

<span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>

<span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>**WINSTATION \_ QUERY** (0)


</dt> <dd>

Permiso para consultar información sobre una sesión.

</dd> <dt>

<span id="WINSTATION_SET"></span><span id="winstation_set"></span>

<span id="WINSTATION_SET"></span><span id="winstation_set"></span>**WINSTATION \_ SET** (1)


</dt> <dd>

Permiso para modificar parámetros de conexión.

</dd> <dt>

<span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>

<span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**WINSTATION \_ RESET** (6)


</dt> <dd>

Permiso para restablecer o finalizar una sesión o conexión.

</dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**WINSTATION \_ DERECHOS \| ESTÁNDAR \_ VIRTUALES \_ NECESARIOS** (3)


</dt> <dd>

Permiso para usar canales virtuales. Los canales virtuales proporcionan acceso desde un programa de servidor a los dispositivos cliente.

</dd> <dt>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**WINSTATION \_ SHADOW** (4)


</dt> <dd>

Permiso para crear sombras o controlar de forma remota la sesión de otro usuario.

</dd> <dt>

<span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>

<span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**WINSTATION \_ LOGON** (5)


</dt> <dd>

Permiso para iniciar sesión en una sesión en el servidor.

</dd> <dt>

<span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>

<span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**WINSTATION \_ LOGOFF** (2)


</dt> <dd>

Permiso para cerrar la sesión de un usuario.

</dd> <dt>

<span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>

<span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**WINSTATION \_ MSG** (7)


</dt> <dd>

Permiso para enviar un mensaje a la sesión de otro usuario.

</dd> <dt>

<span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>

<span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**WINSTATION \_ CONNECT** (8)


</dt> <dd>

Permiso para conectarse a otra sesión.

</dd> <dt>

<span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>

<span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**WINSTATION \_ DISCONNECT** (9)


</dt> <dd>

Permiso para desconectar una sesión.

</dd> </dl> </dd> <dt>

*Correcto* \[ En\]
</dt> <dd>

Especifica si se permite o deniega el conjunto de permisos especificado por el valor del parámetro *PermissionMask.*

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Se permite el conjunto de permisos especificado.

</dd> <dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Se deniega el conjunto de permisos especificado.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error WMI. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.

## <a name="remarks"></a>Observaciones

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Win32 \_ TSAccount**](win32-tsaccount.md)
</dt> </dl>

 

