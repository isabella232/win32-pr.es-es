---
title: Protocolo punto a punto a través de conexiones Ethernet
description: Windows Server 2003, Windows XP y sistemas operativos posteriores proporcionan compatibilidad con Protocolo punto a punto a través de Ethernet (PPPoE). Para una conexión PPPoE, establezca los siguientes valores en la estructura RASENTRY.
ms.assetid: abdbf22c-abeb-4363-bfa6-e0002d1637f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92703bac13d129ed29cee1c22328825de67325239c1906c1728b96d53398647b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789815"
---
# <a name="point-to-point-protocol-over-ethernet-connections"></a>Protocolo punto a punto a través de conexiones Ethernet

Windows Server 2003, Windows XP y sistemas operativos posteriores proporcionan compatibilidad con Protocolo punto a punto a través de Ethernet (PPPoE). Para una conexión PPPoE, establezca los siguientes valores en la [**estructura RASENTRY.**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85))



| Miembro                      | Valor             |
|-----------------------------|-------------------|
| RASENTRY.dwType             | Banda \_ ancha RASET  |
| RAENTRY.szDeviceType        | RASDT \_ PPPoE      |
| RASENTRY.szLocalPhoneNumber | Nombre del servicio. |



 

Use la [**función RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) para establecer estos valores.

También puede usar [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) y la marca RASEDFLAG \_ NewBroadbandEntry para [**RASENTRYDLG**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) para mostrar un asistente para crear una entrada de la guía telefónica PPPoE.

 

 