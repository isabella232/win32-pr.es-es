---
description: Una vez iniciada una sesión de seguimiento de eventos, puede usar TraceSetInformation para indicar al sistema que devuelva datos de seguimiento de eventos adicionales.
ms.assetid: 65CCD658-869E-40C4-83AE-34CC2720B7CB
title: Recuperación de datos de seguimiento de eventos adicionales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef864de40b924e0210603646d5ba5430d5d9b643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001335"
---
# <a name="retrieving-additional-event-tracing-data"></a>Recuperación de datos de seguimiento de eventos adicionales

Una vez iniciada una sesión de seguimiento de eventos, puede usar [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) para indicar al sistema que devuelva datos de seguimiento de eventos adicionales. La información adicional se colocará en la sección de datos extendidos del seguimiento de eventos pertinente.

En el procedimiento siguiente se describe cómo usar la función [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) para recuperar datos adicionales de una sesión de seguimiento de eventos.

**Para recuperar datos de seguimiento de eventos adicionales**

1.  Inicie la sesión con una llamada a [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea).

    Para obtener más información, vea [configurar e iniciar una sesión de seguimiento de eventos](configuring-and-starting-an-event-tracing-session.md).

2.  Llame a [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) para establecer datos de seguimiento de eventos adicionales.

    Use la enumeración [**\_ \_ clase de información de eventos**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) en el parámetro *ClassInformation* para describir la información adicional que desea recuperar. En el ejemplo siguiente se describe cómo llamar a [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation)con el identificador de sesión devuelto por la llamada a [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)y el valor **TraceProviderBinaryTracking** de la **clase de \_ información \_ de evento**.

    ```C++
    BOOLEAN enabled = TRUE;
    Win32Error error = TraceSetInformation(
        m_sessionHandle,
        TraceProviderBinaryTracking,
        &enabled,
        sizeof(enabled));
    ```

    

3.  Como alternativa, puede usar [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) para recuperar información sobre la configuración de la sesión de seguimiento de eventos actual.

    Al igual que [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation), [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) usa la enumeración de [**clases de \_ información \_ de eventos**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) para describir la información que se debe recuperar del sistema.

 

 
