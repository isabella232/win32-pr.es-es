---
title: Schtasks.exe
description: Permite a un administrador crear, eliminar, consultar, cambiar, ejecutar y finalizar tareas programadas en un equipo local o remoto.
ms.assetid: 3cf973de-14c4-4ca9-86a7-7f97181bd9e0
keywords:
- Schtasks.exe Programador de tareas
topic_type:
- apiref
api_name:
- Schtasks.exe
api_type:
- NA
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 1c9ba2c13053a8c550128f5d66623b5eed3a9dec
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314638"
---
# <a name="schtasksexe"></a>Schtasks.exe

Permite a un administrador crear, eliminar, consultar, cambiar, ejecutar y finalizar tareas programadas en un equipo local o remoto. Al ejecutar Schtasks.exe sin argumentos, se muestra el estado y el siguiente tiempo de ejecución de cada tarea registrada. 

Para obtener más información sobre Programador de tareas, vea esta introducción: [programador de tareas para desarrolladores](task-scheduler-start-page.md).

## <a name="creating-a-task"></a>Crear una tarea

La siguiente sintaxis se usa para crear una tarea en el equipo local o remoto.

``` syntax
schtasks /Create 
[/S system [/U username [/P [password]]]]
[/RU username [/RP [password]] /SC schedule [/MO modifier] [/D day]
[/M months] [/I idletime] /TN taskname /TR taskrun [/ST starttime]
[/RI interval] [ {/ET endtime | /DU duration} [/K] 
[/XML xmlfile] [/V1]] [/SD startdate] [/ED enddate] [/IT] [/Z] [/F]
```

### <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **sistema**
</dt> <dd>

Valor que especifica el equipo remoto al que se va a conectar. Si se omite, el valor predeterminado del parámetro System es el equipo local.

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **nombreDeUsuario**
</dt> <dd>

Valor que especifica el contexto de usuario en el que se debe ejecutar Schtasks.exe.

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ contraseña \]**
</dt> <dd>

Valor que especifica la contraseña para un contexto de usuario determinado. Si se omite, Schtasks.exe solicita la intervención del usuario.

</dd> <dt>

<span id="_RU_username"></span><span id="_ru_username"></span><span id="_RU_USERNAME"></span> **Nombre de usuario** /RU
</dt> <dd>

Valor que especifica el contexto de usuario en el que se ejecuta la tarea. En la cuenta del sistema, los valores válidos son "", "NT AUTHORITY \\ System" o "System". Por Programador de tareas 2,0 tareas, "NT AUTHORITY \\ LOCALSERVICE" y "NT Authority \\ NETWORKSERVICE" también son valores válidos.

</dd> <dt>

<span id="_RP__password_"></span><span id="_rp__password_"></span><span id="_RP__PASSWORD_"></span>**/RP** **\[ contraseña \]**
</dt> <dd>

Valor que especifica la contraseña para el usuario especificado con el parámetro/RU. Para solicitar la contraseña, el valor debe ser " \* " o ningún valor. Esta contraseña se omite para la cuenta del sistema. Este parámetro debe combinarse con el modificador/RU o/XML.

</dd> <dt>

<span id="_SC_schedule"></span><span id="_sc_schedule"></span><span id="_SC_SCHEDULE"></span>**/SC** ( **programación** )
</dt> <dd>

Valor que especifica la frecuencia de programación. Los valores válidos son: MINUTE, HOURly, DAILY, WEEKly, MONTHly, ONCE, ONLOGON, OnIdle e ONEVENT.

</dd> <dt>

<span id="_MO_modifier"></span><span id="_mo_modifier"></span><span id="_MO_MODIFIER"></span>**/Mo** ( **modificador** )
</dt> <dd>

Un valor que refina el tipo de programación para permitir un mayor control sobre la periodicidad de la programación. Los valores válidos son:

