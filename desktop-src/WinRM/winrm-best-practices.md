---
title: Procedimientos recomendados de WinRM
description: En este tema se explican algunos de los procedimientos recomendados para usar las distintas características de la API de WinRM.
ms.assetid: FC2CD030-199F-43C2-804E-9827EA2A46D5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dc780ec299c3249006085d348d983f8dab5b76a462c991a2d3665fed7d18f123
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733805"
---
# <a name="winrm-best-practices"></a>Procedimientos recomendados de WinRM

En este tema se explican algunos de los procedimientos recomendados para usar las distintas características de la API de WinRM.

## <a name="quotas"></a>Cuotas

Cuando se alcanzó una cuota, el servicio WinRM devuelve un error al cliente. Como resultado, la lógica de cliente debe reintentar explícitamente la operación en función del error devuelto.

## <a name="event-subscriptions"></a>Suscripciones a eventos

Al usar suscripciones iniciadas por el recopilador, limite el número de equipos remotos a 500 y aísle el servicio recopilador de eventos de [Windows](/windows/desktop/WEC/windows-event-collector) (wecsvc) en un proceso de host independiente.

Un error de conexión contendrán un subproceso hasta que se haya pasado el tiempo de espera. Un gran número de errores de conexión simultáneos puede provocar el agotamiento del grupo de subprocesos y hacer que el servidor deje de responder.

 

 