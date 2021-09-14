---
description: CodecFile de Win32 \_&\# 32; La clase WMI representa el códec de audio o vídeo instalado en el sistema del equipo.
ms.assetid: 48ea3b92-0ea1-4aba-b067-bce0ec356cd2
ms.tgt_platform: multiple
title: Win32_CodecFile clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile
- Win32_CodecFile.AccessMask
- Win32_CodecFile.Archive
- Win32_CodecFile.Caption
- Win32_CodecFile.Compressed
- Win32_CodecFile.CompressionMethod
- Win32_CodecFile.CreationClassName
- Win32_CodecFile.CreationDate
- Win32_CodecFile.CSCreationClassName
- Win32_CodecFile.CSName
- Win32_CodecFile.Description
- Win32_CodecFile.Drive
- Win32_CodecFile.EightDotThreeFileName
- Win32_CodecFile.Encrypted
- Win32_CodecFile.EncryptionMethod
- Win32_CodecFile.Extension
- Win32_CodecFile.FileName
- Win32_CodecFile.FileSize
- Win32_CodecFile.FileType
- Win32_CodecFile.FSCreationClassName
- Win32_CodecFile.FSName
- Win32_CodecFile.Group
- Win32_CodecFile.Hidden
- Win32_CodecFile.InstallDate
- Win32_CodecFile.InUseCount
- Win32_CodecFile.LastAccessed
- Win32_CodecFile.LastModified
- Win32_CodecFile.Manufacturer
- Win32_CodecFile.Name
- Win32_CodecFile.Path
- Win32_CodecFile.Readable
- Win32_CodecFile.Status
- Win32_CodecFile.System
- Win32_CodecFile.Version
- Win32_CodecFile.Writeable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fc7a6073ab2841fde4492cd59ae1696aeca9f6a7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160320"
---
# <a name="win32_codecfile-class"></a>Clase CodecFile de Win32 \_

