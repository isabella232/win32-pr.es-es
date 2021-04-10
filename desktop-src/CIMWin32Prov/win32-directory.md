---
description: El \_ directorio Win32&\# 32; La clase WMI representa una entrada de directorio en un equipo que ejecuta Windows.
ms.assetid: d61cb5ee-8e87-4604-95e6-325c9b543411
ms.tgt_platform: multiple
title: Win32_Directory (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory
- Win32_Directory.Caption
- Win32_Directory.Description
- Win32_Directory.InstallDate
- Win32_Directory.Name
- Win32_Directory.Status
- Win32_Directory.AccessMask
- Win32_Directory.Archive
- Win32_Directory.Compressed
- Win32_Directory.CompressionMethod
- Win32_Directory.CreationClassName
- Win32_Directory.CreationDate
- Win32_Directory.CSCreationClassName
- Win32_Directory.CSName
- Win32_Directory.Drive
- Win32_Directory.EightDotThreeFileName
- Win32_Directory.Encrypted
- Win32_Directory.EncryptionMethod
- Win32_Directory.Extension
- Win32_Directory.FileName
- Win32_Directory.FileSize
- Win32_Directory.FileType
- Win32_Directory.FSCreationClassName
- Win32_Directory.FSName
- Win32_Directory.Hidden
- Win32_Directory.InUseCount
- Win32_Directory.LastAccessed
- Win32_Directory.LastModified
- Win32_Directory.Path
- Win32_Directory.Readable
- Win32_Directory.System
- Win32_Directory.Writeable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6185b9c0d427b7410d36f3fddfaf70c0ed8d364b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275052"
---
# <a name="win32_directory-class"></a>\_Clase de directorio Win32

La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) de **\_ directorio Win32** representa una entrada de directorio en un equipo que ejecuta Windows. Un directorio es un tipo de archivo que agrupa lógicamente los archivos de datos y proporciona información de ruta de acceso para los archivos agrupados. Ejemplo: C: \\ temp. **Win32 \_ El directorio** no incluye los directorios de las unidades de red.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4C7-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Directory : CIM_Directory
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
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
};
```

## <a name="members"></a>Miembros

La clase de **\_ directorio Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase de **\_ directorio Win32** tiene estos métodos.



| Método                                                                                             | Descripción                                                                                                                                                                                                                             |
|:---------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-directory.md)     | Método de clase que cambia los permisos de seguridad para el archivo lógico especificado en la ruta de acceso del objeto.<br/>                                                                                                                        |
| [**ChangeSecurityPermissionsEx**](changesecuritypermissionsex-method-in-class-win32-directory.md) | Método de clase que cambia los permisos de seguridad para el archivo lógico especificado en la ruta de acceso del objeto.<br/>                                                                                                                        |
| [**Comprimir**](compress-method-in-class-win32-directory.md)                                       | Método de clase que comprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.<br/>                                                                                                                                   |
| [**CompressEx**](compressex-method-in-class-win32-directory.md)                                   | Método de clase que comprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.<br/>                                                                                                                                   |
| [**Copiar**](copy-method-in-class-win32-directory.md)                                               | Método de clase que copia el archivo lógico o el directorio especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro de entrada.<br/>                                                                                        |
| [**CopyEx**](copyex-method-in-class-win32-directory.md)                                           | Método de clase que copia el archivo lógico o el directorio especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro *filename* .<br/>                                                                                   |
| [**Elimínelos**](delete-method-in-class-win32-directory.md)                                           | Método de clase que elimina el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.<br/>                                                                                                                                      |
| [**DeleteEx**](deleteex-method-in-class-win32-directory.md)                                       | Método de clase que elimina el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.<br/>                                                                                                                                      |
| [**GetEffectivePermission**](geteffectivepermission-method-in-class-win32-directory.md)           | Método de clase que determina si el llamador tiene los permisos agregados especificados por el argumento *Permissions* no solo en el objeto de archivo, sino en el recurso compartido en el que reside el archivo o directorio (si está en un recurso compartido).<br/> |
| [**Cambiar el nombre**](rename-method-in-class-win32-directory.md)                                           | Método de clase que cambia el nombre del archivo lógico (o directorio) especificado en la ruta de acceso del objeto.<br/>                                                                                                                                      |
| [**TakeOwnerShip**](takeownership-method-in-class-win32-directory.md)                             | Método de clase que obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto.<br/>                                                                                                                                        |
| [**TakeOwnerShipEx**](takeownershipex-method-in-class-win32-directory.md)                         | Método de clase que obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto.<br/>                                                                                                                                        |
| [**Descomprimir**](uncompress-method-in-class-win32-directory.md)                                   | Método de clase que descomprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.<br/>                                                                                                                                 |
| [**UncompressEx**](uncompressex-method-in-class-win32-directory.md)                               | Método de clase que descomprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.<br/>                                                                                                                                 |



 

### <a name="properties"></a>Propiedades

La clase de **\_ directorio Win32** tiene estas propiedades.

<dl> <dt>

**AccessMask**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("derechos de acceso")
</dt> </dl>

Máscara de máscara que representa los derechos de acceso necesarios para obtener acceso o realizar operaciones específicas en el directorio. Para los valores de bit, consulte [**constantes de derechos de acceso a archivos y directorios**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants).

> [!Note]  
> En los volúmenes FAT, se devuelve el valor de **\_ acceso completo** en su lugar, lo que indica que no se ha establecido ninguna seguridad en el objeto.

 

Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**Archivo \_ de LEER \_ datos (archivo) o directorio de lista de archivos \_ \_ (directorio)** (1)


</dt> <dd>

Concede el derecho a leer los datos del archivo. Para un directorio, este valor concede el derecho para mostrar el contenido del directorio.

</dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**Archivo \_ de ESCRIBIR \_ datos (archivo) o archivo \_ agregar \_ archivo (directorio)** (2)


</dt> <dd>

Concede el derecho para escribir datos en el archivo. Para un directorio, este valor concede el derecho a crear un archivo en el directorio.

</dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>**Archivo \_ de ANEXAr \_ datos (archivo) o \_ \_ subdirectorio de adición de archivo** (4)


</dt> <dd>

Concede el derecho para anexar datos al archivo. Para un directorio, este valor concede el derecho a crear un subdirectorio.

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**Archivo \_ de LEER \_ EA** (8)


</dt> <dd>

Concede el derecho para leer atributos extendidos.

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**Archivo \_ de ESCRIBIR \_ EA** (16)


</dt> <dd>

Concede el derecho para escribir atributos extendidos.

</dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**Archivo \_ de EJECUTAR (archivo) o \_ atravesar archivos (directorio)** (32)


</dt> <dd>

Concede el derecho para ejecutar un archivo. Para un directorio, se puede atravesar el directorio.

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**Archivo \_ de ELIMINAR \_ secundario (directorio)** (64)


</dt> <dd>

Concede el derecho para eliminar un directorio y todos los archivos que contiene (sus elementos secundarios), incluso si los archivos son de solo lectura.

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**Archivo \_ de \_Atributos de lectura** (128)


</dt> <dd>

Concede el derecho a leer los atributos de archivo.

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**Archivo \_ de \_Atributos de escritura** (256)


</dt> <dd>

Concede el derecho para cambiar los atributos de archivo.

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span id="DELETE"></span><span id="delete"></span>**Eliminar** (65536)


</dt> <dd>

Concede acceso de eliminación.

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span id="READ_CONTROL"></span><span id="read_control"></span>**Leer \_ CONTROL** (131072)


</dt> <dd>

Concede acceso de lectura al descriptor de seguridad y al propietario.

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span id="WRITE_DAC"></span><span id="write_dac"></span>**Escribir \_ DAC** (262144)


</dt> <dd>

Concede acceso de escritura a la ACL discrecional.

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>**Escribir \_ PROPIETARIO** (524288)


</dt> <dd>

Asigna el propietario de la escritura.

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Sincronizar** (1048576)


</dt> <dd>

Sincroniza el acceso y permite que un proceso espere a que un objeto entre en el estado señalado.

</dd> <dt>

<span id="ACCESS_SYSTEM_SECURITY"></span><span id="access_system_security"></span>

<span id="ACCESS_SYSTEM_SECURITY"></span><span id="access_system_security"></span>**Acceso a \_ \_Seguridad del sistema** (18809343)


</dt> <dd>

Controla la capacidad de obtener o establecer la SACL en el descriptor de seguridad de un objeto.

</dd> </dl>

</dd> <dt>

**Archivar**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("se debe archivar")
</dt> </dl>

Indica si se ha establecido el bit de archivo en la carpeta. Los programas de copia de seguridad utilizan el bit de archivo para identificar los archivos de los que se debe hacer una copia de seguridad. Si **es true**, se debe archivar el archivo.

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

Indica si la carpeta se ha comprimido o no. WMI reconoce las carpetas comprimidas mediante WMI o mediante la interfaz gráfica de usuario; sin embargo, no reconoce. Archivos ZIP como comprimidos. Si es **true**, el archivo se comprime.

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

Algoritmo o herramienta (normalmente un método) que se usa para comprimir el archivo lógico. Si no es posible (o no desea) describir el esquema de compresión (quizás porque no se conoce), use las siguientes palabras: "Unknown" para indicar que no se conoce si el archivo lógico está comprimido; "Compressed" para representar que el archivo está comprimido, pero su esquema de compresión no se conoce o no se revela; y "no comprimido" para representar que el archivo lógico no está comprimido.

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

Nombre de la primera clase concreta que debe aparecer en la cadena de herencia utilizada en la creación de una instancia. Cuando se usa con las otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.

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

Fecha en que se creó el objeto de sistema de archivos. Para obtener más información sobre cómo trabajar con formatos de fecha y hora de WMI, vea [tareas de WMI: fechas y horas](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).

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

Nombre de la clase de creación del sistema de ámbito del equipo.

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

Nombre del equipo en el que se almacena el objeto de sistema de archivos.

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

Letra de unidad de la unidad (incluidos los dos puntos) donde se almacena el objeto de sistema de archivos.

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

Nombre compatible con MS-DOS para la carpeta.

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

Indica si la carpeta está cifrada o no. Si es **true**, la carpeta está cifrada.

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

Algoritmo o herramienta que se usa para cifrar el archivo lógico. Si no es posible (o no desea) describir el esquema de cifrado (quizás por motivos de seguridad), use las siguientes palabras: "Unknown" para representar que no se conoce si el archivo lógico está cifrado; "Cifrado" para representar que el archivo está cifrado, pero el esquema de cifrado no es conocido o no se ha divulgado. y "no cifrado" para representar que el archivo lógico no está cifrado.

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

Extensión de nombre de archivo del objeto del sistema de archivos, sin incluir el punto (.) que separa la extensión del nombre de archivo.

Ejemplos: "txt", "MOF", "mdb"

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

Nombre de archivo (sin el punto o la extensión) del archivo.

Ejemplo: "Autoexec"

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

Tamaño del objeto del sistema de archivos, en bytes. Aunque las carpetas poseen una propiedad de **archivo** , siempre se devuelve el valor 0. Para determinar el tamaño de una carpeta, use FileSystemObject o agregue el tamaño de todos los archivos almacenados en la carpeta.

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

Tipo de archivo (indicado por la propiedad de **extensión** ).

Por ejemplo, es probable que un archivo. mdb tenga el tipo de archivo aplicación de Microsoft Access. Es probable que un archivo. asp tenga el tipo de archivo documento HTML. Las carpetas se suelen presentar simplemente como carpeta.

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

Tipo de sistema de archivos (NTFS, FAT, FAT32) instalado en la unidad donde se encuentra el archivo o la carpeta.

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

Indica si el objeto del sistema de archivos está oculto. Si es **true**, el archivo está oculto.

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

Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**LastAccessed**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("último acceso")
</dt> </dl>

Fecha en que se produjo el último acceso al archivo. Para obtener más información sobre cómo trabajar con formatos de fecha y hora de WMI, vea [tareas de WMI: fechas y horas](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).

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

Fecha en que se modificó el archivo por última vez. Para obtener más información sobre cómo trabajar con formatos de fecha y hora de WMI, vea [tareas de WMI: fechas y horas](/windows/desktop/WmiSdk/wmi-tasks--dates-and-times).

Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

La propiedad Name es una cadena que representa el nombre heredado que actúa como clave de una instancia de archivo lógico dentro de un sistema de archivos. Se deben proporcionar los nombres de ruta de acceso completa. Ejemplo: C: \\ Windows \\ System \\win.ini

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

Ruta de acceso del archivo. La ruta de acceso incluye las barras diagonales inversas iniciales y finales, pero no la letra de unidad o el nombre de la carpeta.

En la carpeta c: \\ Windows \\ system32 \\ WBEM, la ruta de acceso es \\ Windows \\ system32 \\ . Para la carpeta c: \\ scripts, la ruta de acceso es \\ .

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

Indica si se pueden leer los elementos de la carpeta. Si **es true**, se puede leer el archivo.

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

Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("archivo del sistema")
</dt> </dl>

Indica si el objeto es un archivo del sistema. Si es **true**, el archivo es un archivo del sistema

Esta propiedad se hereda de [**\_ LogicalFile CIM**](cim-logicalfile.md).

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

La clase de **\_ directorio Win32** se deriva [**del \_ directorio CIM**](cim-directory.md).

**Información general**

Las carpetas son objetos del sistema de archivos diseñados para contener otros objetos del sistema de archivos. Sin embargo, esto no significa que todas las carpetas sean iguales. En su lugar, las carpetas pueden variar considerablemente. Algunas carpetas son carpetas del sistema operativo, que por lo general no deben modificarse mediante un script. Algunas carpetas son de solo lectura, lo que significa que los usuarios pueden tener acceso al contenido de la carpeta pero no pueden agregar, eliminar o modificar el contenido. Algunas carpetas están comprimidas para un almacenamiento óptimo, mientras que otras están ocultas y no son visibles para los usuarios.

WMI utiliza la clase de **\_ directorio Win32** para administrar carpetas. De forma significativa, las propiedades y los métodos disponibles en esta clase son idénticos a las propiedades y los métodos disponibles en la clase de [**\_ archivo de archivos CIM**](cim-datafile.md) , la clase que se usa para administrar archivos. Esto significa que, una vez que haya aprendido a administrar carpetas mediante WMI, sin ningún trabajo adicional, también sabrá cómo administrar archivos.

La clase de Asociación de [**\_ subdirectorios de Win32**](win32-subdirectory.md) también se utiliza para administrar archivos y carpetas. La clase de **\_ subdirectorio Win32** relaciona una carpeta y sus subcarpetas inmediatas. Por ejemplo, en la estructura de carpetas C: \\ scripts \\ registros, logs es una subcarpeta de scripts y scripts es una subcarpeta de la carpeta raíz C: \\ . Sin embargo, los registros no se consideran una subcarpeta de C: \\ .

Puede recuperar las propiedades de cualquier carpeta en el sistema de archivos mediante la clase de **\_ directorio Win32** . Las propiedades disponibles mediante esta clase se muestran en la tabla 11,1. Para recuperar las propiedades de una sola carpeta, construya una consulta WQL (lenguaje de consulta de Windows) para la clase de **\_ directorio Win32** , asegurándose de incluir el nombre de la carpeta. Por ejemplo, esta consulta se enlaza a la carpeta D: \\ Archive:

`        Copy     "SELECT * FROM Win32_Directory WHERE Name = 'D:\\Archive'"`

Al especificar un nombre de archivo o carpeta en una consulta WQL, asegúrese de usar dos barras diagonales inversas ( \\ \\ ) para separar los componentes de la ruta de acceso.

Si desea limitar la recuperación de datos a una sola unidad de disco, incluya una cláusula WHERE que especifique la letra de unidad. Por ejemplo, esta consulta devuelve una lista de todas las carpetas de la unidad C:

`"SELECT * FROM Win32_Directory WHERE Drive = 'C:'"`

Si tiene que enumerar todas las carpetas de un equipo, tenga en cuenta que esta consulta puede tardar mucho tiempo en completarse.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de VBScript se recuperan las propiedades de la carpeta C: \\ scripts.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFolders = objWMIService.ExecQuery("SELECT * FROM Win32_Directory WHERE Name = 'c:\\Scripts'")
For Each objFolder in colFolders
 Wscript.Echo "Archive: " & objFolder.Archive
 Wscript.Echo "Caption: " & objFolder.Caption
 Wscript.Echo "Compressed: " & objFolder.Compressed
 Wscript.Echo "Compression method: " & objFolder.CompressionMethod
 Wscript.Echo "Creation date: " & objFolder.CreationDate
 Wscript.Echo "Encrypted: " & objFolder.Encrypted
 Wscript.Echo "Encryption method: " & objFolder.EncryptionMethod
 Wscript.Echo "Hidden: " & objFolder.Hidden
 Wscript.Echo "In use count: " & objFolder.InUseCount
 Wscript.Echo "Last accessed: " & objFolder.LastAccessed
 Wscript.Echo "Last modified: " & objFolder.LastModified
 Wscript.Echo "Name: " & objFolder.Name
 Wscript.Echo "Path: " & objFolder.Path
 Wscript.Echo "Readable: " & objFolder.Readable
 Wscript.Echo "System: " & objFolder.System
 Wscript.Echo "Writeable: " & objFolder.Writeable
Next
```



El siguiente ejemplo de VBScript devuelve una lista de todas las carpetas ocultas de un equipo.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFiles = objWMIService.ExecQuery("SELECT * FROM Win32_Directory WHERE Hidden = True")
For Each objFile in colFiles
 Wscript.Echo objFile.Name
Next
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

[**\_Directorio CIM**](cim-directory.md)
</dt> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

