---
title: Método RestoreDefaults de la Win32_TSPermissionsSetting (Netfw.h)
description: Restaura los valores predeterminados del conjunto de permisos para el terminal.
ms.assetid: bdd01290-7c7c-4355-85dc-ade51b2abd94
ms.tgt_platform: multiple
keywords:
- Método RestoreDefaults Servicios de Escritorio remoto
- Método RestoreDefaults Servicios de Escritorio remoto , Win32_TSPermissionsSetting clase
- Win32_TSPermissionsSetting clase Servicios de Escritorio remoto , método RestoreDefaults
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
ms.openlocfilehash: 8ef81f4b3008f68129026a90d1b2e98e8c13c298537952175e116c9c8e02c4f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769455"
---
# <a name="restoredefaults-method-of-the-win32_tspermissionssetting-class"></a>Método RestoreDefaults de la \_ clase TSPermissionsSetting de Win32

El **método RestoreDefaults** restaura los valores predeterminados del conjunto de permisos para el terminal.

## <a name="syntax"></a>Sintaxis


```mof
uint32 RestoreDefaults();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve Correcto si se ejecuta correctamente; de lo contrario, Error.

## <a name="remarks"></a>Comentarios

Los permisos predeterminados son los siguientes:

-   Las cuentas administradores, sistema y Escritorio remoto asistente de ayuda tienen [todos Servicios de Escritorio remoto permisos](terminal-services-permissions.md).
-   La Escritorio remoto usuarios tiene el permiso Logon, Conectar, Query Information y Send Message.
-   Las cuentas Servicio local y Servicio de red tienen información de consulta y permiso Enviar mensaje.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del Kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\TerminalServices de CIMv2 \\ raíz<br/>                                                |
| Header<br/>                   | <dl> <dt>Netfw.h</dt> </dl>      |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSPermissionsSetting**](win32-tspermissionssetting.md)
</dt> </dl>

 

