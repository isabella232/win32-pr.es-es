---
title: Win32_TerminalError (clase)
description: Representa un error de terminal.
ms.assetid: d3f622cd-e4ce-4c7e-999e-940b67fd116c
ms.tgt_platform: multiple
keywords:
- Win32_TerminalError clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TerminalError de clase, se describe
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150026"
---
# <a name="win32_terminalerror-class"></a>\_Clase Win32 TerminalError

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

## <a name="members"></a>Miembros

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

Cualquier cadena definida por el usuario que describa un estado operativo o de error.

Esta propiedad se hereda de [**\_ \_ ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).

</dd> <dt>

**Operación**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Operación que tiene lugar en el momento en que se produce un error o una anomalía. Normalmente, WMI establece esta propiedad en el nombre de una API COM para un método WMI como el siguiente: [**IWbemServices:: CreateInstanceEnum**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum).

Esta propiedad se hereda de [**\_ \_ ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).

</dd> <dt>

**ParameterInfo**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Los parámetros implicados en un error o un cambio de estado. Por ejemplo, si una aplicación intenta recuperar una clase que no existe, esta propiedad se establece en el nombre de clase infractora.

Esta propiedad se hereda de [**\_ \_ ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).

</dd> <dt>

**ProviderName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identifica el proveedor que produce o informa de un error o un cambio de estado. Si un proveedor no está implicado, esta cadena se establece en "administración de Windows".

Esta propiedad se hereda de [**\_ \_ ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).

</dd> <dt>

**StatusCode**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Contiene un código de error o de información para una operación. Puede ser cualquier valor definido por el proveedor, pero el valor 0 (cero) normalmente se reserva para indicar que la operación se ha realizado correctamente. Esta propiedad se hereda de [**\_ \_ NotifyStatus**](/windows/desktop/WmiSdk/--notifystatus).

</dd> <dt>

**TerminalName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del terminal sin el que se produjo el error.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Raíz de \\ cimv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_\_ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus)
</dt> </dl>

 

