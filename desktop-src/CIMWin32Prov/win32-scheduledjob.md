---
description: Representa un trabajo creado con el comando AT.
ms.assetid: 2fa69e3f-9a6c-4aa9-8a6c-ea28eb4342ca
ms.tgt_platform: multiple
title: Win32_ScheduledJob (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ScheduledJob
- Win32_ScheduledJob.Caption
- Win32_ScheduledJob.Description
- Win32_ScheduledJob.InstallDate
- Win32_ScheduledJob.Name
- Win32_ScheduledJob.Status
- Win32_ScheduledJob.ElapsedTime
- Win32_ScheduledJob.Notify
- Win32_ScheduledJob.Owner
- Win32_ScheduledJob.Priority
- Win32_ScheduledJob.TimeSubmitted
- Win32_ScheduledJob.UntilTime
- Win32_ScheduledJob.Command
- Win32_ScheduledJob.DaysOfMonth
- Win32_ScheduledJob.DaysOfWeek
- Win32_ScheduledJob.InteractWithDesktop
- Win32_ScheduledJob.JobId
- Win32_ScheduledJob.JobStatus
- Win32_ScheduledJob.RunRepeatedly
- Win32_ScheduledJob.StartTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 50162221e7ca18e07e3599deca2dba67b18ba708
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080125"
---
# <a name="win32_scheduledjob-class"></a>\_Clase Win32 ScheduledJob

La  [clase WMI](../wmisdk/retrieving-a-class.md) **\_ ScheduledJob de Win32**   representa un trabajo creado con el comando **at** .

> [!Note]  
> La **clase \_ ScheduledJob de Win32** no representa un trabajo creado con el Asistente para tareas programadas desde el panel de control. No se puede cambiar una tarea creada por WMI en la interfaz de usuario de tareas programadas. Para obtener más información, vea la sección Comentarios.

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4E0-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("Delete"), AMENDMENT]
class Win32_ScheduledJob : CIM_Job
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  datetime ElapsedTime;
  string   Notify;
  string   Owner;
  uint32   Priority;
  datetime TimeSubmitted;
  datetime UntilTime;
  string   Command;
  uint32   DaysOfMonth;
  uint32   DaysOfWeek;
  boolean  InteractWithDesktop;
  uint32   JobId;
  string   JobStatus;
  boolean  RunRepeatedly;
  datetime StartTime;
};
```

## <a name="members"></a>Miembros

La **clase \_ ScheduledJob de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **Win32 \_ ScheduledJob** tiene estos métodos.



| Método                                                      | Descripción                                                                                                           |
|:------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**A**](create-method-in-class-win32-scheduledjob.md) | Método de clase que envía un trabajo al sistema operativo para su ejecución en una fecha y hora futuras especificadas.<br/> |
| [**Elimínelos**](delete-method-in-class-win32-scheduledjob.md) | Método de clase que elimina un trabajo programado.<br/>                                                                 |



 

### <a name="properties"></a>Propiedades

La **clase \_ ScheduledJob de Win32** tiene estas propiedades.

<dl> <dt>

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

**Comando**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| \| [**de administración de red en la \_ información**](/windows/win32/api/lmat/ns-lmat-at_info) \| ")
</dt> </dl>

Nombre del comando, programa por lotes o archivo binario (y argumentos de la línea de comandos) que el servicio de programación utiliza para invocar el trabajo.

Ejemplo: "**Defrag** **/q/f**"

</dd> <dt>

**DaysOfMonth**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**at \_ info**](/windows/win32/api/lmat/ns-lmat-at_info) \| **DaysOfMonth**")
</dt> </dl>

Días del mes en que el trabajo está programado para ejecutarse. Si un trabajo está programado para ejecutarse en varios días del mes, estos valores se pueden combinar en un operador lógico OR. Por ejemplo, si un trabajo se va a ejecutar el 1 y el 16 de cada mes, el valor de la propiedad **DaysOfMonth** sería 1 o 32768.

<dt>

<span id="1"></span>

<span id="1"></span>**1** (1)


</dt> <dd>

1a

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2** (2)


</dt> <dd>

secundaria

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3** (4)


</dt> <dd>

3rd (tercero)

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4** (8)


</dt> <dd>

4.º

</dd> <dt>

<span id="5"></span>

<span id="5"></span>**5** (16)


</dt> <dd>

5.º

</dd> <dt>

<span id="6"></span>

<span id="6"></span>**6** (32)


</dt> <dd>

6.º

</dd> <dt>

<span id="7"></span>

<span id="7"></span>**7** (64)


</dt> <dd>

7.º

</dd> <dt>

<span id="8"></span>

<span id="8"></span>**8** (128)


</dt> <dd>

8.º

</dd> <dt>

<span id="9"></span>

<span id="9"></span>**9** (256)


</dt> <dd>

9.º

</dd> <dt>

<span id="10"></span>

<span id="10"></span>**10** (512)


</dt> <dd>

10

</dd> <dt>

<span id="11"></span>

<span id="11"></span>**11** (1024)


</dt> <dd>

11°

</dd> <dt>

<span id="12"></span>

<span id="12"></span>**12** (2048)


</dt> <dd>

12°

</dd> <dt>

<span id="13"></span>

<span id="13"></span>**13** (4096)


</dt> <dd>

13°

</dd> <dt>

<span id="14"></span>

<span id="14"></span>**14** (8192)


</dt> <dd>

14

</dd> <dt>

<span id="15"></span>

<span id="15"></span>**15** (16384)


</dt> <dd>

día

</dd> <dt>

<span id="16"></span>

<span id="16"></span>**16** (32768)


</dt> <dd>

16

</dd> <dt>

<span id="17"></span>

<span id="17"></span>**17** (65536)


</dt> <dd>

17

</dd> <dt>

<span id="18"></span>

<span id="18"></span>**18** (131072)


</dt> <dd>

18

</dd> <dt>

<span id="19"></span>

<span id="19"></span>**19** (262144)


</dt> <dd>

19

</dd> <dt>

<span id="20"></span>

<span id="20"></span>**20** (524288)


</dt> <dd>

20

</dd> <dt>

<span id="21"></span>

<span id="21"></span>**21** (1048576)


</dt> <dd>

21°

</dd> <dt>

<span id="22"></span>

<span id="22"></span>**22** (2097152)


</dt> <dd>

22°

</dd> <dt>

<span id="23"></span>

<span id="23"></span>**23** (4194304)


</dt> <dd>

23°

</dd> <dt>

<span id="24"></span>

<span id="24"></span>**24** (8388608)


</dt> <dd>

24

</dd> <dt>

<span id="25"></span>

<span id="25"></span>**25** (16777216)


</dt> <dd>

25

</dd> <dt>

<span id="26"></span>

<span id="26"></span>**26** (33554432)


</dt> <dd>

26

</dd> <dt>

<span id="27"></span>

<span id="27"></span>**27** (67108864)


</dt> <dd>

27

</dd> <dt>

<span id="28"></span>

<span id="28"></span>**28** (134217728)


</dt> <dd>

28

</dd> <dt>

<span id="29"></span>

<span id="29"></span>**29** (268435456)


</dt> <dd>

29

</dd> <dt>

<span id="30"></span>

<span id="30"></span>**30** (536870912)


</dt> <dd>

semestre

</dd> <dt>

<span id="31"></span>

<span id="31"></span>**31** (1073741824)


</dt> <dd>

día

</dd> </dl>

</dd> <dt>

**DaysOfWeek**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**at \_ info**](/windows/win32/api/lmat/ns-lmat-at_info) \| **DaysOfWeek**")
</dt> </dl>

Días de la semana en los que está programada la ejecución de un trabajo. Si un trabajo está programado para ejecutarse en varios días de la semana, los valores se pueden combinar en un operador lógico OR. Por ejemplo, si un trabajo está programado para ejecutarse los lunes, miércoles y viernes, el valor de la propiedad **DaysOfWeek** sería 1 o 4 o 16.

<dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

**Lunes** (1)


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

**Martes** (2)


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

**Miércoles** (4)


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

**Jueves** (8)


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

**Viernes** (16)


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

**Sábado** (32)


</dt> <dd></dd> <dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

**Domingo** (64)


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

**ElapsedTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Período de tiempo durante el que se ha estado ejecutando el trabajo.

Esta propiedad se hereda del [**\_ trabajo CIM**](cim-job.md).

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

**InteractWithDesktop**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**at \_ info**](/windows/win32/api/lmat/ns-lmat-at_info) \| **Flags** no \| **\_ Interactive**")
</dt> </dl>

El trabajo especificado es interactivo, lo que significa que un usuario puede proporcionar la entrada a un trabajo programado mientras se está ejecutando.

</dd> <dt>

**JobId**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**at \_ enum**](/windows/win32/api/lmat/ns-lmat-at_enum) \| **JobID**")
</dt> </dl>

Número de identificación del trabajo. Los métodos los usan como identificador de un trabajo programado en este equipo.

</dd> <dt>

**Estado del trabajo**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](../wmisdk/standard-qualifiers.md) ("JobStatus"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| estructuras de administración \| [**de red en las marcas de \_ enumeración**](/windows/win32/api/lmat/ns-lmat-at_enum) \|  \| **\_ \_ error de trabajo exec**")
</dt> </dl>

Estado de la ejecución la última vez que se programó la ejecución de este trabajo.

<dt>

<span id="Success"></span><span id="success"></span><span id="SUCCESS"></span>

**Correcto** ("correcto")


</dt> <dd></dd> <dt>

<span id="Failure"></span><span id="failure"></span><span id="FAILURE"></span>

**Error** ("error")


</dt> <dd></dd> </dl>

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Name")
</dt> </dl>

Etiqueta por la que se conoce el objeto. Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**Notificar**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Se notifica al usuario sobre la finalización o el error del trabajo.

Esta propiedad se hereda del [**\_ trabajo CIM**](cim-job.md).

</dd> <dt>

**Propietario**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Usuario que envió el trabajo.

Esta propiedad se hereda del [**\_ trabajo CIM**](cim-job.md).

</dd> <dt>

**Prioridad**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Importancia de la ejecución de un trabajo.

Esta propiedad se hereda del [**\_ trabajo CIM**](cim-job.md).

</dd> <dt>

**RunRepeatedly**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| \| de estructuras de administración de red en el trabajo marcas [**de \_ información**](/windows/win32/api/lmat/ns-lmat-at_info)se \|  \| **\_ ejecutan \_ periódicamente**")
</dt> </dl>

El trabajo programado se ejecuta repetidamente en los días en los que está programado el trabajo. Si es **false**, el trabajo se ejecuta una vez.

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](../wmisdk/standard-qualifiers.md) ("startTime"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**at \_ enum**](/windows/win32/api/lmat/ns-lmat-at_enum) \| **JobTime**")
</dt> </dl>

Hora UTC para ejecutar el trabajo, con el formato "AAAAMMDDHHMMSS. MMMMMM (+-) OOO ", donde" AAAAMMDD "debe reemplazarse por" \* \* \* \* \* \* \* \* ". El reemplazo es necesario porque el servicio de programación solo permite configurar los trabajos para que se ejecuten una vez, o se ejecuten en un día del mes o de la semana. No se puede ejecutar un trabajo en una fecha concreta.

La sección "(+-) OOO" del valor de la propiedad **startTime** es la diferencia actual de la conversión de hora local. La diferencia es la diferencia entre la hora UTC y la hora local. Para calcular la diferencia de la zona horaria, multiplique el número de horas que la zona horaria está por encima o por detrás de la hora del meridiano de Greenwich (GMT) en 60 (use un número positivo para el número de horas si la zona horaria está por detrás de GMT y un número negativo si la zona horaria está tras la hora GMT). Agregue un 60 adicional al cálculo si la zona horaria usa el horario de verano. Por ejemplo, la zona horaria estándar del Pacífico es de ocho horas tras la hora GMT, por lo que la diferencia es igual a-420 (-8 \* 60 + 60) cuando el horario de verano está en uso y-480 (-8 \* 60) cuando el horario de verano no está en uso. También puede determinar el valor de la diferencia consultando la propiedad bias de la clase [**\_ TimeZone de Win32**](win32-timezone.md) .

Por ejemplo: " \* \* \* \* \* \* \* \* 123000.000000-420" especifica 14,30 (2:30 P.M.) PST con horario de verano en vigor.

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

**TimeSubmitted**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Hora a la que se envió el trabajo.

Esta propiedad se hereda del [**\_ trabajo CIM**](cim-job.md).

</dd> <dt>

**UntilTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Hora en la que el trabajo no es válido o debe detenerse.

Esta propiedad se hereda del [**\_ trabajo CIM**](cim-job.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Cada trabajo programado en el servicio de programación se almacena de forma persistente (el programador puede iniciar un trabajo después de un reinicio) y se ejecuta a la hora especificada y al día de la semana o mes. Si el equipo no está activo o si el servicio programado no se está ejecutando en el tiempo de trabajo especificado, el servicio de programación ejecuta el trabajo especificado el día siguiente a la hora especificada.

Los trabajos se programan de acuerdo con la hora universal coordinada (UTC) con el desplazamiento de diferencia de la hora del meridiano de Greenwich (GMT), lo que significa que se puede especificar un trabajo mediante cualquier zona horaria. La **clase \_ ScheduledJob de Win32** devuelve la hora local con el desplazamiento de UTC al enumerar un objeto y se convierte en la hora local al crear nuevos trabajos. Por ejemplo, un trabajo especificado para ejecutarse en un equipo de Boston a las 10:30 P.M. La hora del lunes PST se programará para ejecutarse localmente a las 1:30 A.M. Martes EST.

> [!Note]  
> Un cliente debe tener en cuenta si el horario de verano está en funcionamiento en el equipo local, y si es así, reste una diferencia de 60 minutos a partir del desplazamiento de UTC.

 

La **clase \_ ScheduledJob de Win32** se deriva [**del \_ trabajo CIM**](cim-job.md). Debe ser miembro del grupo administradores para crear un trabajo programado mediante esta clase.

La **clase \_ ScheduledJob de Win32** usa internamente el protocolo at, que está enlazado a la degradación a partir de Windows 8 y Windows Server 2012. Como primer paso, el protocolo AT está deshabilitado de forma predeterminada. Si se deshabilita el protocolo, por ejemplo, al llamar al método [**Create**](create-method-in-class-win32-scheduledjob.md) en un objeto **\_ ScheduledJob de Win32** se producirá un error 0x8. Puede volver a activar el protocolo AT si agrega la siguiente entrada del registro:

``` syntax
Key: HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Schedule\Configuration 
Name: EnableAt 
Type: REG_DWORD
Value: 1
```

Es posible que tenga que reiniciar el equipo para que la configuración sea efectiva.

Dado que **Win32 \_ ScheduledJob** se basa en la API de Win32 [**NetScheduleJobGetInfo**](/windows/win32/api/lmat/nf-lmat-netschedulejobgetinfo) , no puede usar esta clase junto con el programador de tareas. Si desea usar Programador de tareas, use la API de Programador de tareas. Para obtener más información, consulte la [referencia de programador de tareas](../taskschd/task-scheduler-reference.md).

## <a name="examples"></a>Ejemplos

El siguiente ejemplo de código de VBScript programa Notepad.exe para que se ejecute de forma interactiva en 1:25 por la hora del equipo local cada miércoles.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set objNewJob = objWMIService.Get("Win32_ScheduledJob")
errJobCreated = objNewJob.Create("Notepad.exe", "********012500.000000-420", True , 4, , True, JobId) 
If errJobCreated <> 0 Then
Wscript.Echo "Error on task creation"
Else
Wscript.Echo "Task created"
End If
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

[**Trabajo de CIM \_**](cim-job.md)
</dt> <dt>

[Clases de sistema operativo](./operating-system-classes.md)
</dt> <dt>

[Tareas de WMI: tareas programadas](../wmisdk/wmi-tasks--scheduled-tasks.md)
</dt> </dl>

 

 
