---
description: La \_ clase de recurso compartido de Win32 representa un recurso compartido en un equipo que ejecuta Windows. Puede tratarse de una unidad de disco, impresora, comunicación entre procesos u otro dispositivo compartible. Para obtener más información sobre cómo recuperar clases WMI, vea recuperar una clase.
ms.assetid: 2d47b726-a0fe-47f3-9e96-d1d507655e56
ms.tgt_platform: multiple
title: Win32_Share (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share
- Win32_Share.Caption
- Win32_Share.Description
- Win32_Share.InstallDate
- Win32_Share.Status
- Win32_Share.AccessMask
- Win32_Share.AllowMaximum
- Win32_Share.MaximumAllowed
- Win32_Share.Name
- Win32_Share.Path
- Win32_Share.Type
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e871880da5aa9819de4a9eaaf3c6f074bd198d23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153347"
---
# <a name="win32_share-class"></a>\_Clase de recurso compartido Win32

La clase de **\_ recurso compartido de Win32** representa un recurso compartido en un equipo que ejecuta Windows. Puede tratarse de una unidad de disco, impresora, comunicación entre procesos u otro dispositivo compartible. Para obtener más información sobre cómo recuperar clases WMI, vea [recuperar una clase](../wmisdk/retrieving-a-class.md).

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D6-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), AMENDMENT]
class Win32_Share : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   AccessMask;
  boolean  AllowMaximum;
  uint32   MaximumAllowed;
  string   Name;
  string   Path;
  uint32   Type;
};
```

## <a name="members"></a>Miembros

La clase de **\_ recurso compartido de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase de **\_ recurso compartido de Win32** tiene estos métodos.



| Método                                                             | Descripción                                                                                                                                                                                                         |
|:-------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**A**](create-method-in-class-win32-share.md)               | Método de clase que inicia el uso compartido para un recurso de servidor.<br/>                                                                                                                                               |
| [**Elimínelos**](delete-method-in-class-win32-share.md)               | Método de clase que elimina un nombre de recurso compartido de la lista de recursos compartidos de un servidor y desconecta las conexiones al recurso compartido.<br/>                                                                       |
| [**GetAccessMask**](getaccessmask-method-in-class-win32-share.md) | Devuelve los derechos de acceso al recurso compartido mantenido por el usuario o grupo en cuyo nombre se devuelve la instancia. Debe utilizar este método en lugar de la propiedad **AccessMask** , que es siempre **null**.<br/> |
| [**SetShareInfo**](setshareinfo-method-in-class-win32-share.md)   | Método de clase que establece los parámetros de un recurso compartido.<br/>                                                                                                                                              |



 

### <a name="properties"></a>Propiedades

La clase de **\_ recurso compartido de Win32** tiene estas propiedades.

<dl> <dt>

**AccessMask**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **desusados**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Esta propiedad está obsoleta y ya no se utiliza. En su lugar, use el método [**\_ share. GetAccessMask de Win32**](getaccessmask-method-in-class-win32-share.md) . WMI establece el valor de la propiedad **AccessMask** en **null** . Para obtener más información sobre cómo configurar el acceso cuando se crea un recurso compartido, vea el método [**Create**](create-method-in-class-win32-share.md) .

</dd> <dt>

**AllowMaximum**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**reshare \_ info \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ Max \_ use")
</dt> </dl>

Se ha limitado el número de usuarios simultáneos para este recurso. Si es **true**, se omite el valor de la propiedad **MaximumAllowed** .

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

**MaximumAllowed**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**reshare \_ info \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ Max \_ use")
</dt> </dl>

Límite en el número máximo de usuarios a los que se les permite usar este recurso al mismo tiempo. El valor solo es válido si la propiedad **AllowMaximum** está establecida en **false**.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**share \_ info \_ 1**](/windows/win32/api/lmshare/ns-lmshare-share_info_1)shi1 nombre de red \| \_ ")
</dt> </dl>

Alias dado a una ruta de acceso configurada como un recurso compartido en un equipo con Windows.

Windows 2008 ejemplo: " \\ SERVER01 \\ Public": windows Server 2008 requiere que se coloque la UNC en el nombre.

</dd> <dt>

**Ruta de acceso**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**reshare \_ info \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ path")
</dt> </dl>

Ruta de acceso local del recurso compartido de Windows.

Ejemplo: "C: \\ archivos de programa"

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

**Tipo**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**reshare \_ info \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ type")
</dt> </dl>

Tipo de recurso que se va a compartir. Entre los tipos se incluyen las unidades de disco, las colas de impresión, las comunicaciones entre procesos (IPC) y los dispositivos generales.

<dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

**Unidad de disco** (0)


</dt> <dd></dd> <dt>

<span id="Print_Queue"></span><span id="print_queue"></span><span id="PRINT_QUEUE"></span>

**Cola de impresión** (1)


</dt> <dd></dd> <dt>

<span id="Device"></span><span id="device"></span><span id="DEVICE"></span>

**Dispositivo** (2)


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

**IPC** (3)


</dt> <dd></dd> <dt>

<span id="Disk_Drive_Admin"></span><span id="disk_drive_admin"></span><span id="DISK_DRIVE_ADMIN"></span>

**Administrador de unidad de disco** (2147483648)


</dt> <dd></dd> <dt>

<span id="Print_Queue_Admin"></span><span id="print_queue_admin"></span><span id="PRINT_QUEUE_ADMIN"></span>

**Administrador** de la cola de impresión (2147483649)


</dt> <dd></dd> <dt>

<span id="Device_Admin"></span><span id="device_admin"></span><span id="DEVICE_ADMIN"></span>

**Administrador de dispositivos** (2147483650)


</dt> <dd></dd> <dt>

<span id="IPC_Admin"></span><span id="ipc_admin"></span><span id="IPC_ADMIN"></span>

**Administración de IPC** (2147483651)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase de **\_ recurso compartido de Win32** se deriva de [**CIM \_ LogicalElement**](cim-logicalelement.md).

El método Create de esta clase es un método estático. Los métodos **Delete**, **GetAccessMask** y **SetShareInfo** son métodos de instancia.

En función de los permisos de seguridad, es posible que no pueda recuperar todas las propiedades de esta clase. Por ejemplo, las propiedades **AllowMaximum**, **MaximumAllowed**, **path** y **Type** pueden devolver null. En general, los usuarios avanzados y los administradores podrán recuperar todos los valores de propiedad.

## <a name="examples"></a>Ejemplos

En el siguiente[ejemplo de código](https://Gallery.TechNet.Microsoft.Com/scriptcenter/List-Share-Permissions-83f8c419) del centro de script se enumeran todos los recursos compartidos de un equipo y se enumeran todos los permisos de recurso compartido para cada recurso compartido.

La [información del recurso compartido Get similar a Win32 \_ share](https://Gallery.TechNet.Microsoft.Com/Get-Share-Information-5cc71b2c) PowerShell Sample queries Win32 \_ share y proporciona los resultados.

En el siguiente ejemplo de PowerShell se muestran los recursos compartidos en el sistema local.


```PowerShell
$shares = Get-WMIObject -class Win32_share
"Shares on : {0}" -f $((gwmi win32_computersystem).name)
$shares | sort name | ft -auto
```



Como alternativa, si desea filtrar más de manera precisa, puede usar el siguiente fragmento de código de PowerShell:


```PowerShell
gwmi -q "SELECT * FROM Win32_Share WHERE Name != 'ADMIN$' AND Name != 'IPC$'"
```



En el siguiente ejemplo de VBScript se muestran los recursos compartidos del sistema local.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_Share")


For Each objItem in colItems 
 Wscript.Echo "Name: " & objItem.Name
 Wscript.Echo "Caption: " & objItem.Caption & "=" & objItem.Path
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
</dt> <dt>

[Tareas de WMI: archivos y carpetas](../wmisdk/wmi-tasks--files-and-folders.md)
</dt> </dl>

 

 
