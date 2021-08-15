---
description: Una vez que haya iniciado una sesión de seguimiento de eventos, puede usar TraceSetInformation para indicar al sistema que devuelva datos de seguimiento de eventos adicionales.
ms.assetid: 65CCD658-869E-40C4-83AE-34CC2720B7CB
title: Recuperación de datos de seguimiento de eventos adicionales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afbae65e516a63154fb76d3d558e02e9533e58e119e977f851c2404f0a218ec5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393903"
---
# <a name="retrieving-additional-event-tracing-data"></a>Recuperación de datos de seguimiento de eventos adicionales

Una vez que haya iniciado una sesión de seguimiento de eventos, puede usar [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) para indicar al sistema que devuelva datos de seguimiento de eventos adicionales. La información adicional se colocará en la sección de datos extendidos del seguimiento de eventos pertinente.

En el procedimiento siguiente se describe cómo usar la [**función TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) para recuperar datos adicionales de una sesión de seguimiento de eventos.

**Para recuperar datos de seguimiento de eventos adicionales**

1.  Inicie la sesión con una llamada a [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea).

    Para obtener más información, vea [Configuring and Starting an Event Tracing Session](configuring-and-starting-an-event-tracing-session.md).

2.  Llame [**a TraceSetInformation para**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) establecer datos de seguimiento de eventos adicionales.

    use la [**enumeración EVENT \_ INFO \_ CLASS**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) del *parámetro ClassInformation* para describir la información adicional que desea recuperar. En el ejemplo siguiente se describe cómo llamar a [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation)mediante el identificador de sesión devuelto por la llamada a [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)y el valor **TraceProviderBinaryTracking** de **EVENT INFO \_ \_ CLASS**.

    ```C++
    BOOLEAN enabled = TRUE;
    Win32Error error = TraceSetInformation(
        m_sessionHandle,
        TraceProviderBinaryTracking,
        &enabled,
        sizeof(enabled));
    ```

    

3.  Como alternativa, puede usar [**TraceQueryInformation para**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) recuperar información sobre la configuración actual de la sesión de seguimiento de eventos.

    Al [**igual que TraceSetInformation,**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) [**TraceQueryInformation usa**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) la [**enumeración EVENT INFO \_ \_ CLASS**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) para describir qué información se va a recuperar del sistema.

 

 
