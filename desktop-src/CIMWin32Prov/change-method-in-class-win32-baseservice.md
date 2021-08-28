---
description: Modifica un objeto de servicio derivado de \_ BaseService win32.
ms.assetid: d5f4f472-e7d9-4664-9430-9c77034a5978
ms.tgt_platform: multiple
title: Cambio del método de Win32_BaseService clase (Mbnapi.h)
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
ms.openlocfilehash: 306f771df0e44cb11ec61631b2d6b51f11ccefac9a719776d3a483d5cc861133
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085835"
---
# <a name="change-method-of-the-win32_baseservice-class"></a>Cambio del método de la clase BaseService win32 \_

El **método de** clase CHANGE [WMI](/windows/desktop/WmiSdk/retrieving-a-class) modifica un objeto de servicio derivado de [**\_ BaseService de Win32.**](win32-baseservice.md) El [**parámetro \_ LoadOrderGroup de Win32**](win32-loadordergroup.md) representa un grupo de servicios del sistema que definen las dependencias de ejecución. Los servicios deben iniciarse en el orden especificado por el grupo de pedidos de carga, porque los servicios dependen entre sí. Estos servicios dependientes requieren servicios antecedentes para funcionar correctamente.

En este tema se usa Managed Object Format sintaxis MOF (MOF). Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

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

*DisplayName* \[ En\]
</dt> <dd>

Nombre para mostrar de un servicio. Esta cadena tiene una longitud máxima de 256 caracteres. El nombre se conserva en mayúsculas y minúsculas en el administrador de control de servicios. *Las comparaciones* de DisplayName siempre no tienen en cuenta las mayúsculas y minúsculas.

Restricciones: acepta el mismo valor que el *parámetro Name.*

Ejemplo: "Atdisk".

</dd> <dt>

*PathName* \[ En\]
</dt> <dd>

Ruta de acceso completa al archivo ejecutable que implementa un servicio.

Ejemplo: " \\ SystemRoot \\ System32 \\ drivers \\afd.sys".

</dd> <dt>

*ServiceType* \[ En\]
</dt> <dd>

Tipo de servicios proporcionados a los procesos que los llaman.

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>**Kernel Driver** (1)


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>**Controlador del sistema de** archivos (2)


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>**Adaptador** (4)


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>**Controlador recognizer** (8)


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>**Proceso propio** (16)


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>**Proceso de recurso** compartido (32)


</dt> <dd></dd> <dt>



 (256)


</dt> <dd>

Proceso interactivo

</dd> </dl> </dd> <dt>

*ErrorControl* \[ En\]
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

El sistema se reinicia con la última configuración buena.

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** (3)


</dt> <dd>

El sistema intenta reiniciarse con una configuración válida.

</dd> </dl> </dd> <dt>

*StartMode* \[ En\]
</dt> <dd>

Modo de inicio del Windows base.

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Inicio de arranque** ("Arranque")


</dt> <dd>

Controlador de dispositivo que inicia el cargador del sistema operativo.

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**Inicio del sistema** ("Sistema")


</dt> <dd>

Controlador de dispositivo iniciado por el proceso de inicialización del sistema operativo. Este valor solamente es válido para servicios de controladores.

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Inicio automático** ("Automático")


</dt> <dd>

Servicio que el administrador de control de servicios inicia automáticamente durante el inicio del sistema.

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Inicio de la demanda** ("Manual")


</dt> <dd>

Servicio que el administrador de control de servicios inicia cuando un proceso llama al [**método StartService.**](startservice-method-in-class-win32-baseservice.md)

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** ("Deshabilitado")


</dt> <dd>

Servicio que no se puede iniciar.

</dd> </dl> </dd> <dt>

*DesktopInteract* \[ En\]
</dt> <dd>

Si **es True,** el servicio puede crear o comunicarse con una ventana en el escritorio.

</dd> <dt>

*StartName* \[ En\]
</dt> <dd>

Nombre de cuenta en el que se ejecuta el servicio, que depende del tipo de servicio. El nombre de la cuenta puede tener el formato nombreDe DomainName \\ Username o . \\ nombre de usuario. Cuando se ejecuta, el proceso de servicio se registra mediante uno de los dos formularios anteriores. Si la cuenta pertenece al dominio integrado, . \\ Se puede especificar el nombre de usuario. Si se especifica una cadena vacía, el servicio se inicia sesión como la cuenta LocalSystem. Para los controladores de nivel de sistema o kernel, *StartName* contiene el nombre del objeto de controlador, por ejemplo, FileSystem Rdr o Driver Xns, que el sistema de entrada y salida \\ \\ \\ (E/S) usa para cargar el controlador de \\ dispositivo. Si se especifica **NULL,** el controlador se ejecuta con un nombre de objeto predeterminado que el sistema de E/S crea en función del nombre del servicio, por ejemplo, DWDOM \\ Admin.

