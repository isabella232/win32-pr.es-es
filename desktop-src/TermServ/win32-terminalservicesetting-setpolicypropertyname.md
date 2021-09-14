---
title: Método SetPolicyPropertyName de la Win32_TerminalServiceSetting clase
description: El método SetPolicyPropertyName establece la propiedad DeleteTempFolders, UseTempFolders o Help para la clase .
ms.assetid: 18d9927a-b7db-46c7-90ee-00da6de06202
ms.tgt_platform: multiple
keywords:
- Método SetPolicyPropertyName Servicios de Escritorio remoto
- Método SetPolicyPropertyName Servicios de Escritorio remoto , Win32_TerminalServiceSetting clase
- Win32_TerminalServiceSetting clase Servicios de Escritorio remoto , método SetPolicyPropertyName
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetPolicyPropertyName
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f49732fa916dd3c37539dc35d6cef7a4d920d81
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967948"
---
# <a name="setpolicypropertyname-method-of-the-win32_terminalservicesetting-class"></a>Método SetPolicyPropertyName de la clase TerminalServiceSetting de Win32 \_

El **método SetPolicyPropertyName** establece **la propiedad DeleteTempFolders**, **UseTempFolders** **o Help** para la clase .

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetPolicyPropertyName(
  [in] string  PropertyName,
  [in] boolean Value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PropertyName* \[ En\]
</dt> <dd>

Especifica la propiedad de directiva que el método está estableciendo.

<dt>

<span id="DeleteTempFolders"></span><span id="deletetempfolders"></span><span id="DELETETEMPFOLDERS"></span>

<span id="DeleteTempFolders"></span><span id="deletetempfolders"></span><span id="DELETETEMPFOLDERS"></span>**DeleteTempFolders**


</dt> <dd>

El método establece la **propiedad DeleteTempFolders.**

</dd> <dt>

<span id="UseTempFolders"></span><span id="usetempfolders"></span><span id="USETEMPFOLDERS"></span>

<span id="UseTempFolders"></span><span id="usetempfolders"></span><span id="USETEMPFOLDERS"></span>**UseTempFolders**


</dt> <dd>

El método establece la **propiedad UseTempFolders.**

</dd> <dt>

<span id="Help"></span><span id="help"></span><span id="HELP"></span>

<span id="Help"></span><span id="help"></span><span id="HELP"></span>**Ayuda**


</dt> <dd>

El método establece la **propiedad Help.**

**Nota:**  **No se** admite la Ayuda

</dd> </dl> </dd> <dt>

*Valor* \[ En\]
</dt> <dd>

Valor que indica si se debe habilitar o deshabilitar la propiedad especificada por el *parámetro PropertyName.*

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

Devuelve Success si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores. El método devuelve un error si la configuración está bajo control de directiva de grupo.

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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**TerminalServiceSetting de Win32 \_**](win32-terminalservicesetting.md)
</dt> </dl>

 

