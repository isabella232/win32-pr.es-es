---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 40d26ea1-3081-4afd-8b12-bc6521fad390
ms.tgt_platform: multiple
title: E (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffbd1ce4685ee9901dfedca2a4b3a1b948d91c8f5b56def28494eb6c4c63e726
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118319224"
---
# <a name="e-wmi"></a>E (WMI)

[A](gloss-a.md) B [C](gloss-c.md) [D](gloss-d.md) E [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) M [N](gloss-m.md) [O](gloss-n.md) [](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z

<dl> <dt>

<span id="wmi.gloss_event_class"></span><span id="WMI.GLOSS_EVENT_CLASS"></span>**clase de eventos**
</dt> <dd>

Clase WMI a la *que los consumidores de* eventos pueden suscribirse mediante una consulta de *eventos*. La clase notifica un tipo específico de repetición. Por ejemplo, la [**clase \_ ProcessStopTrace de Win32**](/previous-versions/windows/desktop/krnlprov/win32-processstoptrace) informa de que se ha detenido un proceso específico.

</dd> <dt>

<span id="wmi.gloss_event_consumer"></span><span id="WMI.GLOSS_EVENT_CONSUMER"></span>**consumidor de eventos**
</dt> <dd>

Destinatario de las notificaciones que informan de la aparición de un evento. Un consumidor de eventos es [*temporal o*](gloss-t.md) [*permanente.*](gloss-p.md)

</dd> <dt>

<span id="wmi.gloss_event_consumer_provider"></span><span id="WMI.GLOSS_EVENT_CONSUMER_PROVIDER"></span>**proveedor de consumidores de eventos**
</dt> <dd>

Proveedor que determina qué consumidor de evento permanente controla un evento determinado. Un proveedor de consumidores de eventos se registra con WMI mediante una instancia de [](gloss-l.md) [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md), que contiene una lista de las clases de consumidor lógico que admite el proveedor de consumidores de eventos. Un proveedor de consumidores de eventos es un servidor COM que asigna [*consumidores físicos*](gloss-p.md) a *consumidores lógicos.* Un proveedor de consumidores de eventos admite [**la interfaz IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) y es un componente de la arquitectura de consumidor permanente.

</dd> <dt>

<span id="wmi.gloss_event_filter"></span><span id="WMI.GLOSS_EVENT_FILTER"></span>**filtro de eventos**
</dt> <dd>

Instancia de la [**\_ \_ clase del sistema EventFilter**](--eventfilter.md) que describe un tipo de evento y las condiciones para entregar una notificación. Un consumidor usa un filtro de eventos para registrarse para recibir la notificación de un tipo específico de evento.

</dd> <dt>

<span id="wmi.gloss_event_provider"></span><span id="WMI.GLOSS_EVENT_PROVIDER"></span>**proveedor de eventos**
</dt> <dd>

Proveedor WMI que supervisa un origen de eventos y notifica a WMI cuando se producen eventos. Un proveedor de eventos implementa las interfaces [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) [**e IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) y, a veces, [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink).

</dd> <dt>

<span id="wmi.gloss_event_query"></span><span id="WMI.GLOSS_EVENT_QUERY"></span>**consulta de eventos**
</dt> <dd>

Una [*lenguaje de consulta de WMI*](gloss-w.md) que los consumidores de eventos usan para registrarse y recibir notificaciones de eventos específicos. Un proveedor de eventos utiliza una consulta de eventos para registrarse y generar notificaciones de eventos concretos.

</dd> <dt>

<span id="wmi.gloss_extension_schema"></span><span id="WMI.GLOSS_EXTENSION_SCHEMA"></span>**esquema de extensión**
</dt> <dd>

La tercera capa del esquema [*CIM,*](gloss-c.md)que incluye extensiones específicas de la plataforma del esquema CIM, como Windows, UNIX y Exchange Server. Consulte también [*Common Model (Modelo común)*](gloss-c.md) y Core Model (Modelo principal).

</dd> <dt>

<span id="wmi.gloss_extrinsic_event"></span><span id="WMI.GLOSS_EXTRINSIC_EVENT"></span>**evento extrínsico**
</dt> <dd>

Notificación de eventos de un proveedor. La mayoría de los proveedores crean una instancia de una clase de eventos definida en los archivos MOF del proveedor. Un evento extrínsico hereda de [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md). Por ejemplo, el proveedor [de registro de eventos](/previous-versions/windows/desktop/eventlogprov/event-log-provider) define la clase de eventos [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent). Vea también [*el evento intrínseco*](gloss-i.md).

</dd> </dl>

 

 
