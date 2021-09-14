---
description: La clase LogicalFile de CIM representa una colección con nombre de datos, que puede ser código ejecutable, que se encuentra en un sistema de archivos \_ en una extensión de almacenamiento.
ms.assetid: 96bf95a1-c8d7-4035-8d5a-38cdb9c75cce
ms.tgt_platform: multiple
title: CIM_LogicalFile clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile
- CIM_LogicalFile.Caption
- CIM_LogicalFile.Description
- CIM_LogicalFile.InstallDate
- CIM_LogicalFile.Status
- CIM_LogicalFile.AccessMask
- CIM_LogicalFile.Archive
- CIM_LogicalFile.Compressed
- CIM_LogicalFile.CompressionMethod
- CIM_LogicalFile.CreationClassName
- CIM_LogicalFile.CreationDate
- CIM_LogicalFile.CSCreationClassName
- CIM_LogicalFile.CSName
- CIM_LogicalFile.Drive
- CIM_LogicalFile.EightDotThreeFileName
- CIM_LogicalFile.Encrypted
- CIM_LogicalFile.EncryptionMethod
- CIM_LogicalFile.Name
- CIM_LogicalFile.Extension
- CIM_LogicalFile.FileName
- CIM_LogicalFile.FileSize
- CIM_LogicalFile.FileType
- CIM_LogicalFile.FSCreationClassName
- CIM_LogicalFile.FSName
- CIM_LogicalFile.Hidden
- CIM_LogicalFile.InUseCount
- CIM_LogicalFile.LastAccessed
- CIM_LogicalFile.LastModified
- CIM_LogicalFile.Path
- CIM_LogicalFile.Readable
- CIM_LogicalFile.System
- CIM_LogicalFile.Writeable
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a06d2abd1c4ad92d751afa6c8aa47c0cfaa8b1f9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127254751"
---
# <a name="cim_logicalfile-class"></a>Cim \_ LogicalFile (clase)