-   MINUTO: 1-1439 minutos.
-   CADA hora: 1-23 horas.
-   DIARIAMENTE: 1-365 días.
-   SEMANAL: semanas 1-52.
-   UNA vez: sin modificadores.
-   OnStart: sin modificadores.
-   ONLOGON: sin modificadores.
-   OnIdle: sin modificadores.
-   MONTHly: 1-12, or FIRST, SECOND, THIRD, cuarto, LAST y LASTDAY.
-   ONEVENT: cadena de consulta de evento XPath.

</dd> <dt>

<span id="_D_days"></span><span id="_d_days"></span><span id="_D_DAYS"></span>**/D** **días**
</dt> <dd>

Valor que especifica el día de la semana en el que se va a ejecutar la tarea. Los valores válidos son: MON, mar, Mié, THU, Vie, SAT, SUN y para las programaciones mensuales 1-31 (días del mes). El carácter comodín ( \* ) especifica todos los días.

</dd> <dt>

<span id="_M_months"></span><span id="_m_months"></span><span id="_M_MONTHS"></span>**/M** **meses**
</dt> <dd>

Valor que especifica los meses del año. El valor predeterminado es el primer día del mes. Los valores válidos son: JAN, FEB, MAR, APR, mayo, JUN, JUL, ago, SEP, OCT, NOV y DEC. El carácter comodín ( \* ) especifica todos los meses.

</dd> <dt>

<span id="_I_idletime"></span><span id="_i_idletime"></span><span id="_I_IDLETIME"></span>**/I** **tiempodeinactividad**
</dt> <dd>

Valor que especifica la cantidad de tiempo de inactividad que se va a esperar antes de ejecutar una tarea de OnIdle programada. El intervalo válido es de 1-999 minutos.

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **nombredetarea**
</dt> <dd>

Valor que especifica un nombre que identifica de forma única la tarea programada.

</dd> <dt>

<span id="_TR_taskrun"></span><span id="_tr_taskrun"></span><span id="_TR_TASKRUN"></span>**/TR** 
</dt> <dd>

Valor que especifica la ruta de acceso y el nombre de archivo de la tarea que se va a ejecutar en el momento programado. Por ejemplo: C: \\ Windows \\ system32 \\calc.exe.

</dd> <dt>

<span id="_ST_starttime"></span><span id="_st_starttime"></span><span id="_ST_STARTTIME"></span>**/St** **startTime**
</dt> <dd>

Valor que especifica la hora de inicio para ejecutar la tarea. El formato de hora es HH: mm (hora de 24 horas). Por ejemplo, 14:30 especifica 2: las 16:30. El valor predeterminado es la hora actual en que no se especifica/ST. Esta opción es necesaria para el argumento/SC una vez.

</dd> <dt>

<span id="_RI_interval"></span><span id="_ri_interval"></span><span id="_RI_INTERVAL"></span>**/RI** **intervalo**
</dt> <dd>

Valor que especifica el intervalo de repetición en minutos. Esto no es aplicable a los siguientes tipos de programación: MINUTE, HOURly, OnStart, ONLOGON, OnIdle e ONEVENT. El intervalo válido es de 1-599940 minutos. Si se especifican los parámetros/ET o/DU, el valor predeterminado es 10 minutos.

**Windows XP y Windows Server 2003:** Esta opción no está disponible.

</dd> <dt>

<span id="_ET_endtime"></span><span id="_et_endtime"></span><span id="_ET_ENDTIME"></span>**/Et** **EndTime**
</dt> <dd>

Valor que especifica la hora de finalización para ejecutar la tarea. El formato de hora es HH: mm (hora de 24 horas). Por ejemplo, 14:50 especifica 2:50PM. Esto no es aplicable a los siguientes tipos de programación: OnStart, ONLOGON, OnIdle e ONEVENT.

**Windows XP y Windows Server 2003:** Esta opción no está disponible.

</dd> <dt>

