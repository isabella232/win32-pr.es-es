---
title: Eventos de Windows
description: Los eventos se suelen usar para solucionar problemas de software de aplicaciones y controladores. Antes de Windows Vista, usaría el seguimiento de eventos para Windows (ETW) o el registro de eventos para registrar los eventos. Windows Vista presentó un nuevo modelo de eventos que unifica tanto el seguimiento de eventos para Windows (ETW) como la API del registro de eventos de Windows. Windows 10 presenta TraceLogging, que se basa en ETW y proporciona una manera simplificada de instrumentar el código para los desarrolladores nativos, de .NET y de WinRT.
ms.assetid: c10baa8d-50b9-4fda-89d0-d00b1d9f5404
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c3d22580c38e45d06f5362e99626642eebdfe20
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077701"
---
# <a name="windows-events"></a>Eventos de Windows

Los eventos se suelen usar para solucionar problemas de software de aplicaciones y controladores.

-   Antes de Windows Vista, usaría el [seguimiento de eventos para Windows](/windows/desktop/ETW/event-tracing-portal) (ETW) o el [registro de eventos](/windows/desktop/EventLog/event-logging) para registrar los eventos.
-   Windows Vista presentó un nuevo modelo de eventos que unifica tanto el [seguimiento de eventos para Windows](/windows/desktop/ETW/event-tracing-portal) (ETW) como la API del [registro de eventos de Windows](/windows/desktop/WES/windows-event-log) .
-   Windows 10 presenta [TraceLogging](/windows/desktop/tracelogging/trace-logging-portal) , que se basa en ETW y proporciona una manera simplificada de instrumentar el código para los desarrolladores nativos, de .net y de WinRT.

El nuevo modelo [TraceLogging](/windows/desktop/tracelogging/trace-logging-portal) permite incluir datos estructurados con eventos, correlacionar eventos y no requiere un archivo XML de manifiesto de instrumentación independiente.

El modelo de Windows Vista utiliza un manifiesto XML para definir los eventos que desea publicar. Los eventos se pueden publicar en un canal o en una sesión de ETW. Puede publicar los eventos en los siguientes tipos de canales: admin, Operational, Analytics y Debug. Si solo usa ETW para habilitar el publicador, no es necesario especificar los canales en el manifiesto. Para obtener información detallada acerca de cómo escribir un manifiesto, consulte [escribir un manifiesto de instrumentación](/windows/desktop/WES/writing-an-instrumentation-manifest)y, para obtener información sobre los canales, consulte [definir canales](/windows/desktop/WES/defining-channels).

Para registrar el publicador de eventos y publicar eventos, se usa la API ETW. Para obtener más información, consulte [proporcionar eventos](/windows/desktop/ETW/providing-events) y [desarrollar un proveedor](/windows/desktop/WES/developing-a-provider). El publicador de eventos escribirá automáticamente los eventos en los canales especificados en el manifiesto, si están habilitados.

Si desea controlar los eventos que publica un publicador de eventos en un nivel más detallado de granularidad, use la API ETW. Por ejemplo, si el manifiesto define eventos de escritura y lectura, solo puede habilitar los eventos de escritura. Un evento también puede especificar un valor de nivel como advertencia o error, de modo que puede limitar los eventos que se escriben en los que especifican el nivel de error. Para obtener más información, vea [controlar las sesiones de seguimiento de eventos](/windows/desktop/ETW/controlling-event-tracing-sessions). Los eventos se escriben en el archivo de registro de la sesión.

El consumo de eventos implica la recuperación de los eventos de un canal de eventos, un archivo de registro de eventos (archivos. evtx o. evt), un archivo de seguimiento (archivos. ETL) o una sesión de ETW en tiempo real. Para consumir eventos de un archivo de seguimiento de ETW o una sesión de ETW en tiempo real, use las funciones de la aplicación auxiliar de datos de seguimiento (TDH) en ETW para consumir los eventos. También puede usar TDH para leer los metadatos del evento. Para obtener más información, consulte [consumo de eventos](/windows/desktop/ETW/consuming-events). Para consumir eventos de un canal de eventos o de un archivo de registro de eventos, use las funciones del registro de eventos de Windows para consultar o suscribirse a eventos. Para obtener más información, vea [consultar eventos](/windows/desktop/WES/querying-for-events) o [suscribirse a eventos](/windows/desktop/WES/subscribing-to-events).

Antes de Windows Vista, debe usar el [seguimiento de eventos para Windows](/windows/desktop/ETW/event-tracing-portal) o el [registro de eventos](/windows/desktop/EventLog/event-logging) para publicar y consumir eventos.

 

 