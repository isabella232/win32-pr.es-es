---
description: En esta sección se describen las nuevas características que se agregaron al seguimiento de eventos Windows en cada versión.
ms.assetid: 5d94a6d2-2280-4a97-aa5a-c9ca2c016c84
title: Novedades del seguimiento de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2da1c6f1b54ae8bc4b91bd511bface8569bcf43b2893329b1b0462b46c001724
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102025"
---
# <a name="whats-new-in-event-tracing"></a>Novedades del seguimiento de eventos

En esta sección se describen las nuevas características que se agregaron al seguimiento de eventos Windows en cada versión.

## <a name="windows-10-version-1709"></a>Windows 10, versión 1709

ETW ahora puede realizar un seguimiento opcional de los archivos binarios de todos los proveedores que están habilitados para la sesión. El seguimiento se aplica con carácter retroactivo a los proveedores que se habilitaron en la sesión antes de la llamada, así como a todos los proveedores futuros que están habilitados para la sesión. Ahora también puede consultar el número máximo configurado actualmente de registradores del sistema permitidos por el sistema operativo. Para obtener más información, vea los valores **TraceProviderBinaryTracking** y **TraceMaxLoggersQuery** de la enumeración [**TRACE INFO \_ \_ CLASS,**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class) así como [Retrieving Additional Event Tracing Data](retrieving-additional-event-tracing-data.md).

ETW ahora puede filtrar eventos en función del nombre del evento. También puede determinar qué eventos capturan sus pilas. Para obtener más información, vea los valores EVENT NAME de **EVENT \_ \_ \_ \_ FILTER TYPE**, EVENT FILTER TYPE **\_ \_ \_ STACKWALK \_ NAME** y **EVENT FILTER TYPE \_ \_ \_ STACKWALK LEVEL \_ \_ KW** de la estructura EVENT [**FILTER \_ \_ DESCRIPTOR,**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) así como las estructuras [**EVENT FILTER EVENT \_ \_ \_ NAME**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_event_name) y [**EVENT FILTER LEVEL \_ \_ \_ KW**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_level_kw) asociadas.

## <a name="windows-10"></a>Windows 10

[TraceLogging](../tracelogging/trace-logging-portal.md) se basa en ETW y proporciona una manera simplificada de instrumentar código para desarrolladores nativos de .NET y WinRT. TraceLogging permite incluir datos estructurados con eventos, correlacionar eventos y no requiere un archivo XML de manifiesto de instrumentación independiente.

[Los rasgos de](provider-traits.md) proveedor se agregaron como método para adjuntar más datos a un registro de proveedor individual. Se pueden usar para proveedores de registro de seguimiento o basados en manifiestos. Actualmente, esto incluye compatibilidad para agregar un nombre de proveedor o un grupo de proveedores a un registro de proveedor individual. Los grupos de proveedores son una nueva característica que permite controlar varios proveedores ETW de forma agregada por el grupo al que pertenecen.

El estado de captura periódico es una manera de permitir que las notificaciones de estado de captura se envíen de forma rutinaria a los proveedores. Cuando esta opción está habilitada, las notificaciones solo se enviarán a los registros de proveedor que se hayan habilitado previamente en la sesión actual. Cada proveedor puede definir su propia respuesta (si la hay) a una notificación. Para obtener detalles de implementación, [**vea TRACE PERIODIC CAPTURE STATE \_ \_ \_ \_ INFO**](/windows/win32/api/evntrace/ns-evntrace-trace_periodic_capture_state_info).

## <a name="windows-81-and-windows-server-2012-r2"></a>Windows 8.1 y Windows Server 2012 R2:

Se han agregado las siguientes características al seguimiento de eventos en Windows 8.1 y Windows Server 2012 R2.

Funciones que admiten el uso de filtros de carga de eventos, ámbito y recorrido de pila usados por la función [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) y las estructuras [**ENABLE TRACE \_ \_ PARAMETERS**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) y [**EVENT FILTER \_ \_ DESCRIPTOR**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) para filtrar por condiciones específicas en una sesión de registrador. Para más información, consulte:

