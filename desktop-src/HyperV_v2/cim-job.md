---
description: Elemento lógico que representa una unidad de trabajo que se debe ejecutar, como un script o un trabajo de impresión. Un trabajo es distinto de un proceso porque un trabajo se puede programar o poner en cola, y su ejecución no se limita a un único sistema.
ms.assetid: 35e35c3f-617b-429b-b68f-fa0c0c330e92
title: CIM_Job (administración de Hyper-V)
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
ms.openlocfilehash: 8eb8f63ec9d2cdd881a2ba0946f83a40fb8be866
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474591"
---
# <a name="cim_job-class-hyper-v-management"></a>CIM_Job (administración de Hyper-V)

Elemento lógico que representa una unidad de trabajo que se debe ejecutar, como un script o un trabajo de impresión. Un trabajo es distinto de un proceso porque un trabajo se puede programar o poner en cola, y su ejecución no se limita a un único sistema.

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

La **clase de \_ trabajo CIM** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase de \_ trabajo CIM** tiene estos métodos.




| Método | Descripción | 
|--------|-------------|
| <a href="cim-job-killjob.md"><strong>KillJob</strong></a> | Este método es desusado. En su lugar, use <strong>el método RequestStateChange.</strong><br /><blockquote>[!Note]<br />Descripción en desuso: cierra un trabajo.</blockquote><br /> | 




 

### <a name="properties"></a>Propiedades

La **clase de \_ trabajo CIM** tiene estas propiedades.

<dl> <dt>

**DeleteOnCompletion**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

**True** para eliminar el trabajo tras la finalización; de lo contrario, **false**.

> [!Note]  
> Esta propiedad no eliminará los trabajos que se completen antes de que esta propiedad se establezca en **True.**

 

</dd> <dt>

**ElapsedTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La duración durante la que se ha ejecutado el trabajo.

</dd> <dt>

**ErrorCode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Cim \_ Job**.**ErrorDescription**")
</dt> </dl>

Código de error específico del proveedor que captura la información de procesamiento de trabajos periódicos. El valor debe establecerse en cero si el trabajo se completó sin errores.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Cim \_ Job**.**ErrorCode**")
</dt> </dl>

Cadena de forma libre que contiene una descripción del código de error correspondiente en la **propiedad ErrorCode.**

</dd> <dt>

**JobRunTimes**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Número de veces que se ejecuta el trabajo.

</dd> <dt>

**Estado del trabajo**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).**OperationalStatus**")
</dt> </dl>

Cadena de forma libre que representa el estado del trabajo.

</dd> <dt>

**LocalOrUtcTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Indica si las horas de las propiedades **RunStartInterval** y **UntilTime** representan horas locales o UTC.

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

Tipo de acceso: lectura y escritura
</dt> </dl>

El usuario al que se notificará cuando se complete o se produce un error en un trabajo.

</dd> <dt>

**OtherRecoveryAction**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Cim \_ Job**.**RecoveryAction**")
</dt> </dl>

Cadena que describe la acción de recuperación cuando la **propiedad RecoveryAction** es **Other** ("1").

</dd> <dt>

**Propietario**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OwningJobElement**](cim-owningjobelement.md).")
</dt> </dl>

El usuario que envió el trabajo o el nombre del servicio o método que solicitó el trabajo.

</dd> <dt>

**PercentComplete**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Percent"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (101), **PUnit** ("percent")
</dt> </dl>

Porcentaje del trabajo que se ha completado.

> [!Note]  
> El valor "101" no está definido y no se permitirá en la siguiente revisión principal de la especificación.

 

</dd> <dt>

**Prioridad**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Importancia del trabajo. Cuanto menor sea el número, mayor será la prioridad.

</dd> <dt>

**RecoveryAction**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Cim \_ Job**.**OtherRecoveryAction**")
</dt> </dl>

Describe la acción de recuperación que se debe realizar cuando se produce un error en un trabajo de ejecución.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)


</dt> <dd>

No se sabe qué acción de recuperación realizar.

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otros** (1)


</dt> <dd>

La acción de recuperación se especificará en la **propiedad OtherRecoveryAction.**

</dd> <dt>

<span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>

<span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**No continuar** (2)


</dt> <dd>

Detenga la ejecución del trabajo y actualice correctamente su estado.

</dd> <dt>

<span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>

<span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continuar con el siguiente trabajo** (3)


</dt> <dd>

Continúe con el siguiente trabajo en la cola.

</dd> <dt>

<span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>

<span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Volver a ejecutar el trabajo** (4)


