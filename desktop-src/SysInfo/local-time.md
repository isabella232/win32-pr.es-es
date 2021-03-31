---
description: Aunque el sistema utiliza la hora basada en UTC internamente, las aplicaciones suelen mostrar la hora local, que es la fecha y la hora del día de la zona horaria.
ms.assetid: a6570ec5-ac77-427a-86d9-32cbecc62e37
title: Hora local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c60eb9ca53245a12eba1bc0096b522eae97de75a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908163"
---
# <a name="local-time"></a>Hora local

Aunque el sistema utiliza la hora basada en UTC internamente, las aplicaciones suelen mostrar la **hora local**, que es la fecha y la hora del día de la zona horaria. Por lo tanto, para asegurarse de que los resultados son correctos, debe tener en cuenta si una función espera recibir una hora basada en UTC o una hora local, y si la función devuelve una hora basada en UTC o una hora local.

La configuración de zona horaria actual controla cómo el sistema convierte entre la hora UTC y la hora local. Puede recuperar la configuración de zona horaria actual mediante la función [**GetTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-gettimezoneinformation) . La función copia el resultado en una estructura de [**\_ \_ información de zona horaria**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) y devuelve un valor que indica si la hora local está actualmente en horario estándar o en horario de verano (DST). Puede establecer la configuración de zona horaria mediante la función [**SetTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-settimezoneinformation) . Para admitir límites para el horario de verano que cambian de un año a otro, use las funciones [**GetTimeZoneInformationForYear**](/windows/win32/api/timezoneapi/nf-timezoneapi-gettimezoneinformationforyear), [**GetDynamicTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-getdynamictimezoneinformation) y [**SetDynamicTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-setdynamictimezoneinformation) .

Para recuperar la hora local, utilice la función [**GetLocalTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlocaltime) . **GetLocalTime** convierte la hora del sistema en una hora local en función de la configuración actual de la zona horaria y copia el resultado en una estructura [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) . Puede establecer la hora del sistema mediante la función [**SetLocalTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setlocaltime) . **SetLocalTime** supone que ha especificado una hora local y se convierte en UTC antes de establecer la hora del sistema.

Cuando se llama a [**SetLocalTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setlocaltime), el sistema usa la información de zona horaria actual, incluido el valor de horario de verano, para realizar la conversión. Tenga en cuenta que el sistema utiliza la configuración de horario de verano de la hora actual, no la nueva hora que se establece. Por lo tanto, para garantizar el resultado correcto, llame a **SetLocalTime** por segunda vez, ahora que la primera llamada ha actualizado el valor de horario de verano.

Para convertir una hora basada en UTC en una hora local, utilice la función [**SystemTimeToTzSpecificLocalTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltime) . Para convertir una hora local a una hora basada en UTC, utilice la función [**TzSpecificLocalTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-tzspecificlocaltimetosystemtime) .

 

 
