---
description: El archivo de \_ paginación de Win32&\# 32; La clase WMI representa el archivo usado para controlar el intercambio de archivos de memoria virtual en un sistema Win32. Esta clase está en desuso.
ms.assetid: 5599d09d-a2fd-4217-8560-5fd56f09d47b
ms.tgt_platform: multiple
title: Win32_PageFile (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile
- Win32_PageFile.Caption
- Win32_PageFile.Description
- Win32_PageFile.InstallDate
- Win32_PageFile.Archive
- Win32_PageFile.Compressed
- Win32_PageFile.CompressionMethod
- Win32_PageFile.CreationClassName
- Win32_PageFile.CreationDate
- Win32_PageFile.CSCreationClassName
- Win32_PageFile.CSName
- Win32_PageFile.Drive
- Win32_PageFile.EightDotThreeFileName
- Win32_PageFile.Encrypted
- Win32_PageFile.EncryptionMethod
- Win32_PageFile.Extension
- Win32_PageFile.FileName
- Win32_PageFile.FileSize
- Win32_PageFile.FileType
- Win32_PageFile.FSCreationClassName
- Win32_PageFile.FSName
- Win32_PageFile.Hidden
- Win32_PageFile.InUseCount
- Win32_PageFile.LastAccessed
- Win32_PageFile.LastModified
- Win32_PageFile.Path
- Win32_PageFile.Readable
- Win32_PageFile.System
- Win32_PageFile.Writeable
- Win32_PageFile.AccessMask
- Win32_PageFile.Manufacturer
- Win32_PageFile.Status
- Win32_PageFile.Version
- Win32_PageFile.FreeSpace
- Win32_PageFile.InitialSize
- Win32_PageFile.MaximumSize
- Win32_PageFile.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fb63c4242ae8fa3cca5133a25d2742d07210ca1c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659697"
---
# <a name="win32_pagefile-class"></a>Clase de archivo de \_ paginación Win32

La [clase WMI](../wmisdk/retrieving-a-class.md) de archivo de **\_ paginación de Win32** representa el archivo usado para controlar el intercambio de archivos de memoria virtual en un sistema Win32. Esta clase está en desuso.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[DEPRECATED, Dynamic, Provider("CIMWin32"), Privileges("SeCreatePagefilePrivilege"), UUID("{8502C4C6-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("PutInstance"), SupportsDelete, DeleteBy("DeleteInstance"), SupportsUpdate, AMENDMENT]
class Win32_PageFile : CIM_DataFile
{
  string   Caption;
  string   Description;
  datetime InstallDate;
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
  uint32   AccessMask;
  string   Manufacturer;
  string   Status;
  string   Version;
  uint32   FreeSpace;
  uint32   InitialSize;
  uint32   MaximumSize;
  string   Name;
};
```

## <a name="members"></a>Miembros

La clase de archivo de **\_ paginación Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase de archivo de **\_ paginación Win32** tiene estos métodos.



| Método                                                                                            | Descripción                                                                                                                                                                                                                            |
|:--------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-pagefile.md)     | Método de clase que cambia los permisos de seguridad para el archivo lógico especificado en la ruta de acceso del objeto.<br/>                                                                                                                       |
| [**ChangeSecurityPermissionsEx**](changesecuritypermissionsex-method-in-class-win32-pagefile.md) | Método de clase que cambia los permisos de seguridad para el archivo lógico especificado en la ruta de acceso del objeto.<br/>                                                                                                                       |
| [**Comprimir**](compress-method-in-class-win32-pagefile.md)                                       | Método de clase que comprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.<br/>                                                                                                                                  |
| [**CompressEx**](compressex-method-in-class-win32-pagefile.md)                                   | Método de clase que comprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.<br/>                                                                                                                                  |
| [**Copiar**](copy-method-in-class-win32-pagefile.md)                                               | Método de clase que copia el archivo lógico o el directorio especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro de entrada.<br/>                                                                                       |
| [**CopyEx**](copyex-method-in-class-win32-pagefile.md)                                           | Método de clase que copia el archivo lógico o el directorio especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro FileName.<br/>                                                                                    |
| [**Elimínelos**](delete-method-in-class-win32-pagefile.md)                                           | Método de clase que elimina el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.<br/>                                                                                                                                     |
| [**DeleteEx**](deleteex-method-in-class-win32-pagefile.md)                                       | Método de clase que elimina el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.<br/>                                                                                                                                     |
| [**GetEffectivePermission**](geteffectivepermission-method-in-class-win32-pagefile.md)           | Método de clase que determina si el llamador tiene los permisos agregados especificados por el argumento *Permission* no solo en el objeto File, sino en el recurso compartido en el que reside el archivo o directorio (si está en un recurso compartido).<br/> |
| [**Cambiar el nombre**](rename-method-in-class-win32-pagefile.md)                                           | Método de clase que cambia el nombre del archivo lógico (o directorio) especificado en la ruta de acceso del objeto.<br/>                                                                                                                                     |
| [**TakeOwnerShip**](takeownership-method-in-class-win32-pagefile.md)                             | Método de clase que obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto.<br/>                                                                                                                                       |
| [**TakeOwnerShipEx**](takeownershipex-method-in-class-win32-pagefile.md)                         | Método de clase que obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto.<br/>                                                                                                                                       |
| [**Descomprimir**](uncompress-method-in-class-win32-pagefile.md)                                   | Método de clase que descomprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.<br/>                                                                                                                                |
| [**UncompressEx**](uncompressex-method-in-class-win32-pagefile.md)                               | Método de clase que descomprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.<br/>                                                                                                                                |



 

### <a name="properties"></a>Propiedades

La clase de archivo de **\_ paginación Win32** tiene estas propiedades.

<dl> <dt>

**AccessMask**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**displayName**](../wmisdk/standard-qualifiers.md) ("derechos de acceso")
</dt> </dl>

Máscara de archivos que representa los derechos de acceso necesarios para obtener acceso o realizar operaciones específicas en el archivo. Para ver los valores, consulte [**constantes de derechos de acceso a archivos y directorios**](../wmisdk/file-and-directory-access-rights-constants.md).

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

Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**displayName**](../wmisdk/standard-qualifiers.md) ("se debe archivar")
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

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")
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

Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**displayName**](../wmisdk/standard-qualifiers.md) ("comprimido")
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

Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("método de compresión")
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

Calificadores: [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**displayName**](../wmisdk/standard-qualifiers.md) ("nombre de clase")
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

Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("fecha de creación")
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

Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema de archivos CIM**](cim-filesystem.md).**CSCreationClassName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**displayName**](../wmisdk/standard-qualifiers.md) (" nombre de clase de sistema de equipo ")
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

Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema de archivos CIM**](cim-filesystem.md).**CSName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**displayName**](../wmisdk/standard-qualifiers.md) (" Computer System Name ")
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

Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")
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

Calificadores: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**displayName**](../wmisdk/standard-qualifiers.md) ("Drive")
</dt> </dl>

Letra de unidad (incluidos los dos puntos que siguen a la letra de unidad) del archivo. Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).

Ejemplo: "c:"

Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**EightDotThreeFileName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**displayName**](../wmisdk/standard-qualifiers.md) ("nombre de archivo de ocho puntos tres")
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

Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**displayName**](../wmisdk/standard-qualifiers.md) ("cifrado")
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

Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("método de cifrado")
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

Calificadores: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**displayName**](../wmisdk/standard-qualifiers.md) ("extensión de archivo")
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

Calificadores: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**displayName**](../wmisdk/standard-qualifiers.md) ("nombre de archivo")
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

Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("size"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Tamaño del archivo, en bytes.

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).

Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**FileType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**displayName**](../wmisdk/standard-qualifiers.md) ("tipo de archivo")
</dt> </dl>

Descriptor que representa el tipo de archivo indicado por la propiedad de **extensión** .

Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**FreeSpace**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**desusados**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estructuras de administración de memoria inesperados win32api \| [**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus) \| dwAvailPageFile"), [**unidades**](../wmisdk/standard-qualifiers.md) ("megabytes")
</dt> </dl>

Espacio disponible en el archivo de paginación. El sistema operativo puede aumentar el archivo de paginación según sea necesario, hasta el límite impuesto por el usuario. Esta propiedad muestra la diferencia entre el tamaño de la memoria asignada actual y el tamaño actual del archivo de paginación; no muestra el mayor tamaño posible del archivo de paginación.

</dd> <dt>

**FSCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema de archivos CIM**](cim-filesystem.md).**CreationClassName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**displayName**](../wmisdk/standard-qualifiers.md) (" nombre de clase del sistema de archivos ")
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

Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema de archivos CIM**](cim-filesystem.md).**Nombre**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**displayName**](../wmisdk/standard-qualifiers.md) (" nombre del sistema de archivos ")
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

Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**displayName**](../wmisdk/standard-qualifiers.md) ("Hidden")
</dt> </dl>

Si es **true**, el archivo está oculto.

Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**InitialSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**desusado**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Regstry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Session Manager \\ \\ Administración \| de memoria PagingFiles"), [**unidades**](../wmisdk/standard-qualifiers.md) ("megabytes")
</dt> </dl>

Tamaño inicial del archivo de paginación.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")
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

Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("recuento de apertura de archivos actuales")
</dt> </dl>

Número de "archivos abiertos" que están activos actualmente en el archivo.

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).

Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**LastAccessed**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("último acceso")
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

Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("última modificación")
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

Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**displayName**](../wmisdk/standard-qualifiers.md) ("manufacturer")
</dt> </dl>

Cadena del fabricante del recurso de versión (si está presente).

Esta propiedad se hereda del [**\_ archivo**](cim-datafile.md)de propiedades CIM.

</dd> <dt>

**Tamañomáximo**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**desusados**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estructuras de administración de memoria inesperados win32api \| [**MEMORYSTATUS**](/windows/win32/api/winbase/ns-winbase-memorystatus) \| dwTotalPageFile"), [**unidades**](../wmisdk/standard-qualifiers.md) ("megabytes")
</dt> </dl>

Tamaño máximo del archivo de paginación establecido por el usuario. El sistema operativo no permitirá que el archivo de paginación supere este límite.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**desusados**](../wmisdk/standard-wmi-qualifiers.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32DLL \|NTDLL.DLL\| [**NtQuerySystemInformation**](/windows/win32/api/winternl/nf-winternl-ntquerysysteminformation) \| SystemPageFileInformation \| PageFileName")
</dt> </dl>

Nombre del archivo de paginación.

Ejemplo: "C: \\PAGEFILE.SYS"

</dd> <dt>

**Ruta de acceso**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**displayName**](../wmisdk/standard-qualifiers.md) ("path")
</dt> </dl>

Ruta de acceso del archivo, incluidas las barras diagonales inversas iniciales y finales.

Ejemplo: " \\ sistema de Windows \\ \\ "

Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**Puedan**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("legible")
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

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")
</dt> </dl>

Cadena que indica el estado actual del objeto.

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

Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**displayName**](../wmisdk/standard-qualifiers.md) ("archivo del sistema")
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

Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32"), [**displayName**](../wmisdk/standard-qualifiers.md) ("versión")
</dt> </dl>

Cadena de versión del recurso de versión (si está presente).

Esta propiedad se hereda del [**\_ archivo**](cim-datafile.md)de propiedades CIM.

</dd> <dt>

**Writeable (Grabable)**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("grabable")
</dt> </dl>

Si **es true**, se puede escribir el archivo.

Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase de archivo de **\_ paginación Win32** se deriva del [**\_ directorio CIM**](cim-directory.md).

## <a name="examples"></a>Ejemplos

En el ejemplo de código de VBScript siguiente se muestra cómo recuperar estadísticas de archivo de paginación desde instancias del archivo de **\_ paginación de Win32**.


```VB
Set PageFileSet = GetObject("winmgmts:").InstancesOf ("Win32_PageFile")

for each PageFile in PageFileSet
 WScript.Echo PageFile.Name & Chr(13) 
 WScript.Echo " Initial: " & PageFile.InitialSize & " MB"
 WScript.Echo " Max: " & PageFile.MaximumSize & " MB" 

next
```



En el ejemplo de código Perl siguiente se muestra cómo recuperar estadísticas del archivo de paginación desde instancias del archivo de **\_ paginación de Win32**.


```
use strict;
use Win32::OLE;

my $PageFileSet;

eval { $PageFileSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
 InstancesOf ("Win32_PageFile"); };
if (!$@ && defined $PageFileSet)
{
 foreach my $PageFileInst (in $PageFileSet)
 {
  print "\n$PageFileInst->{Name}\n";
  print " Initial: $PageFileInst->{InitialSize} MB\n";
  print " Maximum: $PageFileInst->{MaximumSize} MB\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
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

[**\_Archivo de archivos CIM**](cim-datafile.md)
</dt> <dt>

[Clases de sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
