---
description: Envía un trabajo a un sistema operativo para su ejecución en una fecha y hora especificadas en el futuro.
ms.assetid: 9d582fbb-24cb-401d-8b77-af7671a24e6d
ms.tgt_platform: multiple
title: Método Create de la clase Win32_ScheduledJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ScheduledJob.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9f1acae94ea29d2d57b2952c0b0adc267ad3066c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360069"
---
# <a name="create-method-of-the-win32_scheduledjob-class"></a>Método Create de la \_ clase Win32 ScheduledJob

El método **crear** [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) envía un trabajo a un sistema operativo para su ejecución en una fecha y hora especificadas en el futuro. Este método requiere que el servicio de programación se inicie en el equipo al que se envía el trabajo.

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 Create(
  [in]           string   Command,
  [in]           datetime StartTime,
  [in, optional] boolean  RunRepeatedly,
  [in, optional] uint32   DaysOfWeek,
  [in, optional] uint32   DaysOfMonth,
  [in, optional] boolean  InteractWithDesktop,
  [out]          uint32   JobId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Comando* \[ de\]
</dt> <dd>

Nombre del comando, programa por lotes, archivo binario y parámetros de la línea de comandos que el servicio de programación utiliza para invocar el trabajo.

Ejemplo: "Defrag/q/f".

</dd> <dt>

*StartTime* \[ de\]
</dt> <dd>

Hora universal coordinada (hora UTC) para ejecutar un trabajo. El formato debe ser: "AAAAMMDDHHMMSS. MMMMMM (+-) OOO ", donde" AAAAMMDD "debe reemplazarse por" \* \* \* \* \* \* \* \* ". Por ejemplo: " \* \* \* \* \* \* \* \* 143000.000000-420" especifica 14,30 (2:30 P.M.) PST con horario de verano en vigor.

La sección "(+-) OOO" del valor de la propiedad StartTime es la diferencia actual de la conversión de hora local. La diferencia es la diferencia entre la hora UTC y la hora local. Para calcular la diferencia de la zona horaria, multiplique el número de horas que la zona horaria está por encima o por detrás de la hora del meridiano de Greenwich (GMT) en 60 (use un número positivo para el número de horas si la zona horaria está por detrás de GMT y un número negativo si la zona horaria está tras la hora GMT). Agregue un 60 adicional al cálculo si la zona horaria usa el horario de verano. Por ejemplo, la zona horaria estándar del Pacífico es de ocho horas tras la hora GMT, por lo que la diferencia es igual a-420 (-8 \* 60 + 60) cuando el horario de verano está en uso y-480 (-8 \* 60) cuando el horario de verano no está en uso. También puede determinar el valor de la diferencia consultando la propiedad bias de la clase [**\_ TimeZone de Win32**](win32-timezone.md) .

</dd> <dt>

*RunRepeatedly* \[ en, opcional\]
</dt> <dd>

Si **es true**, un trabajo programado se ejecuta repetidamente en días específicos. El valor predeterminado es **False**.

</dd> <dt>

*DaysOfWeek* \[ en, opcional\]
</dt> <dd>

Días de la semana en los que está programada la ejecución de un trabajo; solo se usa cuando el parámetro *RunRepeatedly* es **true**. Para programar un trabajo durante más de un día de la semana, combine los valores adecuados en un operador lógico OR. Por ejemplo, para programar un trabajo para los martes y viernes, el valor de *DaysOfWeek* es 2 o 16.

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


</dt> <dd></dd> </dl> </dd> <dt>

*DaysOfMonth* \[ en, opcional\]
</dt> <dd>

Días del mes en que se programa la ejecución de un trabajo; solo se usa cuando el parámetro *RunRepeatedly* es **true**.

<dt>

<span id="1"></span>

<span id="1"></span>**1** (1)


</dt> <dd>

Día 1 de un mes

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2** (2)


</dt> <dd>

Día 2 de un mes

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3** (4)


</dt> <dd>

Día 3 de un mes

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4** (8)


</dt> <dd>

Día 4 de un mes

</dd> <dt>

<span id="5"></span>

<span id="5"></span>**5** (16)


</dt> <dd>

Día 5 de un mes

</dd> <dt>

<span id="6"></span>

<span id="6"></span>**6** (32)


</dt> <dd>

Día 6 de un mes

</dd> <dt>

<span id="7"></span>

<span id="7"></span>**7** (64)


</dt> <dd>

Día 7 de un mes

</dd> <dt>

<span id="8"></span>

<span id="8"></span>**8** (128)


</dt> <dd>

Día 8 de un mes

</dd> <dt>

<span id="9"></span>

<span id="9"></span>**9** (256)


</dt> <dd>

Día 9 de un mes

</dd> <dt>

<span id="10"></span>

<span id="10"></span>**10** (512)


</dt> <dd>

Día 10 de un mes

</dd> <dt>

<span id="11"></span>

<span id="11"></span>**11** (1024)


</dt> <dd>

Día 11 de un mes

</dd> <dt>

<span id="12"></span>

<span id="12"></span>**12** (2048)


</dt> <dd>

Día 12 de un mes

</dd> <dt>

<span id="13"></span>

<span id="13"></span>**13** (4096)


</dt> <dd>

Día 13 de un mes

</dd> <dt>

<span id="14"></span>

<span id="14"></span>**14** (8192)


</dt> <dd>

Día 14 de un mes

</dd> <dt>

<span id="15"></span>

<span id="15"></span>**15** (16384)


</dt> <dd>

Día 15 de un mes

</dd> <dt>

<span id="16"></span>

<span id="16"></span>**16** (32768)


</dt> <dd>

Día 16 de un mes

</dd> <dt>

<span id="17"></span>

<span id="17"></span>**17** (65536)


</dt> <dd>

Día 17 de un mes

</dd> <dt>

<span id="18"></span>

<span id="18"></span>**18** (131072)


</dt> <dd>

Día 18 de un mes

</dd> <dt>

<span id="19"></span>

<span id="19"></span>**19** (262144)


</dt> <dd>

Día 19 de un mes

</dd> <dt>

<span id="20"></span>

<span id="20"></span>**20** (524288)


</dt> <dd>

Día 20 de un mes

</dd> <dt>

<span id="21"></span>

<span id="21"></span>**21** (1048576)


</dt> <dd>

Día 21 de un mes

</dd> <dt>

<span id="22"></span>

<span id="22"></span>**22** (2097152)


</dt> <dd>

Día 22 de un mes

</dd> <dt>

<span id="23"></span>

<span id="23"></span>**23** (4194304)


</dt> <dd>

Día 23 de un mes

</dd> <dt>

<span id="24"></span>

<span id="24"></span>**24** (8388608)


</dt> <dd>

Día 24 de un mes

</dd> <dt>

<span id="25"></span>

<span id="25"></span>**25** (16777216)


</dt> <dd>

Día 25 de un mes

</dd> <dt>

<span id="26"></span>

<span id="26"></span>**26** (33554432)


</dt> <dd>

Día 26 de un mes

</dd> <dt>

<span id="27"></span>

<span id="27"></span>**27** (67108864)


</dt> <dd>

Día 27 de un mes

</dd> <dt>

<span id="28"></span>

<span id="28"></span>**28** (134217728)


</dt> <dd>

Día 28 de un mes

</dd> <dt>

<span id="29"></span>

<span id="29"></span>**29** (268435456)


</dt> <dd>

Día 29 de un mes

</dd> <dt>

<span id="30"></span>

<span id="30"></span>**30** (536870912)


</dt> <dd>

Día 30 de un mes

</dd> <dt>

<span id="31"></span>

<span id="31"></span>**31** (1073741824)


</dt> <dd>

Día 31 de un mes

</dd> </dl> </dd> <dt>

*InteractWithDesktop* \[ en, opcional\]
</dt> <dd>

Si es **true**, el trabajo especificado debe ser interactivo, lo que significa que un usuario puede proporcionar la entrada a un trabajo programado mientras se está ejecutando el trabajo. El valor predeterminado es **False**.

</dd> <dt>

*JobID* \[ enuncia\]
</dt> <dd>

Número de identificación de un trabajo. Este parámetro es un identificador de un trabajo programado en un equipo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) cuando se realiza correctamente y un número diferente para indicar un error. Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Completado correctamente.**
</dt> <dd>