<span id="_DU_duration"></span><span id="_du_duration"></span><span id="_DU_DURATION"></span>**/Du** **duración**
</dt> <dd>

Valor que especifica la duración para ejecutar la tarea. El formato de hora es HH: mm (hora de 24 horas). Por ejemplo, 14:50 especifica 2:50PM. Esto no es aplicable con/ET y para los siguientes tipos de programación: OnStart, ONLOGON, OnIdle e ONEVENT. En el caso de las tareas de/V1 (Programador de tareas 1,0), si se especifica/RI, el valor predeterminado de Duration es una hora.

**Windows XP:** Esta opción no está disponible.

</dd> <dt>

<span id="_K_"></span><span id="_k_"></span>**/K** 
</dt> <dd>

Valor que finaliza la tarea en la hora de finalización o en el tiempo de duración. Esto no es aplicable a los siguientes tipos de programación: OnStart, ONLOGON, OnIdle e ONEVENT. Se debe especificar/ET o/DU.

**Windows XP y Windows Server 2003:** Esta opción no está disponible.

</dd> <dt>

<span id="_SD_startdate"></span><span id="_sd_startdate"></span><span id="_SD_STARTDATE"></span>**/SD** **startDate**
</dt> <dd>

Valor que especifica la primera fecha en la que se va a ejecutar la tarea. El formato es mm/dd/aaaa. El valor predeterminado es la fecha actual. Esto no es aplicable a los siguientes tipos de programación: una vez, OnStart, ONLOGON, OnIdle e ONEVENT.

</dd> <dt>

<span id="_ED_enddate"></span><span id="_ed_enddate"></span><span id="_ED_ENDDATE"></span>**/Ed** **EndDate**
</dt> <dd>

Valor que especifica la última fecha en la que se ejecutará la tarea. El formato es mm/dd/aaaa. Esto no es aplicable a los siguientes tipos de programación: una vez, OnStart, ONLOGON, OnIdle e ONEVENT.

</dd> <dt>

<span id="_EC_ChannelName"></span><span id="_ec_channelname"></span><span id="_EC_CHANNELNAME"></span>**/EC** **ChannelName**
</dt> <dd>

Valor que especifica el canal de eventos para los desencadenadores ONEVENT.

**Windows XP y Windows Server 2003:** Esta opción no está disponible.

</dd> <dt>

<span id="_IT_"></span><span id="_it_"></span>**/IT** 
</dt> <dd>

Un valor que permite que la tarea se ejecute de forma interactiva solo si el usuario/RU está conectado actualmente en el momento en que se ejecuta la tarea. La tarea solo se ejecuta si el usuario ha iniciado sesión.

**Windows XP y Windows Server 2003:** Esta opción no está disponible.

</dd> <dt>

<span id="_NP_"></span><span id="_np_"></span>**/NP** 
</dt> <dd>

Valor que indica que no hay ninguna contraseña almacenada. La tarea no se ejecuta de forma interactiva como el usuario determinado. Solo están disponibles los recursos locales.

**Windows XP y Windows Server 2003:** Esta opción no está disponible.

</dd> <dt>

<span id="_Z_"></span><span id="_z_"></span>**/Z** 
</dt> <dd>

Valor que marca la tarea que se va a eliminar después de su última ejecución.

**Windows XP y Windows Server 2003:** Esta opción no está disponible.

</dd> <dt>

<span id="_XML_xmlfile"></span><span id="_xml_xmlfile"></span><span id="_XML_XMLFILE"></span> **Xmlfile** de/XML
</dt> <dd>

Valor que crea una tarea a partir de un archivo XML. Este parámetro se puede combinar con los modificadores/RU y/RP, o con el modificador/RP solo cuando el XML de la tarea ya contiene la entidad de seguridad.

**Windows XP y Windows Server 2003:** Esta opción no está disponible.

</dd> <dt>

<span id="_V1_"></span><span id="_v1_"></span>**/V1** 
</dt> <dd>

