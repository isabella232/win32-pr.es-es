---
title: Método SetSingleSession de la Win32_TerminalServiceSetting clase
description: El método SetSingleSession establece la propiedad SingleSession para la clase .
ms.assetid: 67ccfa9d-86a5-4501-9d61-c7f1677ec3d5
ms.tgt_platform: multiple
keywords:
- Método SetSingleSession Servicios de Escritorio remoto
- Método SetSingleSession Servicios de Escritorio remoto , Win32_TerminalServiceSetting clase
- Win32_TerminalServiceSetting clase Servicios de Escritorio remoto , método SetSingleSession
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetSingleSession
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40a6ff702020b7682938b7174c65623eba30076a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967943"
---
# <a name="setsinglesession-method-of-the-win32_terminalservicesetting-class"></a>Método SetSingleSession de la clase TerminalServiceSetting de Win32 \_

El **método SetSingleSession** establece la **propiedad SingleSession** para la clase .

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetSingleSession(
  [in] uint32 SingleSession
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SingleSession* \[ En\]
</dt> <dd>

Marca la deshabilitación o habilitación de **la propiedad SingleSession,** que determina si los usuarios están limitados a una o varias Servicios de Escritorio remoto sesión.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Deshabilite la propiedad .

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Habilite la propiedad .

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve Success si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.

## <a name="remarks"></a>Observaciones

Managed Object Format (MOF) contienen las definiciones de las clases Windows Management Instrumentation (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\TerminalServices de CIMv2 \\ raíz<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**TerminalServiceSetting de Win32 \_**](win32-terminalservicesetting.md)
</dt> </dl>

 

