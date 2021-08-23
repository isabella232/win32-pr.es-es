---
title: Eventos (Windows administración remota)
description: El servicio Recopilador de eventos usa el WS-Management para recopilar eventos de equipos remotos.
ms.assetid: 5c8e0559-c576-4ac6-b636-c4a6fc399c9f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e081a0f4a5cea3f0ecac782a1dc5b07d3eae2160866f2582377a0e5e750f2133
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993805"
---
# <a name="events-windows-remote-management"></a>Eventos (Windows administración remota)

El servicio Recopilador de eventos usa el WS-Management para recopilar eventos de equipos remotos. Con el servicio Recopilador de eventos, puede crear suscripciones para Windows eventos en equipos remotos y eventos de hardware generados por controladores de administración de placa base (BMC). Los BMC deben admitir el WS-Management protocolo.

Al crear una suscripción, los eventos se reenvía al equipo en el que se ha creado la suscripción. Aparecerán en la Visor de eventos.

Los eventos de hardware generados por Intelligent Platform Management Interface (IPMI) en equipos basados en Windows se recopilan localmente mediante el controlador IPMI y se almacenan en el registro de eventos de hardware, después de lo cual se pueden reenviar como otros eventos del sistema operativo Windows.

Puede crear suscripciones mediante la herramienta Wecutil.exe línea de comandos. Para obtener más información sobre cómo usar esta herramienta, en un símbolo del sistema, **escriba wecutil /?**. Para obtener más información sobre el servicio Recopilador de eventos, [vea Windows Event Collector](/windows/desktop/WEC/windows-event-collector).

> [!Note]  
> Windows Las API de administración remota requieren que todas las direcciones IPv6 estén entre corchetes.

 

> [!Caution]
>
> Al usar suscripciones iniciadas por el recopilador, limite el número de equipos remotos a 500 y aísle el servicio recopilador de eventos de [Windows](/windows/desktop/WEC/windows-event-collector) (wecsvc) en un proceso de host independiente.
>
> Un error de conexión contendrán un subproceso hasta que se haya pasado el tiempo de espera. Un gran número de errores de conexión simultáneos puede provocar el agotamiento del grupo de subprocesos y hacer que el servidor deje de responder.

 

 

 
