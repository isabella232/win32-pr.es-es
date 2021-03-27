---
description: En esta sección se describen las nuevas características que se agregaron al seguimiento de eventos para Windows en cada versión.
ms.assetid: 5d94a6d2-2280-4a97-aa5a-c9ca2c016c84
title: Novedades del seguimiento de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 613433834e5a11f2886b6ee314fdb60114f66976
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810922"
---
# <a name="whats-new-in-event-tracing"></a>Novedades del seguimiento de eventos

En esta sección se describen las nuevas características que se agregaron al seguimiento de eventos para Windows en cada versión.

## <a name="windows-10-version-1709"></a>Windows 10, versión 1709

ETW ahora puede realizar el seguimiento de los binarios para todos los proveedores que están habilitados para la sesión. El seguimiento se aplica de forma retroactiva para los proveedores que se habilitaron en la sesión antes de la llamada, así como para todos los proveedores futuros que están habilitados para la sesión. Ahora también puede consultar el número máximo configurado actualmente de registradores del sistema permitidos por el sistema operativo. Para obtener más información, vea los valores **TraceProviderBinaryTracking** y **TraceMaxLoggersQuery** de la enumeración de [**clases de \_ información \_ de seguimiento**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class) , así como la recuperación de [datos de seguimiento de eventos adicionales](retrieving-additional-event-tracing-data.md).

ETW ahora puede filtrar eventos basándose en el nombre del evento. También puede determinar qué eventos obtienen sus pilas capturadas. Para obtener más información, vea **el \_ tipo de filtro de evento \_ \_ \_ nombre de evento**, el tipo de filtro de **evento \_ \_ \_ \_ nombre STACKWALK** y el **tipo de filtro de eventos \_ \_ \_ STACKWALK \_ nivel \_ kW** de la estructura de [**\_ \_ descriptores de filtro de eventos**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) , así como el [**\_ \_ \_ nombre del evento de filtro**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_event_name) de eventos asociado y las estructuras [**\_ \_ \_ kW del nivel de filtro de eventos**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_level_kw) .

## <a name="windows-10"></a>Windows 10

[TraceLogging](../tracelogging/trace-logging-portal.md) se basa en ETW y proporciona una manera simplificada de instrumentar el código para los desarrolladores nativos, .net y WinRT. TraceLogging permite incluir datos estructurados con eventos, correlacionar eventos y no requiere un archivo XML de manifiesto de instrumentación independiente.

Los [rasgos de proveedor](provider-traits.md) se agregaron como un método para adjuntar más datos a un registro de proveedor individual. Se pueden usar para los proveedores de TraceLogging o basados en manifiestos. Esto incluye actualmente compatibilidad para agregar un nombre de proveedor o un grupo de proveedores a un registro de proveedor individual. Los grupos de proveedores son una característica nueva que permite que varios proveedores ETW se controlen de forma agregada por el grupo al que pertenecen.

El estado de captura periódica es una manera de permitir que las notificaciones de estado de captura se envíen de forma rutinaria a los proveedores. Cuando esta opción está habilitada, las notificaciones solo se enviarán a los registros del proveedor que se hayan habilitado anteriormente en la sesión actual. Cada proveedor puede definir su propia respuesta (si existe) a una notificación. Para obtener información detallada sobre la implementación, consulte [**seguimiento \_ periódico de estado de \_ captura \_ \_**](/windows/win32/api/evntrace/ns-evntrace-trace_periodic_capture_state_info).

## <a name="windows-81-and-windows-server-2012-r2"></a>Windows 8.1 y Windows Server 2012 R2:

Se han agregado las siguientes características al seguimiento de eventos en Windows 8.1 y Windows Server 2012 R2.

Funciones que admiten el uso de los filtros de carga de eventos, ámbito y recorrido de pila usados por la función [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) y las estructuras de [**\_ \_ descriptor de filtro de eventos**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) y [**habilitar \_ \_ parámetros de seguimiento**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) para filtrar determinadas condiciones en una sesión del registrador. Para más información, consulte:

