---
description: Aunque el sistema usa la hora basada en UTC internamente, las aplicaciones generalmente mostrarán la hora local, que es la fecha y hora del día para la zona horaria.
ms.assetid: a6570ec5-ac77-427a-86d9-32cbecc62e37
title: Hora local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95835b76f09ae328c3e1509da68e0fbd989286b2e2669efc9f2280dbce72e35a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117764004"
---
# <a name="local-time"></a>Hora local

Aunque el sistema usa la hora basada en UTC internamente, las aplicaciones generalmente mostrarán la hora **local**, que es la fecha y hora del día para la zona horaria. Por lo tanto, para garantizar resultados correctos, debe tener en cuenta si una función espera recibir una hora UTC o una hora local, y si la función devuelve una hora utc o una hora local.

La configuración de zona horaria actual controla cómo se convierte el sistema entre la hora UTC y la hora local. Puede recuperar la configuración de zona horaria actual mediante la [**función GetTimeZoneInformation.**](/windows/win32/api/timezoneapi/nf-timezoneapi-gettimezoneinformation) La función copia el resultado en una estructura [**TIME \_ ZONE \_ INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) y devuelve un valor que indica si la hora local está actualmente en horario estándar o en horario de verano (DST). Puede establecer la configuración de zona horaria mediante la [**función SetTimeZoneInformation.**](/windows/win32/api/timezoneapi/nf-timezoneapi-settimezoneinformation) Para admitir los límites del horario de verano que cambian de año a año, use las funciones [**GetTimeZoneInformationForYear**](/windows/win32/api/timezoneapi/nf-timezoneapi-gettimezoneinformationforyear), [**GetDynamicTimeZoneInformation**](/windows/win32/api/timezoneapi/nf-timezoneapi-getdynamictimezoneinformation) y [**SetDynamicTimeZoneInformation.**](/windows/win32/api/timezoneapi/nf-timezoneapi-setdynamictimezoneinformation)

Para recuperar la hora local, use la [**función GetLocalTime.**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlocaltime) **GetLocalTime** convierte la hora del sistema en una hora local en función de la configuración de zona horaria actual y copia el resultado en una [**estructura SYSTEMTIME.**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) Puede establecer la hora del sistema mediante la [**función SetLocalTime.**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setlocaltime) **SetLocalTime supone** que ha especificado una hora local y se convierte a UTC antes de establecer la hora del sistema.

Cuando se llama a [**SetLocalTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setlocaltime), el sistema usa la información de zona horaria actual, incluida la configuración del horario de verano, para realizar la conversión. Tenga en cuenta que el sistema usa la configuración del horario de verano de la hora actual, no la nueva hora que está estableciendo. Por lo tanto, para garantizar el resultado correcto, llame a **SetLocalTime** una segunda vez, ahora que la primera llamada ha actualizado la configuración del horario de verano.

Para convertir una hora basada en UTC a una hora local, use la [**función SystemTimeToTzSpecificLocalTime.**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltime) Para convertir una hora local a una hora utc, use la [**función TzSpecificLocalTimeToSystemTime.**](/windows/win32/api/timezoneapi/nf-timezoneapi-tzspecificlocaltimetosystemtime)

 

 
