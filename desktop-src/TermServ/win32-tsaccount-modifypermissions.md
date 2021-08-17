---
title: Método ModifyPermissions de la Win32_TSAccount clase
description: Establece un permiso para la cuenta especificada.
ms.assetid: cef36f7f-d327-4bb6-9bff-282036c1a5d5
ms.tgt_platform: multiple
keywords:
- Método ModifyPermissions Servicios de Escritorio remoto
- Método ModifyPermissions Servicios de Escritorio remoto , Win32_TSAccount clase
- Win32_TSAccount clase Servicios de Escritorio remoto método , ModifyPermissions
topic_type:
- apiref
api_name:
- Win32_TSAccount.ModifyPermissions
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6265290fa3604c426609f51d0518f1f6762ea02718757d86ff9ed69b10bd018
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119421675"
---
# <a name="modifypermissions-method-of-the-win32_tsaccount-class"></a>Método ModifyPermissions de la clase TSAccount de Win32 \_

Establece un permiso para la cuenta especificada.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ModifyPermissions(
  [in] uint32  PermissionMask,
  [in] boolean Allow
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PermissionMask* \[ En\]
</dt> <dd>

El [Escritorio remoto host de sesión que se establece.](terminal-services-permissions.md)

Los valores posibles son:

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

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**WINSTATION \_ DERECHOS \| ESTÁNDAR \_ VIRTUALES \_ REQUERIDOS** (3)


</dt> <dd>

Permiso para usar canales virtuales. Los canales virtuales proporcionan acceso desde un programa de servidor a los dispositivos cliente.

</dd> <dt>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**WINSTATION \_ SHADOW** (4)


</dt> <dd>

Permiso para sombrar o controlar de forma remota la sesión de otro usuario.

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

*Permitir* \[ En\]
</dt> <dd>

Especifica si se permite o se deniega el permiso en el parámetro *PermissionMask.*

Los valores posibles son:

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

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.

## <a name="remarks"></a>Observaciones

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\TerminalServices de CIMv2 \\ raíz<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSAccount**](win32-tsaccount.md)
</dt> </dl>

 