Valor que crea una tarea visible para las plataformas Windows 2000, Windows Server 2003 y Windows XP.

**Windows XP y Windows Server 2003:** Esta opción no está disponible.

</dd> <dt>

<span id="_F_"></span><span id="_f_"></span>**/F** 
</dt> <dd>

Valor que fuerza la creación de la tarea y suprime las advertencias si la tarea especificada ya existe.

**Windows XP y Windows Server 2003:** Esta opción no está disponible.

</dd> <dt>

<span id="_RL_level"></span><span id="_rl_level"></span><span id="_RL_LEVEL"></span> **Nivel** de/RL
</dt> <dd>

Valor que establece el nivel de ejecución de la tarea. Los valores válidos son LIMITED y HIGHEST. El valor predeterminado es limitado.

**Windows XP y Windows Server 2003:** Esta opción no está disponible.

</dd> <dt>

<span id="_DELAY_delaytime"></span><span id="_delay_delaytime"></span><span id="_DELAY_DELAYTIME"></span>**/Delay** **Delaytime**
</dt> <dd>

Valor que especifica el tiempo de espera para retrasar la tarea después de que se desencadene el desencadenador. El formato de hora es mmmm: SS. Esta opción solo es válida para los tipos de programación OnStart, ONLOGON e ONEVENT.

**Windows XP y Windows Server 2003:** Esta opción no está disponible.

</dd> <dt>

<span id="___"></span>**/?** 
</dt> <dd>

Valor que muestra el mensaje de ayuda para Schtasks.exe.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Al crear una tarea en un equipo remoto que se ejecuta en el sistema operativo Windows XP, Windows Server 2003 o Windows 2000, use el modificador/v1

No se puede crear una tarea remota Programador de tareas 1,0 no interactiva (cree una tarea sin usar el modificador/IT y usando el modificador/V1) si el equipo remoto tiene habilitada la excepción de Firewall compartir archivos e impresoras y la excepción de Firewall administración remota de tareas programadas.

## <a name="deleting-a-task"></a>Eliminar una tarea

La siguiente sintaxis se usa para eliminar una o varias tareas programadas.

``` syntax
schtasks /Delete 
[/S system [/U username [/P [password]]]]
[/TN taskname] [/F]
```

### <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **sistema**
</dt> <dd>

Valor que especifica el equipo remoto al que se va a conectar. Si se omite, el valor predeterminado del parámetro System es el equipo local.

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **nombreDeUsuario**
</dt> <dd>

Valor que especifica el contexto de usuario en el que se debe ejecutar Schtasks.exe.

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ contraseña \]**
</dt> <dd>

Valor que especifica la contraseña para el contexto de usuario determinado. Si se omite, Schtasks.exe solicita la intervención del usuario.

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **nombredetarea**
</dt> <dd>

Valor que especifica el nombre de la tarea programada que se va a eliminar. El carácter comodín ( \* ) se puede usar para eliminar todas las tareas.

</dd> <dt>

<span id="_F_"></span><span id="_f_"></span>**/F** 
</dt> <dd>

Valor que fuerza la eliminación de la tarea y suprime las advertencias si se está ejecutando la tarea especificada.

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Valor que muestra la ayuda para Schtasks.exe.

</dd> </dl>

## <a name="running-a-task"></a>Ejecutar una tarea

La siguiente sintaxis se usa para ejecutar inmediatamente una tarea programada.

``` syntax
schtasks /Run 
[/S system [/U username [/P [password]]]]
/TN taskname
```

### <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **sistema**
</dt> <dd>

Valor que especifica el equipo remoto al que se va a conectar. Si se omite, el valor predeterminado del parámetro System es el equipo local.

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **nombreDeUsuario**
</dt> <dd>

Valor que especifica el contexto de usuario en el que se debe ejecutar Schtasks.exe.

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ contraseña \]**
</dt> <dd>

