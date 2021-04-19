---
title: Método de cambio de la clase Win32_Service (Mbnapi. h) (TerminalService)
description: Modifica un TerminalService de Win32 \_ .
ms.assetid: 19E43A80-47C9-4C5A-8E73-723F206AA7C0
ms.tgt_platform: multiple
keywords:
- Cambiar método Servicios de Escritorio remoto
- Cambiar Servicios de Escritorio remoto de método, Win32_Service clase
- Win32_Service Servicios de Escritorio remoto de clase, Change (método)
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
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/05/2021
ms.locfileid: "106389209"
---
# <a name="change-method-of-the-win32_service-class-mbnapih---terminalservice"></a>Método de cambio de la clase Win32_Service (Mbnapi. h)-TerminalService

El método de clase **Change** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) modifica un [**\_ TerminalService de Win32**](win32-terminalservice.md).

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

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

*DisplayName* \[ de\]
</dt> <dd>

Nombre para mostrar del servicio. Esta cadena tiene una longitud máxima de 256 caracteres. El nombre se conserva en las mayúsculas y minúsculas en el administrador de control de servicios. Las comparaciones de *displayName* siempre distinguen mayúsculas de minúsculas.

Constraints: acepta el mismo valor que la propiedad **Name** .

Ejemplo, "Endisco".

</dd> <dt>

*Nombreruta* \[ de\]
</dt> <dd>

Ruta de acceso completa al archivo ejecutable que implementa el servicio, por ejemplo, " \\ raízDelSistema \\ System32 \\ drivers \\afd.sys".

</dd> <dt>

*ServiceType* \[ de\]
</dt> <dd>

Tipo de servicios proporcionados a los procesos que los llaman.

<dt>

1 (0x1)
</dt> <dd>

Controlador de kernel

</dd> <dt>

2 (0X2)
</dt> <dd>

Controlador del sistema de archivos

</dd> <dt>

4 (0x4)
</dt> <dd>

Adapter (Adaptador)

</dd> <dt>

8 (0x8)
</dt> <dd>

Controlador del reconocedor

</dd> <dt>

16 (0x10)
</dt> <dd>

Proceso propio

</dd> <dt>

32 (0x20)
</dt> <dd>

Compartir proceso

</dd> <dt>

256 (0x100)
</dt> <dd>

Proceso interactivo

</dd> </dl> </dd> <dt>

*ErrorControl* \[ de\]
</dt> <dd>

Gravedad del error si este servicio no se inicia durante el inicio. El valor indica la acción realizada por el programa de inicio si se produce un error. El sistema registra todos los errores.

<dt>

0
</dt> <dd>

**Ignore**. El inicio continúa. No se proporciona ninguna notificación al usuario de que se produjo un error en el servicio.

</dd> <dt>

1
</dt> <dd>

**Sin.** El inicio continúa. Antes de que el usuario inicie sesión, el usuario recibe la notificación, "error al menos un servicio o dispositivo durante el inicio".

</dd> <dt>

2
</dt> <dd>

**Fuertes.** El equipo intenta reiniciarse con la última configuración válida conocida. Si se produce un error de nuevo en el servicio, el inicio continúa y se le concede una notificación al usuario.

</dd> <dt>

3
</dt> <dd>

**Suma.** El equipo intenta reiniciarse con la última configuración válida conocida. Si se produce un error en el servicio, se detiene el inicio.

</dd> </dl> </dd> <dt>

*StartMode* \[ de\]
</dt> <dd>

Modo de inicio del servicio base de Windows. Para obtener más información, vea la sección Comentarios.

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Arranque**


</dt> <dd>

Controlador de dispositivo Iniciado por el cargador del sistema operativo.

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Integrado**


</dt> <dd>

Controlador de dispositivo Iniciado por el proceso de inicialización del sistema operativo. Este valor solamente es válido para servicios de controladores.

</dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automático**


</dt> <dd>

El administrador de control de servicios inicia automáticamente el servicio durante el inicio del sistema. Los servicios de inicio automático se inician antes de que un usuario inicie sesión en el equipo y se ejecuten incluso si ningún usuario inicia sesión en el equipo.

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual**


</dt> <dd>

Servicio que el administrador de control de servicios iniciará cuando un proceso llame al método [**StartService**](win32-terminalservice-startservice.md) . Aunque los servicios manuales deben ser iniciados específicamente por un usuario (o mediante un script), siguen ejecutándose incluso si el usuario cierra la sesión. Los servicios manuales se suelen denominar servicios a petición.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disponible**


</dt> <dd>

Servicio que ya no se puede iniciar. Para iniciar un servicio deshabilitado, primero debe cambiar la opción de inicio a automático o manual.

</dd> </dl> </dd> <dt>

*DesktopInteract* \[ de\]
</dt> <dd>

Si **es true**, el servicio puede crear o comunicarse con una ventana en el escritorio.

</dd> <dt>

*StartName* \[ de\]
</dt> <dd>

