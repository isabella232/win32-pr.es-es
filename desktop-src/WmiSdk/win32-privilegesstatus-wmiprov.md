---
description: El estado de privilegios de Win32 \_ &\# 8194; La clase WMI informa sobre los privilegios necesarios para completar una operación. Se puede devolver cuando se ha producido un error en una operación o cuando se ha devuelto una instancia parcialmente rellenada.
ms.assetid: 85bda855-1488-4d7a-99ed-798e9859fef7
ms.tgt_platform: multiple
title: Win32_PrivilegesStatus clase (WMI)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrivilegesStatus
- Win32_PrivilegesStatus.Description
- Win32_PrivilegesStatus.Operation
- Win32_PrivilegesStatus.ParameterInfo
- Win32_PrivilegesStatus.ProviderName
- Win32_PrivilegesStatus.StatusCode
- Win32_PrivilegesStatus.PrivilegesNotHeld
- Win32_PrivilegesStatus.PrivilegesRequired
api_type:
- Schema
api_location:
- Root\WMI
ms.openlocfilehash: 97276023325dc4e2a460daefd35ee01104b5c0adf5c855f145e0f11c954eba1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757635"
---
# <a name="win32_privilegesstatus-class-wmi"></a>Win32_PrivilegesStatus clase (WMI)

La clase [WMI](retrieving-a-class.md) **Win32 \_ PrivilegesStatus** informa sobre los privilegios necesarios para completar una operación.    Se puede devolver cuando se ha producido un error en una operación o cuando se ha devuelto una instancia parcialmente rellenada.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[UUID("{BE46D060-7A7C-11d2-BC85-00104B2CF71C}")]
class Win32_PrivilegesStatus : __ExtendedStatus
{
  string Description;
  string Operation;
  string ParameterInfo;
  string ProviderName;
  uint32 StatusCode;
  string PrivilegesNotHeld[];
  string PrivilegesRequired[];
};
```

## <a name="members"></a>Miembros

La **clase \_ PrivilegesStatus de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ PrivilegesStatus de Win32** tiene estas propiedades.

<dl> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cualquier cadena definida por el usuario que describa un error o un estado operativo.

Esta propiedad se hereda de [**\_ \_ ExtendedStatus.**](--extendedstatus.md)

</dd> <dt>

**operación**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Operación que tiene lugar en el momento de un error o anomalía. Normalmente, Windows Management Instrumentation (WMI) establece esta propiedad en el nombre de una API COM para el método WMI como el siguiente: [**IWbemServices::CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum).

Esta propiedad se hereda de [**\_ \_ ExtendedStatus.**](--extendedstatus.md)

</dd> <dt>

**ParameterInfo**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Parámetros implicados en un error o cambio de estado. Por ejemplo, si una aplicación intenta recuperar una clase que no existe, esta propiedad se establece en el nombre de clase infractora.

Esta propiedad se hereda de [**\_ \_ ExtendedStatus.**](--extendedstatus.md)

</dd> <dt>

**PrivilegesNotHeld**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Lista de los privilegios de acceso necesarios que faltan para completar una operación. Los tipos de privilegios de acceso se pueden encontrar en la Windows privilegios.

Ejemplo: "SE \_ SHUTDOWN \_ NAME"

</dd> <dt>

**PrivilegesRequired**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Lista de todos los privilegios necesarios para realizar una operación. Esto incluye valores de la **propiedad PrivilegesNotHeld.**

Ejemplo: "SE \_ SHUTDOWN \_ NAME"

</dd> <dt>

**ProviderName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identifica el proveedor que produce o notifica un error o cambio de estado. Si un proveedor no está implicado, esta cadena se establece en "Windows Management".

Esta propiedad se hereda de [**\_ \_ ExtendedStatus.**](--extendedstatus.md)

</dd> <dt>

**StatusCode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Contiene un error o código de información para una operación. Puede ser cualquier valor definido por el proveedor, pero el valor 0 (cero) normalmente se reserva para indicar que se ha establecido correctamente. Esta propiedad se hereda de [**\_ \_ NotifyStatus.**](--notifystatus.md)

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ PrivilegesStatus de Win32** se deriva de [**\_ \_ ExtendedStatus**](--extendedstatus.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                     |
| Espacio de nombres<br/>                | \\WMI raíz<br/>                                                               |
| MOF<br/>                      | <dl> <dt>Wmi.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_\_ExtendedStatus**](--extendedstatus.md)
</dt> </dl>

 

 