Valor que especifica la contraseña para el contexto de usuario determinado. Si se omite, Schtasks.exe solicita la intervención del usuario.

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **nombredetarea**
</dt> <dd>

Valor que especifica el nombre de la tarea programada que se va a ejecutar.

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Valor que muestra la ayuda para Schtasks.exe.

</dd> </dl>

## <a name="ending-a-running-task"></a>Finalizar una tarea en ejecución

La siguiente sintaxis se usa para detener una tarea programada en ejecución.

> [!Note]  
> Para detener la ejecución de una tarea remota, asegúrese de que el equipo remoto tenga habilitadas las excepciones de Firewall administración de archivos e impresoras y tareas programadas remotas.

 

``` syntax
schtasks /End 
[/S system [/U username [/P [password]]]]
/TN taskname
```

### <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **sistema**
</dt> <dd>

Valor que especifica el equipo remoto al que se va a conectar. Si se omite, el valor predeterminado del parámetro System es el equipo local.

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **nombreDeUsuario**
</dt> <dd>

Valor que especifica el contexto de usuario en el que se debe ejecutar Schtasks.exe.

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ contraseña \]**
</dt> <dd>

Valor que especifica la contraseña para el contexto de usuario determinado. Si se omite, Schtasks.exe solicita la intervención del usuario.

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **nombredetarea**
</dt> <dd>

Valor que especifica el nombre de la tarea programada que se va a detener.

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Valor que muestra la ayuda para Schtasks.exe.

</dd> </dl>

## <a name="querying-for-task-information"></a>Consultar la información de la tarea

La siguiente sintaxis se usa para mostrar las tareas programadas desde el equipo local o remoto.

``` syntax
schtasks /Query 
[/S system [/U username [/P [password]]]]
[/FO format | /XML] [/NH] [/V] [/TN taskname] [/?]
```

### <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **sistema**
</dt> <dd>

Valor que especifica el equipo remoto al que se va a conectar. Si se omite, el valor predeterminado del parámetro System es el equipo local.

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **nombreDeUsuario**
</dt> <dd>

Valor que especifica el contexto de usuario en el que se debe ejecutar Schtasks.exe.

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ contraseña \]**
</dt> <dd>

Valor que especifica la contraseña para el contexto de usuario determinado. Si se omite, Schtasks.exe solicita la intervención del usuario.

</dd> <dt>

<span id="_FO_format"></span><span id="_fo_format"></span><span id="_FO_FORMAT"></span>**/FO** **formato**
</dt> <dd>

Valor que especifica el formato de salida. Los valores válidos son TABLE, LIST y CSV.

</dd> <dt>

<span id="_NH_"></span><span id="_nh_"></span>**/NH** 
</dt> <dd>

Valor que especifica que el encabezado de columna no debe mostrarse en la salida. Esto solo es válido para los formatos de tabla y CSV.

</dd> <dt>

<span id="_V_"></span><span id="_v_"></span>**/V** 
</dt> <dd>

Valor que muestra el resultado detallado de la tarea.

> [!Note]  
> Si una tarea estaba programada para ejecutarse una sola vez, la información de programación mostrada es "la programación de datos no está disponible en este formato".

 

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **nombredetarea**
</dt> <dd>

Valor que especifica el nombre de la tarea para la que se va a recuperar la información. Si no se especifica ningún nombre de tarea, se mostrará la información de todas las tareas.

**Windows XP y Windows Server 2003:** Esta opción no está disponible.

</dd> <dt>

<span id="_XML_"></span><span id="_xml_"></span>**/XML** 
</dt> <dd>

Valor que se usa para mostrar las definiciones de tarea en formato XML.

**Windows XP y Windows Server 2003:** Esta opción no está disponible.

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Valor que se usa para mostrar la ayuda de Schtasks.exe.

</dd> </dl>

## <a name="changing-a-task"></a>Cambiar una tarea

