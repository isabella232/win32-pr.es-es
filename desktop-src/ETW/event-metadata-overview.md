---
description: 'Esta es una visión general de lo que se espera para el recorrido de un extremo a otro de un evento para cada una de las cuatro tecnologías de seguimiento proporcionadas por Microsoft: TraceLogging, basado en manifiesto, WPP y MOF.'
ms.assetid: 6102593C-C6D5-4BDB-A0EF-067AF91DE00B
title: Información general sobre metadatos de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c16853ef2639fd560f5b5da30447556119ec877
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497026"
---
# <a name="event-metadata-overview"></a>Información general sobre metadatos de eventos

Esta es una visión general de lo que se espera para el recorrido de un extremo a otro de un evento para cada una de las cuatro tecnologías de seguimiento proporcionadas por Microsoft: [TraceLogging](../tracelogging/trace-logging-about.md), [basado en manifiesto](writing-manifest-based-events.md), [WPP](windows-software-trace-preprocessor.md)y [MOF](tracing-events.md). Se aproxima al problema con respecto a la carga de un evento individual y a los metadatos adjuntos que describen su estructura, lo que permite descodificar posteriormente el evento en fragmentos de datos razonables. Es importante comprender el recorrido de cada parte de un evento a la hora de elegir qué tecnología de seguimiento es adecuada para un proyecto. No hay ninguna solución única para el seguimiento.

## <a name="event-payloads"></a>Cargas de eventos

Para cualquiera de las tecnologías de seguimiento proporcionadas por Microsoft, al llamar al comando Write (por ejemplo, [**EventWrite**](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) para la instancia basada en manifiesto o [**TraceLoggingWrite**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) para TraceLogging), los datos proporcionados para el evento en tiempo de ejecución se doblan en un BLOB binario contiguo denominado carga del evento. Esto es independiente del esquema de eventos o de los metadatos de eventos (se describe a continuación), que describe el diseño de este BLOB binario para las herramientas de descodificación. La precisión de la generación de la carga del evento varía en función de la tecnología de seguimiento utilizada y, en última instancia, de si el evento es clásico (estilo de [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) ) o moderno (estilo **EventWrite** ).

En el caso de los eventos clásicos, la marca del [**\_ \_ encabezado de seguimiento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) se pasa a [**TraceEvent**](/windows/win32/api/evntrace/nf-evntrace-traceevent) que determina cómo se produce esto:

\- Si se especifica la **\_ marca WNODE \_ use \_ MOF \_ ptr** , una matriz [**de \_ campos MOF**](/windows/win32/api/evntrace/ns-evntrace-mof_field) sigue [**el \_ \_ encabezado de seguimiento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) en la memoria. El tiempo de ejecución de ETW concatenará los datos de evento tal y como se especifica en estos campos para formar la carga del evento.

\- Si no se especifica la **\_ marca WNODE \_ use \_ MOF \_ ptr** , el usuario crea la carga del evento directamente en la memoria que sigue al [**encabezado de \_ seguimiento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header).

Tanto MOF como WPP son proveedores clásicos. Sin embargo, la implementación de WPP se encarga de todo esto.

En el caso de los eventos no clásicos, se pasa un número de [**\_ \_ descriptores de datos de eventos**](/windows/desktop/api/Evntprov/ns-evntprov-event_data_descriptor) a [**EventWrite**](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite). El tiempo de ejecución de ETW concatenará los datos de evento tal y como se especifica en estos descriptores para formar la carga del evento.

Las tecnologías basadas en manifiesto y TraceLogging suelen ser proveedores modernos. Con basado en manifiesto, si permite que mc.exe genere código de registro automáticamente (MU o conmutador km), la generación de carga se realizará en su interés. La generación de carga útil siempre se realiza por TraceLogging.

El resultado final es que se genera una carga para un evento en tiempo de ejecución. Todas las cargas son fundamentalmente similares, ya que son blobs binarios de datos que contienen solo los datos de campo de ese evento concreto, independientemente de la tecnología de seguimiento utilizada y de los tipos de campo que admite esa tecnología de seguimiento. Sin los metadatos del evento, la carga del evento no tiene sentido y unintelligable.

El deber del tiempo de ejecución de ETW es llevar a cabo este BLOB de eventos desde el proveedor al consumidor, donde se vuelve a asociar a sus metadatos y se convierte en descodificable. El tiempo de ejecución de ETW agregará un poco de metadatos adicionales que indican las circunstancias de la carga (por ejemplo, la marca de tiempo, el identificador del subproceso y las palabras clave del evento). Esta información es relevante para el modo en que el evento se enrutó a través del tiempo de ejecución y también es útil para comprender la identidad y el contexto del evento en el momento de la descodificación. Finalmente, se muestran como parte del seguimiento de [**eventos \_**](/windows/win32/api/evntrace/ns-evntrace-event_trace) o del [**\_ registro de eventos**](/windows/win32/api/evntcons/ns-evntcons-event_record) del consumidor.

