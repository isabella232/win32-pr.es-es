---
description: Las siguientes funciones se usan con la hora del sistema.
ms.assetid: 3733f611-c6a1-4d48-b21e-ada3490c5de1
title: Funciones Time
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1187c029bac34411fdca28dd3b27322478de678
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668152"
---
# <a name="time-functions"></a>Funciones Time

Las siguientes funciones se usan con la hora del sistema.



| Función                                                                   | Descripción                                                                                            |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**GetSystemTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtime)                                     | Recupera la fecha y hora actuales del sistema en formato UTC.                                              |
| [**GetSystemTimeAdjustment**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeadjustment)                 | Determina si el sistema está aplicando ajustes de hora periódicos a su reloj de hora del día.          |
| [**GetTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata)                                    | Da formato a una hora del sistema como una cadena de hora para una configuración regional especificada.                                         |
| [**NtQuerySystemTime**](/windows/desktop/api/Winternl/nf-winternl-ntquerysystemtime)                             | Devuelve la hora del sistema.                                                                               |
| [**RtlLocalTimeToSystemTime**](/windows/desktop/api/Winternl/nf-winternl-rtllocaltimetosystemtime)               | Convierte la hora local especificada en la hora del sistema.                                                      |
| [**RtlTimeToSecondsSince1970**](/windows/desktop/api/Winternl/nf-winternl-rtltimetosecondssince1970)             | Convierte la hora del sistema especificada en el número de segundos transcurridos desde el primer segundo del 1 de enero de 1970. |
| [**SetSystemTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setsystemtime)                                     | Establece la fecha y hora actuales del sistema.                                                                 |
| [**SetSystemTimeAdjustment**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setsystemtimeadjustment)                 | Habilita o deshabilita los ajustes periódicos del tiempo en el reloj del sistema del sistema.                       |
| [**SystemTimeToFileTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetofiletime)                       | Convierte una hora del sistema en una hora de archivo.                                                                 |
| [**SystemTimeToTzSpecificLocalTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltime) | Convierte una hora UTC en la hora local correspondiente de la zona horaria especificada.                               |
| [**TzSpecificLocalTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-tzspecificlocaltimetosystemtime) | Convierte una hora local a una hora UTC.                                                                   |



 

Las siguientes funciones se usan con la hora local.



| Función                                                                                           | Descripción                                                                                                                                     |
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumDynamicTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-enumdynamictimezoneinformation)                           | Enumera las entradas de información del horario de verano dinámica almacenadas en el registro.                                                             |
| [**FileTimeToLocalFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-filetimetolocalfiletime)                                         | Convierte una hora de archivo UTC en una hora de archivo local.                                                                                                  |
| [**GetDynamicTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-getdynamictimezoneinformation)                             | Recupera la zona horaria actual y la configuración dinámica del horario de verano.                                                                      |
| [**GetDynamicTimeZoneInformationEffectiveYears**](/windows/win32/api/timezoneapi/nf-timezoneapi-getdynamictimezoneinformationeffectiveyears) | Recupera un intervalo, expresado en años, para el que una [**\_ información de \_ zona \_ horaria dinámica**](/windows/win32/api/timezoneapi/ns-timezoneapi-dynamic_time_zone_information) tiene entradas válidas. |
| [**GetLocalTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlocaltime)                                                               | Recupera la fecha y hora locales actuales.                                                                                                      |
| [**GetTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-gettimezoneinformation)                                           | Recupera la configuración de zona horaria actual.                                                                                                       |
| [**GetTimeZoneInformationForYear**](/windows/win32/api/timezoneapi/nf-timezoneapi-gettimezoneinformationforyear)                             | Recupera la configuración de zona horaria para el año y la zona horaria especificados.                                                                          |
| [**RtlLocalTimeToSystemTime**](/windows/desktop/api/Winternl/nf-winternl-rtllocaltimetosystemtime)                                       | Convierte la hora local especificada en la hora del sistema.                                                                                               |
| [**SetDynamicTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-setdynamictimezoneinformation)                             | Establece la zona horaria actual y la configuración dinámica del horario de verano.                                                                           |
| [**SetLocalTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setlocaltime)                                                               | Establece la hora local y la fecha actuales.                                                                                                           |
| [**SetTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-settimezoneinformation)                                           | Establece la configuración de zona horaria actual.                                                                                                            |
| [**SystemTimeToTzSpecificLocalTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltime)                         | Convierte una hora UTC en la hora local correspondiente de la zona horaria especificada.                                                                        |
| [**SystemTimeToTzSpecificLocalTimeEx**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltimeex)                     | Convierte una hora UTC con la configuración dinámica del horario de verano en la hora local correspondiente de la zona horaria especificada.                             |
| [**TzSpecificLocalTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-tzspecificlocaltimetosystemtime)                         | Convierte una hora local a una hora UTC.                                                                                                            |
| [**TzSpecificLocalTimeToSystemTimeEx**](/windows/win32/api/timezoneapi/nf-timezoneapi-tzspecificlocaltimetosystemtimeex)                     | Convierte una hora local con la configuración dinámica del horario de verano.                                                                   |



 

