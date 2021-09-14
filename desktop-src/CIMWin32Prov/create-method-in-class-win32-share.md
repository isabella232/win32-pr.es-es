---
description: Inicia el uso compartido de un recurso de servidor.
ms.assetid: 36530e1b-9109-4a6c-bba9-d9358101f5e2
ms.tgt_platform: multiple
title: Método Create de la Win32_Share clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d7a74838d9f6c532d3433240a5b8a70846b63776
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062274"
---
# <a name="create-method-of-the-win32_share-class"></a>Método Create de la clase Win32 \_ Share

El **método create** WMI [class](/windows/desktop/WmiSdk/retrieving-a-class) inicia el uso compartido de un recurso de servidor.   

En este tema se usa Managed Object Format sintaxis MOF . Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 Create(
  [in]           string                   Path,
  [in]           string                   Name,
  [in]           uint32                   Type,
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] string                   Password,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Ruta de acceso* \[ En\]
</dt> <dd>

Ruta de acceso local del recurso Windows compartido.

Ejemplo, "C: \\ Archivos de programa".

</dd> <dt>

*Nombre* \[ En\]
</dt> <dd>

Pasa el alias a una ruta de acceso configurada como un recurso compartido en un sistema informático que ejecuta Windows.

Ejemplo, "public".

</dd> <dt>

*Tipo* \[ En\]
</dt> <dd>

Pasa el tipo de recurso que se comparte. Los tipos incluyen unidades de disco, colas de impresión, comunicaciones entre procesos (IPC) y dispositivos generales. Puede ser uno de los siguientes valores.

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

**Administrador de unidad de** disco (2147483648)


</dt> <dd></dd> <dt>

<span id="Print_Queue_Admin"></span><span id="print_queue_admin"></span><span id="PRINT_QUEUE_ADMIN"></span>

**Administrador de cola de** impresión (2147483649)


</dt> <dd></dd> <dt>

<span id="Device_Admin"></span><span id="device_admin"></span><span id="DEVICE_ADMIN"></span>

**Administrador de dispositivos** (2147483650)


</dt> <dd></dd> <dt>

<span id="IPC_Admin"></span><span id="ipc_admin"></span><span id="IPC_ADMIN"></span>

**Administrador de IPC** (2147483651)


</dt> <dd></dd> </dl> </dd> <dt>

*MaximumAllowed* \[ en, opcional\]
</dt> <dd>

Limite el número máximo de usuarios que pueden usar simultáneamente este recurso.

Ejemplo: 10. Este parámetro es opcional.

</dd> <dt>

*Descripción* \[ en, opcional\]
</dt> <dd>

Comentario opcional para describir el recurso que se comparte. Este parámetro es opcional.

</dd> <dt>

*Contraseña* \[ en, opcional\]
</dt> <dd>

Contraseña (cuando el servidor se ejecuta con seguridad de nivel de recurso compartido) para el recurso compartido. Si el servidor se ejecuta con seguridad de nivel de usuario, se omite este parámetro. Este parámetro es opcional.

</dd> <dt>

*Acceso* \[ en, opcional\]
</dt> <dd>

Descriptor de seguridad para permisos de nivel de usuario. Un descriptor de seguridad contiene información sobre los permisos, el propietario y las funcionalidades de acceso del recurso. Si no se proporciona este parámetro o es **NULL,** todos los usuarios tienen acceso de lectura al recurso compartido. Para obtener más información, vea [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) y [Changing Access Security on Securable Objects](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error. Para obtener códigos de error adicionales, [**vea Constantes de error WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores **HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Correcto** (0)
</dt> <dt>

**Acceso denegado** (2)
</dt> <dt>

**Error desconocido** (8)
</dt> <dt>

**Nombre no válido** (9)
</dt> <dt>

**Nivel no válido** (10)
</dt> <dt>

**Parámetro no válido** (21)
</dt> <dt>

**Recurso compartido duplicado** (22)
</dt> <dt>

**Ruta de acceso redirigida** (23)
</dt> <dt>

**Dispositivo o directorio desconocido** (24)
</dt> <dt>

**Nombre de red no encontrado** (25)
</dt> <dt>

**Otros** (26 4294967295)
</dt> </dl>

## <a name="remarks"></a>Observaciones

**Create** es un método estático.

Solo los miembros del grupo local Administradores u Operadores de cuenta o aquellos con pertenencia a grupos de operadores de comunicación, impresión o servidor pueden ejecutar **correctamente Crear**. El operador Print solo puede agregar colas de impresora. El operador Communication solo puede agregar colas de dispositivos de comunicación.

## <a name="examples"></a>Ejemplos

El [ejemplo de PowerShell Export and Import Fileshares exporta](https://Gallery.TechNet.Microsoft.Com/Export-and-Import-84d4fce1) e importa recursos compartidos de archivos y establece permisos de recurso compartido. De forma similar, [el ejemplo Crear un recurso compartido](https://gallery.technet.microsoft.com/scriptcenter/Create-a-Share-and-Set-eb177a79) y Establecer permisos también crea un nuevo recurso compartido y establece los permisos de recurso compartido.

El siguiente código de PowerShell crea un recurso compartido.


```PowerShell
# create pointer to class
$comp=[WMICLASS]"Win32_share"

# create a new share
$comp.create("c:\","mynewshare",0)

# see results
gwmi win32_share 
```



El ejemplo de código anterior devuelve lo siguiente:

``` syntax
__GENUS          : 2
__CLASS          : __PARAMETERS
__SUPERCLASS     : 
__DYNASTY        : __PARAMETERS
__RELPATH        : 
__PROPERTY_COUNT : 1
__DERIVATION     : {}
__SERVER         : 
__NAMESPACE      : 
__PATH           : 
ReturnValue      : 2
PSComputerName   : 

Name        : ADMIN$
Path        : C:\Windows
Description : Remote Admin

Name        : C$
Path        : C:\
Description : Default share

Name        : CCMLOGS$
Path        : C:\Windows\CCM\Logs
Description : Public Share

Name        : ccmsetup$
Path        : C:\Windows\ccmsetup
Description : Public Share

Name        : Drop
Path        : C:\Drop
Description : 

Name        : IPC$
Path        : 
Description : Remote IPC

Name        : Share
Path        : C:\Share
Description : 
```

En el siguiente ejemplo de código de C \# se describe cómo llamar al método create.


```CSharp
private static void makeShare(string servername, string filepath, string sharename)
{
try
 {
 // assemble the string so the scope represents the remote server
 string scope = string.Format("\\\\{0}\\root\\cimv2", servername);

 // connect to WMI on the remote server
 ManagementScope ms = new ManagementScope(scope);

 // create a new instance of the Win32_Share WMI object
 ManagementClass cls = new ManagementClass("Win32_Share");

 // set the scope of the new instance to that created above
 cls.Scope = ms;

 // assemble the arguments to be passed to the Create method
 object[] methodargs = { filepath, sharename, "0" };

 // invoke the Create method to create the share
 object result = cls.InvokeMethod("Create", methodargs);
 }
catch (SystemException e)
 {
  Console.WriteLine("Error attempting to create share {0}:", sharename);
  Console.WriteLine(e.Message);
 }

}
```



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

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Recurso compartido de \_ Win32**](win32-share.md)
</dt> </dl>

 

