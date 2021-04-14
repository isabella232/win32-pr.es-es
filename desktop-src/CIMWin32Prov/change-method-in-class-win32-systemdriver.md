---
description: Modifica un \_ servicio SystemDriver de Win32.
ms.assetid: 61ee3297-2a66-466e-bdba-74d683f3ea70
ms.tgt_platform: multiple
title: Método de cambio de la clase Win32_SystemDriver (Mbnapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.Change
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: da814c8321e35189594bc350bd1e278a219bac59
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496426"
---
# <a name="change-method-of-the-win32_systemdriver-class"></a>Método de cambio de la \_ clase Win32 SystemDriver

El método de clase **Change** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) modifica un [**servicio \_ SystemDriver de Win32**](win32-systemdriver.md) . El [**parámetro \_ LoadOrderGroup de Win32**](win32-loadordergroup.md) representa una agrupación de los servicios del sistema que definen las dependencias de ejecución. Los servicios deben iniciarse en el orden especificado por el grupo de orden de carga, ya que los servicios dependen entre sí. Estos servicios dependientes requieren la presencia de los servicios antecedentes para que funcionen correctamente.

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 Change(
  [in] string  DisplayName,
  [in] string  PathName,
  [in] uint8   ServiceType,
  [in] uint8   ErrorControl,
  [in] string  StartMode,
  [in] boolean DesktopInteract,
  [in] string  StartName,
  [in] string  StartPassword,
  [in] string  LoadOrderGroup,
  [in] string  LoadOrderGroupDependencies[],
  [in] string  ServiceDependencies[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DisplayName* \[ de\]
</dt> <dd>

Nombre para mostrar del servicio. Esta cadena tiene una longitud máxima de 256 caracteres. El nombre se conserva en las mayúsculas y minúsculas en el administrador de control de servicios. Las comparaciones de *displayName* siempre distinguen mayúsculas de minúsculas.

Constraints: acepta el mismo valor que el parámetro *Name* .

Ejemplo: "Endisco"

</dd> <dt>

*Nombreruta* \[ de\]
</dt> <dd>

Ruta de acceso completa al archivo ejecutable que implementa el servicio.

Ejemplo: *\\ raíz_sistema \\ system32 \\ drivers \\afd.sys*

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

La gravedad del error si este servicio no se inicia durante el inicio. El valor indica la acción realizada por el programa de inicio si se produce un error. El sistema registra todos los errores.

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Omitir** (0)


</dt> <dd>

No se notifica al usuario.

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)


</dt> <dd>

Normal. Se notifica al usuario.

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Grave** (2)


</dt> <dd>

El sistema se reinicia con la última configuración válida.

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** (3)


</dt> <dd>

El sistema intenta reiniciarse con una configuración válida.

</dd> </dl> </dd> <dt>

*StartMode* \[ de\]
</dt> <dd>

Modo de inicio del servicio base de Windows.

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Inicio de arranque**


</dt> <dd>

Controlador de dispositivo Iniciado por el cargador del sistema operativo.

</dd> <dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Inicio de arranque**


</dt> <dd>

Controlador de dispositivo que inicia el cargador del sistema operativo.

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**Inicio del sistema**


</dt> <dd>

Controlador de dispositivo Iniciado por el proceso de inicialización del sistema operativo. Este valor solamente es válido para servicios de controladores.

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Inicio automático**


</dt> <dd>

Servicio que el administrador de control de servicios inicia automáticamente durante el inicio del sistema.

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Inicio de la demanda**


</dt> <dd>

Servicio que va a iniciar el administrador de control de servicios cuando un proceso llama al método [**StartService**](startservice-method-in-class-win32-systemdriver.md) .

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disponible**


</dt> <dd>

Servicio que no se puede iniciar.

</dd> </dl> </dd> <dt>

*DesktopInteract* \[ de\]
</dt> <dd>

Valor que, si **es true**, el servicio puede crear o comunicarse con las ventanas del escritorio.

</dd> <dt>

*StartName* \[ de\]
</dt> <dd>

Nombre de cuenta con el que se ejecuta el servicio. Dependiendo del tipo de servicio, el nombre de la cuenta puede tener el formato nombreDeDominio \\ nombreDeUsuario o. \\ Nombre. Cuando se ejecuta, el proceso de servicio se registra con una de estas dos formas. Si la cuenta pertenece al dominio integrado,. \\ Se puede especificar el nombre de usuario. Si se especifica una cadena vacía, el servicio inicia sesión como la cuenta LocalSystem. En el caso de los controladores de kernel o de nivel de sistema, *StartName* contiene el nombre de objeto del controlador, por ejemplo, \\ filesystem \\ RDR o \\ \\ el controlador XNS, que el sistema de entrada y salida (e/s) utiliza para cargar el controlador de dispositivo. Si se especifica **null** , el controlador se ejecuta con un nombre de objeto predeterminado que el sistema de e/s crea en función del nombre del servicio, por ejemplo, DWDOM \\ admin.

También puede usar el formato de nombre principal de usuario (UPN) para especificar **StartName**, por ejemplo, *Username@DomainName* .

</dd> <dt>

*StartPassword* \[ de\]
</dt> <dd>

Contraseña del nombre de cuenta especificado por el parámetro *StartName* . Especifique **null** si no va a cambiar la contraseña. Especifique una cadena vacía si el servicio no tiene contraseña.

> [!Note]  
> Al cambiar un servicio de un sistema local a una red, o de una red a un sistema local, *StartPassword* debe ser una cadena vacía ("") y no **null**.

 

</dd> <dt>

*LoadOrderGroup* \[ de\]
</dt> <dd>

Nombre del grupo al que está asociado. Los grupos de pedidos de carga se incluyen en el registro del sistema y determinan la secuencia en la que se cargan los servicios en el sistema operativo. Si el puntero es **null**, o si apunta a una cadena vacía, el servicio no pertenece a un grupo. Las dependencias entre grupos deben aparecer en el parámetro *LoadOrderGroupDependencies* . Los servicios de la lista de grupos de orden de carga se inician en primer lugar, seguidos de los servicios de los grupos que no están en la lista de grupos de orden de carga, seguidos de los servicios que no pertenecen a un grupo. El registro del sistema tiene una lista de grupos de orden de carga que se encuentran en:

**HKEY \_ \_** \\  \\  \\ **Control** CurrentControlSet del sistema \\  de equipo local ServiceGroupOrder

</dd> <dt>

*LoadOrderGroupDependencies* \[ de\]
</dt> <dd>

Lista de grupos de orden de carga que deben iniciarse antes de que se inicie este servicio. La matriz termina en **null**. Si el puntero es **null**, o si apunta a una cadena vacía, el servicio no tiene dependencias. Los nombres de grupo deben ir precedidos del **\_ \_ identificador de grupo SC** (definido en el archivo WinSvc. h) para diferenciarlos de los nombres de servicio, ya que los servicios y los grupos de servicios comparten el mismo espacio de nombres. La dependencia de un grupo significa que este servicio se puede ejecutar si se está ejecutando al menos un miembro del grupo después de un intento de iniciar todos los miembros del grupo.

</dd> <dt>

*ServiceDependencies* \[ de\]
</dt> <dd>

Lista que contiene los nombres de los servicios que deben iniciarse antes de que se inicie este servicio. La matriz termina en **null**. Si el puntero es **null**, o si apunta a una cadena vacía, el servicio no tiene dependencias. La dependencia de un servicio significa que este servicio solo se puede ejecutar si se está ejecutando el servicio del que depende.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de cero (0) si el servicio se modificó correctamente, 1 (uno) si no se admite la solicitud y cualquier otro número para indicar un error.

<dl> <dt>

**Correcto** (0)
</dt> <dt>

**No compatible** (1)
</dt> <dt>

**Acceso denegado** (2)
</dt> <dt>

**Servicios dependientes en ejecución** (3)
</dt> <dt>

**Control de servicio no válido** (4)
</dt> <dt>

El **servicio no puede aceptar el control** (5)
</dt> <dt>

**Servicio no activo** (6)
</dt> <dt>

**Tiempo de espera de solicitud de servicio** (7)
</dt> <dt>

**Error desconocido** (8)
</dt> <dt>

**No se encontró la ruta de acceso** (9)
</dt> <dt>

El **servicio ya se está ejecutando** (10)
</dt> <dt>

**Base de datos de servicio bloqueada** (11)
</dt> <dt>

**Dependencia de servicio eliminada** (12)
</dt> <dt>

**Error de dependencia de servicio** (13)
</dt> <dt>

**Servicio deshabilitado** (14)
</dt> <dt>

**Error de inicio de sesión de servicio** (15)
</dt> <dt>

**Servicio marcado para eliminación** (16)
</dt> <dt>

**Servicio sin subproceso** (17)
</dt> <dt>

**Estado dependencia circular** (18)
</dt> <dt>

**Estado nombre duplicado** (19)
</dt> <dt>

**Estado nombre no válido** (20)
</dt> <dt>

**Estado parámetro no válido** (21)
</dt> <dt>

**Estado cuenta de servicio no válida** (22)
</dt> <dt>

El **servicio de estado existe** (23)
</dt> <dt>

**Servicio ya pausado** (24)
</dt> <dt>

**Otro** (25 4294967295)
</dt> </dl>

## <a name="remarks"></a>Observaciones

Para cambiar un servicio de un servicio de red al sistema local, use los siguientes valores para los parámetros *StartName* y *StartPassword* :


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



Para cambiar un servicio de un servicio de sistema local a servicio de red, utilice los siguientes valores para los parámetros *StartName* y *StartPassword* :


```C++
StartName = "NT AUTHORITY\NetworkService"
StartPassword = "" // - empty string, not NULL
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| Encabezado<br/>                   | <dl> <dt>Mbnapi. h</dt> </dl>     |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32 \_ SystemDriver**](win32-systemdriver.md)
</dt> </dl>

 