0

Se acepta la solicitud.

</dd> <dt>

**No admitido**
</dt> <dd>

1

No se admite la solicitud.

</dd> <dt>

**Acceso denegado**
</dt> <dd>

2

El usuario no tiene el acceso necesario.

</dd> <dt>

**Error desconocido**
</dt> <dd>

8

Proceso interactivo.

</dd> <dt>

**No se encuentra la ruta de acceso**
</dt> <dd>

9

No se encuentra la ruta de acceso al directorio del archivo ejecutable del servicio.

</dd> <dt>

**parámetro no válido**
</dt> <dd>

21

Se han pasado parámetros no válidos al servicio.

</dd> <dt>

**Servicio no iniciado**
</dt> <dd>

22

La cuenta con la que se ejecuta este servicio no es válida o carece de permisos para ejecutar el servicio.

</dd> <dt>

**Otros**
</dt> <dd>

23 4294967295

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si el trabajo programado inicia un programa interactivo como el Bloc de notas, la propiedad **InteractWithDeskto** debe establecerse en **true** o la pantalla del programa no está visible. El proceso sigue apareciendo en el **Administrador de tareas** aunque no aparezca en la pantalla.

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

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32 \_ ScheduledJob**](win32-scheduledjob.md)
</dt> </dl>

 

