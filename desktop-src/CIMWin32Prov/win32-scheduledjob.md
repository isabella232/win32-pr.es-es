---
description: Representa un trabajo creado con el comando AT.
ms.assetid: 2fa69e3f-9a6c-4aa9-8a6c-ea28eb4342ca
ms.tgt_platform: multiple
title: Win32_ScheduledJob clase
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174330"
---
# <a name="win32_scheduledjob-class"></a>Clase ScheduledJob de Win32 \_

La **clase \_ WMI ScheduledJob de Win32** representa un trabajo creado con el comando  [](../wmisdk/retrieving-a-class.md)   **AT.**

> [!Note]  
> La **clase \_ ScheduledJob de Win32** no representa un trabajo creado con el Asistente para tareas programadas desde el Panel de control. No se puede cambiar una tarea creada por WMI en la interfaz de usuario tareas programadas. Para obtener más información, vea la sección Comentarios.

 

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

## <a name="members"></a>Members

La **clase \_ ScheduledJob de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ ScheduledJob de Win32** tiene estos métodos.



| Método                                                      | Descripción                                                                                                           |
|:------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**Crear**](create-method-in-class-win32-scheduledjob.md) | Método de clase que envía un trabajo al sistema operativo para su ejecución en una fecha y hora futuras especificadas.<br/> |
| [**Eliminar**](delete-method-in-class-win32-scheduledjob.md) | Método de clase que elimina un trabajo programado.<br/>                                                                 |



 

### <a name="properties"></a>Propiedades

La **clase \_ ScheduledJob de Win32** tiene estas propiedades.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Breve descripción textual del objeto.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Comando**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Comando Win32API \| Network Management Structures AT \| [**\_ INFO**](/windows/win32/api/lmat/ns-lmat-at_info) \| ")
</dt> </dl>

Nombre del comando, programa por lotes o archivo binario (y argumentos de línea de comandos) que usa el servicio de programación para invocar el trabajo.

Ejemplo: "**defrag** **/q/f**"

</dd> <dt>

**DaysOfMonth**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures AT \| [**\_ INFO**](/windows/win32/api/lmat/ns-lmat-at_info) \| **DaysOfMonth")**
</dt> </dl>

Días del mes en que el trabajo está programado para ejecutarse. Si un trabajo está programado para ejecutarse varios días del mes, estos valores se pueden unir en un or lógico. Por ejemplo, si un trabajo se va a ejecutar el 1 y el 16 de cada mes, el valor de la propiedad **DaysOfMonth** sería 1 O 32768.

<dt>

<span id="1"></span>

<span id="1"></span>**1** (1)


</dt> <dd>

Primera

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2** (2)


</dt> <dd>

Segundo

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

10th

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

14.

</dd> <dt>

<span id="15"></span>

<span id="15"></span>**15** (16384)


</dt> <dd>

15.

</dd> <dt>

<span id="16"></span>

<span id="16"></span>**16** (32768)


</dt> <dd>

16.

</dd> <dt>

<span id="17"></span>

<span id="17"></span>**17** (65536)


</dt> <dd>

17.

</dd> <dt>

<span id="18"></span>

<span id="18"></span>**18** (131072)


</dt> <dd>

18.

</dd> <dt>

<span id="19"></span>

<span id="19"></span>**19** (262144)


</dt> <dd>

Xix

</dd> <dt>

<span id="20"></span>

<span id="20"></span>**20** (524288)


</dt> <dd>

Xx

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

24.

</dd> <dt>

<span id="25"></span>

<span id="25"></span>**25** (16777216)


</dt> <dd>

25.

</dd> <dt>

<span id="26"></span>

<span id="26"></span>**26** (33554432)


</dt> <dd>

26.

</dd> <dt>

<span id="27"></span>

<span id="27"></span>**27** (67108864)


</dt> <dd>

27.

</dd> <dt>

<span id="28"></span>

<span id="28"></span>**28** (134217728)


</dt> <dd>

28.

</dd> <dt>

<span id="29"></span>

<span id="29"></span>**29** (268435456)


</dt> <dd>

29.

</dd> <dt>

<span id="30"></span>

<span id="30"></span>**30** (536870912)


</dt> <dd>

30.

</dd> <dt>

<span id="31"></span>

<span id="31"></span>**31** (1073741824)


</dt> <dd>

31.

</dd> </dl>

</dd> <dt>

**DaysOfWeek**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Estructuras de administración de red win32API \| AT \| [**\_ INFO**](/windows/win32/api/lmat/ns-lmat-at_info) \| **DaysOfWeek**")
</dt> </dl>

