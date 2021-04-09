---
title: Prácticas recomendadas de WinRM
description: En este tema se explican algunas de las prácticas recomendadas para usar las distintas características de la API de WinRM.
ms.assetid: FC2CD030-199F-43C2-804E-9827EA2A46D5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3452f2b8e61fb72b1fd5f99a073b48afb26dafb0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995307"
---
# <a name="winrm-best-practices"></a>Prácticas recomendadas de WinRM

En este tema se explican algunas de las prácticas recomendadas para usar las distintas características de la API de WinRM.

## <a name="quotas"></a>Cuotas

Cuando se alcanza una cuota, el servicio WinRM devuelve un error al cliente. Como resultado, la lógica del cliente debe reintentar explícitamente la operación según el error devuelto.

## <a name="event-subscriptions"></a>Suscripciones a eventos

Al usar suscripciones iniciadas por el recopilador, limite el número de equipos remotos a 500 y aísle el servicio [recopilador de eventos de Windows](/windows/desktop/WEC/windows-event-collector) (wecsvc) en un proceso de host independiente.

Un error de conexión contendrá un subproceso hasta que se agote el tiempo de espera. Un gran número de errores de conexión simultáneos puede provocar el agotamiento del grupo de subprocesos y dejar que el servidor deje de responder.

 

 