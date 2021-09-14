---
title: Método SetProfilePath de la Win32_TerminalServiceSetting clase
description: El método SetProfilePath establece la propiedad ProfilePath para la clase .
ms.assetid: a0dfe6a4-929c-45ec-bd31-7e0ffb6ce5de
ms.tgt_platform: multiple
keywords:
- Método SetProfilePath Servicios de Escritorio remoto
- Método SetProfilePath Servicios de Escritorio remoto , Win32_TerminalServiceSetting clase
- Win32_TerminalServiceSetting clase Servicios de Escritorio remoto , método SetProfilePath
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetProfilePath
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 434909471accc191e79c92287ab6e4ac427bf949
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967947"
---
# <a name="setprofilepath-method-of-the-win32_terminalservicesetting-class"></a>Método SetProfilePath de la clase TerminalServiceSetting de Win32 \_

El **método SetProfilePath** establece la **propiedad ProfilePath** para la clase .

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetProfilePath(
  [in] string ProfilePath
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ProfilePath* \[ En\]
</dt> <dd>

Nuevo valor de la propiedad **ProfilePath,** que especifica la ruta de acceso del perfil para el equipo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve Correcto si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.

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

[**TerminalServiceSetting de Win32 \_**](win32-terminalservicesetting.md)
</dt> </dl>

 