También puede usar el formato de nombre principal de usuario (UPN) para especificar **startName**, por ejemplo, *Username@DomainName* .

</dd> <dt>

*StartPassword* \[ En\]
</dt> <dd>

Contraseña del nombre de cuenta que especifica el parámetro *StartName.* Especifique **NULL** cuando no cambie la contraseña. Especifique una cadena vacía si el servicio no tiene una contraseña.

> [!Note]  
> Al cambiar un servicio de sistema local a red o de red a sistema local, *StartPassword* debe ser una cadena vacía ("") y no **NULL.**

 

</dd> <dt>

*LoadOrderGroup* \[ En\]
</dt> <dd>

Nombre de grupo al que está asociado. Los grupos de pedidos de carga se encuentran en el registro del sistema y determinan la secuencia en la que se cargan los servicios en un sistema operativo. Si el puntero es **NULL** o apunta a una cadena vacía, el servicio no pertenece a un grupo. Las dependencias entre grupos deben aparecer en el *parámetro LoadOrderGroupDependencies.* Los servicios de la lista de grupos de ordenación de carga se inician primero, seguidos de los servicios de los grupos que no están en la lista de grupos de ordenación de carga, seguidos de los servicios que no pertenecen a un grupo. El registro del sistema tiene una lista de grupos de ordenación de carga ubicados en **HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **ServiceGroupOrder**.

</dd> <dt>

*LoadOrderGroupDependencies* \[ En\]
</dt> <dd>

Lista de grupos de ordenación de carga que deben iniciarse antes de que se inicie este servicio. La matriz está doblemente **terminada en null.** Si el puntero es **NULL** o si apunta a una cadena vacía, el servicio no tiene dependencias. Los nombres de grupo deben ir precedidos por el carácter **SC \_ GROUP \_ IDENTIFIER** (definido en el archivo Winsvc.h) para diferenciarlos de los nombres de servicio, ya que los servicios y los grupos de servicios comparten el mismo espacio de nombres. La dependencia de un grupo significa que este servicio se puede ejecutar si al menos un miembro del grupo se está ejecutando después de un intento de iniciar todos los miembros del grupo.

</dd> <dt>

*ServiceDependencies* \[ En\]
</dt> <dd>

Lista que contiene los nombres de los servicios que deben iniciarse antes de que se inicie este servicio. La matriz está doblemente **terminada en null.** Si el puntero es **NULL** o apunta a una cadena vacía, el servicio no tiene dependencias. La dependencia de un servicio significa que este servicio solo se puede ejecutar si el servicio del que depende se está ejecutando.

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

El código de control solicitado no se puede enviar al servicio porque la propiedad [**State**](win32-baseservice.md) del objeto [**\_ BaseService de Win32**](win32-baseservice.md) es igual a 0, 1 o 2.

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

No se encuentra la ruta de acceso del directorio al archivo ejecutable del servicio.

</dd> <dt>

**Servicio que ya se está ejecutando**
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

Se quita del sistema una dependencia en la que se basa este servicio.

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

**Dependencia circular de estado**
</dt> <dd>

18

Hay dependencias circulares al iniciarse el servicio.

</dd> <dt>

**Nombre duplicado de estado**
</dt> <dd>

19

Hay un servicio que se ejecuta con el mismo nombre.

</dd> <dt>

**Nombre no válido del estado**
</dt> <dd>

20

Hay caracteres no válidos en el nombre del servicio.

</dd> <dt>

**Parámetro Status Invalid**
</dt> <dd>

21

Se han pasado parámetros no válidos al servicio.

</dd> <dt>

**Cuenta de servicio de estado no válida**
</dt> <dd>

22

La cuenta en la que se va a ejecutar este servicio no es válida o no tiene los permisos para ejecutar el servicio.

</dd> <dt>

**El servicio de estado existe**
</dt> <dd>

23

El servicio existe en la base de datos de servicios disponibles del sistema.

</dd> <dt>

**Servicio ya en pausa**
</dt> <dd>

24

El servicio se encuentra en pausa actualmente en el sistema.

</dd> <dt>

**Otros**
</dt> <dd>

25 4294967295

</dd> </dl>

## <a name="remarks"></a>Comentarios

Para cambiar un servicio de una red a un sistema local, use los siguientes valores para los parámetros *StartName* *y StartPassword:*


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



Para cambiar un servicio de un sistema local a una red, use los siguientes valores para los parámetros *StartName* *y StartPassword:*


```C++
StartName = "NT AUTHORITY\NetworkService"
StartPassword = "" // - empty string, not NULL
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| Header<br/>                   | <dl> <dt>Mbnapi.h</dt> </dl>     |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**BaseService de Win32 \_**](win32-baseservice.md)
</dt> </dl>

 

