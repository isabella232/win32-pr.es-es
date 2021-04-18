---
title: Método AddAccount de la clase Win32_TSPermissionsSetting (Faxcomex. h)
description: El método AddAccount se prepara para agregar una cuenta al terminal con el conjunto de permisos especificado. Puede Agregar usuarios, grupos o equipos.
ms.assetid: da4d8f5b-7aa2-4b55-bf0f-b3e98b70a06b
ms.tgt_platform: multiple
keywords:
- Método AddAccount Servicios de Escritorio remoto
- Método AddAccount Servicios de Escritorio remoto, clase Win32_TSPermissionsSetting
- Win32_TSPermissionsSetting de clase Servicios de Escritorio remoto, método AddAccount
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491590"
---
# <a name="addaccount-method-of-the-win32_tspermissionssetting-class"></a>Método AddAccount de la \_ clase TSPermissionsSetting de Win32

El método **AddAccount** se prepara para agregar una cuenta al terminal con el conjunto de permisos especificado. Puede Agregar usuarios, grupos o equipos.

## <a name="syntax"></a>Sintaxis


```mof
uint32 AddAccount(
  [in] string AccountName,
  [in] uint32 PermissionPreSet
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AccountName* \[ de\]
</dt> <dd>

Nombre de la cuenta que se va a agregar al terminal.

</dd> <dt>

*PermissionPreSet* \[ de\]
</dt> <dd>

Conjunto de permisos que se va a asociar a la cuenta especificada. Este parámetro puede ser uno o todos los valores siguientes. Para obtener más información, vea [permisos de servicios de escritorio remoto](terminal-services-permissions.md).

<dt>

<span id="WINSTATION_GUEST_ACCESS"></span><span id="winstation_guest_access"></span>

<span id="WINSTATION_GUEST_ACCESS"></span><span id="winstation_guest_access"></span>**Estación \_ de \_Acceso de invitado** (0)


</dt> <dd>

La cuenta tiene permiso de inicio de sesión.

</dd> <dt>

<span id="WINSTATION_USER_ACCESS"></span><span id="winstation_user_access"></span>

<span id="WINSTATION_USER_ACCESS"></span><span id="winstation_user_access"></span>**Estación \_ de \_Acceso de usuario** (1)


</dt> <dd>

La cuenta tiene los siguientes permisos: Inicio de sesión, información de consulta, enviar mensaje y conectar.

</dd> <dt>

<span id="WINSTATION_ALL_ACCESS"></span><span id="winstation_all_access"></span>

<span id="WINSTATION_ALL_ACCESS"></span><span id="winstation_all_access"></span>**Estación \_ de TODO el \_ acceso** (2)


</dt> <dd>

La cuenta tiene todos los permisos de Servicios de Escritorio remoto.

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
| Encabezado<br/>                   | <dl> <dt>Faxcomex. h</dt> </dl>   |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSPermissionsSetting**](win32-tspermissionssetting.md)
</dt> </dl>

 