</dt> <dd>

El trabajo debe volver a ejecutarse.

</dd> <dt>

<span id="Run_Recovery_Job"></span><span id="run_recovery_job"></span><span id="RUN_RECOVERY_JOB"></span>

<span id="Run_Recovery_Job"></span><span id="run_recovery_job"></span><span id="RUN_RECOVERY_JOB"></span>**Ejecutar trabajo de recuperación** (5)


</dt> <dd>

Ejecute el trabajo asociado mediante la **relación RecoveryJob.** Tenga en cuenta que el trabajo de recuperación ya debe estar en la cola desde la que se ejecutará.

</dd> </dl>

</dd> <dt>

**RunDay**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint8**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (-31), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (31), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Cim \_ Job**.**RunMonth**", "**Cim \_ Job**.**RunDayOfWeek**", "**Cim \_ Job**.**RunStartInterval**")
</dt> </dl>

Entero que se usa junto con la **propiedad RunDayOfWeek** para indicar el día en que se procesa el trabajo; o bien, **si RunDayOfWeek** se establece en cero, **RunDay** indica el día del mes en que se procesa el trabajo. Si **RunDay** es un entero negativo, especifica un día con respecto al final del mes, o si **RunDay** es un entero positivo, especifica un día con respecto al principio del mes.

</dd> <dt>

**RunDayOfWeek**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint8**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Cim \_ Job**.**RunMonth**", "**Cim \_ Job**.**RunDay**", "**Cim \_ Job**.**RunStartInterval**")
</dt> </dl>

Entero que se usa junto con la **propiedad RunDay** para indicar el día en que se procesa el trabajo; o bien, **si RunDayOfWeek** se establece en cero, **RunDay** indica el día del mes en que se procesa el trabajo.

<dt>

<span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>

**-Saturday** (-7)


</dt> <dd></dd> <dt>

<span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>

**-Friday** (-6)


</dt> <dd></dd> <dt>

<span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>

**-Thursday** (-5)


</dt> <dd></dd> <dt>

<span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>

**-Miércoles** (-4)


</dt> <dd></dd> <dt>

<span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>

**-Tuesday** (-3)


</dt> <dd></dd> <dt>

<span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>

**-Monday** (-2)


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

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Cim \_ Job**.**RunDay**", "**Cim \_ Job**.**RunDayOfWeek**", "**Cim \_ Job**.**RunStartInterval**")
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

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Cim \_ Job**.**RunMonth**", "**Cim \_ Job**.**RunDay**", "**Cim \_ Job**.**RunDayOfWeek**", "**Cim \_ Job**.**RunStartInterval**")
</dt> </dl>

Intervalo de tiempo después de medianoche en el que se procesa el trabajo. Por ejemplo, "00000000020000.000000:000" indica que el trabajo se ejecuta en o después de las dos de la hora local, o la hora UTC (UTC se especifica con la **propiedad LocalOrUtcTime).**

</dd> <dt>

**ScheduledStartTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**En desuso**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**Trabajo \_ CIM**.**RunMonth**", "**Cim \_ Job**.**RunDay**", "**Cim \_ Job**.**RunDayOfWeek**", "**Cim \_ Job**.**RunStartInterval**")
</dt> </dl>

> [!Note]  
> Esta propiedad está desusada. En su lugar, se recomienda usar las propiedades **RunMonth**, **RunDay**, **RunDayOfWeek** y **RunStartInterval.**

 

Hora a la que se programa el inicio del trabajo actual. Esta hora se puede representar mediante una fecha y hora, o un intervalo relativo a la hora en que se solicita la propiedad. Un valor de todos los ceros indica que el trabajo ya se está ejecutando.

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Hora a la que se inició el trabajo. Esta hora se puede representar mediante una fecha y hora, o mediante un intervalo relativo a la hora en que se solicita la propiedad.

</dd> <dt>

**TimeSubmitted**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Hora a la que se envió el trabajo. Un valor de todos los ceros indica que el elemento primario no es capaz de notificar una fecha y hora.

</dd> <dt>

**UntilTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Cim \_ Job**.**LocalOrUtcTime**")
</dt> </dl>

La hora después de la cual el trabajo deja de ser válido o debe detenerse. La hora se puede representar mediante una fecha y hora, o mediante un intervalo relativo a la hora en que se solicita esta propiedad. Un valor de los nueves indica que el trabajo se puede ejecutar indefinidamente.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Elemento \_ lógico CIM**](cim-logicalelement.md)
</dt> </dl>

 

