---
description: La \_ clase CIM LocalFileSystem representa el almacén de archivos controlado por un sistema informático a través de medios locales (por ejemplo, acceso directo al controlador de dispositivo).
ms.assetid: eab52a25-ca24-4a69-b030-091603d3582c
ms.tgt_platform: multiple
title: CIM_LocalFileSystem (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LocalFileSystem
- CIM_LocalFileSystem.Caption
- CIM_LocalFileSystem.Description
- CIM_LocalFileSystem.InstallDate
- CIM_LocalFileSystem.Name
- CIM_LocalFileSystem.Status
- CIM_LocalFileSystem.AvailableSpace
- CIM_LocalFileSystem.BlockSize
- CIM_LocalFileSystem.CasePreserved
- CIM_LocalFileSystem.CaseSensitive
- CIM_LocalFileSystem.CodeSet
- CIM_LocalFileSystem.CompressionMethod
- CIM_LocalFileSystem.CreationClassName
- CIM_LocalFileSystem.CSCreationClassName
- CIM_LocalFileSystem.CSName
- CIM_LocalFileSystem.EncryptionMethod
- CIM_LocalFileSystem.FileSystemSize
- CIM_LocalFileSystem.MaxFileNameLength
- CIM_LocalFileSystem.ReadOnly
- CIM_LocalFileSystem.Root
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6a4a45541a651c92b45baba70828ba99c911d59a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907284"
---
# <a name="cim_localfilesystem-class"></a>\_Clase LocalFileSystem de CIM

La clase **CIM \_ LocalFileSystem** representa el almacén de archivos controlado por un sistema informático a través de medios locales (por ejemplo, acceso directo al controlador de dispositivo). El almacén de archivos se puede administrar directamente mediante el sistema del equipo, sin necesidad de que otro equipo actúe como servidor de archivos. Sin embargo, para un sistema de archivos en clúster, el sistema de archivos es local y, por lo tanto, se pospone al clúster.

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{5B6C820A-E3D0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_LocalFileSystem : CIM_FileSystem
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint64   AvailableSpace;
  uint64   BlockSize;
  boolean  CasePreserved;
  boolean  CaseSensitive;
  uint16   CodeSet[];
  string   CompressionMethod;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   EncryptionMethod;
  uint64   FileSystemSize;
  uint32   MaxFileNameLength;
  boolean  ReadOnly;
  string   Root;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ LocalFileSystem** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ LocalFileSystem** tiene estas propiedades.

<dl> <dt>

**AvailableSpace**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Partición DMTF \| 002,4 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")
</dt> </dl>

Cantidad de espacio disponible, en bytes, para el sistema de archivos. Si es desconocido, escriba 0.

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).

</dd> <dt>

**BlockSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")
</dt> </dl>

Tamaño de bloque del sistema de archivos para el almacenamiento y la recuperación de datos.

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Breve descripción textual del objeto.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**CasePreserved**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es true**, se conserva el caso de los nombres de archivo.

Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).

</dd> <dt>

**CaseSensitive**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es true**, se admiten los nombres de archivo que distinguen mayúsculas de minúsculas.

Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).

</dd> <dt>

**Dese**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz que define los juegos de caracteres o la codificación admitidos por el sistema de archivos.

Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otro** (1)


</dt> <dd></dd> <dt>

<span id="ASCII"></span><span id="ascii"></span>

**ASCII** (2)


</dt> <dd></dd> <dt>

<span id="Unicode"></span><span id="unicode"></span><span id="UNICODE"></span>

**Unicode** (3)


</dt> <dd></dd> <dt>

<span id="ISO2022"></span><span id="iso2022"></span>

**Iso2022** (4)


</dt> <dd></dd> <dt>

<span id="ISO8859"></span><span id="iso8859"></span>

**ISO8859** (5)


</dt> <dd></dd> <dt>

<span id="Extended_UNIX_Code"></span><span id="extended_unix_code"></span><span id="EXTENDED_UNIX_CODE"></span>

**Código UNIX extendido** (6)


</dt> <dd></dd> <dt>

<span id="UTF-8"></span><span id="utf-8"></span>

**UTF-8** (7)


</dt> <dd></dd> <dt>

<span id="UCS-2"></span><span id="ucs-2"></span>

**UCS-2** (8)


</dt> <dd></dd> </dl>

</dd> <dt>

**CompressionMethod**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Partición DMTF \| 002,7 ")
</dt> </dl>

Cadena de forma libre que indica el algoritmo o la herramienta que se usa para comprimir el archivo lógico. Si el esquema de compresión es desconocido o no se ha descrito, use "Unknown". Si el archivo lógico está comprimido, pero el esquema de compresión es desconocido o no se ha descrito, use "comprimido". Si el archivo lógico no está comprimido, use "no comprimido".

Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nombre de la clase o subclase utilizada en la creación de una instancia de. Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.

Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).

</dd> <dt>

**CSCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**")
</dt> </dl>

Ámbito del nombre de la clase de creación del sistema del equipo.

Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Nombre**")
</dt> </dl>

Ámbito del nombre del sistema del equipo.

Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")
</dt> </dl>

Una descripción textual del objeto.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**EncryptionMethod**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Partición DMTF \| 002,8 ")
</dt> </dl>

Cadena de forma libre que identifica el algoritmo o la herramienta que se usa para cifrar un archivo lógico. Si el esquema de cifrado no es indulged (por motivos de seguridad, por ejemplo), use "Unknown". Si el archivo está cifrado, pero el esquema de cifrado es desconocido o no se ha divulgado, use "cifrado". Si el archivo lógico no está cifrado, use "no cifrado".

Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).

</dd> <dt>

**FileSystemSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")
</dt> </dl>

Tamaño del sistema de archivos, en bytes. Si es desconocido, escriba 0 (cero).

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")
</dt> </dl>

Indica cuándo se instaló el objeto. La falta de un valor no indica que el objeto no está instalado.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**MaxFileNameLength**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Longitud máxima de un nombre de archivo en el sistema de archivos. Un valor de 0 (cero) indica que no hay límite para la longitud del nombre de archivo.

Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")
</dt> </dl>

Etiqueta por la que se conoce el objeto. Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**ReadOnly**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrFSAccess ")
</dt> </dl>

Si es **true**, el sistema de archivos se designa como de solo lectura.

Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).

</dd> <dt>

**Raíces**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrFSMountPoint ")
</dt> </dl>

Nombre de ruta de acceso u otra información que define la raíz del sistema de archivos.

Esta propiedad se hereda del [**\_ sistema de archivos CIM**](cim-filesystem.md).

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")
</dt> </dl>

Cadena que indica el estado actual del objeto. Se puede definir un estado operativo y no operativo. El estado operativo puede ser "correcto", "degradado" y "Pred FAIL". "Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).

El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio". "Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo. No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

Los valores son los siguientes:

<dt>

<span id="OK"></span><span id="ok"></span>

**Aceptar** ("Aceptar")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Error** ("error")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Degradado** ("degradado")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** ("desconocido")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred FAIL** ("Pred FAIL")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Iniciando** ("iniciando")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Detener** ("detener")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Servicio** ("servicio")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

Con **estrés** ("acentuado")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**Recover** ("Recover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Sin contacto** ("sin contacto")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Comunicación perdida** ("pérdida de comunicación")


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **CIM \_ LocalFileSystem** se deriva del [**sistema de \_ archivos CIM**](cim-filesystem.md).

WMI no implementa esta clase.

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Sistema de archivos CIM**](cim-filesystem.md)
</dt> </dl>

 

