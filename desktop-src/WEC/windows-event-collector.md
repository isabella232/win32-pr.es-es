---
title: Recopilador de eventos de Windows
description: Puede suscribirse para recibir y almacenar eventos en un equipo local (recopilador de eventos) que se reenvían desde un equipo remoto (origen del evento).
ms.assetid: 7725e06d-4df1-4b3e-9f2f-2b8bdd805cb6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1efa767ecb80960fc3461380435ea1d44992656d7c67df990574f7155ee976fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997885"
---
# <a name="windows-event-collector"></a>Recopilador de eventos de Windows

Puede suscribirse para recibir y almacenar eventos en un equipo local (recopilador de eventos) que se reenvían desde un equipo remoto (origen del evento). Las [Windows del recopilador de](windows-event-collector-functions.md) eventos admiten la suscripción a eventos mediante el protocolo WS-Management eventos. Para obtener más información sobre WS-Management, vea [About Windows Remote Management](/windows/desktop/WinRM/about-windows-remote-management).

## <a name="event-forwarding-and-event-collection-architecture"></a>Arquitectura de recopilación de eventos y reenvío de eventos

La recopilación de eventos permite a los administradores obtener eventos de equipos remotos y almacenarlos en un registro de eventos local en el equipo recopilador. La ruta de acceso del registro de destino para los eventos es una propiedad de la suscripción. Todos los datos del evento reenviado se guardan en el registro de eventos del equipo recopilador (no se pierde ninguna información). También se agrega al evento información adicional relacionada con el reenvío de eventos. Para obtener más información sobre cómo permitir que un equipo reciba eventos recopilados o reenviados, vea Configurar equipos para reenviar [y recopilar eventos](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748890(v=ws.11)).

## <a name="subscriptions"></a>Suscripciones

En la lista siguiente se describen los tipos de suscripciones de eventos:

-   Suscripciones iniciadas por el origen: permite definir una suscripción de eventos en un equipo del recopilador de eventos sin definir los equipos de origen de eventos. A continuación, se pueden configurar varios equipos de origen de eventos remotos (mediante una configuración de directiva de grupo) para reenviar eventos al equipo del recopilador de eventos. Para obtener más información, vea [Configurar una suscripción iniciada por el origen](setting-up-a-source-initiated-subscription.md). Este tipo de suscripción es útil cuando no conoce o no desea especificar todos los equipos de orígenes de eventos que reenviarán eventos.
-   Suscripciones iniciadas por el recopilador: le permite crear una suscripción de eventos si conoce todos los equipos de origen de eventos que reenviarán eventos. Especifique todos los orígenes de eventos en el momento de crear la suscripción. Para obtener más información, vea [Crear una suscripción iniciada por el recopilador.](creating-an-event-collector-subscription.md)

## <a name="windows-event-collector-functions"></a>Windows Funciones del recopilador de eventos

Para obtener más información y ejemplos de código que usan las funciones del recopilador de eventos, vea [Using Windows Event Collector](using-windows-event-collector.md).

Para obtener más información sobre las funciones que se usan para recopilar y reenviar eventos, [vea Windows event collector functions](windows-event-collector-functions.md).

 

 