---
description: La hora de Windows es el número de milisegundos transcurridos desde la última vez que se inició el sistema.
ms.assetid: 95c00204-bfdf-4376-9aae-8d8139ba6750
title: Hora de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33af776e2cc5a36993f6be0e0776d5b73fab6622
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156129"
---
# <a name="windows-time"></a>Hora de Windows

La *hora de Windows* es el número de milisegundos transcurridos desde la última vez que se inició el sistema. Este formato existe principalmente para la compatibilidad con versiones anteriores de Windows de 16 bits. Para asegurarse de que las aplicaciones diseñadas para Windows de 16 bits sigan ejecutándose correctamente, la función [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) devuelve la hora actual de Windows.

Normalmente se usa la función [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) o [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) para comparar la hora actual de Windows con la hora devuelta por la función [**GetMessageTime**](/windows/win32/api/winuser/nf-winuser-getmessagetime) . **GetMessageTime** devuelve la hora de Windows en la que se creó el mensaje especificado. **GetTickCount** y **GetTickCount64** se limitan a la resolución del temporizador del sistema, que es aproximadamente de 10 milisegundos a 16 milisegundos. El tiempo transcurrido recuperado por **GetTickCount** o **GetTickCount64** incluye el tiempo que el sistema invierte en suspensión o hibernación.

Si necesita un temporizador de mayor resolución, use la función [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) , un [temporizador multimedia](/windows/desktop/Multimedia/multimedia-timers)o un [temporizador de alta resolución](../winmsg/about-timers.md). El tiempo transcurrido recuperado por la función **QueryUnbiasedInterruptTime** solo incluye el tiempo que el sistema invierte en el estado de funcionamiento.

**Windows server 2008, Windows Vista, Windows server 2003 y Windows XP/2000:** La función [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) está disponible a partir de Windows 7 y windows Server 2008 R2.

Puede usar el contador de rendimiento del sistema de tiempo de actividad para obtener el número de segundos transcurridos desde que se inició el equipo. Este contador de rendimiento se puede recuperar de los datos de rendimiento en la clave del registro **HKEY \_ performance \_ Data**. El valor devuelto es un valor de 8 bytes. Para más información, consulte [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).

 

 
