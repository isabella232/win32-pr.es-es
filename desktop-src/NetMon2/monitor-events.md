---
description: Los monitores están diseñados para usar Instrumental de administración de Windows (WMI) para activar eventos en equipos locales o remotos.
ms.assetid: b20746dd-d8d9-49b6-95b7-5151ee02901d
title: Supervisar eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d98241081d8a59c33ab173447eaedd903e72eb09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497614"
---
# <a name="monitor-events"></a>Supervisar eventos

Los monitores están diseñados para usar [instrumental de administración de Windows](/windows/desktop/WmiSdk/wmi-start-page) (WMI) para activar eventos en equipos locales o remotos.

> [!Note]  
> Dado que los monitores usan una captura en tiempo real, solo pueden capturar datos en el equipo local. Se trata de una limitación de la interfaz **IRTC** del proveedor de paquetes de red. Sin embargo, mediante el uso de eventos de WMI, los datos capturados se pueden examinar localmente mientras se pueden enviar eventos a equipos locales o remotos.

 

Los monitores no se comunican directamente con WMI. El [*servicio de control de supervisión*](m.md) (MCSVC) proporciona una interfaz (denominada [IMonitorEventer](imonitoreventer.md)) que el monitor puede utilizar para obtener una estructura de datos de evento y rellenarla con la información pertinente. A continuación, MCSVC puede enviar la estructura de datos de evento a WMI, que a su vez activa el evento.

 

 
