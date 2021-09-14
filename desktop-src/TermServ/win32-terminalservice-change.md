---
title: Método change de la Win32_Service (Mbnapi.h) (TerminalService)
description: Modifica un TerminalService de \_ Win32.
ms.assetid: 19E43A80-47C9-4C5A-8E73-723F206AA7C0
ms.tgt_platform: multiple
keywords:
- Cambiar el método Servicios de Escritorio remoto
- Cambiar método Servicios de Escritorio remoto , Win32_Service clase
- Win32_Service clase Servicios de Escritorio remoto , Change (método)
topic_type:
- apiref
api_name:
- Win32_Service.Change
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa34ea0c9c38cd0b11f97a0bbf651f1aebf37a46
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126890820"
---
# <a name="change-method-of-the-win32_service-class-mbnapih---terminalservice"></a>Método de cambio de Win32_Service clase (Mbnapi.h): TerminalService

El **método de** la clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) Change modifica un [**\_ terminalService de Win32.**](win32-terminalservice.md)

En este tema se usa Managed Object Format sintaxis de MOF. Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 Change(
  [in] string  DisplayName,
  [in] string  PathName,
  [in] uint32  ServiceType,
  [in] uint32  ErrorControl,
  [in] string  StartMode,
  [in] boolean DesktopInteract,
  [in] string  StartName,
  [in] string  StartPassword,
  [in] string  LoadOrderGroup,
  [in] string  LoadOrderGroupDependencies,
  [in] string  ServiceDependencies
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DisplayName* \[ En\]
</dt> <dd>

Nombre para mostrar del servicio. Esta cadena tiene una longitud máxima de 256 caracteres. El nombre se conserva entre mayúsculas y minúsculas en el administrador de control de servicios. *Las comparaciones* de DisplayName siempre no tienen en cuenta mayúsculas de minúsculas.

Restricciones: acepta el mismo valor que la **propiedad Name.**

Ejemplo, "Atdisk".

</dd> <dt>

*PathName* \[ En\]
</dt> <dd>

Ruta de acceso completa al archivo ejecutable que implementa el servicio, por ejemplo, \\ "SystemRoot \\ System32 \\ drivers \\afd.sys".

</dd> <dt>

*ServiceType* \[ En\]
</dt> <dd>

Tipo de servicios proporcionados a los procesos que los llaman.

<dt>

1 (0x1)
</dt> <dd>

Kernel Driver

</dd> <dt>

2 (0x2)
</dt> <dd>

Controlador del sistema de archivos

</dd> <dt>

4 (0x4)
</dt> <dd>

Adapter (Adaptador)

</dd> <dt>

8 (0x8)
</dt> <dd>

Controlador de reconocedor

</dd> <dt>

16 (0x10)
</dt> <dd>

Proceso propio

</dd> <dt>

32 (0x20)
</dt> <dd>

Proceso de recurso compartido

</dd> <dt>

256 (0x100)
</dt> <dd>

Proceso interactivo

</dd> </dl> </dd> <dt>

*ErrorControl* \[ En\]
</dt> <dd>

Gravedad del error si este servicio no se inicia durante el inicio. El valor indica la acción realizada por el programa de inicio si se produce un error. El sistema registra todos los errores.

<dt>

0
</dt> <dd>

**Ignore**. El inicio continúa. No se envía ninguna notificación al usuario de que se ha registrado un error en el servicio.

</dd> <dt>

1
</dt> <dd>

**Normal.** El inicio continúa. Antes de que el usuario inicie sesión, el usuario recibe la notificación "Al menos un servicio o dispositivo no se pudo realizar durante el inicio".

</dd> <dt>

2
</dt> <dd>

**Severa.** El equipo intenta reiniciarse con la última configuración buena conocida. Si el servicio vuelve a dar error, el inicio continúa y se envía una notificación al usuario.

</dd> <dt>

3
</dt> <dd>

**Crítico.** El equipo intenta reiniciarse con la última configuración buena conocida. Si se produce un error de nuevo en el servicio, el inicio se detiene.

</dd> </dl> </dd> <dt>

*StartMode* \[ En\]
</dt> <dd>

Modo de inicio del Windows base. Para obtener más información, vea la sección Comentarios.

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Arranque**


</dt> <dd>

Controlador de dispositivo iniciado por el cargador del sistema operativo.

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Sistema**


</dt> <dd>

Controlador de dispositivo iniciado por el proceso de inicialización del sistema operativo. Este valor solamente es válido para servicios de controladores.

</dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automático**


</dt> <dd>

El administrador de control de servicios inicia automáticamente el servicio durante el inicio del sistema. Los servicios de inicio automático se inician antes de que un usuario inicie sesión en el equipo y se ejecuten incluso si ningún usuario inicia sesión en el equipo.

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual**


</dt> <dd>

Servicio que va a iniciar el administrador de control de servicios cuando un proceso llame al [**método StartService.**](win32-terminalservice-startservice.md) Aunque los servicios manuales deben ser iniciados específicamente por un usuario (o por un script), siguen funcionando incluso si el usuario cierra la sesión. Los servicios manuales a menudo se conocen como servicios a petición.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado**


</dt> <dd>

Servicio que ya no se puede iniciar. Para iniciar un servicio deshabilitado, primero debe cambiar la opción de inicio a Automático o Manual.

</dd> </dl> </dd> <dt>

*DesktopInteract* \[ En\]
</dt> <dd>

Si **es True,** el servicio puede crear o comunicarse con una ventana en el escritorio.

</dd> <dt>

*StartName* \[ En\]
</dt> <dd>

Nombre de cuenta en el que se ejecuta el servicio. Dependiendo del tipo de servicio, el nombre de cuenta puede tener el formato nombreDeUsuario nombreDeServidor o \\ . \\ Nombre de usuario. El proceso de servicio se registrará mediante uno de estos dos formularios cuando se ejecute. Si la cuenta pertenece al dominio integrado, . \\ Se puede especificar el nombre de usuario. Si se especifica **NULL,** el servicio se inicia sesión como la cuenta LocalSystem. Para los controladores de kernel o de nivel de sistema, *StartName* contiene el nombre del objeto de controlador (es decir, FileSystem Rdr o Driver Xns) que el sistema de entrada y salida \\ \\ \\ (E/S) usa para cargar el controlador de \\ dispositivo. Si se especifica **NULL,** el controlador se ejecuta con un nombre de objeto predeterminado creado por el sistema de E/S basado en el nombre del servicio, por ejemplo, "DWDOM \\ Admin".

También puede usar el formato de nombre principal de usuario (UPN) para especificar **startName,** por ejemplo, *Username@DomainName* .

</dd> <dt>

*StartPassword* \[ En\]
</dt> <dd>

Contraseña del nombre de cuenta especificado por el *parámetro StartName.* Especifique **NULL** si no va a cambiar la contraseña. Especifique una cadena vacía si el servicio no tiene contraseña.

> [!Note]  
> Al cambiar un servicio de un sistema local a una red o de una red a un sistema local, *StartPassword* debe ser una cadena vacía ("") y no **NULL.**

 

</dd> <dt>

*LoadOrderGroup* \[ En\]
</dt> <dd>

Nombre de grupo al que está asociado. Los grupos de orden de carga se encuentran en el registro del sistema y determinan la secuencia en la que se cargan los servicios en el sistema operativo. Si el puntero es **NULL** o si apunta a una cadena vacía, el servicio no pertenece a un grupo. Para obtener más información, vea la sección Comentarios.

Las dependencias entre grupos deben aparecer en el *parámetro LoadOrderGroupDependencies.* Los servicios de la lista de grupos de ordenación de carga se inician primero, seguidos de los servicios de los grupos que no están en la lista de grupos de ordenación de carga, seguidos de los servicios que no pertenecen a un grupo. El registro del sistema tiene una lista de grupos de pedidos de carga ubicados en:

**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **ServiceGroupOrder**

</dd> <dt>

*LoadOrderGroupDependencies* \[ En\]
</dt> <dd>

Lista de grupos de ordenación de carga que deben iniciarse antes de que se inicie este servicio. La matriz está doblemente **terminada en null.** Si el puntero es **NULL** o si apunta a una cadena vacía, el servicio no tiene dependencias. Los nombres de grupo deben ir precedidos por el carácter **SC \_ GROUP \_ IDENTIFIER** (definido en el archivo Winsvc.h) para diferenciarlos de los nombres de servicio, ya que los servicios y los grupos de servicios comparten el mismo espacio de nombres. La dependencia de un grupo significa que este servicio se puede ejecutar si al menos un miembro del grupo se está ejecutando después de un intento de iniciar todos los miembros del grupo.

</dd> <dt>

*ServiceDependencies* \[ En\]
</dt> <dd>

Lista que contiene los nombres de los servicios que deben iniciarse antes de que se inicie este servicio. La matriz está doblemente terminada en **NULL.** Si el puntero es **NULL** o si apunta a una cadena vacía, el servicio no tiene dependencias. La dependencia de un servicio indica que este servicio solo se puede ejecutar si el servicio del que depende se está ejecutando.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error. Para obtener códigos de error adicionales, [**vea Wmi Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores **HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**0**
</dt> <dd>

Se aceptó la solicitud.

</dd> <dt>

**1**
</dt> <dd>

No se admite la solicitud.

</dd> <dt>

**2**
</dt> <dd>

El usuario no tenía el acceso necesario.

</dd> <dt>

**3**
</dt> <dd>

No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.

</dd> <dt>

**4**
</dt> <dd>

El código de control solicitado no es válido o no es aceptable para el servicio.

</dd> <dt>

**5**
</dt> <dd>

El código de control solicitado no se puede enviar al servicio porque el estado del servicio ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**Propiedad** State) es igual a 0, 1 o 2.

</dd> <dt>

**6**
</dt> <dd>

El servicio no se ha iniciado.

</dd> <dt>

**7**
</dt> <dd>

El servicio no respondió a tiempo a la solicitud de inicio.

</dd> <dt>

**8**
</dt> <dd>

Error desconocido al iniciar el servicio.

</dd> <dt>

**9**
</dt> <dd>

No se encontró la ruta de acceso del directorio al archivo ejecutable del servicio.

</dd> <dt>

**10**
</dt> <dd>

El servicio ya se está ejecutando.

</dd> <dt>

**11**
</dt> <dd>

La base de datos para agregar un nuevo servicio está bloqueada.

</dd> <dt>

**12**
</dt> <dd>

Se ha quitado del sistema una dependencia en la que se basa este servicio.

</dd> <dt>

**13**
</dt> <dd>

El servicio no pudo encontrar el servicio necesario de un servicio dependiente.

</dd> <dt>

**14**
</dt> <dd>

El servicio se ha deshabilitado del sistema.

</dd> <dt>

**15**
</dt> <dd>

El servicio no tiene la autenticación correcta para ejecutarse en el sistema.

</dd> <dt>

**16**
</dt> <dd>

Este servicio se está quitando del sistema.

</dd> <dt>

**17**
</dt> <dd>

El servicio no tiene ningún subproceso de ejecución.

</dd> <dt>

**18**
</dt> <dd>

El servicio tiene dependencias circulares cuando se inicia.

</dd> <dt>

**19**
</dt> <dd>

Un servicio se ejecuta con el mismo nombre.

</dd> <dt>

**20**
</dt> <dd>

El nombre del servicio tiene caracteres no válidos.

</dd> <dt>

**21**
</dt> <dd>

Se han pasado parámetros no válidos al servicio.

</dd> <dt>

**22**
</dt> <dd>

La cuenta con la que se ejecuta este servicio no es válida o carece de los permisos para ejecutar el servicio.

</dd> <dt>

**23**
</dt> <dd>

El servicio existe en la base de datos de servicios disponibles del sistema.

</dd> <dt>

**24**
</dt> <dd>

El servicio se encuentra en pausa actualmente en el sistema.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Cuando se inicia un equipo, también se inician todos los servicios de inicio automático. En ocasiones, uno de estos servicios podría no iniciarse junto con el equipo. Cuando se produce un error en un servicio durante el inicio del sistema, el equipo realiza una acción basada en el valor del código de control de errores del servicio.

La mayoría de los servicios se instalan mediante el código de control de errores Normal. Algunas de las excepciones, que se instalan mediante el código de error Omitir, incluyen:

-   Servicio de replicación de archivos
-   Tarjeta inteligente
-   Inicio de sesión secundario
-   WMI

En el caso de los servicios instalados mediante el código de error Omitir, no se envía ninguna notificación al usuario de que se ha producido un error en el servicio. Si prefiere la notificación en pantalla de que un servicio no se pudo iniciar, puede usar WMI para cambiar el código de control de errores. Los códigos de control de errores solo se aplican al inicio del equipo; Los códigos de control de errores no se usan si detiene e intenta reiniciar un servicio después de que el equipo se esté ejecutando.

En ocasiones, es posible que tenga que cambiar la cuenta con la que se ejecuta un servicio determinado. Por ejemplo, puede ejecutar un servicio en una cuenta administrativa. Dado que esto puede crear una vulnerabilidad de seguridad, puede cambiar el servicio a una cuenta con menos privilegios. Como alternativa, es posible que tenga servicios que se ejecuten en una cuenta que esté a punto de eliminarse, o que desee asegurarse de que, en todos los servidores, determinados servicios se ejecutan con determinadas cuentas. Puede usar el método **Change de** la clase [**\_ TerminalService de Win32**](win32-terminalservice.md) para configurar los servicios para que se ejecuten en una cuenta de usuario especificada. Al seleccionar una cuenta, tenga en cuenta lo siguiente:

-   La cuenta que se usa como cuenta de servicio debe tener el derecho de iniciar sesión como servicio. Este derecho se puede conceder mediante directiva de grupo.
-   La cuenta que se usa como cuenta de servicio no debe ser miembro de un grupo de administradores local, de dominio o de empresa.
-   Cada instancia de un servicio debe ejecutarse en una cuenta de usuario única. Esto proporciona seguridad adicional y permite la auditoría de instancias de servicio individuales.
-   Si el servicio es interactivo, el servicio debe ejecutarse en la cuenta LocalSystem.

    LocalSystem es necesario porque solo una estación de ventana (WinSta0) puede ser visible e interactiva a la vez. Si un servicio se ejecuta en una cuenta que no sea LocalSystem, se ejecuta en la estación de ventana Service-0x03e7$ Default, que \\ es una ventana invisible. Los servicios que se ejecutan en esta estación de ventana no pueden recibir la entrada o la salida de visualización.

Al asignar una cuenta a un servicio, el SCM requiere la contraseña correcta para esa cuenta antes de realizar la asignación. Si proporciona una contraseña incorrecta, el SCM rechaza la cuenta. Si configura una cuenta de servicio mediante la cuenta LocalSystem, LocalService o NetworkService, no es necesario proporcionar una contraseña de cuenta porque estas cuentas no tienen contraseñas.

El SCM almacena la contraseña de la cuenta en la base de datos de servicios. Sin embargo, una vez asignada la contraseña, el SCM no garantiza que la contraseña almacenada en la base de datos de servicios y la contraseña asignada a la cuenta de usuario de Active Directory sigan coincidendo. Por lo tanto, podría producirse una situación similar a la siguiente:

-   . Configure un servicio para que se ejecute en una cuenta de usuario determinada.
-   El servicio se inicia en esa cuenta mediante la contraseña de la cuenta actual.
-   La contraseña de la cuenta de usuario se cambia.
-   El servicio continúa en ejecución. Sin embargo, si el servicio se detiene, no se puede reiniciar porque el SCM sigue utilizando la contraseña antigua no válida. El cambio de la contraseña Active Directory no cambia la contraseña almacenada en la base de datos de servicios.

Si ejecuta servicios con cuentas de usuario normales, debe actualizar esas contraseñas de servicio cada vez que cambie la contraseña de la cuenta de usuario. Esto puede llevar mucho tiempo si no está seguro de qué servicios se ejecutan en esa cuenta o qué equipos tienen servicios que se ejecutan en esa cuenta. Afortunadamente, puede usar WMI para comprobar las cuentas de servicio en todos los equipos y, si es necesario, cambiar la contraseña de la cuenta de servicio.

El [**parámetro \_ LoadOrderGroup de Win32**](/windows/desktop/CIMWin32Prov/win32-loadordergroup) representa un grupo de servicios del sistema que definen las dependencias de ejecución. Los servicios deben iniciarse en el orden especificado por el grupo de pedidos de carga porque los servicios dependen entre sí. Estos servicios dependientes requieren la presencia de los servicios antecedentes para funcionar correctamente.

Para cambiar un servicio de un servicio de red a un sistema local, los parámetros *StartName* y *StartPassword* deben tener los siguientes valores:


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



Para cambiar un servicio de un servicio de sistema local a una red, los parámetros *StartName* y *StartPassword* deben tener los siguientes valores:


```C++
StartName = "NT AUTHORITY\NetworkService"
StartPassword = "" // - empty string, not NULL
```



## <a name="examples"></a>Ejemplos

El siguiente vbscript cambia la cuenta de servicio para que los servicios se ejecuten con una cuenta de usuario especificada a LocalSystem.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colServiceList = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objService in colServices
 errServiceChange = objService.Change _
 ( , , , , , , ".\LocalSystem" , "")
Next
```



El siguiente VBScript cambia la contraseña de la cuenta de servicio para todos los scripts que se ejecutan en Netsvc


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colServiceList = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objservice in colServiceList
 errReturn = objService.Change( , , , , , , , "password")
Next
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>Mbnapi.h</dt> </dl>     |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Servicio \_ Win32**](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[Clases de sistema operativo](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[**TerminalService de Win32 \_**](win32-terminalservice.md)
</dt> <dt>

[Tareas wmi: servicios](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

