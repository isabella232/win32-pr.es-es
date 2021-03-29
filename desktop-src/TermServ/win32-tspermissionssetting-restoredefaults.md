---
title: Método RestoreDefaults de la clase Win32_TSPermissionsSetting (Netfw. h)
description: Restaura los valores del conjunto de permisos predeterminados para el terminal.
ms.assetid: bdd01290-7c7c-4355-85dc-ade51b2abd94
ms.tgt_platform: multiple
keywords:
- Método RestoreDefaults Servicios de Escritorio remoto
- Método RestoreDefaults Servicios de Escritorio remoto, clase Win32_TSPermissionsSetting
- Win32_TSPermissionsSetting de clase Servicios de Escritorio remoto, método RestoreDefaults
topic_type:
- apiref
api_name:
- Win32_TSPermissionsSetting.RestoreDefaults
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 073a8f8267ab9e7f7cbd50f15f4f3f20594d2e39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905152"
---
# <a name="restoredefaults-method-of-the-win32_tspermissionssetting-class"></a>Método RestoreDefaults de la \_ clase TSPermissionsSetting de Win32

El método **RestoreDefaults** restaura los valores del conjunto de permisos predeterminados para el terminal.

## <a name="syntax"></a>Sintaxis


```mof
uint32 RestoreDefaults();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve SUCCESS si se realizó correctamente; de lo contrario, error.

## <a name="remarks"></a>Observaciones

Los permisos predeterminados son los siguientes:

-   Los administradores, el sistema y Escritorio remoto las cuentas del asistente de ayuda tienen todos los [permisos de servicios de escritorio remoto](terminal-services-permissions.md).
-   La cuenta de Escritorio remoto usuarios tiene el permiso de inicio de sesión, conexión, información de consulta y envío de mensaje.
-   Las cuentas servicio local y servicio de red tienen información de consulta y el permiso enviar mensaje.

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>Netfw. h</dt> </dl>      |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSPermissionsSetting**](win32-tspermissionssetting.md)
</dt> </dl>

 

