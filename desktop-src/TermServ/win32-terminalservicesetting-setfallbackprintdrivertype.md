---
title: Método SetFallbackPrintDriverType de la clase Win32_TerminalServiceSetting
description: El método SetFallbackPrintDriverType establece la propiedad FallbackPrintDriverType para la clase.
ms.assetid: be738134-199a-41a6-b2f8-cccfa14fa02b
ms.tgt_platform: multiple
keywords:
- Método SetFallbackPrintDriverType Servicios de Escritorio remoto
- Método SetFallbackPrintDriverType Servicios de Escritorio remoto, clase Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de clase Servicios de Escritorio remoto, método SetFallbackPrintDriverType
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetFallbackPrintDriverType
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16e445fef86970e89d5b0f09abebecd40f49ab7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079694"
---
# <a name="setfallbackprintdrivertype-method-of-the-win32_terminalservicesetting-class"></a>Método SetFallbackPrintDriverType de la \_ clase TerminalServiceSetting de Win32

El método **SetFallbackPrintDriverType** establece la propiedad **FallbackPrintDriverType** para la clase.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetFallbackPrintDriverType(
  [in] uint32 FallbackPrintDriverType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FallbackPrintDriverType* \[ de\]
</dt> <dd>

Establece la propiedad **FallbackPrintDriverType** , que permite o deniega las nuevas conexiones servicios de escritorio remoto.

<dt>

<span id="0"></span>

<span id="0"></span>**0,1**


</dt> <dd>

No hay controladores de reserva.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Mejor aproximación.

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Mejor aproximación. Si no se encuentra ninguna coincidencia, retroceder a Hewlett-Packard el lenguaje de control de impresoras (PCL).

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3**


</dt> <dd>

Mejor aproximación. Si no se encuentra ninguna coincidencia, retroceder a PostScript (PS).

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4**


</dt> <dd>

Mejor aproximación. Si no se encuentra ninguna coincidencia, muestre los controladores PS y PCL.

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

 

