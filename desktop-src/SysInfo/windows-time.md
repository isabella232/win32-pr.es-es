---
description: Windows tiempo es el número de milisegundos transcurridos desde que se inició por última vez el sistema.
ms.assetid: 95c00204-bfdf-4376-9aae-8d8139ba6750
title: Hora de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 363f455842a144decc9db7f4d15fa3353b16e74290252b911a814eb62832a790
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118884051"
---
# <a name="windows-time"></a>Hora de Windows

*Windows tiempo es* el número de milisegundos transcurridos desde que se inició por última vez el sistema. Este formato existe principalmente por compatibilidad con versiones anteriores con archivos de 16 Windows. Para asegurarse de que las aplicaciones diseñadas para Windows de 16 bits siguen funcionando correctamente, la función [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) devuelve la hora Windows actual.

Normalmente se usan las funciones [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) o [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) para comparar la hora Windows actual con la hora devuelta por la [**función GetMessageTime.**](/windows/win32/api/winuser/nf-winuser-getmessagetime) **GetMessageTime** devuelve la Windows hora en que se creó el mensaje especificado. **GetTickCount** y **GetTickCount64** se limitan a la resolución del temporizador del sistema, que es aproximadamente de 10 milisegundos a 16 milisegundos. El tiempo transcurrido recuperado por **GetTickCount** o **GetTickCount64** incluye el tiempo que el sistema pasa en suspensión o hibernación.

Si necesita un temporizador de mayor resolución, use la función [**QueryUnbiasedInterruptTime,**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) un [temporizador multimedia](/windows/desktop/Multimedia/multimedia-timers)o un temporizador [de alta resolución](../winmsg/about-timers.md). El tiempo transcurrido recuperado por la función **QueryUnbiasedInterruptTime** incluye solo el tiempo que el sistema pasa en el estado de trabajo.

**Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP/2000:** La [**función QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) está disponible a partir de Windows 7 y Windows Server 2008 R2.

Puede usar el contador de rendimiento Tiempo de funcionamiento del sistema para obtener el número de segundos transcurridos desde que se inició el equipo. Este contador de rendimiento se puede recuperar de los datos de rendimiento de la clave del Registro **HKEY \_ PERFORMANCE \_ DATA**. El valor devuelto es un valor de 8 bytes. Para más información, consulte [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).

 

 
