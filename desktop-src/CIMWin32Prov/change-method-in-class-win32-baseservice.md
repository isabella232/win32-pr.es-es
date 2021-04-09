---
description: Modifica un objeto de servicio derivado de Win32 \_ BaseService.
ms.assetid: d5f4f472-e7d9-4664-9430-9c77034a5978
ms.tgt_platform: multiple
title: Método de cambio de la clase Win32_BaseService (Mbnapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.Change
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a70ee83229a830e22fba4241a6c50eb8d971c5ad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153301"
---
# <a name="change-method-of-the-win32_baseservice-class"></a>Método de cambio de la \_ clase Win32 BaseService

El método de clase **Change** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) modifica un objeto de servicio derivado de [**Win32 \_ BaseService**](win32-baseservice.md). El [**parámetro \_ LoadOrderGroup de Win32**](win32-loadordergroup.md) representa un grupo de servicios del sistema que definen las dependencias de la ejecución. Los servicios deben iniciarse en el orden especificado por el grupo de orden de carga, ya que los servicios dependen entre sí. Estos servicios dependientes requieren que los servicios antecedentes funcionen correctamente.

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

Nombre para mostrar de un servicio. Esta cadena tiene una longitud máxima de 256 caracteres. El nombre es mayúsculas y minúsculas en el administrador de control de servicios. Las comparaciones de *displayName* siempre distinguen mayúsculas de minúsculas.

Constraints: acepta el mismo valor que el parámetro *Name* .

Ejemplo: "Endisco".

</dd> <dt>

*Nombreruta* \[ de\]
</dt> <dd>

Ruta de acceso completa al archivo ejecutable que implementa un servicio.

Ejemplo: " \\ systemroot \\ System32 \\ drivers \\afd.sys".

</dd> <dt>

*ServiceType* \[ de\]
</dt> <dd>

Tipo de servicios proporcionados a los procesos que los llaman.

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>**Controlador de kernel** (1)


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>**Controlador del sistema de archivos** (2)


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>**Adaptador** (4)


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>**Controlador de reconocedor** (8)


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>**Proceso propio** (16)


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>**Proceso de uso compartido** (32)


</dt> <dd></dd> <dt>



 (256)


</dt> <dd>

Proceso interactivo

</dd> </dl> </dd> <dt>

*ErrorControl* \[ de\]
</dt> <dd>

Gravedad de un error si este servicio no se inicia durante el inicio. El valor indica la acción que realiza el programa de inicio si se produce un error. El sistema registra todos los errores.

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

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Inicio de arranque** ("arranque")


</dt> <dd>

Controlador de dispositivo que inicia el cargador del sistema operativo.

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**Inicio del sistema** ("System")


</dt> <dd>

Controlador de dispositivo Iniciado por el proceso de inicialización del sistema operativo. Este valor solamente es válido para servicios de controladores.

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Inicio automático** ("automático")


</dt> <dd>

Servicio que el administrador de control de servicios inicia automáticamente durante el inicio del sistema.

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Inicio** de la demanda ("manual")


</dt> <dd>

Servicio que va a iniciar el administrador de control de servicios cuando un proceso llama al método [**StartService**](startservice-method-in-class-win32-baseservice.md) .

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** ("deshabilitado")


</dt> <dd>

Servicio que no se puede iniciar.

</dd> </dl> </dd> <dt>

*DesktopInteract* \[ de\]
</dt> <dd>

Si **es true**, el servicio puede crear o comunicarse con una ventana en el escritorio.

</dd> <dt>

*StartName* \[ de\]
</dt> <dd>

Nombre de cuenta con el que se ejecuta el servicio, que depende del tipo de servicio. El nombre de la cuenta puede tener el formato nombreDeDominio \\ nombreDeUsuario o. \\ Nombre. Cuando se ejecuta, el proceso de servicio se registra con una de las dos formas anteriores. Si la cuenta pertenece al dominio integrado,. \\ Se puede especificar el nombre de usuario. Si se especifica una cadena vacía, el servicio inicia sesión como la cuenta LocalSystem. En el caso de los controladores de kernel o de nivel de sistema, *StartName* contiene el nombre de objeto del controlador, por ejemplo, \\ filesystem \\ RDR o \\ \\ el controlador XNS, que el sistema de entrada y salida (e/s) utiliza para cargar el controlador de dispositivo. Si se especifica **null** , el controlador se ejecuta con un nombre de objeto predeterminado que el sistema de e/s crea en función del nombre del servicio, por ejemplo, DWDOM \\ admin.

También puede usar el formato de nombre principal de usuario (UPN) para especificar **StartName**, por ejemplo, *Username@DomainName* .

</dd> <dt>

*StartPassword* \[ de\]
</dt> <dd>

Contraseña del nombre de la cuenta que especifica el parámetro *StartName* . Especifique **null** cuando no cambie la contraseña. Especifique una cadena vacía si el servicio no tiene una contraseña.

> [!Note]  
> Al cambiar un servicio de sistema local a red o de red a sistema local, *StartPassword* debe ser una cadena vacía ("") y no **null**.

 

</dd> <dt>

*LoadOrderGroup* \[ de\]
</dt> <dd>

Nombre del grupo al que está asociado. Los grupos de pedidos de carga se incluyen en el registro del sistema y determinan la secuencia en la que se cargan los servicios en un sistema operativo. Si el puntero es **null**, o apunta a una cadena vacía, el servicio no pertenece a un grupo. Las dependencias entre grupos deben aparecer en el parámetro *LoadOrderGroupDependencies* . Los servicios de la lista de grupos de orden de carga se inician en primer lugar, seguidos de los servicios de los grupos que no están en la lista de grupos de orden de carga, seguidos de los servicios que no pertenecen a un grupo. El registro del sistema tiene una lista de grupos de orden de carga ubicados en **HKEY \_ local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **control** \\ **ServiceGroupOrder**.