La siguiente sintaxis se usa para cambiar la forma en que se ejecuta el programa, o para cambiar la cuenta de usuario y la contraseña que usa una tarea programada.

``` syntax
schtasks /Change 
[/S system [/U username [/P [password]]]] /TN taskname
{ [/RU runasuser] [/RP runaspassword] [/TR taskrun] [/ST starttime] 
[/RI interval] [ {/ET endtime | /DU duration} [/K] ]
[/SD startdate] [/ED enddate] [/ENABLE | /DISABLE] [/IT] [/Z] }
```

### <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **sistema**
</dt> <dd>

Valor que especifica el equipo remoto al que se va a conectar. Si se omite, el valor predeterminado del parámetro System es el equipo local.

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **nombreDeUsuario**
</dt> <dd>

Valor que especifica el contexto de usuario en el que se debe ejecutar Schtasks.exe.

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ contraseña \]**
</dt> <dd>

Valor que especifica la contraseña para el contexto de usuario determinado. Si se omite, Schtasks.exe solicita la intervención del usuario.

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **nombredetarea**
</dt> <dd>

Valor que especifica la tarea programada que se va a cambiar.

</dd> <dt>

<span id="_RU_runasuser"></span><span id="_ru_runasuser"></span><span id="_RU_RUNASUSER"></span>**/RU** **como_usuario**
</dt> <dd>

Valor que cambia el nombre de usuario (contexto de usuario) en el que se ejecutará la tarea programada. En la cuenta del sistema, los valores válidos son "", "NT AUTHORITY \\ System" o "System". Por Programador de tareas tareas 2,0, "NT AUTHORITY \\ LOCALSERVICE" y "NT Authority \\ NETWORKSERVICE" también son valores válidos.

</dd> <dt>

<span id="_RP_runaspassword"></span><span id="_rp_runaspassword"></span><span id="_RP_RUNASPASSWORD"></span>**/RP** **runaspassword**
</dt> <dd>

Valor que especifica una nueva contraseña para el contexto de usuario existente o la contraseña de una nueva cuenta de usuario. Esta contraseña se omite para la cuenta del sistema.

</dd> <dt>

<span id="_TR_taskrun"></span><span id="_tr_taskrun"></span><span id="_TR_TASKRUN"></span>**/TR** 
</dt> <dd>

Valor que especifica un nuevo programa que ejecutará la tarea.

</dd> <dt>

<span id="_ST_starttime"></span><span id="_st_starttime"></span><span id="_ST_STARTTIME"></span>**/St** **startTime**
</dt> <dd>

Valor que especifica la hora de inicio para ejecutar la tarea. El formato de hora es HH: mm (hora de 24 horas). Por ejemplo, 14:30 especifica 2: las 16:30.

**Windows XP y Windows Server 2003:** Esta opción no está disponible.

</dd> <dt>

<span id="_RI_interval"></span><span id="_ri_interval"></span><span id="_RI_INTERVAL"></span>**/RI** **intervalo**
</dt> <dd>

Valor que especifica el intervalo de repetición, en minutos. El intervalo válido es de 1-599940 minutos.

**Windows XP y Windows Server 2003:** Esta opción no está disponible.

</dd> <dt>

<span id="_ET_endtime"></span><span id="_et_endtime"></span><span id="_ET_ENDTIME"></span>**/Et** **EndTime**
</dt> <dd>

Valor que especifica la hora de finalización de la tarea. El formato de hora es HH: mm (hora de 24 horas). Por ejemplo, 14:50 especifica 2:50PM.

**Windows XP y Windows Server 2003:** Esta opción no está disponible.

</dd> <dt>

<span id="_DU_duration"></span><span id="_du_duration"></span><span id="_DU_DURATION"></span>**/Du** **duración**
</dt> <dd>

Valor que especifica la duración para ejecutar la tarea. El formato de hora es HH: mm (hora de 24 horas). Por ejemplo, 14:50 especifica 2:50PM. Esto no es aplicable con el parámetro/ET.