La **clase \_ WMI CodecFile** [de](/windows/desktop/WmiSdk/retrieving-a-class) Win32 representa el códec de audio o vídeo instalado en el sistema del equipo. Los códecs convierten un tipo de formato multimedia en otro, normalmente un formato comprimido en un formato sin comprimir. El nombre "codec" se deriva de una combinación de comprimir y descomprimir. Por ejemplo, un códec puede convertir un formato comprimido, como MS-ADPCM, a un formato sin comprimir como PCM, que la mayoría del hardware de audio puede reproducir directamente.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4C3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_CodecFile : CIM_DataFile
{
  uint32   AccessMask;
  boolean  Archive;
  string   Caption;
  boolean  Compressed;
  string   CompressionMethod;
  string   CreationClassName;
  datetime CreationDate;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  string   Drive;
  string   EightDotThreeFileName;
  boolean  Encrypted;
  string   EncryptionMethod;
  string   Extension;
  string   FileName;
  uint64   FileSize;
  string   FileType;
  string   FSCreationClassName;
  string   FSName;
  string   Group;
  boolean  Hidden;
  datetime InstallDate;
  uint64   InUseCount;
  datetime LastAccessed;
  datetime LastModified;
  string   Manufacturer;
  string   Name;
  string   Path;
  boolean  Readable;
  string   Status;
  boolean  System;
  string   Version;
  boolean  Writeable;
};
```

## <a name="members"></a>Members

La **clase \_ CodecFile de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ CodecFile de Win32** tiene estos métodos.



| Método                                                                                             | Descripción                                                                                                                                                                                                            |
|:---------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-codecfile.md)     | Cambia los permisos de seguridad para el archivo lógico especificado en la ruta de acceso del objeto.<br/>                                                                                                                         |
| [**ChangeSecurityPermissionsEx**](changesecuritypermissionsex-method-in-class-win32-codecfile.md) | Cambia los permisos de seguridad para el archivo lógico especificado en la ruta de acceso del objeto.<br/>                                                                                                                         |
| [**Comprimir**](compress-method-in-class-win32-codecfile.md)                                       | Comprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.<br/>                                                                                                                                    |
| [**CompressEx**](compressex-method-in-class-win32-codecfile.md)                                   | Comprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.<br/>                                                                                                                                    |
| [**Copiar**](copy-method-in-class-win32-codecfile.md)                                               | Copia el archivo lógico o directorio especificado en la ruta de acceso del objeto a la ubicación especificada por el parámetro de entrada.<br/>                                                                                         |
| [**CopyEx**](copyex-method-in-class-win32-codecfile.md)                                           | Método de clase que copia el archivo lógico o directorio especificado en la ruta de acceso del objeto a la ubicación especificada por el parámetro FileName.<br/>                                                                    |
| [**Eliminar**](delete-method-in-class-win32-codecfile.md)                                           | Elimina el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.<br/>                                                                                                                                       |
| [**DeleteEx**](deleteex-method-in-class-win32-codecfile.md)                                       | Elimina el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.<br/>                                                                                                                                       |
| [**GetEffectivePermission**](geteffectivepermission-method-in-class-win32-codecfile.md)           | Determina si el autor de la llamada tiene  los permisos agregados especificados por el argumento de permiso no solo en el objeto de archivo, sino también en el recurso compartido en el que reside el archivo o directorio (si se encuentra en un recurso compartido).<br/> |
| [**Cambiar nombre**](rename-method-in-class-win32-codecfile.md)                                           | Método de clase que cambia el nombre del archivo lógico (o directorio) especificado en la ruta de acceso del objeto.<br/>                                                                                                                     |
| [**TakeOwnerShip**](takeownership-method-in-class-win32-codecfile.md)                             | Obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto.<br/>                                                                                                                                         |
| [**TakeOwnerShipEx**](takeownershipex-method-in-class-win32-codecfile.md)                         | Método de clase que obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto.<br/>                                                                                                                       |
| [**Descomprimir**](uncompress-method-in-class-win32-codecfile.md)                                   | Descomprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.<br/>                                                                                                                                  |
| [**UncompressEx**](uncompressex-method-in-class-win32-codecfile.md)                               | Descomprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.<br/>                                                                                                                                  |



 

### <a name="properties"></a>Propiedades

La **clase \_ CodecFile de Win32** tiene estas propiedades.

<dl> <dt>

**Máscara de acceso**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Access Rights")
</dt> </dl>

Máscara de bits que representa los derechos de acceso necesarios para acceder o realizar operaciones específicas en el archivo de códec. Para obtener valores de bits, vea Constantes de derechos de [**acceso a archivos y directorios.**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)

> [!Note]  
> En los volúmenes FAT, se devuelve el valor **\_ FULL ACCESS** en su lugar, lo que indica que no se ha establecido ninguna seguridad en el objeto.

 

Esta propiedad se hereda de [**CIM \_ LogicalFile**](cim-logicalfile.md).

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

**FILE \_ READ \_ DATA (archivo) o FILE \_ LIST DIRECTORY \_ (directorio)** (1)


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

**FILE \_ WRITE \_ DATA (archivo) o FILE \_ ADD FILE \_ (directorio)** (2)


</dt> <dd></dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

**FILE \_ APPEND \_ DATA (archivo) o \_ SUBDIRECTORIO AGREGAR ARCHIVO \_ (directorio)** (4)


</dt> <dd></dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

**FILE \_ READ \_ EA** (8)


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

**FILE \_ WRITE \_ EA** (16)


</dt> <dd></dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

**FILE \_ EXECUTE (archivo) o FILE \_ TRAVERSE (directorio)** (32)


</dt> <dd></dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

**FILE \_ DELETE \_ CHILD (directorio)** (64)


</dt> <dd></dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

**FILE \_ ATRIBUTOS \_ DE LECTURA** (128)


</dt> <dd></dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

**FILE \_ ATRIBUTOS \_ DE** ESCRITURA (256)


</dt> <dd></dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

**DELETE** (65536)


</dt> <dd></dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

**READ \_ CONTROL** (131072)


</dt> <dd></dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

**ESCRITURA \_ DAC** (262144)


</dt> <dd></dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

**ESCRITURA \_ OWNER** (524288)


</dt> <dd></dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

**SYNCHRONIZE** (1048576)


</dt> <dd></dd> </dl>

</dd> <dt>

**Archivar**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Should Be Archived")
</dt> </dl>

Si **es True**, el archivo se debe archivar.

Esta propiedad se hereda de [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Breve descripción del objeto.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Compressed**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Compressed")
</dt> </dl>

Si **es True**, el archivo se comprime.

Esta propiedad se hereda de [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**CompressionMethod**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Método de compresión")
</dt> </dl>

Algoritmo o herramienta que se usa para comprimir el archivo lógico. Si no es posible (o no se desea) describir el esquema de compresión (quizás porque no se conoce), use las siguientes palabras: "Desconocido" para representar que no se sabe si el archivo lógico está comprimido o no; "Compressed" para representar que el archivo está comprimido, pero su esquema de compresión no se conoce o no se ha divulgado; y "No comprimido" para representar que el archivo lógico no está comprimido.

Esta propiedad se hereda de [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Nombre de clase")
</dt> </dl>

Nombre de la primera clase concreta que aparece en la cadena de herencia utilizada en la creación de una instancia de . Cuando se usa con las otras propiedades clave de la clase , la propiedad permite identificar de forma única todas las instancias de esta clase y sus subclases.

Esta propiedad se hereda de [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**CreationDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Fecha de creación")
</dt> </dl>

Fecha de creación del archivo.

Esta propiedad se hereda de [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**CSCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ FileSystem**](cim-filesystem.md).**CSCreationClassName**"), [**Clave CIM \_**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Nombre de clase del sistema de equipo")
</dt> </dl>

Clase del sistema del equipo.

Esta propiedad se hereda de [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ FileSystem**](cim-filesystem.md).**CSName**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Computer System Name")
</dt> </dl>

Cadena que representa el nombre del sistema del equipo.

Esta propiedad se hereda de [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Description), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet control \\ \\ \\ \\ MediaResources \\ \\ icm \| Description")
</dt> </dl>

Nombre completo del controlador de códec. Esta cadena está pensada para mostrarse en espacios grandes (descriptivos).

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

Ejemplo: "Microsoft PCM Converter"

</dd> <dt>

**Unidad**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")
</dt> </dl>

Letra de unidad (incluidos los dos puntos) del archivo.

Esta propiedad se hereda de [**CIM \_ LogicalFile**](cim-logicalfile.md).

Ejemplo: "c:"

</dd> <dt>

**EightDotThreeFileName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Eight Dot Three File Name")
</dt> </dl>

Nombre de archivo compatible con DOS para este archivo.

Esta propiedad se hereda de [**CIM \_ LogicalFile**](cim-logicalfile.md).

Ejemplo: "c: \\ progra~1"

</dd> <dt>

**Cifrado**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Encrypted")
</dt> </dl>

Si **es True**, el archivo está cifrado.

Esta propiedad se hereda de [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**EncryptionMethod**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Método de cifrado")
</dt> </dl>

Algoritmo o herramienta que se usa para cifrar el archivo lógico. Si no es posible (o no se desea) describir el esquema de cifrado (quizás por motivos de seguridad), use las siguientes palabras: "Desconocido" para representar que no se sabe si el archivo lógico está cifrado o no; "Encrypted" para representar que el archivo está cifrado pero su esquema de cifrado no se conoce o no se ha divulgado; y "Not Encrypted" para representar que el archivo lógico no está cifrado.

Esta propiedad se hereda de [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Extensión**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Extension")
</dt> </dl>

Extensión de nombre de archivo (sin el punto).

Esta propiedad se hereda de [**CIM \_ LogicalFile**](cim-logicalfile.md).

Ejemplos: "txt", "mof", "mdb"

</dd> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Name")
</dt> </dl>

Nombre (sin la extensión) del archivo.

Esta propiedad se hereda de [**CIM \_ LogicalFile**](cim-logicalfile.md).

Ejemplo: "autoexec"

</dd> <dt>

**FileSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tamaño"), [**Unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")
</dt> </dl>

Tamaño del archivo (en bytes).

Esta propiedad se hereda de [**CIM \_ LogicalFile**](cim-logicalfile.md).

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> <dt>

**FileType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Type")
</dt> </dl>

Tipo de archivo (indicado por la **propiedad Extension).**

Esta propiedad se hereda de [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**FSCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ FileSystem**](cim-filesystem.md).**CreationClassName**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Nombre de clase del sistema de archivos")
</dt> </dl>

Clase del sistema de archivos.

Esta propiedad se hereda de [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**FSName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ FileSystem**](cim-filesystem.md).**Name**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File System Name")
</dt> </dl>

Nombre del sistema de archivos.

Esta propiedad se hereda de [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Grupo**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| SOFTWARE Microsoft Windows NT \\ \\ \\ \\ \\ \\ CurrentVersion \\ \\ drivers.desc")
</dt> </dl>

Códec representado por esta clase.

Los valores son:

<dl> <dd>"Audio"</dd> <dd>"Vídeo"</dd> </dl>

<dt>

<span id="Audio"></span><span id="audio"></span><span id="AUDIO"></span>

**Audio** ("Audio")


</dt> <dd></dd> <dt>

<span id="Video"></span><span id="video"></span><span id="VIDEO"></span>

**Vídeo** ("Vídeo")


</dt> <dd></dd> </dl>

</dd> <dt>

**Oculto**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hidden")
</dt> </dl>

Si **es True**, el archivo está oculto.

Esta propiedad se hereda de [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Fecha de instalación")
</dt> </dl>

Se instaló el objeto . Esta propiedad no requiere un valor para indicar que el objeto está instalado.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**InUseCount**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Current File Open Count")
</dt> </dl>

Número de "archivos que se abren" que están activos actualmente en el archivo.

Esta propiedad se hereda de [**CIM \_ LogicalFile**](cim-logicalfile.md).

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> <dt>

**LastAccessed**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Último acceso")
</dt> </dl>

Se ha accedido por última vez al archivo.

Esta propiedad se hereda de [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**LastModified**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Última modificación")
</dt> </dl>

El archivo se modificó por última vez.

Esta propiedad se hereda de [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Fabricante**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer")
</dt> </dl>

Cadena de fabricante del recurso de versión, si hay alguno.

Esta propiedad se hereda de [**CIM \_ DataFile**](cim-datafile.md).

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **Clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nombre heredado que actúa como clave de una instancia de archivo lógico dentro de un sistema de archivos. Se deben proporcionar nombres de ruta de acceso completos.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

Ejemplo: "C: \\ Windows \\ sistema \\win.ini"

</dd> <dt>

**Path**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")
</dt> </dl>

Ruta de acceso del archivo. Esto incluye barras diagonales inversas iniciales y finales.

Esta propiedad se hereda de [**CIM \_ LogicalFile**](cim-logicalfile.md).

Ejemplo: " \\ sistema windows \\ \\ "

</dd> <dt>

**Legible**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Readable")
</dt> </dl>

El archivo se puede leer.

Esta propiedad se hereda de [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Estado actual del objeto. Se pueden definir varios estados operativos y no operativos. Los estados operativos incluyen: "Ok", "Degraded" y "Pred Fail" (un elemento, como una unidad de disco duro habilitada para SMART, puede funcionar correctamente pero predecir un error en un futuro próximo). Los estados no operativo incluyen: "Error", "Starting", "Stopping" y "Service". El último, "Servicio", podría aplicarse durante la resilvering de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo. No todo este trabajo está en línea, pero el elemento administrado no es "correcto" ni está en uno de los demás estados.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

Los valores son los siguientes:

<dt>

<span id="OK"></span><span id="ok"></span>

**Ok** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Error** ("Error")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Degradado** ("Degradado")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** ("Desconocido")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Error de pred** ("error previo")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**A partir** de ("Starting")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Detención** ("Deteniendo")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Servicio** ("Servicio")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Estresado** ("estresado")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ("NonRecover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Sin contacto** ("Sin contacto")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Comm perdido** ("Comm perdido")


</dt> <dd></dd> </dl>

</dd> <dt>

**Sistema**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System File")
</dt> </dl>

Si **es True**, el archivo es un archivo del sistema.

Esta propiedad se hereda de [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> <dt>

**Versión**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version")
</dt> </dl>

Cadena de versión del recurso de versión, si hay alguno.

Esta propiedad se hereda de [**CIM \_ DataFile**](cim-datafile.md).

</dd> <dt>

**Writeable (Grabable)**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Writeable")
</dt> </dl>

Si **es True**, se puede escribir el archivo.

Esta propiedad se hereda de [**CIM \_ LogicalFile**](cim-logicalfile.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ CodecFile de Win32** se deriva de [**CIM \_ DataFile**](cim-datafile.md).

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

[**CIM \_ DataFile**](cim-datafile.md)
</dt> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