Días de la semana en los que se programa la ejecución de un trabajo. Si un trabajo está programado para ejecutarse varios días de la semana, los valores se pueden unir en un or lógico. Por ejemplo, si un trabajo está programado para ejecutarse los lunes, miércoles y viernes, el valor de la propiedad **DaysOfWeek** sería 1 O 4 O 16.

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

Calificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Descripción textual del objeto.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**ElapsedTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Período de tiempo durante el que se ha estado ejecutando el trabajo.

Esta propiedad se hereda del [**trabajo \_ cim**](cim-job.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Fecha de instalación")
</dt> </dl>

Indica cuándo se instaló el objeto. La falta de un valor no indica que el objeto no está instalado.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**InteractWithDesktop**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures AT \| [**\_ INFO**](/windows/win32/api/lmat/ns-lmat-at_info) \| **Flags** \| **JOB \_ NONINTERACTIVE")**
</dt> </dl>

El trabajo especificado es interactivo, lo que significa que un usuario puede proporcionar entradas a un trabajo programado mientras se está ejecutando.

</dd> <dt>

**JobId**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures AT \| [**\_ ENUM**](/windows/win32/api/lmat/ns-lmat-at_enum) \| **JobId")**
</dt> </dl>

Identificación del número del trabajo. Los métodos lo usan como identificador de un trabajo que se está programando en este equipo.

</dd> <dt>

**Estado del trabajo**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](../wmisdk/standard-qualifiers.md) ("JobStatus"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures AT \| [**\_ ENUM**](/windows/win32/api/lmat/ns-lmat-at_enum) \| **Flags** \| **JOB \_ EXEC \_ ERROR**")
</dt> </dl>

Estado de ejecución la última vez que se programó la ejecución de este trabajo.

<dt>

<span id="Success"></span><span id="success"></span><span id="SUCCESS"></span>

**Correcto** ("Correcto")


</dt> <dd></dd> <dt>

<span id="Failure"></span><span id="failure"></span><span id="FAILURE"></span>

**Error** ("Error")


</dt> <dd></dd> </dl>

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Nombre")
</dt> </dl>

Etiqueta por la que se conoce el objeto. Cuando se subclasifica, esta propiedad se puede invalidar para que sea una propiedad de clave.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Notificar**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Se notifica al usuario tras la finalización o el error del trabajo.

Esta propiedad se hereda del [**trabajo \_ cim**](cim-job.md).

</dd> <dt>

**Propietario**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Usuario que envió el trabajo.

Esta propiedad se hereda del [**trabajo \_ cim**](cim-job.md).

</dd> <dt>

**Prioridad**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Importancia de la ejecución de un trabajo.

Esta propiedad se hereda del [**trabajo \_ cim**](cim-job.md).

</dd> <dt>

**RunRepeatedly**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures AT \| [**\_ INFO**](/windows/win32/api/lmat/ns-lmat-at_info) \| **Flags** \| **JOB RUN \_ \_ PERIODICALLY")**
</dt> </dl>

El trabajo programado se ejecuta repetidamente en los días en que se programa el trabajo. Si **es False**, el trabajo se ejecuta una vez.

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](../wmisdk/standard-qualifiers.md) ("StartTime"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures AT \| [**\_ ENUM**](/windows/win32/api/lmat/ns-lmat-at_enum) \| **JobTime")**
</dt> </dl>

Hora UTC para ejecutar el trabajo, con el formato "AAAAMMDDHHMMSS. MMMMMM(+-)OOO", donde "YYYYMMDD" debe reemplazarse por " \* \* \* \* \* \* \* \* ". El reemplazo es necesario porque el servicio de programación solo permite que los trabajos se configuren para que se ejecuten una vez o que se ejecuten un día del mes o la semana. Un trabajo no se puede ejecutar en una fecha específica.

La sección "(+-)OOO" del valor de la propiedad **StartTime** es el sesgo actual para la traducción de la hora local. El sesgo es la diferencia entre la hora UTC y la hora local. Para calcular el sesgo de la zona horaria, multiplique el número de horas que la zona horaria está por delante o por detrás de la hora media de Greenwich (GMT) por 60 (use un número positivo para el número de horas si la zona horaria está por delante de GMT y un número negativo si la zona horaria está detrás de GMT). Agregue 60 adicionales al cálculo si la zona horaria usa el horario de verano. Por ejemplo, la zona horaria estándar del Pacífico está ocho horas por detrás de GMT, por lo que el sesgo es igual a -420 (-8 60 + 60) cuando el horario de verano está en uso y \* -480 (-8 60) cuando el horario de verano no está \* en uso. También puede determinar el valor del sesgo consultando la propiedad bias de la clase [**\_ TimeZone de Win32.**](win32-timezone.md)

Por ejemplo: \* \* \* \* \* \* \* \* "123000.000000-420" especifica 14.30 (2:30 p. m.) PST con el horario de verano en vigor.

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

Cadena que indica el estado actual del objeto. Se puede definir el estado operativo y no operativo. El estado operativo puede incluir "Ok", "Degraded" y "Pred Fail". "Error previo" indica que un elemento funciona correctamente, pero predice un error (por ejemplo, una unidad de disco duro habilitada para SMART).

El estado no operativo puede incluir "Error", "Starting", "Stopping" y "Service". "Servicio" se puede aplicar durante la resilvering de reflejo del disco, volver a cargar una lista de permisos de usuario u otro trabajo administrativo. No todo este trabajo está en línea, pero el elemento administrado no es "Correcto" ni está en uno de los demás estados.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

Los valores son los siguientes:

<dt>

<span id="OK"></span><span id="ok"></span>

**Ok** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Error** ("Error")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Degradado** ("Degradado")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unknown** ("Unknown")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Error de pred** ("error previo")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Starting** ("Starting")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Detención** ("Detención")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Servicio** ("Servicio")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Estresado** ("estresado")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ("NonRecover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Sin contacto** ("Sin contacto")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Comm perdido** ("Comm perdido")


</dt> <dd></dd> </dl>

</dd> <dt>

**TimeSubmitted**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Hora a la que se envió el trabajo.

Esta propiedad se hereda del trabajo [**\_ cim**](cim-job.md).

</dd> <dt>

**UntilTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Hora en la que el trabajo no es válido o debe detenerse.

Esta propiedad se hereda del trabajo [**\_ cim**](cim-job.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Cada trabajo programado en el servicio de programación se almacena de forma persistente (el programador puede iniciar un trabajo después de un reinicio) y se ejecuta a la hora y el día especificados de la semana o el mes. Si el equipo no está activo o si el servicio programado no se está ejecutando a la hora de trabajo especificada, el servicio de programación ejecuta el trabajo especificado al día siguiente a la hora especificada.

Los trabajos se programan según la hora universal coordinada (UTC) con desplazamiento de sesgo con respecto a la hora media de Greenwich (GMT), lo que significa que un trabajo se puede especificar mediante cualquier zona horaria. La **clase \_ ScheduledJob de Win32** devuelve la hora local con desplazamiento UTC al enumerar un objeto y se convierte a la hora local al crear nuevos trabajos. Por ejemplo, un trabajo especificado para ejecutarse en un equipo de Boston a las 10:30 p. m. La hora del lunes pst se programará para ejecutarse localmente a la 1:30 a. m. Martes EST.

> [!Note]  
> Un cliente debe tener en cuenta si el horario de verano está en funcionamiento o no en el equipo local y, si es así, restar un sesgo de 60 minutos del desplazamiento UTC.

 

La **clase \_ ScheduledJob de Win32** se deriva del [**trabajo CIM \_**](cim-job.md). Debe ser miembro del grupo de administradores para crear un trabajo programado con esta clase.

La **clase \_ ScheduledJob de Win32** usa internamente el protocolo AT, que está enlazado a desuso a partir de Windows 8 y Windows Server 2012. Como primer paso, el protocolo AT está deshabilitado de forma predeterminada. Si el protocolo está deshabilitado, por ejemplo, si se llama al método [**Create**](create-method-in-class-win32-scheduledjob.md) en un objeto **\_ ScheduledJob de Win32,** se producirá un error 0x8. Puede volver a activar el protocolo AT agregando la siguiente entrada del Registro:

``` syntax
Key: HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Schedule\Configuration 
Name: EnableAt 
Type: REG_DWORD
Value: 1
```

Es posible que tenga que reiniciar la máquina para que la configuración sea efectiva.

Dado **que Win32 \_ ScheduledJob** se basa en la API [**Win32 NetScheduleJobGetInfo,**](/windows/win32/api/lmat/nf-lmat-netschedulejobgetinfo) no puede usar esta clase junto con el Programador de tareas. Si desea usar Programador de tareas, use Programador de tareas API. Para obtener más información, vea la [Programador de tareas referencia](../taskschd/task-scheduler-reference.md).

## <a name="examples"></a>Ejemplos

El siguiente ejemplo de código de VBScript Notepad.exe ejecutar de forma interactiva a la 1:25 a la hora del equipo local cada miércoles.


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
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Trabajo \_ cim**](cim-job.md)
</dt> <dt>

[Clases de sistema operativo](./operating-system-classes.md)
</dt> <dt>

[Tareas wmi: tareas programadas](../wmisdk/wmi-tasks--scheduled-tasks.md)
</dt> </dl>

 

 
