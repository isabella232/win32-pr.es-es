---
description: La \_ clase de archivo de datos CIM representa una colección con nombre de datos o código ejecutable. Solo se devolverán las instancias de los archivos de los discos fijos locales.
ms.assetid: e90e1216-e943-4f3a-9f6c-8a0b4568a11f
ms.tgt_platform: multiple
title: CIM_DataFile (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile
- CIM_DataFile.Caption
- CIM_DataFile.Description
- CIM_DataFile.InstallDate
- CIM_DataFile.Status
- CIM_DataFile.AccessMask
- CIM_DataFile.Archive
- CIM_DataFile.Compressed
- CIM_DataFile.CompressionMethod
- CIM_DataFile.CreationClassName
- CIM_DataFile.CreationDate
- CIM_DataFile.CSCreationClassName
- CIM_DataFile.CSName
- CIM_DataFile.Drive
- CIM_DataFile.EightDotThreeFileName
- CIM_DataFile.Encrypted
- CIM_DataFile.EncryptionMethod
- CIM_DataFile.Name
- CIM_DataFile.Extension
- CIM_DataFile.FileName
- CIM_DataFile.FileSize
- CIM_DataFile.FileType
- CIM_DataFile.FSCreationClassName
- CIM_DataFile.FSName
- CIM_DataFile.Hidden
- CIM_DataFile.InUseCount
- CIM_DataFile.LastAccessed
- CIM_DataFile.LastModified
- CIM_DataFile.Path
- CIM_DataFile.Readable
- CIM_DataFile.System
- CIM_DataFile.Writeable
- CIM_DataFile.Manufacturer
- CIM_DataFile.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0badba05eafa5cba06e48b8494ca893936af360e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907302"
---
# <a name="cim_datafile-class"></a>CIM ( \_ clase de archivo de archivos)

La clase de **\_ archivo** de datos CIM representa una colección con nombre de datos o código ejecutable. Solo se devolverán las instancias de los archivos de los discos fijos locales.

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C55A-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("All Files (CIM)"), AMENDMENT]
class CIM_DataFile : CIM_LogicalFile
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   AccessMask;
  boolean  Archive;
  boolean  Compressed;
  string   CompressionMethod;
  string   CreationClassName;
  datetime CreationDate;
  string   CSCreationClassName;
  string   CSName;
  string   Drive;
  string   EightDotThreeFileName;
  boolean  Encrypted;
  string   EncryptionMethod;
  string   Name;
  string   Extension;
  string   FileName;
  uint64   FileSize;
  string   FileType;
  string   FSCreationClassName;
  string   FSName;
  boolean  Hidden;
  uint64   InUseCount;
  datetime LastAccessed;
  datetime LastModified;
  string   Path;
  boolean  Readable;
  boolean  System;
  boolean  Writeable;
  string   Manufacturer;
  string   Version;
};
```

## <a name="members"></a>Miembros

La clase de **\_ archivo de archivos CIM** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase de **\_ archivo de archivos CIM** tiene estos métodos.



| Método                                                                                          | Descripción                                                                                                                                          |
|:------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-datafile.md)     | Cambia los permisos de seguridad para el archivo lógico especificado en la ruta de acceso del objeto. Implementado por WMI.<br/>                                   |
| [**ChangeSecurityPermissionsEx**](changesecuritypermissionsex-method-in-class-cim-datafile.md) | Cambia los permisos de seguridad para el archivo lógico especificado en la ruta de acceso del objeto. Implementado por WMI.<br/>                                   |
| [**Comprimir**](compress-method-in-class-cim-datafile.md)                                       | Usa la compresión NTFS para comprimir el archivo lógico (o directorio) especificado en la ruta de acceso del objeto. Implementado por WMI.<br/>                       |
| [**CompressEx**](compressex-method-in-class-cim-datafile.md)                                   | Comprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto. Implementado por WMI.<br/>                                              |
| [**Copiar**](copy-method-in-class-cim-datafile.md)                                               | Copia el archivo lógico (o directorio) especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro de entrada. Implementado por WMI.<br/> |
| [**CopyEx**](copyex-method-in-class-cim-datafile.md)                                           | Copia el archivo lógico (o directorio) especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro de entrada. Implementado por WMI.<br/> |
| [**Elimínelos**](delete-method-in-class-cim-datafile.md)                                           | Elimina el archivo lógico (o directorio) especificado en la ruta de acceso del objeto. Implementado por WMI.<br/>                                                 |
| [**DeleteEx**](deleteex-method-in-class-cim-datafile.md)                                       | Elimina el archivo lógico (o directorio) especificado en la ruta de acceso del objeto. Implementado por WMI.<br/>                                                 |
| [**GetEffectivePermission**](geteffectivepermission-method-in-class-cim-datafile.md)           | Determina si el llamador tiene los permisos agregados especificados por el argumento de **permiso** . Implementado por WMI.<br/>                |
| [**Cambiar el nombre**](rename-method-in-class-cim-datafile.md)                                           | Cambia el nombre del archivo lógico (o directorio) especificado en la ruta de acceso del objeto. Implementado por WMI.<br/>                                                 |
| [**TakeOwnerShip**](takeownership-method-in-class-cim-datafile.md)                             | Obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto. Implementado por WMI.<br/>                                                   |
| [**TakeOwnerShipEx**](takeownershipex-method-in-class-cim-datafile.md)                         | Obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto. Implementado por WMI.<br/>                                                   |
| [**Descomprimir**](uncompress-method-in-class-cim-datafile.md)                                   | Descomprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto. Implementado por WMI.<br/>                                            |
| [**UncompressEx**](uncompressex-method-in-class-cim-datafile.md)                               | Descomprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto. Implementado por WMI.<br/>                                            |



 

### <a name="properties"></a>Propiedades

La clase de **\_ archivo de archivos CIM** tiene estas propiedades.

<dl> <dt>

**AccessMask**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("derechos de acceso")
</dt> </dl>

Máscara de archivos que representa los derechos de acceso necesarios para obtener acceso o realizar operaciones específicas en el archivo. Para los valores de bit, consulte [**constantes de derechos de acceso a archivos y directorios**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).

> [!Note]  
> En los volúmenes FAT, se devuelve el valor de **\_ acceso completo** en su lugar, lo que indica que no se ha establecido ninguna seguridad en el objeto.

 

Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

**Archivo \_ de LEER \_ datos (archivo) o directorio de lista de archivos \_ \_ (directorio)** (1)


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

**Archivo \_ de ESCRIBIR \_ datos (archivo) o archivo \_ agregar \_ archivo (directorio)** (2)


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

**Archivo \_ de ANEXAr \_ datos (archivo) o archivo \_ agregar \_ subdirectorio (directorio)** (4)


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

**Archivo \_ de LEER \_ EA** (8)


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

**Archivo \_ de ESCRIBIR \_ EA** (16)


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

**Archivo \_ de EJECUTAR (archivo) o \_ atravesar archivos (directorio)** (32)


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

**Archivo \_ de ELIMINAR \_ secundario (directorio)** (64)


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

**Archivo \_ de \_Atributos de lectura** (128)


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

**Archivo \_ de \_Atributos de escritura** (256)


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

**Eliminar** (65536)


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

**Leer \_ CONTROL** (131072)


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

**Escribir \_ DAC** (262144)


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

**Escribir \_ PROPIETARIO** (524288)


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

**Sincronizar** (1048576)


</dt> <dd></dd> </dl>

</dd> <dt>

**Archivar**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("se debe archivar")
</dt> </dl>

Si **es true**, se debe archivar el archivo.

Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).

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

**Compressed**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("comprimido")
</dt> </dl>

Si es **true**, el archivo se comprime.

Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**CompressionMethod**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("método de compresión")
</dt> </dl>

Cadena de forma libre que indica el algoritmo o la herramienta que se usa para comprimir el archivo lógico. Si el esquema de compresión es desconocido o no se ha descrito, use "Unknown". Si el archivo lógico está comprimido, pero el esquema de compresión es desconocido o no se ha descrito, use "comprimido". Si el archivo lógico no está comprimido, use "no comprimido".

Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre de clase")
</dt> </dl>

Nombre de la clase.

Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**CreationDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("fecha de creación")
</dt> </dl>

Fecha y hora de creación del archivo.

Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**CSCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de archivos CIM**](cim-filesystem.md).**CSCreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nombre de clase de sistema de equipo ")
</dt> </dl>

Clase del sistema del equipo.

Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de archivos CIM**](cim-filesystem.md).**CSName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Computer System Name ")
</dt> </dl>

Nombre del sistema del equipo.

Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).

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

**Unidad**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")
</dt> </dl>

Letra de unidad (incluidos los dos puntos que siguen a la letra de unidad) del archivo.

Ejemplo: "c:"

Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**EightDotThreeFileName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre de archivo de ocho puntos tres")
</dt> </dl>

Nombre de archivo compatible con DOS.

Ejemplo: "c: \\ programa ~ 1"

Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**Cifrado**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("cifrado")
</dt> </dl>

Si es **true**, el archivo está cifrado.

Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**EncryptionMethod**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("método de cifrado")
</dt> </dl>

Cadena de forma libre que identifica el algoritmo o la herramienta que se usa para cifrar un archivo lógico. Si el esquema de cifrado no es indulged (por motivos de seguridad, por ejemplo), use "Unknown". Si el archivo está cifrado, pero el esquema de cifrado es desconocido o no se ha divulgado, use "cifrado". Si el archivo lógico no está cifrado, use "no cifrado".

Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**Extensión**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("extensión de archivo")
</dt> </dl>

Extensión de nombre de archivo sin el punto anterior (punto).

Ejemplo: "txt", "MOF", "mdb"

Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre de archivo")
</dt> </dl>

Nombre de archivo sin la extensión de nombre de archivo. Ejemplo: "MyDataFile"

Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**FileSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("size"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")
</dt> </dl>

Tamaño del archivo, en bytes.

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**FileType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo de archivo")
</dt> </dl>

Descriptor que representa el tipo de archivo indicado por la propiedad de **extensión** .

Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**FSCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de archivos CIM**](cim-filesystem.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nombre de clase del sistema de archivos ")
</dt> </dl>

Clase del sistema de archivos.

Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**FSName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de archivos CIM**](cim-filesystem.md).**Nombre**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nombre del sistema de archivos ")
</dt> </dl>

Nombre del sistema de archivos.

Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**Oculto**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")
</dt> </dl>

Si es **true**, el archivo está oculto.

Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).

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

**InUseCount**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("recuento de apertura de archivos actuales")
</dt> </dl>

Número de "archivos abiertos" que están activos actualmente en el archivo.

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**LastAccessed**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("último acceso")
</dt> </dl>

Fecha y hora en que se produjo el último acceso al archivo.

Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**Última**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("última modificación")
</dt> </dl>

Fecha y hora en que se modificó el archivo por última vez.

Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**Le**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("manufacturer")
</dt> </dl>

Cadena del fabricante del recurso de versión (si está presente).

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

La propiedad Name es una cadena que representa el nombre heredado que actúa como clave de una instancia de archivo lógico dentro de un sistema de archivos. Se deben proporcionar los nombres de ruta de acceso completa.

Ejemplo: C: \\ Windows \\ System \\win.ini

Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**Ruta de acceso**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("path")
</dt> </dl>

Ruta de acceso del archivo, incluidas las barras diagonales inversas iniciales y finales. Ejemplo: " \\ sistema de Windows \\ \\ "

Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**Puedan**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("legible")
</dt> </dl>

Si **es true**, se puede leer el archivo.

Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).

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

</dd> <dt>

**Sistema**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("archivo del sistema")
</dt> </dl>

Si es **true**, el archivo es un archivo del sistema.

Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**Versión**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("versión")
</dt> </dl>

Cadena de versión del recurso de versión (si está presente).

</dd> <dt>

**Writeable (Grabable)**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("grabable")
</dt> </dl>

Si **es true**, se puede escribir el archivo.

Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase de **\_ archivo de archivos CIM** se deriva de [**\_ LogicalFile CIM**](cim-logicalfile.md).

WMI implementa la clase **de \_ archivo de archivos CIM** y todos sus métodos. La clase de **\_ archivo de archivos CIM** es una clase dinámica.

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.

Por motivos de seguridad, WMI no admite directamente la llamada a un equipo remoto y le indica que copie archivos en sí mismo. Sin embargo, puede usar el lenguaje de programación pertinente para llamar a FTP o RoboCopy, por ejemplo.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de [código](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Generate-Exchange-2388e7c9) del centro de scripting se usa una clase de **archivo de \_ archivos CIM** como parte de una aplicación más grande para generar informes de entorno de Exchange mediante PowerShell.

El ejemplo de código [Find files with WMI PowerShell](https://Gallery.TechNet.Microsoft.Com/Find-files-with-WMI-8851e1ea) de la galería de TechNet usa un **\_ archivo** de información de CIM para buscar uno o varios archivos en varios equipos.

El siguiente ejemplo de código VBS describe cómo realizar una búsqueda con caracteres comodín estándar en un archivo de archivos. Tenga en cuenta que los delimitadores de barra diagonal inversa deben tener otra barra diagonal inversa ( \\ \\ ). Además, cuando se usa **" \_ archivo de archivos CIM**.**Nombre de archivo**"en la cláusula WHERE, el proceso de WMIPRVSE examinará todos los directorios de cualquier dispositivo de almacenamiento disponible. Esto puede tardar algún tiempo, especialmente si ha asignado recursos compartidos remotos, y puede desencadenar advertencias del antivirus.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFiles = objWMIService.ExecQuery("Select * from CIM_DataFile where FileName Like '%~%'")
For Each objFile in colFiles
   Wscript.Echo objFile.Name
Next
```



El siguiente fragmento de código limita el intervalo de búsqueda a una unidad específica, una ruta de acceso y una extensión de archivo.


```VB
Set colFiles = objWMIService.ExecQuery("Select * from CIM_DataFile where Drive='"C:"' And Path='"\\"' and Name Like '%~%' and Extension='doc' ")
```



El siguiente ejemplo de código de PowerShell recupera un valor de atributo único.


```PowerShell
 $computer = "."

  $path = "C:\\Program Files\\Microsoft SQL Server\\MSSQL.1\\MSSQL\\LOG\\"

  $filename = "ERRORLOG"

  $fullname = $path + $filename

  $wql = 'SELECT Archive FROM CIM_DataFile WHERE Name = "' + $fullname + '"'


  Get-WmiObject -ComputerName $computer -Query $wql | foreach { $_.Archive }
```



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

[**\_LOGICALFILE CIM**](cim-logicalfile.md)
</dt> <dt>

[Tareas de WMI: archivos y carpetas](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[**Constantes de derechos de acceso a archivos y directorios**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

