---
title: Recopilador de eventos de Windows
description: Puede suscribirse para recibir y almacenar eventos en un equipo local (recopilador de eventos) que se reenvían desde un equipo remoto (origen de eventos).
ms.assetid: 7725e06d-4df1-4b3e-9f2f-2b8bdd805cb6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c4ef9e0cb647236daa55771222f25b7e0e370ef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695626"
---
# <a name="windows-event-collector"></a>Recopilador de eventos de Windows

Puede suscribirse para recibir y almacenar eventos en un equipo local (recopilador de eventos) que se reenvían desde un equipo remoto (origen de eventos). Las [funciones del recopilador de eventos de Windows](windows-event-collector-functions.md) admiten la suscripción a eventos mediante el protocolo WS-Management. Para obtener más información acerca de WS-Management, vea [acerca de administración remota de Windows](/windows/desktop/WinRM/about-windows-remote-management).

## <a name="event-forwarding-and-event-collection-architecture"></a>Arquitectura de recopilación de eventos y reenvío de eventos

La recopilación de eventos permite a los administradores obtener eventos de equipos remotos y almacenarlos en un registro de eventos local en el equipo del recopilador. La ruta de acceso del registro de destino para los eventos es una propiedad de la suscripción. Todos los datos del evento reenviado se guardan en el registro de eventos del equipo del recopilador (no se pierde ninguna información). También se agrega al evento información adicional relacionada con el reenvío de eventos. Para obtener más información sobre cómo habilitar un equipo para recibir eventos recopilados o reenviar eventos, consulte [configurar equipos para reenviar y recopilar eventos](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748890(v=ws.11)).

## <a name="subscriptions"></a>Suscripciones

En la lista siguiente se describen los tipos de suscripciones de eventos:

-   Suscripciones iniciadas por el origen: permite definir una suscripción de eventos en un equipo del recopilador de eventos sin definir los equipos de origen de eventos. A continuación, se pueden configurar varios equipos de origen de eventos remotos (mediante una configuración de directiva de grupo) para reenviar eventos al equipo del recopilador de eventos. Para obtener más información, consulte [configuración de una suscripción iniciada por el origen](setting-up-a-source-initiated-subscription.md). Este tipo de suscripción es útil cuando no se conoce o no se desea especificar todos los orígenes de eventos que van a reenviar eventos.
-   Suscripciones iniciadas por el recopilador: le permite crear una suscripción de eventos si conoce todos los equipos de origen de eventos que van a reenviar eventos. Especifique todos los orígenes de eventos en el momento en que se crea la suscripción. Para obtener más información, vea [crear una suscripción iniciada por el recopilador](creating-an-event-collector-subscription.md).

## <a name="windows-event-collector-functions"></a>Funciones del recopilador de eventos de Windows

Para obtener más información y ejemplos de código que usan las funciones del recopilador de eventos, vea [usar el recopilador de eventos de Windows](using-windows-event-collector.md).

Para obtener más información sobre las funciones que se usan para recopilar y reenviar eventos, consulte [funciones del recopilador de eventos de Windows](windows-event-collector-functions.md).

 

 