La **clase \_ LogicalFile** de CIM representa una colección con nombre de datos, que puede ser código ejecutable, que se encuentra en un sistema de archivos en una extensión de almacenamiento.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[SupportsDelete, DeleteBy("DeleteInstance"), Abstract, Provider("CIMWin32"), UUID("{8502C559-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Files (CIM)"), AMENDMENT]
class CIM_LogicalFile : CIM_LogicalElement
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
};
```

## <a name="members"></a>Members

La **clase \_ LogicalFile** de CIM tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ LogicalFile** de CIM tiene estos métodos.



| Método                                                                                             | Descripción                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-logicalfile.md)     | Cambia los permisos de seguridad para el archivo lógico especificado en la ruta de acceso del objeto. Wmi no implementa .<br/>                                   |
| [**ChangeSecurityPermissionsEx**](changesecuritypermissionsex-method-in-class-cim-logicalfile.md) | Cambia los permisos de seguridad para el archivo lógico especificado en la ruta de acceso del objeto. Wmi no implementa .<br/>                                   |
| [**Comprimir**](compress-method-in-class-cim-logicalfile.md)                                       | Comprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto. Wmi no implementa .<br/>                                              |
| [**CompressEx**](compressex-method-in-class-cim-logicalfile.md)                                   | Comprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto. Wmi no implementa .<br/>                                              |
| [**Copiar**](copy-method-in-class-cim-logicalfile.md)                                               | Copia el archivo lógico (o directorio) especificado en la ruta de acceso del objeto a la ubicación especificada por el parámetro de entrada. Wmi no implementa .<br/> |
| [**CopyEx**](copyex-method-in-class-cim-logicalfile.md)                                           | Copia el archivo lógico (o directorio) especificado en la ruta de acceso del objeto a la ubicación especificada por el parámetro de entrada. Wmi no implementa .<br/> |
| [**Eliminar**](delete-method-in-class-cim-logicalfile.md)                                           | Elimina el archivo lógico (o directorio) especificado en la ruta de acceso del objeto. Wmi no implementa .<br/>                                                 |
| [**DeleteEx**](deleteex-method-in-class-cim-logicalfile.md)                                       | Elimina el archivo lógico (o directorio) especificado en la ruta de acceso del objeto. Wmi no implementa .<br/>                                                 |
| [**GetEffectivePermission**](geteffectivepermission-method-in-class-cim-logicalfile.md)           | Determina si el autor de la llamada tiene los permisos agregados especificados por el **argumento Permission.** Wmi no implementa .<br/>                |
| [**Cambiar nombre**](rename-method-in-class-cim-logicalfile.md)                                           | Cambia el nombre del archivo lógico (o directorio) especificado en la ruta de acceso del objeto. Wmi no implementa .<br/>                                                 |
| [**TakeOwnerShip**](takeownership-method-in-class-cim-logicalfile.md)                             | Obtiene la propiedad del archivo lógico (o directorio) especificado en la ruta de acceso del objeto. Wmi no implementa .<br/>                                    |
| [**TakeOwnerShipEx**](takeownershipex-method-in-class-cim-logicalfile.md)                         | Obtiene la propiedad del archivo lógico (o directorio) especificado en la ruta de acceso del objeto. Wmi no implementa .<br/>                                    |
| [**Descomprimir**](uncompress-method-in-class-cim-logicalfile.md)                                   | Descomprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto. Wmi no implementa .<br/>                                            |
| [**UncompressEx**](uncompressex-method-in-class-cim-logicalfile.md)                               | Descomprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto. Wmi no implementa .<br/>                                            |



 

### <a name="properties"></a>Propiedades

La **clase \_ LogicalFile** de CIM tiene estas propiedades.

<dl> <dt>

**Máscara de acceso**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Access Rights")
</dt> </dl>

Máscara de bits que representa los derechos de acceso necesarios para acceder al archivo o realizar operaciones específicas en el archivo. Para obtener valores de bits, vea Constantes de derechos de [**acceso a archivos y directorios.**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)

> [!Note]  
> En los volúmenes FAT, se devuelve el valor **\_ FULL ACCESS** en su lugar, lo que indica que no se ha establecido ninguna seguridad en el objeto.

 

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

Si **es True,** el archivo debe archivarse.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Breve descripción textual del objeto.

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

</dd> <dt>

**CompressionMethod**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Método de compresión")
</dt> </dl>

Cadena de forma libre que indica el algoritmo o la herramienta que se usa para comprimir el archivo lógico. Si el esquema de compresión es desconocido o no se describe, use "Unknown". Si el archivo lógico está comprimido, pero el esquema de compresión es desconocido o no se describe, use "Compressed". Si el archivo lógico no está comprimido, use "No comprimido".

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Nombre de clase")
</dt> </dl>

Nombre de la clase.

</dd> <dt>

**CreationDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Fecha de creación")
</dt> </dl>

Fecha y hora de creación del archivo.

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

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ FileSystem**](cim-filesystem.md).**CSName**"), [**Clave CIM \_**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Nombre del sistema del equipo")
</dt> </dl>

Nombre del sistema del equipo.

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")
</dt> </dl>

Descripción textual del objeto.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Unidad**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Drive")
</dt> </dl>

Letra de unidad (incluidos los dos puntos que siguen a la letra de unidad) del archivo. Esta propiedad se hereda de **CIM \_ LogicalFile**. Ejemplo: "c:"

</dd> <dt>

**EightDotThreeFileName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Eight Dot Three File Name")
</dt> </dl>

Nombre de archivo compatible con DOS. Ejemplo: "c: \\ progra~1"

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

</dd> <dt>

**EncryptionMethod**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Método de cifrado")
</dt> </dl>

Cadena de forma libre que identifica el algoritmo o la herramienta que se usa para cifrar un archivo lógico. Si el esquema de cifrado no está en proceso (por motivos de seguridad, por ejemplo), use "Unknown". Si el archivo está cifrado, pero su esquema de cifrado es desconocido o no se ha divulgado, use "Encrypted". Si el archivo lógico no está cifrado, use "No cifrado".

</dd> <dt>

**Extensión**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Extension")
</dt> </dl>

Extensión de nombre de archivo sin el punto anterior (punto). Ejemplo: "txt", "mof", "mdb"

</dd> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Nombre de archivo")
</dt> </dl>

Nombre de archivo sin la extensión de nombre de archivo. Ejemplo: "MyDataFile"

</dd> <dt>

**FileSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tamaño"), [**Unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")
</dt> </dl>

Tamaño del archivo, en bytes.

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

Descriptor que representa el tipo de archivo indicado por la **propiedad Extension.**

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

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Fecha de instalación")
</dt> </dl>

Indica cuándo se instaló el objeto. La falta de un valor no indica que el objeto no está instalado.

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

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**LastAccessed**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Último acceso")
</dt> </dl>

Fecha y hora en que se ha accedido por última vez al archivo.

</dd> <dt>

**LastModified**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Última modificación")
</dt> </dl>

Fecha y hora en que se modificó por última vez el archivo.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

La propiedad Name es una cadena que representa el nombre heredado que actúa como clave de una instancia de archivo lógica dentro de un sistema de archivos. Se deben proporcionar nombres de ruta de acceso completos. Ejemplo: C: \\ Windows \\ sistema \\win.ini

</dd> <dt>

**Path**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Path")
</dt> </dl>

Ruta de acceso del archivo, incluidas las barras diagonales inversas iniciales y finales. Ejemplo: " \\ windows \\ system \\ "

</dd> <dt>

**Legible**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Readable")
</dt> </dl>

Si **es True**, se puede leer el archivo.

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Cadena que indica el estado actual del objeto. Se puede definir el estado operativo y no operativo. El estado operativo puede incluir "Ok", "Degraded" y "Pred Fail". "Error previo" indica que un elemento funciona correctamente, pero predice un error (por ejemplo, una unidad de disco duro habilitada para SMART).

El estado no operativo puede incluir "Error", "Starting", "Stopping" y "Service". "Servicio" se puede aplicar durante la resilvering de reflejo del disco, volver a cargar una lista de permisos de usuario u otro trabajo administrativo. No todo este trabajo está en línea, pero el elemento administrado no es "Correcto" ni está en uno de los demás estados.

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

**Unknown** ("Unknown")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Error de pred** ("error previo")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Starting** ("Starting")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Detención** ("Detención")


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

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ LogicalFile** de CIM se deriva de [**CIM \_ LogicalElement**](cim-logicalelement.md).

WMI no implementa esta clase. Para las clases derivadas de **\_ CIM LogicalFile**, vea [Clases Win32](win32-provider.md).

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento \_ lógico CIM**](cim-logicalelement.md)
</dt> </dl>

 