</dd> <dt>

*LoadOrderGroupDependencies* \[ de\]
</dt> <dd>

Lista de grupos de orden de carga que deben iniciarse antes de que se inicie este servicio. La matriz termina en **null**. Si el puntero es **null**, o si apunta a una cadena vacía, el servicio no tiene dependencias. Los nombres de grupo deben ir precedidos del **\_ \_ identificador de grupo SC** (definido en el archivo Winsvc. h) para diferenciarlos de los nombres de servicio, ya que los servicios y los grupos de servicios comparten el mismo espacio de nombres. La dependencia de un grupo significa que este servicio se puede ejecutar si se está ejecutando al menos un miembro del grupo después de un intento de iniciar todos los miembros del grupo.

</dd> <dt>

*ServiceDependencies* \[ de\]
</dt> <dd>

Lista que contiene los nombres de los servicios que deben iniciarse antes de que se inicie este servicio. La matriz termina en **null**. Si el puntero es **null**, o apunta a una cadena vacía, el servicio no tiene dependencias. La dependencia de un servicio significa que este servicio solo se puede ejecutar si se está ejecutando el servicio del que depende.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores enumerados en la lista siguiente o un valor diferente para indicar un error.

<dl> <dt>

**Success**
</dt> <dd>

0

Se acepta la solicitud.

</dd> <dt>

**No compatible**
</dt> <dd>

1

No se admite la solicitud.

</dd> <dt>

**Acceso denegado**
</dt> <dd>

2

El usuario no tiene los privilegios de acceso necesarios.

</dd> <dt>

**Servicios dependientes en ejecución**
</dt> <dd>

3

No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.

</dd> <dt>

**Control de servicio no válido**
</dt> <dd>

4

El código de control solicitado no es válido o no es aceptable para el servicio.

</dd> <dt>

**El servicio no puede aceptar el control**
</dt> <dd>

5

El código de control solicitado no se puede enviar al servicio porque la propiedad [**State**](win32-baseservice.md) del objeto [**Win32 \_ BaseService**](win32-baseservice.md) es igual a 0, 1 o 2.

</dd> <dt>

**Servicio no activo**
</dt> <dd>

6

El servicio no se ha iniciado.

</dd> <dt>

**Tiempo de espera de solicitud de servicio**
</dt> <dd>

7

El servicio no responde rápidamente a la solicitud de inicio.

</dd> <dt>

**Error desconocido**
</dt> <dd>

8

Proceso interactivo.

</dd> <dt>

**Ruta de acceso no encontrada**
</dt> <dd>

9

No se encuentra la ruta de acceso al directorio del archivo ejecutable del servicio.

</dd> <dt>

**El servicio ya se está ejecutando**
</dt> <dd>

10

El servicio ya se está ejecutando.

</dd> <dt>

**Base de datos de servicio bloqueada**
</dt> <dd>

11

La base de datos para agregar un nuevo servicio está bloqueada.

</dd> <dt>

**Dependencia de servicio eliminada**
</dt> <dd>

12

Una dependencia para la que se basa este servicio se quita del sistema.

</dd> <dt>

**Error de dependencia de servicio**
</dt> <dd>

13

El servicio no encuentra el servicio necesario de un servicio dependiente.

</dd> <dt>

**Servicio deshabilitado**
</dt> <dd>

14

El servicio está deshabilitado del sistema.

</dd> <dt>

**Error de inicio de sesión de servicio**
</dt> <dd>

15

El servicio no tiene la autenticación correcta para ejecutarse en el sistema.

</dd> <dt>

**Servicio marcado para eliminación**
</dt> <dd>

16

Este servicio se está quitando del sistema.

</dd> <dt>

**Servicio sin subproceso**
</dt> <dd>

17

No hay ningún subproceso de ejecución para el servicio.

</dd> <dt>

**Estado dependencia circular**
</dt> <dd>

18

Hay dependencias circulares al iniciarse el servicio.

</dd> <dt>

**Estado nombre duplicado**
</dt> <dd>

19

Hay un servicio que se ejecuta con el mismo nombre.

</dd> <dt>

**Estado nombre no válido**
</dt> <dd>

20

Hay caracteres no válidos en el nombre del servicio.

</dd> <dt>

**Estado parámetro no válido**
</dt> <dd>

21

Se han pasado parámetros no válidos al servicio.

</dd> <dt>

**Estado cuenta de servicio no válida**
</dt> <dd>

22

La cuenta para la que se ejecuta este servicio no es válida o no tiene permisos para ejecutar el servicio.

</dd> <dt>

**El servicio de estado existe**
</dt> <dd>

23

El servicio existe en la base de datos de servicios disponibles del sistema.

</dd> <dt>

**Servicio ya pausado**
</dt> <dd>

24

El servicio se encuentra en pausa actualmente en el sistema.

</dd> <dt>

**Otros**
</dt> <dd>

25 4294967295

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para cambiar un servicio de una red a un sistema local, use los siguientes valores para los parámetros *StartName* y *StartPassword* :


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



Para cambiar un servicio de un sistema local a una red, use los siguientes valores para los parámetros *StartName* y *StartPassword* :


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

[**Win32 \_ BaseService**](win32-baseservice.md)
</dt> </dl>

 

