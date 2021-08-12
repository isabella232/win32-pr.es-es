---
title: Método ChangeMode de la Win32_TerminalServiceSetting clase
description: El método ChangeMode establece el tipo de licencia del servidor Escritorio remoto de sesión actual (host de sesión de Escritorio remoto).
ms.assetid: 293483ee-51ce-4cd4-ba13-6c7c02bbdbbf
ms.tgt_platform: multiple
keywords:
- Método ChangeMode Servicios de Escritorio remoto
- Método ChangeMode Servicios de Escritorio remoto , Win32_TerminalServiceSetting clase
- Win32_TerminalServiceSetting clase Servicios de Escritorio remoto método , ChangeMode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.ChangeMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2812dd459e13922b1745e55355972092091b4fd9521bc41a46da40769c02021d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118604044"
---
# <a name="changemode-method-of-the-win32_terminalservicesetting-class"></a>Método ChangeMode de la clase \_ TerminalServiceSetting de Win32

El **método ChangeMode** establece el tipo de licencia del servidor Escritorio remoto de sesión actual (host de sesión de Escritorio remoto).

## <a name="syntax"></a>Sintaxis


```mof
uint32 ChangeMode(
  [in] uint32 LicensingType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*LicensingType* \[ En\]
</dt> <dd>

Tipo de licencia que se establece en función del modo de servidor host de sesión de Escritorio remoto.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Servidor host de sesión de Escritorio remoto personal.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Escritorio remoto para la administración.

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Por dispositivo/por puesto. Válido para servidores de aplicaciones.

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4**


</dt> <dd>

Por usuario. Válido para servidores de aplicaciones.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\TerminalServices de CIMv2 \\ raíz<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TerminalServiceSetting de Win32 \_**](win32-terminalservicesetting.md)
</dt> </dl>

 

