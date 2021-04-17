---
title: Método ModifyPermissions de la clase Win32_TSAccount
description: Establece un permiso para la cuenta especificada.
ms.assetid: cef36f7f-d327-4bb6-9bff-282036c1a5d5
ms.tgt_platform: multiple
keywords:
- Método ModifyPermissions Servicios de Escritorio remoto
- Método ModifyPermissions Servicios de Escritorio remoto, clase Win32_TSAccount
- Win32_TSAccount de clase Servicios de Escritorio remoto, método ModifyPermissions
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
ms.openlocfilehash: c4bf6147c215475314f65bb8fa426442884bc82e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676724"
---
# <a name="modifypermissions-method-of-the-win32_tsaccount-class"></a>Método ModifyPermissions de la \_ clase TSAccount de Win32

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

*PermissionMask* \[ de\]
</dt> <dd>

[Permiso de host de sesión escritorio remoto](terminal-services-permissions.md) que se va a establecer.

Los valores posibles son:

<dt>

<span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>

<span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>**Estación \_ de CONSULTA** (0)


</dt> <dd>

Permiso para consultar información acerca de una sesión.

</dd> <dt>

<span id="WINSTATION_SET"></span><span id="winstation_set"></span>

<span id="WINSTATION_SET"></span><span id="winstation_set"></span>**Estación \_ de CONJUNTO** (1)


</dt> <dd>

Permiso para modificar los parámetros de conexión.

</dd> <dt>

<span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>

<span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**Estación \_ de RESTABLECER** (6)


</dt> <dd>

Permiso para restablecer o finalizar una sesión o una conexión.

</dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**Estación \_ de Se \| \_ \_ requieren derechos de estándar virtual** (3)


</dt> <dd>

Permiso para usar canales virtuales. Los canales virtuales proporcionan acceso desde un programa de servidor a los dispositivos cliente.

</dd> <dt>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**Estación \_ de SOMBRA** (4)


</dt> <dd>

Permiso para sombra o control remoto de la sesión de otro usuario.

</dd> <dt>

<span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>

<span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**Estación \_ de Inicio de sesión** (5)


</dt> <dd>

Permiso para iniciar sesión en una sesión en el servidor.

</dd> <dt>

<span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>

<span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**Estación \_ de CERRAR sesión** (2)


</dt> <dd>

Permiso para cerrar la sesión de un usuario.

</dd> <dt>

<span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>

<span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**Estación \_ de MENSAJE** (7)


</dt> <dd>

Permiso para enviar un mensaje a la sesión de otro usuario.

</dd> <dt>

<span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>

<span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**Estación \_ de CONECTAR** (8)


</dt> <dd>

Permiso para conectarse a otra sesión.

</dd> <dt>

<span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>

<span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**Estación \_ de DESCONECTAR** (9)


</dt> <dd>

Permiso para desconectar una sesión.

</dd> </dl> </dd> <dt>

*Permitir* \[ de\]
</dt> <dd>

Especifica si se permite o se deniega el permiso en el parámetro *PermissionMask* .

Los valores posibles son:

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Se permite el conjunto de permisos especificado.

</dd> <dt>

<span id="0"></span>

<span id="0"></span>**0,1**


</dt> <dd>

Se denegó el conjunto de permisos especificado.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI. Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.

## <a name="remarks"></a>Observaciones

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSAccount**](win32-tsaccount.md)
</dt> </dl>

 

