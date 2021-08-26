---
description: La clase CIM RemoteFileSystem representa un sistema de archivos remoto al que se accede mediante \_ un servicio relacionado con la red. En este caso, el almacén de archivos se hospeda en un equipo, que actúa como servidor de archivos.
ms.assetid: 932970a8-0ab3-45d8-912d-c4ba7cf433b5
ms.tgt_platform: multiple
title: CIM_RemoteFileSystem clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RemoteFileSystem
- CIM_RemoteFileSystem.AvailableSpace
- CIM_RemoteFileSystem.BlockSize
- CIM_RemoteFileSystem.Caption
- CIM_RemoteFileSystem.CasePreserved
- CIM_RemoteFileSystem.CaseSensitive
- CIM_RemoteFileSystem.CodeSet
- CIM_RemoteFileSystem.CompressionMethod
- CIM_RemoteFileSystem.CreationClassName
- CIM_RemoteFileSystem.CSCreationClassName
- CIM_RemoteFileSystem.CSName
- CIM_RemoteFileSystem.Description
- CIM_RemoteFileSystem.EncryptionMethod
- CIM_RemoteFileSystem.FileSystemSize
- CIM_RemoteFileSystem.InstallDate
- CIM_RemoteFileSystem.MaxFileNameLength
- CIM_RemoteFileSystem.Name
- CIM_RemoteFileSystem.ReadOnly
- CIM_RemoteFileSystem.Root
- CIM_RemoteFileSystem.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5d21d46de5f3a9a8d85ff94e5996dc3d19481a03f003d7030384ca2f82f0e019
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920515"
---
# <a name="cim_remotefilesystem-class"></a>Clase \_ RemoteFileSystem de CIM