Nombre de la cuenta con la que se ejecuta el servicio. Dependiendo del tipo de servicio, el nombre de la cuenta puede tener el formato nombreDeDominio \\ nombreDeUsuario o. \\ Nombre. El proceso de servicio se registrará con una de estas dos formas cuando se ejecute. Si la cuenta pertenece al dominio integrado,. \\ Se puede especificar el nombre de usuario. Si se especifica **null** , el servicio se iniciará sesión como la cuenta LocalSystem. En el caso de los controladores de kernel o de nivel de sistema, *StartName* contiene el nombre de objeto del controlador (es decir, sistema de \\ archivos \\ RDR o \\ XNS del controlador \\ ) que usa el sistema de entrada y salida (e/s) para cargar el controlador de dispositivo. Si se especifica **null** , el controlador se ejecuta con un nombre de objeto predeterminado creado por el sistema de e/s basado en el nombre del servicio, por ejemplo, "DWDOM \\ admin".

También puede usar el formato de nombre principal de usuario (UPN) para especificar **StartName**, por ejemplo, *Username@DomainName* .

</dd> <dt>

*StartPassword* \[ de\]
</dt> <dd>

Contraseña para el nombre de cuenta especificado por el parámetro *StartName* . Especifique **null** si no va a cambiar la contraseña. Especifique una cadena vacía si el servicio no tiene contraseña.

> [!Note]  
> Al cambiar un servicio de un sistema local a una red, o de una red a un sistema local, *StartPassword* debe ser una cadena vacía ("") y no **null**.

 

</dd> <dt>

*LoadOrderGroup* \[ de\]
</dt> <dd>

Nombre del grupo al que está asociado. Los grupos de pedidos de carga se incluyen en el registro del sistema y determinan la secuencia en la que se cargan los servicios en el sistema operativo. Si el puntero es **null**, o si apunta a una cadena vacía, el servicio no pertenece a un grupo. Para obtener más información, vea la sección Comentarios.

Las dependencias entre grupos deben aparecer en el parámetro *LoadOrderGroupDependencies* . Los servicios de la lista de grupos de orden de carga se inician en primer lugar, seguidos de los servicios de los grupos que no están en la lista de grupos de orden de carga, seguidos de los servicios que no pertenecen a un grupo. El registro del sistema tiene una lista de grupos de orden de carga que se encuentran en:

**HKEY \_ \_** \\  \\  \\ **Control** CurrentControlSet del sistema \\  de equipo local ServiceGroupOrder

</dd> <dt>

*LoadOrderGroupDependencies* \[ de\]
</dt> <dd>

Lista de grupos de orden de carga que deben iniciarse antes de que se inicie este servicio. La matriz termina en **null**. Si el puntero es **null**, o si apunta a una cadena vacía, el servicio no tiene dependencias. Los nombres de grupo deben ir precedidos del **\_ \_ identificador de grupo SC** (definido en el archivo Winsvc. h) para diferenciarlos de los nombres de servicio, ya que los servicios y los grupos de servicios comparten el mismo espacio de nombres. La dependencia de un grupo significa que este servicio se puede ejecutar si se está ejecutando al menos un miembro del grupo después de un intento de iniciar todos los miembros del grupo.

</dd> <dt>

*ServiceDependencies* \[ de\]
</dt> <dd>

Lista que contiene los nombres de los servicios que deben iniciarse antes de que se inicie este servicio. La matriz termina en **null**. Si el puntero es **null**, o si apunta a una cadena vacía, el servicio no tiene dependencias. La dependencia de un servicio indica que este servicio solo se puede ejecutar si se está ejecutando el servicio del que depende.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error. Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

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

El código de control solicitado no se puede enviar al servicio porque el estado del servicio ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** Property) es igual a 0, 1 o 2.

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

No se encontró la ruta de acceso al directorio del archivo ejecutable del servicio.

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

Una dependencia de la que depende este servicio se ha quitado del sistema.

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

El servicio tiene dependencias circulares al iniciarse.

</dd> <dt>

**19**
</dt> <dd>

Se está ejecutando un servicio con el mismo nombre.

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

La cuenta con la que se ejecuta este servicio no es válida o carece de permisos para ejecutar el servicio.

</dd> <dt>

**23**
</dt> <dd>

El servicio existe en la base de datos de servicios disponibles del sistema.

</dd> <dt>

**24**
</dt> <dd>

El servicio se encuentra en pausa actualmente en el sistema.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Cuando se inicia un equipo, también se inician todos los servicios de inicio automático. En ocasiones, es posible que uno de estos servicios no se inicie junto con el equipo. Cuando se produce un error en un servicio durante el inicio del sistema, el equipo toma medidas según el valor del código de control de errores del servicio.

la mayoría de los servicios se instalan con el código de control de errores normal. Algunas de las excepciones, que se instalan con el código de error ignore, incluyen:

