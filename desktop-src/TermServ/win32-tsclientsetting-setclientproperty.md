---
title: Método SetClientProperty de la clase Win32_TSClientSetting
description: El método SetClientProperty establece la propiedad LPTPortMapping, COMPortMapping, AudioMapping, ClipboardMapping, DriveMapping o WindowsPrinterMapping para la clase.
ms.assetid: a8ad922f-d768-4708-9a67-c6b00580baed
ms.tgt_platform: multiple
keywords:
- Método SetClientProperty Servicios de Escritorio remoto
- Método SetClientProperty Servicios de Escritorio remoto, clase Win32_TSClientSetting
- Win32_TSClientSetting de clase Servicios de Escritorio remoto, método SetClientProperty
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetClientProperty
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a89bfdfd7c7f2c4b23f76b50ab671d74541f9dbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676723"
---
# <a name="setclientproperty-method-of-the-win32_tsclientsetting-class"></a>Método SetClientProperty de la \_ clase TSClientSetting de Win32

El método **SetClientProperty** establece la **propiedad LPTPortMapping**, **COMPortMapping**, **AudioMapping**, **ClipboardMapping**, **DriveMapping** o **WindowsPrinterMapping** para la clase.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetClientProperty(
  [in] string  PropertyName,
  [in] boolean Value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NombreDePropiedad* \[ de\]
</dt> <dd>

Especifica la propiedad de cliente que el método está estableciendo.

<dt>

<span id="AudioMapping"></span><span id="audiomapping"></span><span id="AUDIOMAPPING"></span>

<span id="AudioMapping"></span><span id="audiomapping"></span><span id="AUDIOMAPPING"></span>**AudioMapping**


</dt> <dd>

El método está estableciendo la propiedad **AudioMapping** .

</dd> <dt>

<span id="ClipboardMapping"></span><span id="clipboardmapping"></span><span id="CLIPBOARDMAPPING"></span>

<span id="ClipboardMapping"></span><span id="clipboardmapping"></span><span id="CLIPBOARDMAPPING"></span>**ClipboardMapping**


</dt> <dd>

El método está estableciendo la propiedad **ClipboardMapping** .

</dd> <dt>

<span id="COMPortMapping"></span><span id="comportmapping"></span><span id="COMPORTMAPPING"></span>

<span id="COMPortMapping"></span><span id="comportmapping"></span><span id="COMPORTMAPPING"></span>**COMPortMapping**


</dt> <dd>

El método está estableciendo la propiedad **COMPortMapping** .

</dd> <dt>

<span id="DriveMapping"></span><span id="drivemapping"></span><span id="DRIVEMAPPING"></span>

<span id="DriveMapping"></span><span id="drivemapping"></span><span id="DRIVEMAPPING"></span>**DriveMapping**


</dt> <dd>

El método está estableciendo la propiedad **DriveMapping** .

</dd> <dt>

<span id="LPTPortMapping"></span><span id="lptportmapping"></span><span id="LPTPORTMAPPING"></span>

<span id="LPTPortMapping"></span><span id="lptportmapping"></span><span id="LPTPORTMAPPING"></span>**LPTPortMapping**


</dt> <dd>

El método está estableciendo la propiedad **LPTPortMapping** .

</dd> <dt>

<span id="PNPRedirection"></span><span id="pnpredirection"></span><span id="PNPREDIRECTION"></span>

<span id="PNPRedirection"></span><span id="pnpredirection"></span><span id="PNPREDIRECTION"></span>**PNPRedirection**


</dt> <dd>

El método está estableciendo la propiedad **PNPRedirection** .

</dd> <dt>

<span id="WindowsPrinterMapping"></span><span id="windowsprintermapping"></span><span id="WINDOWSPRINTERMAPPING"></span>

<span id="WindowsPrinterMapping"></span><span id="windowsprintermapping"></span><span id="WINDOWSPRINTERMAPPING"></span>**WindowsPrinterMapping**


</dt> <dd>

El método está estableciendo la propiedad **WindowsPrinterMapping** .

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

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI. Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores. El método devuelve un error si la propiedad de cliente especificada no está bajo el control de directiva de grupo o si la configuración de la propiedad no es válida para la invalidación por parte del servidor.

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

[**Win32 \_ TSClientSetting**](win32-tsclientsetting.md)
</dt> </dl>

 