-   [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
-   [**TdhCleanupPayloadEventFilterDescriptor**](/windows/desktop/api/Tdh/nf-tdh-tdhcleanuppayloadeventfilterdescriptor)
-   [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
-   [**TdhDeletePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhdeletepayloadfilter)

Además, consulte la documentación ampliamente revisada para la función [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) y las estructuras [**ENABLE TRACE \_ \_ PARAMETERS**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) y [**EVENT FILTER \_ \_ DESCRIPTOR**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) que usan estas características.

Estructura que define un predicado de filtro de carga de eventos que describe cómo filtrar por un solo campo en una sesión de seguimiento usada por la nueva función [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter) y una nueva estructura que usan los filtros de id. de evento y recorrido de pila. Para más información, consulte:

-   [**IDENTIFICADOR DE \_ EVENTO DEL FILTRO DE \_ \_ EVENTOS**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_event_id)
-   [**PREDICADO \_ DE FILTRO DE CARGA \_ ÚTIL**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)

Funciones que recuperan información sobre los eventos presentes en el manifiesto del proveedor. Para más información, consulte:

-   [**TdhEnumerateManifestProviderEvents**](/windows/desktop/api/Tdh/nf-tdh-tdhenumeratemanifestproviderevents)
-   [**TdhGetManifestEventInformation**](/windows/desktop/api/Tdh/nf-tdh-tdhgetmanifesteventinformation)

Estructura que define una matriz de eventos en un manifiesto de proveedor utilizado por la nueva [**función TdhEnumerateManifestProviderEvents.**](/windows/desktop/api/Tdh/nf-tdh-tdhenumeratemanifestproviderevents) Para más información, consulte:

-   [**INFORMACIÓN DE \_ EVENTOS DEL \_ PROVEEDOR**](/windows/desktop/api/Tdh/ns-tdh-provider_event_info)

## <a name="windows-8-and-windows-server-2012"></a>Windows 8 y Windows Server 2012

Las siguientes características se han agregado al seguimiento de eventos en Windows 8 y Windows Server 2012.

Funciones que realizan operaciones en un objeto de registro, proporcionan análisis de la carga de eventos, proporcionan exploración del proveedor de seguimiento, consultan la configuración de la sesión de seguimiento de eventos y procesan un archivo de seguimiento relogged. Para más información, consulte:

-   [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation)
-   [**TdhCloseDecodingHandle**](/windows/desktop/api/Tdh/nf-tdh-tdhclosedecodinghandle)
-   [**TdhGetDecodingParameter**](/windows/desktop/api/Tdh/nf-tdh-tdhgetdecodingparameter)
-   [**TdhGetWppProperty**](/windows/desktop/api/Tdh/nf-tdh-tdhgetwppproperty)
-   [**TdhGetWppMessage**](/windows/desktop/api/Tdh/nf-tdh-tdhgetwppmessage)
-   [**TdhLoadManifestFromBinary**](/windows/desktop/api/Tdh/nf-tdh-tdhloadmanifestfrombinary)
-   [**TdhOpenDecodingHandle**](/windows/desktop/api/Tdh/nf-tdh-tdhopendecodinghandle)
-   [**TdhSetDecodingParameter**](/windows/desktop/api/Tdh/nf-tdh-tdhsetdecodingparameter)
-   [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation)

Interfaces que proporcionan información al registrador sobre el proceso de seguimiento y cuándo se registran los eventos, acceso a los datos de un evento específico y acceso a características de registrador que permiten la manipulación de archivos de registro de seguimiento de eventos (ETL). Para más información, consulte:

-   [**ITraceEvent**](/windows/desktop/api/Relogger/nn-relogger-itraceevent)
-   [**ITraceEventCallback**](/windows/desktop/api/Relogger/nn-relogger-itraceeventcallback)
-   [**ITraceRelogger**](/windows/desktop/api/Relogger/nn-relogger-itracerelogger)

Enumeraciones adicionales usadas por las nuevas funciones e interfaces. Para más información, consulte:

-   [**EVENT \_ INFO \_ (CLASE)**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class)
-   [**TRACE \_ QUERY \_ INFO \_ (CLASE)**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class)

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 y Windows Server 2008 R2

En esta versión se agregaron las siguientes características:

-   La capacidad de los proveedores de definir filtros en el manifiesto. En Windows Vista, los controladores podrían pasar datos de filtro al proveedor. Sin embargo, el diseño de los datos de filtro no se definió en el manifiesto, por lo que el proveedor tendría que usar otros medios para proporcionar la definición de filtro a los controladores. Con esta versión, los proveedores pueden definir la definición de filtro en el manifiesto (vea el atributo **filters** del tipo complejo [**ProviderType).**](../wes/eventmanifestschema-providertype-complextype.md) A continuación, los controladores pueden usar la función [**TdhEnumerateProviderFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhenumerateproviderfilters) para determinar la definición del filtro. Los proveedores que usan filtros deben usar [**la función EventWriteEx**](/windows/desktop/api/Evntprov/nf-evntprov-eventwriteex) para escribir el evento.
-   La capacidad de usar un solo búfer para recopilar eventos generados en varios procesadores. El uso de un solo búfer evita que los eventos aparezcan desfasados en equipos con varios procesadores. Para obtener más información, consulte el modo de registro EVENT TRACE NO PER PROCESSOR BUFFERING (SEGUIMIENTO DE EVENTOS NO POR PROCESADOR DE ALMACENAMIENTO [**\_ EN \_ \_ \_ \_ BÚFER).**](logging-mode-constants.md) De forma predeterminada, ETW usa búferes por procesador.
-   La capacidad de capturar un seguimiento de pila para eventos. Para habilitar el seguimiento de pila para eventos de kernel, consulte la [**función TraceSetInformation.**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) Para habilitar el seguimiento de pila para eventos de usuario, vea la marca **EVENT ENABLE PROPERTY STACK \_ \_ \_ \_ TRACE** para el **miembro EnableProperty** [**de ENABLE TRACE \_ \_ PARAMETERS**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters).
-   La capacidad de especificar el modo DE ALMACENAMIENTO EN BÚFER DE SEGUIMIENTO DE EVENTOS o el modo de registro **\_ \_ \_ \_ NEWFILE** DEL MODO DE ARCHIVO DE SEGUIMIENTO DE EVENTOS con el modo de registro EVENT **TRACE PRIVATE \_ \_ \_ LOGGER \_ MODE** (vea Constantes del modo de [registro).](logging-mode-constants.md) **\_ \_ \_**
-   La capacidad de habilitar un proveedor de forma sincrónica. De forma predeterminada, los proveedores están habilitados de forma asincrónica. Para habilitar un proveedor de forma sincrónica, establezca el parámetro *Timeout* [**de EnableTraceEx2.**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
-   La capacidad del controlador para solicitar que el proveedor registre su estado. Para obtener más información, vea la **marca EVENT CONTROL CODE CAPTURE \_ \_ \_ \_ STATE** para el *parámetro ControlCode* [**de EnableTraceEx2.**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
-   La capacidad de los consumidores de dar formato a los datos de eventos mediante [**la función TdhFormatProperty.**](/windows/desktop/api/Tdh/nf-tdh-tdhformatproperty)
-   La capacidad de descodificar eventos manifiestos en equipos que no contienen el proveedor. Para más información, consulte [**la función TdhLoadManifest.**](/windows/desktop/api/Tdh/nf-tdh-tdhloadmanifest)

En esta versión se agregaron las siguientes funciones:

-   [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
-   [**EventWriteEx**](/windows/desktop/api/Evntprov/nf-evntprov-eventwriteex)
-   [**TdhEnumerateProviderFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhenumerateproviderfilters)
-   [**TdhFormatProperty**](/windows/desktop/api/Tdh/nf-tdh-tdhformatproperty)
-   [**TdhLoadManifest**](/windows/desktop/api/Tdh/nf-tdh-tdhloadmanifest)
-   [**TdhUnloadManifest**](/windows/desktop/api/Tdh/nf-tdh-tdhunloadmanifest)
-   [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation)

En esta versión se agregaron las siguientes estructuras:

-   [**IDENTIFICADOR \_ DE EVENTO \_ CLÁSICO**](/windows/win32/api/evntrace/ns-evntrace-classic_event_id)
-   [**HABILITAR \_ PARÁMETROS DE \_ SEGUIMIENTO**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
-   [**SEGUIMIENTO DE \_ LA PILA DE ELEMENTOS \_ \_ \_ EXTENDIDOS DE EVENTOS32**](/windows/desktop/api/Evntcons/ns-evntcons-event_extended_item_stack_trace32)
-   [**SEGUIMIENTO DE \_ LA PILA DE ELEMENTOS \_ \_ \_ EXTENDIDOS DE EVENTOS64**](/windows/desktop/api/Evntcons/ns-evntcons-event_extended_item_stack_trace64)
-   [**ENCABEZADO DE \_ FILTRO \_ DE EVENTOS**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_header)
-   [**INFORMACIÓN DEL \_ FILTRO \_ DEL PROVEEDOR**](/windows/desktop/api/Tdh/ns-tdh-provider_filter_info)

En esta versión se agregaron las enumeraciones siguientes:

-   [**TRACE \_ INFO \_ (CLASE)**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class)

En esta versión se agregaron las siguientes clases MOF:

-   [**StackWalk**](stackwalk.md)
-   [**Evento \_ StackWalk**](stackwalk-event.md)

 

 
