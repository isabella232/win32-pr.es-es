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
# <a name="retrieving-additional-event-tracing-data"></a><span data-ttu-id="f8ab7-103">Recuperación de datos de seguimiento de eventos adicionales</span><span class="sxs-lookup"><span data-stu-id="f8ab7-103">Retrieving Additional Event Tracing Data</span></span>

<span data-ttu-id="f8ab7-104">Una vez iniciada una sesión de seguimiento de eventos, puede usar [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) para indicar al sistema que devuelva datos de seguimiento de eventos adicionales.</span><span class="sxs-lookup"><span data-stu-id="f8ab7-104">Once you have begun an event tracing session, you can use [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) to instruct the system to return additional event tracing data.</span></span> <span data-ttu-id="f8ab7-105">La información adicional se colocará en la sección de datos extendidos del seguimiento de eventos pertinente.</span><span class="sxs-lookup"><span data-stu-id="f8ab7-105">The additional information will be placed in the extended data section of the relevant event trace.</span></span>

<span data-ttu-id="f8ab7-106">En el procedimiento siguiente se describe cómo usar la función [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) para recuperar datos adicionales de una sesión de seguimiento de eventos.</span><span class="sxs-lookup"><span data-stu-id="f8ab7-106">The following procedure describes how to use the [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) function to retrieve additional data from an event tracing session.</span></span>

<span data-ttu-id="f8ab7-107">**Para recuperar datos de seguimiento de eventos adicionales**</span><span class="sxs-lookup"><span data-stu-id="f8ab7-107">**To retrieve additional event tracing data**</span></span>

1.  <span data-ttu-id="f8ab7-108">Inicie la sesión con una llamada a [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea).</span><span class="sxs-lookup"><span data-stu-id="f8ab7-108">Start your session with a call to [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea).</span></span>

    <span data-ttu-id="f8ab7-109">Para obtener más información, vea [configurar e iniciar una sesión de seguimiento de eventos](configuring-and-starting-an-event-tracing-session.md).</span><span class="sxs-lookup"><span data-stu-id="f8ab7-109">For more information, see [Configuring and Starting an Event Tracing Session](configuring-and-starting-an-event-tracing-session.md).</span></span>

2.  <span data-ttu-id="f8ab7-110">Llame a [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) para establecer datos de seguimiento de eventos adicionales.</span><span class="sxs-lookup"><span data-stu-id="f8ab7-110">Call [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) to set additional event tracing data.</span></span>

    <span data-ttu-id="f8ab7-111">Use la enumeración [**\_ \_ clase de información de eventos**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) en el parámetro *ClassInformation* para describir la información adicional que desea recuperar.</span><span class="sxs-lookup"><span data-stu-id="f8ab7-111">use the [**EVENT\_INFO\_CLASS**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) enumeration in the *ClassInformation* parameter to describe the additional information you wish to retrieve.</span></span> <span data-ttu-id="f8ab7-112">En el ejemplo siguiente se describe cómo llamar a [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation)con el identificador de sesión devuelto por la llamada a [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)y el valor **TraceProviderBinaryTracking** de la **clase de \_ información \_ de evento**.</span><span class="sxs-lookup"><span data-stu-id="f8ab7-112">The following example describes how to call [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation), using the session handle returned from the call to [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea), and the **TraceProviderBinaryTracking** value from **EVENT\_INFO\_CLASS**.</span></span>

    ```C++
    BOOLEAN enabled = TRUE;
    Win32Error error = TraceSetInformation(
        m_sessionHandle,
        TraceProviderBinaryTracking,
        &enabled,
        sizeof(enabled));
    ```

    

3.  <span data-ttu-id="f8ab7-113">Como alternativa, puede usar [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) para recuperar información sobre la configuración de la sesión de seguimiento de eventos actual.</span><span class="sxs-lookup"><span data-stu-id="f8ab7-113">Alternately, you can use [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) to retrieve information about the current event tracing session settings.</span></span>

    <span data-ttu-id="f8ab7-114">Al igual que [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation), [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) usa la enumeración de [**clases de \_ información \_ de eventos**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) para describir la información que se debe recuperar del sistema.</span><span class="sxs-lookup"><span data-stu-id="f8ab7-114">Like [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation), [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation) uses the [**EVENT\_INFO\_CLASS**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class) enumeration to describe what information to retrieve from the system.</span></span>

 

 