**Windows XP y Windows Server 2003:** Esta opción no está disponible.

</dd> <dt>

<span id="_K_"></span><span id="_k_"></span>**/K** 
</dt> <dd>

Valor que finaliza la tarea en la hora de finalización o en el tiempo de duración.

**Windows XP y Windows Server 2003:** Esta opción no está disponible.

</dd> <dt>

<span id="_SD_startdate"></span><span id="_sd_startdate"></span><span id="_SD_STARTDATE"></span>**/SD** **startDate**
</dt> <dd>

Valor que especifica la primera fecha en la que se va a ejecutar la tarea. El formato es mm/dd/aaaa.

**Windows XP y Windows Server 2003:** Esta opción no está disponible.

</dd> <dt>

<span id="_ED_enddate"></span><span id="_ed_enddate"></span><span id="_ED_ENDDATE"></span>**/Ed** **EndDate**
</dt> <dd>

Valor que especifica la última fecha en la que se ejecutará la tarea. El formato es mm/dd/aaaa.

**Windows XP y Windows Server 2003:** Esta opción no está disponible.

</dd> <dt>

<span id="_IT_"></span><span id="_it_"></span>**/IT** 
</dt> <dd>

Un valor que permite que la tarea se ejecute de forma interactiva solo si el usuario/RU está conectado actualmente en el momento en que se ejecuta la tarea. La tarea solo se ejecuta si el usuario ha iniciado sesión.

**Windows XP y Windows Server 2003:** Esta opción no está disponible.

</dd> <dt>

<span id="_RL_level"></span><span id="_rl_level"></span><span id="_RL_LEVEL"></span> **Nivel** de/RL
</dt> <dd>

Valor que establece el nivel de ejecución de la tarea. Los valores válidos son LIMITED y HIGHEST.

**Windows XP y Windows Server 2003:** Esta opción no está disponible.

</dd> <dt>

<span id="_ENABLE_"></span><span id="_enable_"></span>**/ENABLE** 
</dt> <dd>

Valor que habilita la tarea programada. Se puede ejecutar una tarea habilitada y no se puede ejecutar una tarea deshabilitada.

**Windows XP y Windows Server 2003:** Esta opción no está disponible.

</dd> <dt>

<span id="_DISABLE_"></span><span id="_disable_"></span>**/DISABLE** 
</dt> <dd>

Valor que deshabilita la ejecución de la tarea programada.

> [!Note]  
> Si la tarea Remote Programador de tareas 1,0 está deshabilitada Schtasks.exe y el equipo remoto tiene habilitada la excepción de Firewall compartir archivos e impresoras y la excepción de Firewall administración remota de tareas programadas, la tarea no se deshabilitará cuando se lea desde una API de Programador de tareas 2,0.

 

**Windows XP y Windows Server 2003:** Esta opción no está disponible.

</dd> <dt>

<span id="_Z_"></span><span id="_z_"></span>**/Z** 
</dt> <dd>

Valor que marca la tarea que se va a eliminar después de su última ejecución.

**Windows XP y Windows Server 2003:** Esta opción no está disponible.

</dd> <dt>

<span id="_DELAY_delaytime"></span><span id="_delay_delaytime"></span><span id="_DELAY_DELAYTIME"></span>**/Delay** **Delaytime**
</dt> <dd>

Valor que especifica el tiempo de espera para retrasar la ejecución de la tarea después de que se desencadene el desencadenador. El formato de hora es mmmm: SS. Esta opción solo es válida para las tareas con los tipos de programación OnStart, ONLOGON e ONEVENT.

**Windows XP y Windows Server 2003:** Esta opción no está disponible.

</dd> <dt>

<span id="___"></span>**/?** 
</dt> <dd>

Valor que muestra el mensaje de ayuda para Schtasks.exe.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |



 

 