Las siguientes funciones se usan con la hora de archivo.



| Función                                                   | Descripción                                                                                                     |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**CompareFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-comparefiletime)                 | Compara dos horas de archivo.                                                                                        |
| [**FileTimeToLocalFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-filetimetolocalfiletime) | Convierte una hora de archivo UTC en una hora de archivo local.                                                                  |
| [**FileTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-filetimetosystemtime)       | Convierte una hora de archivo en el formato de hora del sistema.                                                                     |
| [**GetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime)                         | Recupera la fecha y la hora en que se creó el archivo o directorio especificado, se obtuvo acceso por última vez y se modificó por última vez. |
| [**GetSystemTimeAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime) | Recupera la fecha y hora actuales del sistema en formato UTC.                                                       |
| [**LocalFileTimeToFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-localfiletimetofiletime) | Convierte una hora de archivo local en una hora de archivo basándose en la hora UTC.                                                         |
| [**SetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-setfiletime)                         | Establece la fecha y la hora en que se creó el archivo o directorio especificado, se obtuvo acceso por última vez o se modificó por última vez.       |
| [**SystemTimeToFileTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetofiletime)       | Convierte una hora del sistema en una hora de archivo.                                                                          |



 

Las siguientes funciones se usan con la fecha y hora de MS-DOS.



| Función                                               | Descripción                                          |
|--------------------------------------------------------|------------------------------------------------------|
| [**DosDateTimeToFileTime**](/windows/desktop/api/Winbase/nf-winbase-dosdatetimetofiletime) | Convierte los valores de fecha y hora de MS-DOS en una hora de archivo. |
| [**FileTimeToDosDateTime**](/windows/desktop/api/Winbase/nf-winbase-filetimetodosdatetime) | Convierte una hora de archivo en valores de fecha y hora de MS-DOS. |



 

Las siguientes funciones se usan con la hora de Windows.



| Función                                 | Descripción                                                                                           |
|------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**GetSystemTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes) | Recupera la información de tiempo del sistema.                                                                  |
| [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount)     | Recupera el número de milisegundos transcurridos desde que se inició el sistema hasta 49,7 días. |
| [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) | Recupera el número de milisegundos transcurridos desde que se inició el sistema.                  |



 

Las siguientes funciones se usan con los contadores de rendimiento de alta resolución.



| Función                                                              | Descripción                                                             |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)     | Recupera el valor actual del contador de rendimiento de alta resolución. |
| [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) | Recupera la frecuencia del contador de rendimiento de alta resolución.     |



 

Las siguientes funciones se usan con el contador de rendimiento auxiliar.



| Función                                                                                           | Descripción                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**QueryAuxiliaryCounterFrequency**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryauxiliarycounterfrequency)                           | Consulta la frecuencia del contador auxiliar.                                                                                                                                                                      |
| [**ConvertAuxiliaryCounterToPerformanceCounter**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-convertauxiliarycountertoperformancecounter) | Convierte el valor del contador auxiliar especificado en el valor del contador de rendimiento correspondiente; Opcionalmente, proporciona el error de conversión estimado en nanosegundos debido a latencias y el máximo posible desplazamiento. |
| [**ConvertPerformanceCounterToAuxiliaryCounter**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-convertperformancecountertoauxiliarycounter) | Convierte el valor del contador de rendimiento especificado en el valor del contador auxiliar correspondiente; Opcionalmente, proporciona el error de conversión estimado en nanosegundos debido a latencias y el máximo posible desplazamiento. |



 

La siguiente función se usa con tiempo de interrupción.



| Función                                                                       | Descripción                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime)                               | Obtiene el recuento actual de tiempo de interrupción.                                                                                                                                                                                                                |
| [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise)                 | Obtiene el recuento actual de tiempo de interrupción, en un formato más preciso que [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime) .                                                                                                                             |
| [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)               | Obtiene el recuento de tiempo de interrupción no sesgado actual. El recuento de tiempo de interrupción no sesgado no incluye el tiempo que el sistema invierte en suspensión o hibernación.                                                                                                    |
| [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) | Obtiene el recuento de tiempo de interrupción no sesgado actual, en un formato más preciso que [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) . El recuento de tiempo de interrupción no sesgado no incluye el tiempo que el sistema invierte en suspensión o hibernación. |



 

 

 