-   [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
-   [**TdhCleanupPayloadEventFilterDescriptor**](/windows/desktop/api/Tdh/nf-tdh-tdhcleanuppayloadeventfilterdescriptor)
-   [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
-   [**TdhDeletePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhdeletepayloadfilter)

Además, consulte la documentación revisada exhaustivamente para la función [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) y las estructuras de [**habilitar \_ \_ parámetros de seguimiento**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) y [**\_ \_ descriptor de filtro de eventos**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) que usan estas características.

Estructura que define un predicado de filtro de carga de evento que describe cómo filtrar por un solo campo en una sesión de seguimiento utilizada por la nueva función [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter) y una nueva estructura utilizada por los filtros de identificador de evento y recorrido de pila. Para más información, consulte:

-   [**\_ \_ ID. de evento de filtro de eventos \_**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_event_id)
-   [**\_predicado de filtro de carga \_**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)

Funciones que recuperan información sobre eventos presentes en el manifiesto del proveedor. Para más información, consulte:

-   [**TdhEnumerateManifestProviderEvents**](/windows/desktop/api/Tdh/nf-tdh-tdhenumeratemanifestproviderevents)
-   [**TdhGetManifestEventInformation**](/windows/desktop/api/Tdh/nf-tdh-tdhgetmanifesteventinformation)

Estructura que define una matriz de eventos en un manifiesto de proveedor utilizado por la nueva función [**TdhEnumerateManifestProviderEvents**](/windows/desktop/api/Tdh/nf-tdh-tdhenumeratemanifestproviderevents) . Para más información, consulte:

-   [**\_información de evento de proveedor \_**](/windows/desktop/api/Tdh/ns-tdh-provider_event_info)

## <a name="windows-8-and-windows-server-2012"></a>Windows 8 y Windows Server 2012

Se han agregado las siguientes características al seguimiento de eventos en Windows 8 y Windows Server 2012.

Funciones que realizan operaciones en un objeto de registro, proporcionan análisis de carga de eventos, proporcionan exploración del proveedor de seguimiento, configuración de sesión de seguimiento de eventos de consulta y procesamiento de un archivo de seguimiento reiniciado. Para más información, consulte:

-   [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation)
-   [**TdhCloseDecodingHandle**](/windows/desktop/api/Tdh/nf-tdh-tdhclosedecodinghandle)
-   [**TdhGetDecodingParameter**](/windows/desktop/api/Tdh/nf-tdh-tdhgetdecodingparameter)
-   [**TdhGetWppProperty**](/windows/desktop/api/Tdh/nf-tdh-tdhgetwppproperty)
-   [**TdhGetWppMessage**](/windows/desktop/api/Tdh/nf-tdh-tdhgetwppmessage)
-   [**TdhLoadManifestFromBinary**](/windows/desktop/api/Tdh/nf-tdh-tdhloadmanifestfrombinary)
-   [**TdhOpenDecodingHandle**](/windows/desktop/api/Tdh/nf-tdh-tdhopendecodinghandle)
-   [**TdhSetDecodingParameter**](/windows/desktop/api/Tdh/nf-tdh-tdhsetdecodingparameter)
-   [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation)

Interfaces que proporcionan información al reregistrador en el proceso de seguimiento y cuándo se registran los eventos, el acceso a los datos de un evento específico y el acceso a las características de reregistrador que permiten la manipulación de los archivos de registro de seguimiento de eventos (ETL). Para más información, consulte:

-   [**ITraceEvent**](/windows/desktop/api/Relogger/nn-relogger-itraceevent)
-   [**ITraceEventCallback**](/windows/desktop/api/Relogger/nn-relogger-itraceeventcallback)
-   [**ITraceRelogger**](/windows/desktop/api/Relogger/nn-relogger-itracerelogger)

Enumeraciones adicionales usadas por las nuevas funciones e interfaces. Para más información, consulte:

-   [**\_clase de información de eventos \_**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class)
-   [**\_clase de \_ información de consulta de seguimiento \_**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class)

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 y Windows Server 2008 R2

En esta versión se han agregado las siguientes características:

-   La capacidad de los proveedores de definir filtros en el manifiesto. En Windows Vista, los controladores podían pasar datos del filtro al proveedor. Sin embargo, el diseño de los datos de filtro no se definió en el manifiesto, por lo que el proveedor tendría que usar otros medios para proporcionar la definición del filtro a los controladores. Con esta versión, los proveedores pueden definir la definición del filtro en el manifiesto (consulte el atributo **Filters** del tipo complejo de [**ProviderType**](../wes/eventmanifestschema-providertype-complextype.md) ). Los controladores pueden usar la función [**TdhEnumerateProviderFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhenumerateproviderfilters) para determinar la definición del filtro. Los proveedores que usan filtros deben usar la función [**EventWriteEx**](/windows/desktop/api/Evntprov/nf-evntprov-eventwriteex) para escribir el evento.
-   La capacidad de usar un solo búfer para recopilar eventos generados en varios procesadores. El uso de un solo búfer elimina la aparición de eventos desordenados en equipos con varios procesadores. Para obtener más información, [**vea \_ seguimiento de eventos \_ no \_ por \_ \_**](logging-mode-constants.md) el modo de registro de almacenamiento en búfer. De forma predeterminada, ETW usa búferes por procesador.
-   La capacidad de capturar un seguimiento de la pila para los eventos. Para habilitar el seguimiento de la pila para los eventos de kernel, vea la función [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) . Para habilitar el seguimiento de la pila para los eventos de usuario, vea la marca de seguimiento  de la **pila de propiedades de \_ habilitar \_ \_ \_ evento** para el miembro EnableProperty de [**habilitar \_ \_ parámetros de seguimiento**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters).
-   La capacidad de especificar el modo de **almacenamiento en búfer de seguimiento de eventos \_ \_ \_** o el modo de registro de **eventos del \_ \_ \_ \_ modo de seguimiento** de eventos con el modo de registro de **\_ \_ \_ \_ modo** de registro privado del seguimiento de eventos (vea constantes del modo de [registro](logging-mode-constants.md)).
-   La capacidad de habilitar un proveedor de forma sincrónica. De forma predeterminada, los proveedores se habilitan de forma asincrónica. Para habilitar un proveedor de forma sincrónica, establezca el parámetro *timeout* de [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2).
-   La capacidad del controlador para solicitar que el proveedor registre su estado. Para obtener más información, vea la marca de estado de captura de  código de control de **eventos \_ \_ \_ \_** para el parámetro ControlCode de [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2).
-   La capacidad de los consumidores de dar formato a los datos de eventos mediante la función [**TdhFormatProperty**](/windows/desktop/api/Tdh/nf-tdh-tdhformatproperty) .
-   La capacidad de descodificar eventos manifiestos en equipos que no contienen el proveedor. Para obtener más información, consulte la función [**TdhLoadManifest**](/windows/desktop/api/Tdh/nf-tdh-tdhloadmanifest) .

En esta versión se han agregado las siguientes funciones:

-   [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
-   [**EventWriteEx**](/windows/desktop/api/Evntprov/nf-evntprov-eventwriteex)
-   [**TdhEnumerateProviderFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhenumerateproviderfilters)
-   [**TdhFormatProperty**](/windows/desktop/api/Tdh/nf-tdh-tdhformatproperty)
-   [**TdhLoadManifest**](/windows/desktop/api/Tdh/nf-tdh-tdhloadmanifest)
-   [**TdhUnloadManifest**](/windows/desktop/api/Tdh/nf-tdh-tdhunloadmanifest)
-   [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation)

En esta versión se han agregado las siguientes estructuras:

-   [**\_identificador de evento clásico \_**](/windows/win32/api/evntrace/ns-evntrace-classic_event_id)
-   [**HABILITAR \_ parámetros de seguimiento \_**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
-   [**EVENTO \_ de \_ pila de elemento extendido \_ \_ TRACE32**](/windows/desktop/api/Evntcons/ns-evntcons-event_extended_item_stack_trace32)
-   [**EVENTO \_ de \_ pila de elemento extendido \_ \_ TRACE64**](/windows/desktop/api/Evntcons/ns-evntcons-event_extended_item_stack_trace64)
-   [**\_encabezado de filtro de evento \_**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_header)
-   [**\_información de filtro de proveedor \_**](/windows/desktop/api/Tdh/ns-tdh-provider_filter_info)

En esta versión se han agregado las siguientes enumeraciones:

-   [**\_clase de información de seguimiento \_**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class)

En esta versión se han agregado las siguientes clases MOF:

-   [**StackWalk**](stackwalk.md)
-   [**\_Evento StackWalk**](stackwalk-event.md)

 

 
