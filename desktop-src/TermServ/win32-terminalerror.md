---
title: Win32_TerminalError clase
description: Representa un error de terminal.
ms.assetid: d3f622cd-e4ce-4c7e-999e-940b67fd116c
ms.tgt_platform: multiple
keywords:
- Win32_TerminalError clase Servicios de Escritorio remoto
- Win32_TerminalError clase Servicios de Escritorio remoto , descrita
topic_type:
- apiref
api_name:
- Win32_TerminalError
- Win32_TerminalError.Description
- Win32_TerminalError.Operation
- Win32_TerminalError.ParameterInfo
- Win32_TerminalError.ProviderName
- Win32_TerminalError.StatusCode
- Win32_TerminalError.TerminalName
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f99724badc6c1ca7a2e4168e5c062b4dd1495ea6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126890825"
---
# <a name="win32_terminalerror-class"></a>Clase TerminalError de Win32 \_

Representa un error de terminal.

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
class Win32_TerminalError : __ExtendedStatus
{
  string Description;
  string Operation;
  string ParameterInfo;
  string ProviderName;
  uint32 StatusCode;
  string TerminalName;
};
```

## <a name="members"></a>Members

La **clase \_ TerminalError de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ TerminalError de Win32** tiene estas propiedades.

<dl> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cualquier cadena definida por el usuario que describa un error o un estado operativo.

Esta propiedad se hereda de [**\_ \_ ExtendedStatus.**](/windows/desktop/WmiSdk/--extendedstatus)

</dd> <dt>

**operación**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Operación que tiene lugar en el momento de un error o anomalía. Normalmente, WMI establece esta propiedad en el nombre de una API COM para el método WMI como el siguiente: [**IWbemServices::CreateInstanceEnum**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum).

Esta propiedad se hereda de [**\_ \_ ExtendedStatus.**](/windows/desktop/WmiSdk/--extendedstatus)

</dd> <dt>

**ParameterInfo**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Parámetros implicados en un error o cambio de estado. Por ejemplo, si una aplicación intenta recuperar una clase que no existe, esta propiedad se establece en el nombre de clase infractora.

Esta propiedad se hereda de [**\_ \_ ExtendedStatus.**](/windows/desktop/WmiSdk/--extendedstatus)

</dd> <dt>

**ProviderName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identifica el proveedor que produce o notifica un error o cambio de estado. Si un proveedor no está implicado, esta cadena se establece en "Windows Management".

Esta propiedad se hereda de [**\_ \_ ExtendedStatus.**](/windows/desktop/WmiSdk/--extendedstatus)

</dd> <dt>

**StatusCode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Contiene un error o código de información para una operación. Puede ser cualquier valor definido por el proveedor, pero el valor 0 (cero) normalmente se reserva para indicar que se ha establecido correctamente. Esta propiedad se hereda de [**\_ \_ NotifyStatus.**](/windows/desktop/WmiSdk/--notifystatus)

</dd> <dt>

**TerminalName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del sin terminal en el que se produjo el error.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\TerminalServices cimv2 \\ raíz<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**\_\_ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus)
</dt> </dl>

 