-   Servicio de replicación de archivos
-   Tarjeta inteligente
-   Inicio de sesión secundario
-   WMI

En el caso de los servicios que se instalan con el código de error ignore, no se proporciona ninguna notificación al usuario de que se ha producido un error en el servicio. Si prefiere recibir una notificación en pantalla de que no se pudo iniciar un servicio, puede usar WMI para cambiar el código de control de errores. Los códigos de control de errores solo se aplican al inicio del equipo; los códigos de control de errores no se usan si detiene e intenta reiniciar un servicio después de que el equipo se esté ejecutando.

En alguna ocasión, es posible que necesite cambiar la cuenta en la que se ejecuta un servicio determinado. Por ejemplo, puede ejecutar un servicio en una cuenta administrativa. Como esto puede crear una vulnerabilidad de seguridad, puede cambiar el servicio a una cuenta con menos privilegios. Como alternativa, es posible que los servicios se ejecuten en una cuenta que esté a punto de eliminarse, o puede que desee asegurarse de que, en todos los servidores, determinados servicios se ejecuten en determinadas cuentas. Puede usar el método **Change** de la clase [**Win32 \_ TerminalService**](win32-terminalservice.md) para configurar los servicios de para que se ejecuten en una cuenta de usuario especificada. Al seleccionar una cuenta, tenga en cuenta lo siguiente:

-   La cuenta que se usa como cuenta de servicio debe tener el derecho de iniciar sesión como servicio. Este derecho se puede conceder mediante directiva de grupo.
-   La cuenta que se usa como cuenta de servicio no debe ser miembro de un grupo local, de dominio o de administradores de organización.
-   Cada instancia de un servicio se debe ejecutar con una cuenta de usuario única. Esto proporciona seguridad adicional y habilita la auditoría de instancias de servicio individuales.
-   Si el servicio es interactivo, el servicio debe ejecutarse en la cuenta LocalSystem.

    Se requiere LocalSystem porque solo una estación de ventana (WinSta0) puede ser visible e interactiva a la vez. Si un servicio se ejecuta en una cuenta distinta de LocalSystem, se ejecuta en la estación de ventana de servicio-0x03e7 $ \\ predeterminada, que es una ventana invisible. Los servicios que se ejecutan en esta estación de ventana no pueden recibir entradas ni mostrar resultados.

Cuando asigna una cuenta a un servicio, el SCM requiere la contraseña correcta para esa cuenta antes de realizar la asignación. Si proporciona una contraseña incorrecta, el SCM rechazará la cuenta. Si configura una cuenta de servicio con la cuenta LocalSystem, LocalService o NetworkService, no es necesario que proporcione una contraseña de cuenta porque estas cuentas no tienen contraseñas.

El SCM almacena la contraseña de la cuenta en la base de datos de servicios. Sin embargo, una vez asignada la contraseña, el SCM no garantiza que la contraseña almacenada en la base de datos de servicios y la contraseña asignada a la cuenta de usuario en Active Directory sigan coincidiendo. Por consiguiente, podría producirse una situación similar a la siguiente:

-   . Puede configurar un servicio para que se ejecute en una cuenta de usuario determinada.
-   El servicio se inicia con esa cuenta mediante la contraseña de la cuenta actual.
-   Puede cambiar la contraseña de la cuenta de usuario.
-   El servicio continúa ejecutándose. Sin embargo, si el servicio se detiene, no puede reiniciarlo porque el SCM sigue usando la contraseña antigua no válida. El cambio de la contraseña en Active Directory no cambia la contraseña almacenada en la base de datos de servicios.

Si ejecuta servicios en cuentas de usuario normales, deberá actualizar esas contraseñas de servicio cada vez que cambie la contraseña de la cuenta de usuario. Esto puede llevar mucho tiempo si no está seguro de qué servicios se están ejecutando en esa cuenta o qué equipos tienen servicios en ejecución en esa cuenta. Afortunadamente, puede usar WMI para comprobar las cuentas de servicio en todos los equipos y, si es necesario, cambiar la contraseña de la cuenta de servicio.

El [**parámetro \_ LoadOrderGroup de Win32**](/windows/desktop/CIMWin32Prov/win32-loadordergroup) representa un grupo de servicios del sistema que definen las dependencias de la ejecución. Los servicios deben iniciarse en el orden especificado por el grupo de orden de carga, ya que los servicios dependen entre sí. Estos servicios dependientes requieren la presencia de los servicios antecedentes para que funcionen correctamente.

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

El siguiente VBScript cambia la cuenta de servicio para que los servicios se ejecuten con una cuenta de usuario especificada en LocalSystem.


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



El siguiente VBScript cambia la contraseña de la cuenta de servicio para todos los scripts que se ejecutan en netsvc


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



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>Mbnapi. h</dt> </dl>     |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Servicio Win32**](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[Clases de sistema operativo](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[**Win32 \_ TerminalService**](win32-terminalservice.md)
</dt> <dt>

[Tareas WMI: servicios](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

