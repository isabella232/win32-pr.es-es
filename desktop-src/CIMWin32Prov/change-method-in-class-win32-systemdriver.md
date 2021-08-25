---
description: Modifica un servicio \_ SystemDriver de Win32.
ms.assetid: 61ee3297-2a66-466e-bdba-74d683f3ea70
ms.tgt_platform: multiple
title: Método change de la Win32_SystemDriver (Mbnapi.h)
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
ms.openlocfilehash: 96ff327e84d3a5b6c66011506c162810f0fcc91d0cafe4053266aa8928f6e5a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119925115"
---
# <a name="change-method-of-the-win32_systemdriver-class"></a>Cambio del método de la clase SystemDriver de Win32 \_

El **método de** [clase Change WMI](/windows/desktop/WmiSdk/retrieving-a-class) modifica un servicio [**\_ SystemDriver de Win32.**](win32-systemdriver.md) El [**parámetro \_ LoadOrderGroup de Win32**](win32-loadordergroup.md) representa una agrupación de servicios del sistema que definen las dependencias de ejecución. Los servicios deben iniciarse en el orden especificado por el grupo de pedidos de carga, ya que los servicios dependen entre sí. Estos servicios dependientes requieren la presencia de los servicios antecedentes para funcionar correctamente.

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

Nombre para mostrar del servicio. Esta cadena tiene una longitud máxima de 256 caracteres. El nombre se conserva entre mayúsculas y minúsculas en el administrador de control de servicios. *Las comparaciones* de DisplayName siempre no tienen en cuenta las mayúsculas y minúsculas.

Restricciones: acepta el mismo valor que el *parámetro Name.*

Ejemplo: "Atdisk"

</dd> <dt>

*PathName* \[ En\]
</dt> <dd>

Ruta de acceso completa al archivo ejecutable que implementa el servicio.

Ejemplo: *\\ Controladores SystemRoot \\ System32 \\ \\afd.sys*

</dd> <dt>

*ServiceType* \[ En\]
</dt> <dd>

Tipo de servicios proporcionados a los procesos que los llaman.

<dt>

1 (0x1)
</dt> <dd>

Controlador kernel

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

Controlador de Recognizer

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

Gravedad del error si este servicio no se puede iniciar durante el inicio. El valor indica la acción realizada por el programa de inicio si se produce un error. El sistema registra todos los errores.

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

Modo de inicio del servicio Windows base.

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Inicio de arranque**


</dt> <dd>

Controlador de dispositivo iniciado por el cargador del sistema operativo.

</dd> <dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Inicio de arranque**


</dt> <dd>

Controlador de dispositivo que inicia el cargador del sistema operativo.

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**Inicio del sistema**


</dt> <dd>

Controlador de dispositivo iniciado por el proceso de inicialización del sistema operativo. Este valor solamente es válido para servicios de controladores.

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Inicio automático**


</dt> <dd>

Servicio que el administrador de control de servicios inicia automáticamente durante el inicio del sistema.

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Inicio de la demanda**


</dt> <dd>

Servicio que el administrador de control de servicios inicia cuando un proceso llama al [**método StartService.**](startservice-method-in-class-win32-systemdriver.md)

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado**


</dt> <dd>

Servicio que no se puede iniciar.

</dd> </dl> </dd> <dt>

*DesktopInteract* \[ En\]
</dt> <dd>

Valor que, si es **True,** el servicio puede crear o comunicarse con las ventanas del escritorio.

</dd> <dt>

*StartName* \[ En\]
</dt> <dd>

Nombre de cuenta en el que se ejecuta el servicio. Dependiendo del tipo de servicio, el nombre de cuenta puede tener el formato nombreDeServidor de dominio \\ o . \\ nombre de usuario. Cuando se ejecuta, el proceso de servicio se registra mediante uno de estos dos formularios. Si la cuenta pertenece al dominio integrado, . \\ Se puede especificar el nombre de usuario. Si se especifica una cadena vacía, el servicio se inicia sesión como la cuenta LocalSystem. Para los controladores de nivel de sistema o kernel, *StartName* contiene el nombre del objeto de controlador, por ejemplo, FileSystem Rdr o Driver Xns, que el sistema de entrada y salida \\ \\ \\ (E/S) usa para cargar el controlador de \\ dispositivo. Si se especifica **NULL,** el controlador se ejecuta con un nombre de objeto predeterminado que el sistema de E/S crea en función del nombre del servicio, por ejemplo, DWDOM \\ Admin.

