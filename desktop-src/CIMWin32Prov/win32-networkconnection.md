---
description: Representa una conexión de red activa en un entorno basado en Windows.
ms.assetid: e16e5f13-ea28-4d75-9978-4ff2ef5e5506
ms.tgt_platform: multiple
title: Win32_NetworkConnection (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkConnection
- Win32_NetworkConnection.Caption
- Win32_NetworkConnection.Description
- Win32_NetworkConnection.InstallDate
- Win32_NetworkConnection.Status
- Win32_NetworkConnection.AccessMask
- Win32_NetworkConnection.Comment
- Win32_NetworkConnection.ConnectionState
- Win32_NetworkConnection.ConnectionType
- Win32_NetworkConnection.DisplayType
- Win32_NetworkConnection.LocalName
- Win32_NetworkConnection.Name
- Win32_NetworkConnection.Persistent
- Win32_NetworkConnection.ProviderName
- Win32_NetworkConnection.RemoteName
- Win32_NetworkConnection.RemotePath
- Win32_NetworkConnection.ResourceType
- Win32_NetworkConnection.UserName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 96d91008ff8ad2f947e6c9957d16c4f007d15e47
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807832"
---
# <a name="win32_networkconnection-class"></a>\_Clase Win32 NetworkConnection

La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ NetworkConnection de Win32** representa una conexión de red activa en un entorno basado en Windows.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CD-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkConnection : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   AccessMask;
  string   Comment;
  string   ConnectionState;
  string   ConnectionType;
  string   DisplayType;
  string   LocalName;
  string   Name;
  boolean  Persistent;
  string   ProviderName;
  string   RemoteName;
  string   RemotePath;
  string   ResourceType;
  string   UserName;
};
```

## <a name="members"></a>Miembros

La **clase \_ NetworkConnection de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ NetworkConnection de Win32** tiene estas propiedades.

<dl> <dt>

**AccessMask**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")
</dt> </dl>

Lista de derechos de acceso al archivo o directorio especificado que mantiene el usuario o grupo en cuyo nombre se devuelve la instancia. En los volúmenes FAT, se devuelve el valor de **\_ acceso completo** en su lugar, lo que indica que no se ha establecido ninguna seguridad en el objeto.

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

Concede acceso de escritura a la lista de control de acceso discrecional (DACL).

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

</dd> </dl>

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

**Comentario**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| estructuras de redes de Windows \| [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| *lpComment*")
</dt> </dl>

Comentario proporcionado por el proveedor de red.

</dd> <dt>

**ConnectionState**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (20), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**use \_ info \_ 1**](/windows/win32/api/lmuse/ns-lmuse-use_info_1) \| **ui1 \_ status**")
</dt> </dl>

Estado actual de la conexión de red.

<dt>

<span id="Connected"></span><span id="connected"></span><span id="CONNECTED"></span>

**Conectado** ("conectado")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Error** ("error")


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

En **pausa** ("en pausa")


</dt> <dd></dd> <dt>

<span id="Disconnected"></span><span id="disconnected"></span><span id="DISCONNECTED"></span>

**Desconectada** ("desconectada")


</dt> <dd></dd> <dt>

<span id="Connecting"></span><span id="connecting"></span><span id="CONNECTING"></span>

**Conectando** ("conectando")


</dt> <dd></dd> <dt>

<span id="Reconnecting"></span><span id="reconnecting"></span><span id="RECONNECTING"></span>

**Volver a conectar** ("reconectar")


</dt> <dd></dd> </dl>

</dd> <dt>

**ConnectionType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| estructuras de redes de Windows \| [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **dwScope**")
</dt> </dl>

Tipo de persistencia de la conexión utilizada para conectarse a la red.

<dt>

<span id="Current_Connection"></span><span id="current_connection"></span><span id="CURRENT_CONNECTION"></span>

**Conexión actual** ("conexión actual")


</dt> <dd></dd> <dt>

<span id="Persistent_Connection"></span><span id="persistent_connection"></span><span id="PERSISTENT_CONNECTION"></span>

**Conexión persistente** ("conexión persistente")


</dt> <dd></dd> </dl>

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

**TipoDePresentación**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| estructuras de redes de Windows \| [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **dwDisplayType**")
</dt> </dl>

El objeto de red debe mostrarse en una interfaz de usuario de exploración de red.

<dt>

<span id="Domain"></span><span id="domain"></span><span id="DOMAIN"></span>

**Dominio** ("dominio")


</dt> <dd></dd> <dt>

<span id="Generic"></span><span id="generic"></span><span id="GENERIC"></span>

**Generic** ("Generic")


</dt> <dd></dd> <dt>

<span id="Server"></span><span id="server"></span><span id="SERVER"></span>

**Servidor** ("servidor")


</dt> <dd></dd> <dt>

<span id="Share"></span><span id="share"></span><span id="SHARE"></span>

**Compartir** ("compartir")


</dt> <dd></dd> </dl>

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

**LocalName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| estructuras de redes de Windows \| [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **lpLocalName**")
</dt> </dl>

Nombre local del dispositivo de red conectado.

Ejemplo: "c: \\ Public"

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("nombre"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| estructuras de redes de Windows \| [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)")
</dt> </dl>

Nombre de la conexión de red actual. Es la combinación de los valores de **RemoteName** y **localname**.

Ejemplo: " \\ \\ NTRELEASE (c: \\ Public)"

</dd> <dt>

**Persistent**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| funciones de red de Windows \| [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea)")
</dt> </dl>

El sistema operativo volverá a conectar automáticamente la conexión en el siguiente inicio de sesión.

</dd> <dt>

**ProviderName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| estructuras de redes de Windows \| [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **lpProvider**")
</dt> </dl>

Nombre del proveedor que posee el recurso. Esta propiedad puede ser **null** si se desconoce el nombre del proveedor.

</dd> <dt>

**RemoteName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| estructuras de redes de Windows \| [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **lpRemoteName**")
</dt> </dl>

Nombre de recurso de red remota para un recurso de red. Para una conexión actual o persistente, **RemoteName** contiene el nombre de red asociado al nombre del valor en la propiedad **localname** . El nombre de **RemoteName** debe seguir las convenciones de nomenclatura del proveedor de red.

Ejemplo: " \\ \\ NTRELEASE"

</dd> <dt>

**RemotePath**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| estructuras de redes de Windows \| [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **lpRemoteName**")
</dt> </dl>

Ruta de acceso completa al recurso de red.

Ejemplo: " \\ \\ infosrv1 \\ Public"

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| estructuras de redes de Windows \| [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **dwType**")
</dt> </dl>

Tipo de recurso que se va a enumerar o al que se va a conectar.

<dt>

<span id="Disk"></span><span id="disk"></span><span id="DISK"></span>

**Disco** ("disco")


</dt> <dd></dd> <dt>

<span id="Print"></span><span id="print"></span><span id="PRINT"></span>

**Imprimir** ("Imprimir")


</dt> <dd></dd> <dt>

<span id="Any"></span><span id="any"></span><span id="ANY"></span>

**Any** ("any")


</dt> <dd></dd> </dl>

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")
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

**UserName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| funciones de red de Windows \| [**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera)")
</dt> </dl>

Nombre de usuario o nombre de usuario predeterminado que se usa para establecer una conexión de red.

Ejemplo: "SYSTEM"

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ NetworkConnection de Win32** se deriva de [**\_ LogicalElement de CIM**](cim-logicalelement.md).

## <a name="examples"></a>Ejemplos

El siguiente ejemplo de código de VBScript recupera información sobre la conexión de red local.


```VB
On Error Resume Next
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\Root\CIMv2")
Set colItems = objWMIService.ExecQuery("Select * from Win32_NetworkConnection",,48)
For Each objItem in colItems
    Wscript.Echo "AccessMask: " & objItem.AccessMask
    Wscript.Echo "Caption: " & objItem.Caption
    Wscript.Echo "Comment: " & objItem.Comment
    Wscript.Echo "ConnectionState: " & objItem.ConnectionState
    Wscript.Echo "ConnectionType: " & objItem.ConnectionType
    Wscript.Echo "Description: " & objItem.Description
    Wscript.Echo "DisplayType: " & objItem.DisplayType
    Wscript.Echo "InstallDate: " & objItem.InstallDate
    Wscript.Echo "LocalName: " & objItem.LocalName
    Wscript.Echo "Name: " & objItem.Name
    Wscript.Echo "Persistent: " & objItem.Persistent
    Wscript.Echo "ProviderName: " & objItem.ProviderName
    Wscript.Echo "RemoteName: " & objItem.RemoteName
    Wscript.Echo "RemotePath: " & objItem.RemotePath
    Wscript.Echo "ResourceType: " & objItem.ResourceType
    Wscript.Echo "Status: " & objItem.Status
    Wscript.Echo "UserName: " & objItem.UserName
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

[**\_LOGICALELEMENT CIM**](cim-logicalelement.md)
</dt> <dt>

[Clases de sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
