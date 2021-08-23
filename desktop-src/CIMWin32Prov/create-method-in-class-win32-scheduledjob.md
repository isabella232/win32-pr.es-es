---
description: Envía un trabajo a un sistema operativo para su ejecución en una fecha y hora especificadas en el futuro.
ms.assetid: 9d582fbb-24cb-401d-8b77-af7671a24e6d
ms.tgt_platform: multiple
title: Método Create de la Win32_ScheduledJob clase
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
ms.openlocfilehash: a7788c894646b3ebb07fc9d3d98aeeda54b9172b5dde01e7eb65975bb2d95d61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119547415"
---
# <a name="create-method-of-the-win32_scheduledjob-class"></a>Método Create de la clase \_ ScheduledJob de Win32

El **método** [de clase Create WMI](/windows/desktop/WmiSdk/retrieving-a-class) envía un trabajo a un sistema operativo para su ejecución en una hora y fecha especificadas en el futuro. Este método requiere que el servicio de programación se inicia en el equipo al que se envía el trabajo.

En este tema se usa Managed Object Format sintaxis MOF (MOF). Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

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

*Comando* \[ En\]
</dt> <dd>

Nombre del comando, programa por lotes o archivo binario y parámetros de línea de comandos que usa el servicio de programación para invocar el trabajo.

Ejemplo: "defrag /q /f".

</dd> <dt>

*StartTime* \[ En\]
</dt> <dd>

Hora universal coordinada (UTC) para ejecutar un trabajo. El formulario debe ser: "AAAAMMDDHHMMSS. MMMMMM(+-)OOO", donde "YYYYMMDD" debe reemplazarse por " \* \* \* \* \* \* \* \* ". Por ejemplo: \* \* \* \* \* \* \* \* "143000.00000-420" especifica 14.30 (2:30 p. m.) PST con el horario de verano en vigor.

La sección "(+-)OOO" del valor de la propiedad StartTime es el sesgo actual para la traducción de la hora local. El sesgo es la diferencia entre la hora UTC y la hora local. Para calcular el sesgo de la zona horaria, multiplique el número de horas que la zona horaria está por delante o por detrás de la hora media de Greenwich (GMT) por 60 (use un número positivo para el número de horas si la zona horaria está por delante de GMT y un número negativo si la zona horaria está detrás de GMT). Agregue 60 adicionales al cálculo si la zona horaria usa el horario de verano. Por ejemplo, la zona horaria estándar del Pacífico está ocho horas por detrás de GMT, por lo que el sesgo es igual a -420 (-8 60 + 60) cuando el horario de verano está en uso y \* -480 (-8 60) cuando el horario de verano no está \* en uso. También puede determinar el valor del sesgo consultando la propiedad bias de la clase [**\_ TimeZone de Win32.**](win32-timezone.md)

</dd> <dt>

*RunRepeatedly* \[ en, opcional\]
</dt> <dd>

Si **es True,** un trabajo programado se ejecuta repetidamente en días específicos. El valor predeterminado es **False**.

</dd> <dt>

*DaysOfWeek* \[ en, opcional\]
</dt> <dd>

Días de la semana en los que se programa la ejecución de un trabajo; se usa solo cuando *el parámetro RunRepeatedly* es **True.** Para programar un trabajo durante más de un día de la semana, una los valores adecuados en un or lógico. Por ejemplo, para programar un trabajo para martes y viernes, el valor de *DaysOfWeek* es 2 O 16.

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

Días del mes en que se programa la ejecución de un trabajo; se usa solo cuando *el parámetro RunRepeatedly* es **True.**

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

Si **es True**, el trabajo especificado debe ser interactivo, lo que significa que un usuario puede dar entrada a un trabajo programado mientras se ejecuta el trabajo. El valor predeterminado es **False**.

</dd> <dt>

*JobId* \[ out\]
</dt> <dd>

Número de identificador de un trabajo. Este parámetro es un identificador de un trabajo que se programa en un equipo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) cuando se realiza correctamente y un número diferente para indicar un error. Para obtener códigos de error adicionales, [**vea Wmi Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores **HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

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

No se encuentra la ruta de acceso del directorio al archivo ejecutable del servicio.

</dd> <dt>

**parámetro no válido**
</dt> <dd>

21

Se han pasado parámetros no válidos al servicio.

</dd> <dt>

**Servicio no iniciado**
</dt> <dd>

22

La cuenta en la que se ejecuta este servicio no es válida o carece de los permisos para ejecutar el servicio.

</dd> <dt>

**Otros**
</dt> <dd>

23 4294967295

</dd> </dl>

## <a name="remarks"></a>Comentarios

Si el trabajo programado inicia un programa interactivo como Bloc de notas, la propiedad **InteractWithDeskto** debe establecerse en **True** o la pantalla del programa no está visible. El proceso sigue apareciendo en **el Administrador de tareas** incluso si no aparece en la pantalla.

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

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**ScheduledJob de Win32 \_**](win32-scheduledjob.md)
</dt> </dl>

 

