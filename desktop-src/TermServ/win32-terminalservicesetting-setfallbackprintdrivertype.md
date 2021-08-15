---
title: Método SetFallbackPrintDriverType de la Win32_TerminalServiceSetting clase
description: El método SetFallbackPrintDriverType establece la propiedad FallbackPrintDriverType para la clase .
ms.assetid: be738134-199a-41a6-b2f8-cccfa14fa02b
ms.tgt_platform: multiple
keywords:
- Método SetFallbackPrintDriverType Servicios de Escritorio remoto
- Método SetFallbackPrintDriverType Servicios de Escritorio remoto , Win32_TerminalServiceSetting clase
- Win32_TerminalServiceSetting clase Servicios de Escritorio remoto , método SetFallbackPrintDriverType
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
ms.openlocfilehash: d39033a34c75ea94f365ae690b1ac6fe4cd61663e9cd6db19f2cd2c232bd8c89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137868"
---
# <a name="setfallbackprintdrivertype-method-of-the-win32_terminalservicesetting-class"></a>Método SetFallbackPrintDriverType de la clase \_ TerminalServiceSetting de Win32

El **método SetFallbackPrintDriverType** establece la **propiedad FallbackPrintDriverType** para la clase .

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetFallbackPrintDriverType(
  [in] uint32 FallbackPrintDriverType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FallbackPrintDriverType* \[ En\]
</dt> <dd>

Establece la **propiedad FallbackPrintDriverType** que permite o deniega nuevas conexiones Servicios de Escritorio remoto datos.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Sin controladores de reserva.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Mejor suposición.

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Mejor suposición. Si no se encuentra ninguna coincidencia, la reserva se Hewlett-Packard lenguaje de control de impresora (PCL).

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3**


</dt> <dd>

Mejor suposición. Si no se encuentra ninguna coincidencia, reversión a Postscript (PS).

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4**


</dt> <dd>

Mejor suposición. Si no se encuentra ninguna coincidencia, muestre los controladores PS y PCL.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve Success si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores. El método devuelve un error si la configuración está bajo control de directiva de grupo.

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del Kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

