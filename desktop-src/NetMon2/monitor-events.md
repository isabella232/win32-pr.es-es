---
description: Los monitores están diseñados para usar Windows Management Instrumentation (WMI) para que active eventos en equipos locales o remotos.
ms.assetid: b20746dd-d8d9-49b6-95b7-5151ee02901d
title: Supervisar eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ebe76ddd8df02694f871899e0b172dda3529fc29c0e16b6b4a65e2ad15bd2ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995485"
---
# <a name="monitor-events"></a>Supervisar eventos

Los monitores están diseñados [para usar Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-start-page) (WMI) para que active eventos en equipos locales o remotos.

> [!Note]  
> Dado que los monitores usan una captura en tiempo real, solo pueden capturar datos en el equipo local. Se trata de una limitación de la interfaz **IRTC** del proveedor de paquetes de red. Sin embargo, mediante el uso de eventos WMI, los datos capturados se pueden examinar localmente mientras los eventos se pueden enviar a equipos locales o remotos.

 

Los monitores no se comunican directamente con WMI. Monitor [*Control Service*](m.md) (MCSVC) proporciona una interfaz (denominada [IMonitorEventer),](imonitoreventer.md)que el monitor puede usar para obtener una estructura de datos de eventos y rellenarla con la información pertinente. A continuación, MCSVC puede enviar la estructura de datos de eventos a WMI, que a su vez activa el evento.

 

 