La **clase CIM \_ RemoteFileSystem** representa un sistema de archivos remoto al que se accede mediante un servicio relacionado con la red. En este caso, el almacén de archivos se hospeda en un equipo, que actúa como servidor de archivos. Por ejemplo, el almacén de archivos de un sistema de archivos NFS normalmente no se encuentra en los medios controlados localmente de un sistema de equipos, ni se accede directamente a él a través de un controlador de dispositivo. Las subclases **de CIM \_ RemoteFileSystem** contienen información de configuración del lado cliente relacionada con el acceso del sistema de archivos.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se construyen las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintaxis siguiente se simplifica a partir Managed Object Format (MOF) e incluye todas sus propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{75BCF4F9-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_RemoteFileSystem : CIM_FileSystem
{
  uint64   AvailableSpace;
  uint64   BlockSize;
  string   Caption;
  boolean  CasePreserved;
  boolean  CaseSensitive;
  uint16   CodeSet[];
  string   CompressionMethod;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  string   EncryptionMethod;
  uint64   FileSystemSize;
  datetime InstallDate;
  uint32   MaxFileNameLength;
  string   Name;
  boolean  ReadOnly;
  string   Root;
  string   Status;
};
```

## <a name="members"></a>Miembros

La **clase \_ CIM RemoteFileSystem** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ CIM RemoteFileSystem** tiene estas propiedades.

<dl> <dt>

**AvailableSpace**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Partition \| 002.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")
</dt> </dl>

Cantidad de espacio libre para el sistema de archivos, en bytes. Si es desconocido, escriba 0.

Esta propiedad se hereda de [**CIM \_ FileSystem**](cim-filesystem.md).

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> <dt>

**Blocksize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")
</dt> </dl>

Tamaño, en bytes, de los bloques que forman la extensión de almacenamiento. Si es desconocido o si un concepto de bloque no es válido (por ejemplo, para extensiones agregadas, memoria o discos lógicos), escriba 1 (uno).

Esta propiedad se hereda de [**CIM \_ FileSystem**](cim-filesystem.md).

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Descripción textual del objeto.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**CasePreserved**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es TRUE,** se conservan las mayúsculas y minúsculas de los nombres de archivo.

Esta propiedad se hereda de [**CIM \_ FileSystem**](cim-filesystem.md).

</dd> <dt>

**CaseSensitive**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es TRUE,** se admiten nombres de archivo que distinguen mayúsculas de minúsculas.

Esta propiedad se hereda de [**CIM \_ FileSystem**](cim-filesystem.md).

</dd> <dt>

**CodeSet**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Juegos de caracteres o codificación admitidos por el sistema de archivos. Esta propiedad se hereda de [**CIM \_ FileSystem**](cim-filesystem.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otros** (1)


</dt> <dd></dd> <dt>

<span id="ASCII"></span><span id="ascii"></span>

**ASCII** (2)


</dt> <dd></dd> <dt>

<span id="Unicode"></span><span id="unicode"></span><span id="UNICODE"></span>

**Unicode** (3)


</dt> <dd></dd> <dt>

<span id="ISO2022"></span><span id="iso2022"></span>

**ISO2022** (4)


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

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Partición DMTF \| \| 002.7")
</dt> </dl>

Cadena de forma libre que indica el algoritmo o la herramienta que se usa para comprimir el archivo lógico. Si el esquema de compresión es desconocido o no se describe, use "Unknown". Si el archivo lógico está comprimido, pero el esquema de compresión es desconocido o no se describe, use "Compressed". Si el archivo lógico no está comprimido, use "No comprimido".

Esta propiedad se hereda de [**CIM \_ FileSystem**](cim-filesystem.md).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nombre de la clase o subclase usada en la creación de una instancia de . Cuando se usa con otras propiedades clave de la clase , esta propiedad permite identificar de forma única todas las instancias de la clase y sus subclases.

Esta propiedad se hereda de [**CIM \_ FileSystem**](cim-filesystem.md).

</dd> <dt>

**CSCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**")
</dt> </dl>

Ámbito del nombre de clase de creación del sistema de equipo.

Esta propiedad se hereda de [**CIM \_ FileSystem**](cim-filesystem.md).

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Name**")
</dt> </dl>

Ámbito del nombre del sistema del equipo.

Esta propiedad se hereda de [**CIM \_ FileSystem**](cim-filesystem.md).

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

**EncryptionMethod**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Partición DMTF \| \| 002.8")
</dt> </dl>

Cadena de forma libre que identifica el algoritmo o la herramienta que se usa para cifrar un archivo lógico. Si el esquema de cifrado no está en la lista (por motivos de seguridad, por ejemplo), use "Unknown". Si el archivo está cifrado, pero su esquema de cifrado es desconocido o no se ha divulgado, use "Encrypted". Si el archivo lógico no está cifrado, use "No cifrado". Esta propiedad se hereda del sistema [**\_ de archivos CIM.**](cim-filesystem.md)

</dd> <dt>

**FileSystemSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")
</dt> </dl>

Tamaño total del sistema de archivos, en bytes. Si es desconocido, escriba 0.

Esta propiedad se hereda del sistema [**\_ de archivos CIM.**](cim-filesystem.md)

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Fecha de instalación")
</dt> </dl>

Fecha y hora en que se instaló el objeto. Esta propiedad no necesita un valor para indicar que el objeto está instalado.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**MaxFileNameLength**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Longitud máxima de un nombre de archivo dentro del sistema de archivos. Un valor de 0 indica que la longitud del nombre de archivo es ilimitada.

Esta propiedad se hereda del sistema [**\_ de archivos CIM.**](cim-filesystem.md)

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")
</dt> </dl>

Etiqueta por la que se conoce el objeto. Cuando se subclasifica, esta propiedad se puede invalidar para que sea una propiedad de clave.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**ReadOnly**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|HOST-RESOURCES-MIB.hrFSAccess de IETF")
</dt> </dl>

Si **es TRUE,** el sistema de archivos se designa como de solo lectura.

Esta propiedad se hereda del sistema [**\_ de archivos CIM.**](cim-filesystem.md)

</dd> <dt>

**Raíz**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| HOST-RESOURCES-MIB.hrFSMountPoint")
</dt> </dl>

Nombre de ruta de acceso u otra información que define la raíz del sistema de archivos.

Esta propiedad se hereda del sistema [**\_ de archivos CIM.**](cim-filesystem.md)

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Estado actual del objeto.

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

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ CIM RemoteFileSystem** se deriva de [**CIM \_ FileSystem**](cim-filesystem.md).

WMI no implementa esta clase.

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

[**\_Sistema de archivos CIM**](cim-filesystem.md)
</dt> </dl>

 