## <a name="event-metadata"></a>Metadatos de evento

El recorrido de los metadatos de eventos es diferente en función de la tecnología de seguimiento que se use, y es una de las mayores consideraciones a la hora de comparar cada tecnología.

### <a name="mof"></a>MOF

Los metadatos de eventos los crea manualmente el creador del evento en forma de un esquema MOF especial en un archivo. mof. El esquema creado debe coincidir con la carga registrada para que los consumidores puedan descodificar correctamente el evento. Los descodificadores de eventos requieren que el archivo. mof esté registrado en el sistema mediante [mofcomp.exe](../wmisdk/mofcomp.md). Para obtener más información sobre cómo publicar esquemas MOF, vea [publicar el esquema de eventos para un proveedor clásico](publishing-your-event-schema-for-a-classic-provider.md).

### <a name="wpp"></a>WPP

Los metadatos de evento se generan automáticamente y se almacenan en el archivo. pdb de binario mediante tracewpp.exe durante el proceso de compilación. Estos metadatos se pueden extraer más adelante en forma de un archivo. TMF independiente mediante tracepdb.exe. Normalmente, los descodificadores de eventos requieren el archivo. pdb o el archivo. TMF. Para obtener más información sobre tracepdb.exe, consulte [información general de Tracepdb](/windows-hardware/drivers/devtest/tracepdb-overview)y para más información sobre tracewpp.exe, consulte [tarea TraceWPP](/windows-hardware/drivers/devtest/tracewpp-task).

### <a name="manifest-based"></a>Basado en manifiesto

Las definiciones de eventos se crean en un archivo. Man. Los manifiestos de eventos se ejecutan a través del compilador del manifiesto ([mc.exe](../wes/message-compiler--mc-exe-.md)), generando los encabezados necesarios para la compilación de origen, así como varios archivos de recursos binarios. bin. Estos archivos de recursos deben compilarse como recursos en un archivo binario y el binario resultante colocado en el sistema que intenta descodificar los eventos de ese proveedor basado en manifiesto. Además, el manifiesto debe instalarse en el sistema con [wevtutil.exe](../wes/windows-event-log-tools.md) más importante, los atributos **nombrearchivorecursos** y **messageFileName** del elemento XML del proveedor del manifiesto de evento instalado deben identificar correctamente la ruta de acceso absoluta completa al binario en el que se colocaron los archivos de recursos. Tenga en cuenta que estas rutas de acceso se pueden sobrescribir en el momento de la instalación del manifiesto mediante el wevtutil.exe modificadores/RF y/MF. Un sistema que no haya realizado correctamente estos pasos no podrá descodificar los eventos de este proveedor. Por tanto, los descodificadores de eventos requieren un manifiesto instalado y el binario con los recursos asociados instalados en la ubicación especificada por las rutas de acceso del archivo de recursos y mensajes. Para obtener más información sobre la publicación de esquemas basados en manifiestos, vea [publicar el esquema de eventos para un proveedor basado en manifiestos](publishing-your-event-schema-for-a-manifest-base-provider.md).

### <a name="tracelogging"></a>TraceLogging

Todos los eventos TraceLogging son autodescriptivos. Los metadatos de evento necesarios para descodificar el evento se generan y se transmiten automáticamente junto con la carga en un formato binario compacto. Los descodificadores de eventos solo necesitan el evento TraceLogging y una descripción del formato de metadatos TraceLogging.

## <a name="configuring-tdh-for-decoding"></a>Configuración de TDH para la descodificación

Existen muchas herramientas de descodificación. Sin embargo, se recomienda usar TDH siempre que sea posible, ya que descodifica todas las tecnologías de seguimiento con una API unificada. Dependiendo del tipo de seguimiento que le interese descodificar, TDH puede requerir una configuración explícita.

### <a name="mof"></a>MOF

TDH usa datos de descodificación de MOF registrados en el sistema mediante mofcomp.exe. Para obtener más información, vea [publicar el esquema de eventos para un proveedor clásico](publishing-your-event-schema-for-a-classic-provider.md).

### <a name="wpp"></a>WPP

TDH debe apuntar hacia el archivo. pdb o el archivo. TMF asociado para el proveedor de WPP que está intentando descodificar. Esto puede realizarse mediante una llamada a [**TdhSetDecodingParameter**](/windows/desktop/api/Tdh/nf-tdh-tdhsetdecodingparameter). De lo contrario, el motor de descodificación revertirá la ruta de búsqueda del formato de seguimiento de la variable de entorno \_ \_ \_ .

### <a name="manifest-based"></a>Basado en manifiesto

TDH usa todos los proveedores basados en manifiestos registrados en el sistema mediante wevtutil.exe.

### <a name="tracelogging"></a>TraceLogging

Las versiones más recientes de TDH detectan y descodifican automáticamente los eventos de TraceLogging sin necesidad de realizar ningún paso adicional.

 

 
