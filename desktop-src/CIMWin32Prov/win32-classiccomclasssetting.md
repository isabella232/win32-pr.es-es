---
description: Representa la configuración de un componente de Modelo de objetos componentes (COM).
ms.assetid: 18d9ddf2-184d-4680-8d56-f012c608ff7d
ms.tgt_platform: multiple
title: Win32_ClassicCOMClassSetting clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClassicCOMClassSetting
- Win32_ClassicCOMClassSetting.Caption
- Win32_ClassicCOMClassSetting.Description
- Win32_ClassicCOMClassSetting.SettingID
- Win32_ClassicCOMClassSetting.AppID
- Win32_ClassicCOMClassSetting.AutoConvertToClsid
- Win32_ClassicCOMClassSetting.AutoTreatAsClsid
- Win32_ClassicCOMClassSetting.ComponentId
- Win32_ClassicCOMClassSetting.Control
- Win32_ClassicCOMClassSetting.DefaultIcon
- Win32_ClassicCOMClassSetting.InprocHandler
- Win32_ClassicCOMClassSetting.InprocHandler32
- Win32_ClassicCOMClassSetting.InprocServer
- Win32_ClassicCOMClassSetting.InprocServer32
- Win32_ClassicCOMClassSetting.Insertable
- Win32_ClassicCOMClassSetting.JavaClass
- Win32_ClassicCOMClassSetting.LocalServer
- Win32_ClassicCOMClassSetting.LocalServer32
- Win32_ClassicCOMClassSetting.LongDisplayName
- Win32_ClassicCOMClassSetting.ProgId
- Win32_ClassicCOMClassSetting.ShortDisplayName
- Win32_ClassicCOMClassSetting.ThreadingModel
- Win32_ClassicCOMClassSetting.ToolBoxBitmap32
- Win32_ClassicCOMClassSetting.TreatAsClsid
- Win32_ClassicCOMClassSetting.TypeLibraryId
- Win32_ClassicCOMClassSetting.Version
- Win32_ClassicCOMClassSetting.VersionIndependentProgId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5f263a888ce9dea80444023faff57998bc3f2c1c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160332"
---
# <a name="win32_classiccomclasssetting-class"></a>Clase \_ ClassicCOMClassSetting de Win32

La clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **Win32 \_ ClassicCOMClassSetting** representa la configuración de un componente de Modelo de objetos componentes (COM).

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A562-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_ClassicCOMClassSetting : Win32_COMSetting
{
  string  Caption;
  string  Description;
  string  SettingID;
  string  AppID;
  string  AutoConvertToClsid;
  string  AutoTreatAsClsid;
  string  ComponentId;
  boolean Control;
  string  DefaultIcon;
  string  InprocHandler;
  string  InprocHandler32;
  string  InprocServer;
  string  InprocServer32;
  boolean Insertable;
  boolean JavaClass;
  string  LocalServer;
  string  LocalServer32;
  string  LongDisplayName;
  string  ProgId;
  string  ShortDisplayName;
  string  ThreadingModel;
  string  ToolBoxBitmap32;
  string  TreatAsClsid;
  string  TypeLibraryId;
  string  Version;
  string  VersionIndependentProgId;
};
```

## <a name="members"></a>Members

La **clase \_ ClassicCOMClassSetting de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ ClassicCOMClassSetting de Win32** tiene estas propiedades.

<dl> <dt>

**AppID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \[ \] AppID")
</dt> </dl>

Identificador único global (GUID) para la aplicación COM que usa este componente COM.

</dd> <dt>

**AutoConvertToClsid**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ AutoConvertTo \[ \] Default")
</dt> </dl>

GUID de la clase COM a la que se convertirá automáticamente este componente COM.

</dd> <dt>

**AutoTreatAsClsid**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ AutoTreatAs \[ \] Default")
</dt> </dl>

GUID para el componente COM que emulará automáticamente las instancias de esta clase.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Breve descripción textual del objeto actual.

Esta propiedad se hereda de la [**configuración de CIM \_**](cim-setting.md).

</dd> <dt>

**ComponentId**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY LOCAL MACHINE SOFTWARE \_ Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \[ \] Default")
</dt> </dl>

GUID de este componente COM.

</dd> <dt>

**Control**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ Control")
</dt> </dl>

El componente COM es un control OLE.

</dd> <dt>

**DefaultIcon**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ DefaultIcon \[ \] Default")
</dt> </dl>

Ruta de acceso al archivo ejecutable y al identificador de recursos del icono predeterminado utilizado por la clase .

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción textual del objeto actual.

Esta propiedad se hereda de la [**configuración de CIM \_**](cim-setting.md).

</dd> <dt>

**InprocHandler**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocHandler \[ \] Default")
</dt> </dl>

Ruta de acceso completa, incluido nombre de archivo o solo nombre de archivo a un controlador personalizado de 16 bits para el componente COM. El proveedor no siempre devuelve la ruta de acceso completa.

</dd> <dt>

**InprocHandler32**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocHandler32 Default \[ \] ")
</dt> </dl>

Ruta de acceso completa que incluye nombre de archivo o solo nombre de archivo a un controlador personalizado de 32 bits para el componente COM. El proveedor no siempre devuelve la ruta de acceso completa.

</dd> <dt>

**InprocServer**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer \[ \] Default")
</dt> </dl>

Ruta de acceso completa, incluido nombre de archivo o solo nombre de archivo a un archivo DLL de servidor en proceso de 16 bits para este componente COM. El proveedor no siempre devuelve la ruta de acceso completa.

</dd> <dt>

**InprocServer32**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer32 Default \[ \] ")
</dt> </dl>

Ruta de acceso completa, incluido nombre de archivo o solo nombre de archivo a un archivo DLL de servidor en proceso de 32 bits para este componente COM. El proveedor no siempre devuelve la ruta de acceso completa.

</dd> <dt>

**Insertable**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ Insertable")
</dt> </dl>

El componente COM se puede insertar en aplicaciones de contenedor OLE.

</dd> <dt>

**Javaclass**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer32 \[ JavaClass \] ")
</dt> </dl>

El componente COM es un componente de Java.

</dd> <dt>

**LocalServer**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ LocalServer Default \[ \] ")
</dt> </dl>

Ruta de acceso completa, incluido nombre de archivo o solo nombre de archivo a una aplicación de servidor local de 16 bits. El proveedor no siempre devuelve la ruta de acceso completa.

</dd> <dt>

**LocalServer32**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ LocalServer32 Default \[ \] ")
</dt> </dl>

Ruta de acceso completa, incluido nombre de archivo o solo nombre de archivo a una aplicación de servidor local de 32 bits. El proveedor no siempre devuelve la ruta de acceso completa.

</dd> <dt>

**LongDisplayName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ AuxUserType \\ \\ 3 Default \[ \] ")
</dt> </dl>

Nombre completo de la aplicación COM. Se usa en áreas como el campo **Resultados** del cuadro **de diálogo Ole Pegar** especial .

</dd> <dt>

**Progid**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ ProgID \[ \] Default")
</dt> </dl>

Identificador de programación asociado al componente COM. El formato de un ProgID es <Vendor.<Component.<Version. No se garantiza que este identificador sea único.

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Identificador por el que se conoce el objeto actual.

Esta propiedad se hereda de la [**configuración de CIM \_**](cim-setting.md).

</dd> <dt>

**ShortDisplayName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ AuxUserType \\ \\ 2 \[ \] Default")
</dt> </dl>

Nombre corto de la aplicación COM (se usa en menús y elementos emergentes).

</dd> <dt>

**ThreadingModel**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer32 \[ ThreadingModel \] ")
</dt> </dl>

Modelo de subprocesos utilizado por las clases COM en proceso. Si esta propiedad es **NULL,** no se usa ningún modelo de subprocesos. El componente se crea en el subproceso principal del cliente y las llamadas de otros subprocesos se serializan a este subproceso.

El modelo Apartment especifica que los componentes pueden especificarse mediante un solo subproceso. Los datos comunes que mantienen estos tipos de servidores de objetos deben protegerse frente a colisiones de subprocesos porque el servidor de objetos admite varios componentes. Cada componente se puede especificar simultáneamente mediante subprocesos diferentes.

El modelo Free especifica que los componentes no aplican restricciones en qué subprocesos o cuántos subprocesos pueden entrar en el objeto. El objeto no puede contener datos específicos del subproceso y debe proteger sus datos del acceso simultáneo por parte de varios subprocesos. Sin embargo, los subprocesos de apartamento no pueden acceder directamente a los componentes de subproceso libre y las llamadas a ellos se serializan desde el apartamento del cliente.

Cuando se especifica Ambos, los componentes se pueden usar en modos de subprocesos de apartamento o de subproceso libre. Estos componentes se pueden especificar mediante varios subprocesos, proteger sus datos de colisiones de subprocesos y no contienen datos específicos del subproceso.

Los valores son:

<dl> <dd>"Apartment"</dd> <dd>"Gratis"</dd> <dd>"Both"</dd> </dl>

<dt>

<span id="Apartment"></span><span id="apartment"></span><span id="APARTMENT"></span>

**Apartment** ("Apartment")


</dt> <dd></dd> <dt>

<span id="Free"></span><span id="free"></span><span id="FREE"></span>

**Gratis** ("Gratis")


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

**Ambos** ("Ambos")


</dt> <dd></dd> </dl>

</dd> <dt>

**ToolBoxBitmap32**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ ToolBoxBitmap32 Default \[ \] ")
</dt> </dl>

Nombre del módulo e identificador de recursos para un mapa de bits pequeño (16 x 16) usado para la cara de una barra de herramientas o un botón del cuadro de herramientas. Se usa cuando el componente COM es un control OLE ActiveX.

</dd> <dt>

**TreatAsClsid**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ TreatAs \[ \] Default")
</dt> </dl>

GUID de un componente COM que puede emular instancias de este componente.

</dd> <dt>

**TypeLibraryId**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ TypeLib \[ \] Default")
</dt> </dl>

GUID de la biblioteca de tipos para este componente COM.

</dd> <dt>

**Versión**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} Version \\ \\ \[ \] Default")
</dt> </dl>

Número de versión de esta clase COM.

</dd> <dt>

**VersionIndependentProgId**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ VersionIndependentProgId Default \[ \] ")
</dt> </dl>

Identificador de programa coherente para todas las versiones del mismo programa.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ ClassicCOMClassSetting de Win32** se deriva de [**\_ COMSetting de Win32.**](win32-comsetting.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ComSetting de Win32 \_**](win32-comsetting.md)
</dt> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

