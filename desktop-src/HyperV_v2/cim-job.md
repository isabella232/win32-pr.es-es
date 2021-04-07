---
description: Un elemento lógico que representa una unidad de trabajo que se va a ejecutar, como un script o un trabajo de impresión. Un trabajo es distinto de un proceso porque un trabajo se puede programar o poner en cola, y su ejecución no se limita a un solo sistema.
ms.assetid: 35e35c3f-617b-429b-b68f-fa0c0c330e92
title: CIM_Job (clase, administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Job
- CIM_Job.JobStatus
- CIM_Job.TimeSubmitted
- CIM_Job.ScheduledStartTime
- CIM_Job.StartTime
- CIM_Job.ElapsedTime
- CIM_Job.JobRunTimes
- CIM_Job.RunMonth
- CIM_Job.RunDay
- CIM_Job.RunDayOfWeek
- CIM_Job.RunStartInterval
- CIM_Job.LocalOrUtcTime
- CIM_Job.UntilTime
- CIM_Job.Notify
- CIM_Job.Owner
- CIM_Job.Priority
- CIM_Job.PercentComplete
- CIM_Job.DeleteOnCompletion
- CIM_Job.ErrorCode
- CIM_Job.ErrorDescription
- CIM_Job.RecoveryAction
- CIM_Job.OtherRecoveryAction
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6b59a162d36ee677ad00c8cc574282f970bc1d80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002490"
---
# <a name="cim_job-class-hyper-v-management"></a>CIM_Job (clase, administración de Hyper-V)

Un elemento lógico que representa una unidad de trabajo que se va a ejecutar, como un script o un trabajo de impresión. Un trabajo es distinto de un proceso porque un trabajo se puede programar o poner en cola, y su ejecución no se limita a un solo sistema.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_Job : CIM_LogicalElement
{
  string   JobStatus;
  datetime TimeSubmitted;
  datetime ScheduledStartTime;
  datetime StartTime;
  datetime ElapsedTime;
  uint32   JobRunTimes = 1;
  uint8    RunMonth;
  sint8    RunDay;
  sint8    RunDayOfWeek;
  datetime RunStartInterval;
  uint16   LocalOrUtcTime;
  datetime UntilTime;
  string   Notify;
  string   Owner;
  uint32   Priority;
  uint16   PercentComplete;
  boolean  DeleteOnCompletion;
  uint16   ErrorCode;
  string   ErrorDescription;
  uint16   RecoveryAction;
  string   OtherRecoveryAction;
};
```

## <a name="members"></a>Miembros

La clase de **\_ trabajo CIM** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase de **\_ trabajo CIM** tiene estos métodos.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Método</th>
<th style="text-align: left;">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="cim-job-killjob.md"><strong>KillJob</strong></a></td>
<td style="text-align: left;">Este método es desusado. En su lugar, use el método <strong>RequestStateChange</strong> .<br/>
<blockquote>
[!Note]<br />
Descripción desusada: cierra un trabajo.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a>Propiedades

La clase de **\_ trabajo CIM** tiene estas propiedades.

<dl> <dt>

**DeleteOnCompletion**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

**True** para eliminar el trabajo tras su finalización; en caso contrario, **false**.

> [!Note]  
> Esta propiedad no eliminará los trabajos que se completen antes de que esta propiedad se establezca en **true**.

 

</dd> <dt>

**ElapsedTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La duración de la ejecución del trabajo.

</dd> <dt>

**ErrorCode**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ trabajo de CIM**.**ErrorDescription**")
</dt> </dl>

Código de error específico del proveedor que captura la información de procesamiento de los trabajos periódicos. El valor debe establecerse en cero si el trabajo se completó sin errores.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ trabajo de CIM**.**ErrorCode**")
</dt> </dl>

Una cadena de forma libre que contiene una descripción del código de error correspondiente en la propiedad **ErrorCode** .

</dd> <dt>

**JobRunTimes**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Número de veces que se va a ejecutar el trabajo.

</dd> <dt>

**Estado del trabajo**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**el \_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).**OperationalStatus**")
</dt> </dl>

Cadena de forma libre que representa el estado del trabajo.

</dd> <dt>

**LocalOrUtcTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Indica si las horas de las propiedades **RunStartInterval** y **UntilTime** representan horas locales o horas UTC.

<dt>

<span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>

**Hora local** (1)


</dt> <dd></dd> <dt>

<span id="UTC_Time"></span><span id="utc_time"></span><span id="UTC_TIME"></span>

**Hora UTC** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**Notificar**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

El usuario al que se notificará cuando un trabajo se complete o se produzca un error.

</dd> <dt>

**OtherRecoveryAction**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ trabajo de CIM**.**RecoveryAction**")
</dt> </dl>

Una cadena que describe la acción de recuperación cuando la propiedad **RecoveryAction** es **otra** ("1").

</dd> <dt>

**Propietario**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OwningJobElement**](cim-owningjobelement.md).")
</dt> </dl>

El usuario que envió el trabajo, o el nombre de servicio o método que solicitó el trabajo.

</dd> <dt>

**PercentComplete**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("Percent"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (101), **punitivo** ("Percent")
</dt> </dl>

Porcentaje del trabajo que se ha completado.

> [!Note]  
> El valor "101" no está definido y no se permitirá en la siguiente revisión principal de la especificación.

 

</dd> <dt>

**Prioridad**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Importancia del trabajo. Cuanto menor sea el número, mayor será la prioridad.

</dd> <dt>

**RecoveryAction**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ trabajo de CIM**.**OtherRecoveryAction**")
</dt> </dl>

Describe la acción de recuperación que se realizará cuando se produzca un error en un trabajo de ejecución.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)


</dt> <dd>

Se desconoce el modo en que se realiza la acción de recuperación.

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)


</dt> <dd>

La acción de recuperación se especificará en la propiedad **OtherRecoveryAction** .

</dd> <dt>

<span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>

<span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**No continuar** (2)


</dt> <dd>

Detenga la ejecución del trabajo y actualice su estado correctamente.

</dd> <dt>

<span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>

<span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continuar con el trabajo siguiente** (3)


</dt> <dd>

Continúe con el siguiente trabajo de la cola.

</dd> <dt>

<span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>

<span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Volver a ejecutar el trabajo** (4)


</dt> <dd>

Se debe volver a ejecutar el trabajo.

</dd> <dt>

<span id="Run_Recovery_Job"></span><span id="run_recovery_job"></span><span id="RUN_RECOVERY_JOB"></span>

<span id="Run_Recovery_Job"></span><span id="run_recovery_job"></span><span id="RUN_RECOVERY_JOB"></span>**Ejecutar trabajo de recuperación** (5)


</dt> <dd>

Ejecute el trabajo asociado mediante la relación **RecoveryJob** . Tenga en cuenta que el trabajo de recuperación debe estar ya en la cola desde la que se ejecutará.

</dd> </dl>

</dd> <dt>

**RunDay**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint8**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (-31), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (31), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ trabajo de CIM**.**RunMonth**","**\_ trabajo de CIM**.**RunDayOfWeek**","**\_ trabajo de CIM**.**RunStartInterval**")
</dt> </dl>

Entero que se usa junto con la propiedad **RunDayOfWeek** para indicar el día en el que se procesa el trabajo; o bien, si **RunDayOfWeek** se establece en cero, **RunDay** indica el día del mes en el que se procesa el trabajo. Si **RunDay** es un entero negativo, especifica un día relativo al final del mes, o bien, si **RunDay** es un entero positivo, especifica un día relativo al comienzo del mes.

</dd> <dt>

**RunDayOfWeek**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint8**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ trabajo de CIM**.**RunMonth**","**\_ trabajo de CIM**.**RunDay**","**\_ trabajo de CIM**.**RunStartInterval**")
</dt> </dl>

Entero que se usa junto con la propiedad **RunDay** para indicar el día en el que se procesa el trabajo; o bien, si **RunDayOfWeek** se establece en cero, **RunDay** indica el día del mes en el que se procesa el trabajo.

<dt>

<span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>

**-Sábado** (-7)


</dt> <dd></dd> <dt>

<span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>

**-Viernes** (-6)


</dt> <dd></dd> <dt>

<span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>

**-Jueves** (-5)


</dt> <dd></dd> <dt>

<span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>

**-Miércoles** (-4)


</dt> <dd></dd> <dt>

<span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>

**-Martes** (-3)


</dt> <dd></dd> <dt>

<span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>

**-Lunes** (-2)


</dt> <dd></dd> <dt>

<span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>

**-Sunday** (-1)


</dt> <dd></dd> <dt>

<span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>

**ExactDayOfMonth** (0)


</dt> <dd></dd> <dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

**Domingo** (1)


</dt> <dd></dd> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

**Lunes** (2)


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

**Martes** (3)


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

**Miércoles** (4)


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

**Jueves** (5)


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

**Viernes** (6)


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

**Sábado** (7)


</dt> <dd></dd> </dl>

</dd> <dt>

**RunMonth**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ trabajo de CIM**.**RunDay**","**\_ trabajo de CIM**.**RunDayOfWeek**","**\_ trabajo de CIM**.**RunStartInterval**")
</dt> </dl>

Mes en el que se procesa el trabajo.

<dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>

**Enero** (0)


</dt> <dd></dd> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>

**Febrero** (1)


</dt> <dd></dd> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>

**Marzo** (2)


</dt> <dd></dd> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>

**Abril** (3)


</dt> <dd></dd> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>

**Mayo** (4)


</dt> <dd></dd> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>

**Junio** (5)


</dt> <dd></dd> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>

**Julio** (6)


</dt> <dd></dd> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>

**Agosto** (7)


</dt> <dd></dd> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>

**Septiembre** (8)


</dt> <dd></dd> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>

**Octubre** (9)


</dt> <dd></dd> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>

**Noviembre** (10)


</dt> <dd></dd> <dt>

<span id="December"></span><span id="december"></span><span id="DECEMBER"></span>

**Diciembre** (11)


</dt> <dd></dd> </dl>

</dd> <dt>

**RunStartInterval**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ trabajo de CIM**.**RunMonth**","**\_ trabajo de CIM**.**RunDay**","**\_ trabajo de CIM**.**RunDayOfWeek**","**\_ trabajo de CIM**.**RunStartInterval**")
</dt> </dl>

El intervalo de tiempo después de medianoche cuando se procesa el trabajo. Por ejemplo, "00000000020000.000000:000" indica que el trabajo se ejecuta en la hora local o después de dos horas, o la hora UTC (UTC se especifica con la propiedad **LocalOrUtcTime** ).

</dd> <dt>

**ScheduledStartTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) (**" \_ trabajo de CIM**.**RunMonth**","**\_ trabajo de CIM**.**RunDay**","**\_ trabajo de CIM**.**RunDayOfWeek**","**\_ trabajo de CIM**.**RunStartInterval**")
</dt> </dl>

> [!Note]  
> Esta propiedad está desusada. En su lugar, se recomienda usar las propiedades **RunMonth**, **RunDay**, **RunDayOfWeek** y **RunStartInterval** .

 

La hora a la que se programa el inicio del trabajo actual. Esta vez se puede representar mediante una fecha y hora, o un intervalo relativo a la hora a la que se solicita la propiedad. Un valor de ceros indica que el trabajo ya se está ejecutando.

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La hora a la que se inició el trabajo. Esta vez se puede representar mediante una fecha y hora, o por un intervalo relativo a la hora a la que se solicita la propiedad.

</dd> <dt>

**TimeSubmitted**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La hora a la que se envió el trabajo. Un valor de ceros indica que el elemento primario no es capaz de notificar una fecha y hora.

</dd> <dt>

**UntilTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ trabajo de CIM**.**LocalOrUtcTime**")
</dt> </dl>

Hora a partir de la cual el trabajo deja de ser válido o debe detenerse. La hora se puede representar mediante una fecha y una hora, o por un intervalo relativo a la hora a la que se solicita esta propiedad. Un valor de los nueves indica que el trabajo puede ejecutarse indefinidamente.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_LOGICALELEMENT CIM**](cim-logicalelement.md)
</dt> </dl>

 

