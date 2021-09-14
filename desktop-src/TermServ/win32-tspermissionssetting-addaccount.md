---
title: Método AddAccount de la Win32_TSPermissionsSetting (Faxcomex.h)
description: El método AddAccount se prepara para agregar una cuenta al terminal con el conjunto de permisos especificado. Puede agregar usuarios, grupos o equipos.
ms.assetid: da4d8f5b-7aa2-4b55-bf0f-b3e98b70a06b
ms.tgt_platform: multiple
keywords:
- Método AddAccount Servicios de Escritorio remoto
- Método AddAccount Servicios de Escritorio remoto , Win32_TSPermissionsSetting clase
- Win32_TSPermissionsSetting clase Servicios de Escritorio remoto , método AddAccount
topic_type:
- apiref
api_name:
- Win32_TSPermissionsSetting.AddAccount
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de89c34bd7aab20fbfbcbdedfd9d2f91bba866bc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127243447"
---
# <a name="addaccount-method-of-the-win32_tspermissionssetting-class"></a>Método AddAccount de la \_ clase TSPermissionsSetting de Win32

El **método AddAccount** se prepara para agregar una cuenta al terminal con el conjunto de permisos especificado. Puede agregar usuarios, grupos o equipos.

## <a name="syntax"></a>Sintaxis


```mof
uint32 AddAccount(
  [in] string AccountName,
  [in] uint32 PermissionPreSet
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AccountName* \[ En\]
</dt> <dd>

Nombre de la cuenta que se agregará al terminal.

</dd> <dt>

*PermissionPreSet* \[ En\]
</dt> <dd>

Conjunto de permisos que se asociará a la cuenta especificada. Este parámetro puede ser cualquiera o todos los valores siguientes. Para obtener más información, [vea Servicios de Escritorio remoto Permissions](terminal-services-permissions.md).

<dt>

<span id="WINSTATION_GUEST_ACCESS"></span><span id="winstation_guest_access"></span>

<span id="WINSTATION_GUEST_ACCESS"></span><span id="winstation_guest_access"></span>**WINSTATION \_ ACCESO \_ DE INVITADO** (0)


</dt> <dd>

La cuenta tiene permiso de inicio de sesión.

</dd> <dt>

<span id="WINSTATION_USER_ACCESS"></span><span id="winstation_user_access"></span>

<span id="WINSTATION_USER_ACCESS"></span><span id="winstation_user_access"></span>**WINSTATION \_ ACCESO \_ DE USUARIO** (1)


</dt> <dd>

La cuenta tiene los permisos siguientes: Inicio de sesión, Información de consulta, Enviar mensaje y Conectar.

</dd> <dt>

<span id="WINSTATION_ALL_ACCESS"></span><span id="winstation_all_access"></span>

<span id="WINSTATION_ALL_ACCESS"></span><span id="winstation_all_access"></span>**WINSTATION \_ ALL \_ ACCESS** (2)


</dt> <dd>

La cuenta tiene todos Servicios de Escritorio remoto permisos.

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
| Encabezado<br/>                   | <dl> <dt>Faxcomex.h</dt> </dl>   |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSPermissionsSetting**](win32-tspermissionssetting.md)
</dt> </dl>

 