También puede usar el formato de nombre principal de usuario (UPN) para especificar **startName**, por ejemplo, *Username@DomainName* .

</dd> <dt>

*StartPassword* \[ En\]
</dt> <dd>

Contraseña del nombre de cuenta especificado por el *parámetro StartName.* Especifique **NULL** si no va a cambiar la contraseña. Especifique una cadena vacía si el servicio no tiene contraseña.

> [!Note]  
> Al cambiar un servicio de un sistema local a una red o de una red a un sistema local, *StartPassword* debe ser una cadena vacía ("") y no **NULL.**

 

</dd> <dt>

*LoadOrderGroup* \[ En\]
</dt> <dd>

Nombre del grupo al que está asociado. Los grupos de pedidos de carga se encuentran en el registro del sistema y determinan la secuencia en la que se cargan los servicios en el sistema operativo. Si el puntero es **NULL** o si apunta a una cadena vacía, el servicio no pertenece a un grupo. Las dependencias entre grupos deben aparecer en el *parámetro LoadOrderGroupDependencies.* Los servicios de la lista de grupos de ordenación de carga se inician primero, seguidos de los servicios de los grupos que no están en la lista de grupos de ordenación de carga, seguidos de los servicios que no pertenecen a un grupo. El registro del sistema tiene una lista de grupos de ordenación de carga ubicados en:

**HKEY \_ Local \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **ServiceGroupOrder**

</dd> <dt>

*LoadOrderGroupDependencies* \[ En\]
</dt> <dd>

Lista de grupos de ordenación de carga que deben iniciarse antes de que se inicie este servicio. La matriz está doblemente **terminada en null.** Si el puntero es **NULL** o si apunta a una cadena vacía, el servicio no tiene dependencias. Los nombres de grupo deben ir precedidos por el carácter **SC \_ GROUP \_ IDENTIFIER** (definido en el archivo WinSvc.h) para diferenciarlos de los nombres de servicio, ya que los servicios y los grupos de servicios comparten el mismo espacio de nombres. La dependencia de un grupo significa que este servicio se puede ejecutar si al menos un miembro del grupo se está ejecutando después de un intento de iniciar todos los miembros del grupo.

</dd> <dt>

*ServiceDependencies* \[ En\]
</dt> <dd>

Lista que contiene los nombres de los servicios que deben iniciarse antes de que se inicie este servicio. La matriz está doblemente **terminada en null.** Si el puntero es **NULL** o si apunta a una cadena vacía, el servicio no tiene dependencias. La dependencia de un servicio significa que este servicio solo se puede ejecutar si el servicio del que depende se está ejecutando.

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

**El servicio no puede aceptar el control** (5)
</dt> <dt>

**Servicio no activo** (6)
</dt> <dt>

**Tiempo de espera de solicitud de** servicio (7)
</dt> <dt>

**Error desconocido** (8)
</dt> <dt>

**Ruta de acceso no encontrada** (9)
</dt> <dt>

**Servicio ya en ejecución** (10)
</dt> <dt>

**Base de datos de servicio bloqueada** (11)
</dt> <dt>

**Dependencia de servicio eliminada** (12)
</dt> <dt>

**Error de dependencia de** servicio (13)
</dt> <dt>

**Servicio deshabilitado** (14)
</dt> <dt>

**Error de inicio de sesión de** servicio (15)
</dt> <dt>

**Servicio marcado para eliminación** (16)
</dt> <dt>

**Servicio sin subproceso** (17)
</dt> <dt>

**Dependencia circular de** estado (18)
</dt> <dt>

**Nombre duplicado de estado** (19)
</dt> <dt>

**Nombre no válido del estado** (20)
</dt> <dt>

**Parámetro Status Invalid** (21)
</dt> <dt>

**Cuenta de servicio de estado no válida** (22)
</dt> <dt>

**El servicio de estado existe** (23)
</dt> <dt>

**Servicio ya en pausa** (24)
</dt> <dt>

**Otros** (25 4294967295)
</dt> </dl>

## <a name="remarks"></a>Comentarios

Para cambiar un servicio de un servicio de red al sistema local, use los valores siguientes para los parámetros *StartName* *y StartPassword:*


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



Para cambiar un servicio de un servicio de sistema local a un servicio de red, use los valores siguientes para los parámetros *StartName* *y StartPassword:*


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

[**Win32 \_ SystemDriver**](win32-systemdriver.md)
</dt> </dl>

 

