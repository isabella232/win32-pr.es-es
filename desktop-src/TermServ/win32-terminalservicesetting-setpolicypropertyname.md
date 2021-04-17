---
title: Método SetPolicyPropertyName de la clase Win32_TerminalServiceSetting
description: El método SetPolicyPropertyName establece la propiedad DeleteTempFolders, UseTempFolders o help para la clase.
ms.assetid: 18d9927a-b7db-46c7-90ee-00da6de06202
ms.tgt_platform: multiple
keywords:
- Método SetPolicyPropertyName Servicios de Escritorio remoto
- Método SetPolicyPropertyName Servicios de Escritorio remoto, clase Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de clase Servicios de Escritorio remoto, método SetPolicyPropertyName
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492724"
---
# <a name="setpolicypropertyname-method-of-the-win32_terminalservicesetting-class"></a>Método SetPolicyPropertyName de la \_ clase TerminalServiceSetting de Win32

El método **SetPolicyPropertyName** establece la propiedad **DeleteTempFolders**, **UseTempFolders** o **Help** para la clase.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetPolicyPropertyName(
  [in] string  PropertyName,
  [in] boolean Value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NombreDePropiedad* \[ de\]
</dt> <dd>

Especifica la propiedad de directiva que el método está estableciendo.

<dt>

<span id="DeleteTempFolders"></span><span id="deletetempfolders"></span><span id="DELETETEMPFOLDERS"></span>

<span id="DeleteTempFolders"></span><span id="deletetempfolders"></span><span id="DELETETEMPFOLDERS"></span>**DeleteTempFolders**


</dt> <dd>

El método está estableciendo la propiedad **DeleteTempFolders** .

</dd> <dt>

<span id="UseTempFolders"></span><span id="usetempfolders"></span><span id="USETEMPFOLDERS"></span>

<span id="UseTempFolders"></span><span id="usetempfolders"></span><span id="USETEMPFOLDERS"></span>**UseTempFolders**


</dt> <dd>

El método está estableciendo la propiedad **UseTempFolders** .

</dd> <dt>

<span id="Help"></span><span id="help"></span><span id="HELP"></span>

<span id="Help"></span><span id="help"></span><span id="HELP"></span>**Ayuda**


</dt> <dd>

El método está estableciendo la propiedad **Help** .

**Nota:** no se admite la **ayuda**  

</dd> </dl> </dd> <dt>

*Valor* \[ de de\]
</dt> <dd>

Valor que indica si se debe habilitar o deshabilitar la propiedad especificada por el parámetro *PropertyName* .

<dt>

<span id="0"></span>

<span id="0"></span>**0,1**


</dt> <dd>

Deshabilite la propiedad.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Habilite la propiedad.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve SUCCESS si es correcto; de lo contrario, devuelve un código de error de WMI. Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores. El método devuelve un error si la configuración está en control de directiva de grupo.

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

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> </dl>

 

