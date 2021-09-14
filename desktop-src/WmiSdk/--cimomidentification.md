---
description: Describe la instalación local de WMI.
ms.assetid: 907b65b2-a853-40f4-8b36-5a05a2b1cf85
ms.tgt_platform: multiple
title: __CIMOMIdentification clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __CIMOMIdentification
- Root.__CIMOMIdentification.SetupDateTime
- Root.__CIMOMIdentification.VersionCurrentlyRunning
- Root.__CIMOMIdentification.VersionUsedToCreateDB
- Root.__CIMOMIdentification.WorkingDirectory
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: a8590a2a83cdbc9bd06575cf17ddbe65138a4a31
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126965303"
---
# <a name="__cimomidentification-class"></a>\_\_CIMOMIdentification (clase)

La **\_ \_ clase del sistema CIMOMIdentification** describe la instalación local de WMI. Se trata de una clase singleton; solo hay una instancia. La **\_ \_ clase CIMOMIdentification** solo está disponible en los espacios de nombres **Root** y **Root \\ Default.** Los usuarios consultan la instancia de para obtener información sobre la instalación de WMI.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[singleton]
class __CIMOMIdentification : __SystemClass
{
  string SetupDateTime;
  string VersionCurrentlyRunning;
  string VersionUsedToCreateDB;
  string WorkingDirectory;
};
```

## <a name="members"></a>Members

La **\_ \_ clase CIMOMIdentification** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **\_ \_ clase CIMOMIdentification** tiene estas propiedades.

<dl> <dt>

**SetupDateTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha y hora de la instalación. Esta propiedad está vacía después de instalar el sistema operativo por primera vez.

Si el repositorio WMI se ha eliminado y luego se ha creado de nuevo, esta propiedad contiene la fecha y hora en que se vuelve a crear el repositorio.

</dd> <dt>

**VersionCurrentlyRunning**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica la versión de la imagen real que contiene el servicio WMI que creó el repositorio Modelo de información común (CIM). Dado que el formato del repositorio puede cambiar entre versiones de WMI, esta propiedad permite que futuras actualizaciones de WMI determinen si se debe actualizar la base de datos. El formato es:

"1.00.183.0000"

donde el primer dígito es la versión principal, los dos dígitos siguientes son versiones secundarias y los tres dígitos siguientes son el número de compilación. No se usan los dígitos restantes.

</dd> <dt>

**VersionUsedToCreateDB**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica la versión de la imagen real que contiene el servicio WMI que creó el repositorio CIM. Dado que el formato del repositorio puede cambiar entre versiones de WMI, esta propiedad permite que futuras actualizaciones de WMI determinen si se debe actualizar la base de datos. El formato es:

"1.00.183.0000"

donde el primer dígito es la versión principal, los dos dígitos siguientes son versiones secundarias y los tres dígitos siguientes son el número de compilación. No se usan los dígitos restantes.

</dd> <dt>

**WorkingDirectory**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Directorio de instalación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **\_ \_ clase CIMOMIdentification** se deriva de [**\_ \_ SystemClass**](--systemclass.md), que no tiene ninguna propiedad.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de código de VBScript se describe cómo mostrar información de identificación del modelo de objetos CIM y se ha tomado del directorio de ejemplo en Archivos de programa SDK de \\ \\ Microsoft Windows \\ \\ \\ v7.0 \\ Samples \\ sysmgmt wmi scripting (Scripting wmi de sysmgmt de ejemplos de v7.0). \\ \\


```VB
on error resume next 
set cimomid = GetObject("winmgmts:root\default:__cimomidentification=@")

if err <> 0 then
 WScript.Echo ErrNumber, Err.Source, Err.Description
else
 WScript.Echo cimomid.path_.displayname
 WScript.Echo cimomid.versionusedtocreatedb
end if
```



En el siguiente ejemplo de código Perl se describe cómo mostrar la información de identificación del modelo de objetos CIM y se tomó del directorio de ejemplo en Archivos de programa SDK de Microsoft Windows scripting wmi de sysmgmt de ejemplos \\ \\ \\ \\ \\ v7.0. \\ \\ \\ \\


```Perl
use strict;
use Win32::OLE;

my ($Cimomid, $locator, $services);

eval { $Cimomid = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\default")->
 Get("__CIMOMIdentification=@"); };

unless ($@)
{
 print "\n", $Cimomid->Path_()->{displayname}, "\n";
 print $Cimomid->{versionusedtocreatedb}, "\n";
}
else
{ 
 print STDERR "\n", Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Root<br/>                |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**\_\_SystemClass**](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

