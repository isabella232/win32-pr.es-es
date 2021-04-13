---
title: Eventos (Administración remota de Windows)
description: El servicio Recopilador de eventos usa el protocolo WS-Management para recopilar eventos de equipos remotos.
ms.assetid: 5c8e0559-c576-4ac6-b636-c4a6fc399c9f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 06f96877904a5e76ea61a6b2f636e962e4dbd9b9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421765"
---
# <a name="events-windows-remote-management"></a>Eventos (Administración remota de Windows)

El servicio Recopilador de eventos usa el protocolo WS-Management para recopilar eventos de equipos remotos. Con el servicio Recopilador de eventos, puede crear suscripciones a eventos de Windows en equipos remotos y eventos de hardware generados por los controladores de administración de placa base (BMC). Los BMC deben admitir el protocolo de WS-Management.

Cuando se crea una suscripción, los eventos se reenvían al equipo en el que se ha creado la suscripción. Aparecerán en el Visor de eventos.

Los eventos de hardware generados por la interfaz de administración de plataforma inteligente (IPMI) en equipos basados en Windows se recopilan localmente mediante el controlador IPMI y se almacenan en el registro de eventos de hardware, después del cual se pueden reenviar como otros eventos del sistema operativo Windows.

Puede crear suscripciones mediante la herramienta de línea de comandos Wecutil.exe. Para obtener más información sobre cómo usar esta herramienta, escriba **wecutil/?** en el símbolo del sistema. Para obtener más información sobre el servicio Recopilador de eventos, vea [recopilador de eventos de Windows](/windows/desktop/WEC/windows-event-collector).

> [!Note]  
> Administración remota de Windows API requieren que todas las direcciones IPv6 estén entre corchetes.

 

> [!Caution]
>
> Al usar suscripciones iniciadas por el recopilador, limite el número de equipos remotos a 500 y aísle el servicio [recopilador de eventos de Windows](/windows/desktop/WEC/windows-event-collector) (wecsvc) en un proceso de host independiente.
>
> Un error de conexión contendrá un subproceso hasta que se agote el tiempo de espera. Un gran número de errores de conexión simultáneos puede provocar el agotamiento del grupo de subprocesos y dejar que el servidor deje de responder.

 

 

 
