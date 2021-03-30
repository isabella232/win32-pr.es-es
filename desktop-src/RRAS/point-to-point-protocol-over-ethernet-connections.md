---
title: Protocolo punto a punto sobre conexiones Ethernet
description: Los sistemas operativos Windows Server 2003, Windows XP y versiones posteriores proporcionan compatibilidad con Protocolo punto a punto sobre Ethernet (PPPoE). En el caso de una conexión PPPoE, establezca los valores siguientes en la estructura RASENTRY.
ms.assetid: abdbf22c-abeb-4363-bfa6-e0002d1637f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eed66d3a694896bdec9e0f53215a782d5896cd38
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995555"
---
# <a name="point-to-point-protocol-over-ethernet-connections"></a>Protocolo punto a punto sobre conexiones Ethernet

Los sistemas operativos Windows Server 2003, Windows XP y versiones posteriores proporcionan compatibilidad con Protocolo punto a punto sobre Ethernet (PPPoE). En el caso de una conexión PPPoE, establezca los valores siguientes en la estructura [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) .



| Miembro                      | Valor             |
|-----------------------------|-------------------|
| RASENTRY.dwType             | \_Banda ancha Raset  |
| RAENTRY.szDeviceType        | RASDT \_ PPPoE      |
| RASENTRY.szLocalPhoneNumber | Nombre del servicio. |



 

Utilice la función [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) para establecer estos valores.

También puede usar [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) y la marca RASEDFLAG \_ NewBroadbandEntry para [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) para mostrar un asistente para crear una entrada de libreta de teléfonos de PPPoE.

 

 