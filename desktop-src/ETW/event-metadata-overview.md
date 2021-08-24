---
description: 'Esta es una visión general de lo que se puede esperar para el recorrido de un extremo a otro de un evento para cada una de las cuatro tecnologías de seguimiento que ofrece Microsoft: TraceLogging, Manifest-based, WPP y MOF.'
ms.assetid: 6102593C-C6D5-4BDB-A0EF-067AF91DE00B
title: Información general sobre metadatos de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 931b8adbdb22cdbf2e0806e2d69c367e64ad92926390825a48a2fa51d50605ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755065"
---
# <a name="event-metadata-overview"></a>Información general sobre metadatos de eventos

Esta es una visión general de lo que se puede esperar para el recorrido de un extremo a otro de un evento para cada una de las cuatro tecnologías de seguimiento que ofrece Microsoft: [TraceLogging](../tracelogging/trace-logging-about.md), [manifest-based](writing-manifest-based-events.md), [WPP](windows-software-trace-preprocessor.md)y [MOF](tracing-events.md). Aborda el problema con respecto a la carga útil de un evento individual y a los metadatos que lo acompañan, lo que describe su estructura, lo que permite descodificar posteriormente el evento en fragmentos de datos razonables. Comprender el recorrido de cada parte de un evento es importante al elegir qué tecnología de seguimiento es adecuada para un proyecto. No hay ninguna solución única para el seguimiento.

## <a name="event-payloads"></a>Cargas de eventos

Para cualquiera de las tecnologías de seguimiento proporcionadas por Microsoft, al llamar al comando Write (por [**ejemplo, EventWrite**](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) para el manifiesto o [**TraceLoggingWrite**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) para TraceLogging), los datos proporcionados para el evento en tiempo de ejecución se plegan en un blob binario contiguo denominado carga del evento. Esto es independiente del esquema de eventos o los metadatos de eventos (que se describen a continuación), que describe el diseño de este blob binario para las herramientas de codificación. La forma en que se produce exactamente la generación de la carga del evento varía en función de la tecnología de seguimiento utilizada y, en última instancia, si el evento es clásico (estilo [**TraceEvent)**](/windows/win32/api/evntrace/nf-evntrace-traceevent) o moderno (estilo **EventWrite).**

En el caso de los eventos clásicos, la [**marca de EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) se pasa [**a TraceEvent,**](/windows/win32/api/evntrace/nf-evntrace-traceevent) que determina cómo se produce esto:

\- Si **se especifica \_ WNODE FLAG USE \_ \_ MOF \_ PTR,** una matriz de campos [**MOF \_**](/windows/win32/api/evntrace/ns-evntrace-mof_field) sigue al [**ENCABEZADO DE SEGUIMIENTO DE \_ \_ EVENTOS**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) en memoria. El tiempo de ejecución de ETW concatenará los datos del evento como se especifica en estos campos para formar la carga del evento.

\- Si **no se especifica \_ WNODE FLAG USE \_ \_ MOF \_ PTR,** el usuario construye la carga del evento directamente en memoria después de [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header).

MOF y WPP son proveedores clásicos. Sin embargo, la implementación de WPP se encarga de todo esto.

En el caso de los eventos no clásicos, se pasan varios [**\_ \_ DESCRIPTORES**](/windows/desktop/api/Evntprov/ns-evntprov-event_data_descriptor) DE DATOS DE EVENTOS a [**EventWrite**](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite). El tiempo de ejecución de ETW concatenará los datos del evento tal y como se especifica en estos descriptores para formar la carga del evento.

Tanto las tecnologías basadas en manifiestos como las tecnologías tracelogging suelen ser proveedores modernos. Con basado en manifiestos, si mc.exe generar código de registro automáticamente (conmutador um o km), la generación de carga se encarga automáticamente. TraceLogging siempre se encarga de la generación de carga.

El resultado final es que se genera una carga para un evento en tiempo de ejecución. Todas las cargas son fundamentalmente similares, ya que son blobs binarios de datos que contienen solo los datos de campo para ese evento en particular, independientemente de la tecnología de seguimiento usada y de los tipos de campo admitidos por esa tecnología de seguimiento. Sin los metadatos del evento, la carga del evento no tiene sentido e es ininteligible.

A continuación, el trabajo del tiempo de ejecución de ETW es llevar este blob de eventos del proveedor al consumidor, donde se vuelve a asociar a sus metadatos y se puede decodificar. El tiempo de ejecución de ETW agregará un poco de metadatos adicionales que indican las circunstancias de la carga, por ejemplo, elementos como la marca de tiempo, el identificador de subproceso y las palabras clave del evento. Esta información es relevante para la forma en que el evento se enrutó a través del tiempo de ejecución y también es útil para comprender la identidad y el contexto del evento en el momento de la descodación. Finalmente, se muestra como parte de [**EVENT \_ TRACE**](/windows/win32/api/evntrace/ns-evntrace-event_trace) o [**EVENT \_ RECORD**](/windows/win32/api/evntcons/ns-evntcons-event_record) para el consumidor.

## <a name="event-metadata"></a>Metadatos de eventos

El recorrido de los metadatos de eventos es diferente en función de la tecnología de seguimiento que se utilice y es una de las consideraciones más importantes al comparar cada tecnología.

### <a name="mof"></a>MOF

El creador del evento crea los metadatos del evento a mano en forma de un esquema MOF especial en un archivo .mof. El esquema creado debe coincidir con la carga que se registra para que los consumidores descodifican correctamente el evento. Los descodificadores de eventos requieren que el archivo .mof esté registrado en el sistema mediante [mofcomp.exe](../wmisdk/mofcomp.md). Para obtener más información sobre la publicación de esquemas MOF, vea [Publishing Your Event Schema for a Classic Provider](publishing-your-event-schema-for-a-classic-provider.md).

### <a name="wpp"></a>Wpp

Los metadatos de eventos se generan y almacenan automáticamente en el archivo .pdb del archivo binario tracewpp.exe durante el proceso de compilación. Estos metadatos se pueden extraer más adelante en forma de un archivo .tmf independiente mediante tracepdb.exe. Los descodificadores de eventos normalmente requieren el archivo .pdb o .tmf. Para obtener más información sobre tracepdb.exe, vea Información general [de Tracepdb](/windows-hardware/drivers/devtest/tracepdb-overview)y, para obtener más información sobre tracewpp.exe, vea [Tarea TraceWPP](/windows-hardware/drivers/devtest/tracewpp-task).

### <a name="manifest-based"></a>Basado en manifiestos

Las definiciones de eventos se crearon en un archivo .man. Los manifiestos de evento se ejecutan a través del compilador de[ manifiestos (mc.exe](../wes/message-compiler--mc-exe-.md)), generando los encabezados necesarios para la compilación de origen, así como varios archivos de recursos binarios .bin. Estos archivos de recursos se deben compilar como recursos en un binario y el binario resultante colocado en el sistema que pretende descodificar eventos de ese proveedor basado en manifiesto. Además, el manifiesto debe instalarse en el sistema mediante [wevtutil.exe](../wes/windows-event-log-tools.md) Lo más importante es que los atributos **resourceFileName** y **messageFileName** en el elemento XML del proveedor del manifiesto de evento instalado deben identificar correctamente la ruta de acceso absoluta completa al binario en el que se colocaron los archivos de recursos. Tenga en cuenta que estas rutas de acceso se pueden sobrescribir en el momento de la instalación del manifiesto mediante los modificadores de wevtutil.exe /rf y /mf. Un sistema que no haya realizado correcta y completamente estos pasos no podrá descodificar eventos de este proveedor. Por lo tanto, los descodificadores de eventos requieren un manifiesto instalado y el binario con los recursos asociados instalados en la ubicación especificada por las rutas de acceso del archivo de recursos y mensajes. Para obtener más información sobre la publicación de esquemas basados en manifiestos, vea [Publishing Your Event Schema for a Manifest-based Provider](publishing-your-event-schema-for-a-manifest-base-provider.md).

### <a name="tracelogging"></a>TraceLogging

Todos los eventos TraceLogging son autodescriptos. Los metadatos de evento necesarios para descodificar el evento se generan y transmiten automáticamente junto con la carga en un formato binario compacto. Los descodificadores de eventos solo necesitan el evento TraceLogging y un conocimiento del formato de metadatos TraceLogging.

## <a name="configuring-tdh-for-decoding"></a>Configuración de TDH para lacoding

Hay muchas herramientas de decodificación. Sin embargo, se recomienda usar TDH siempre que sea posible, ya que descodifica todas las tecnologías de seguimiento con una API unificada. En función del tipo de seguimiento que le interese lacodización, TDH puede requerir una configuración explícita.

### <a name="mof"></a>MOF

TDH utiliza los datos de la decodificación MOF registrados en el sistema mediante mofcomp.exe. Para obtener más información, [vea Publicar el esquema de eventos para un proveedor clásico.](publishing-your-event-schema-for-a-classic-provider.md)

### <a name="wpp"></a>Wpp

TDH debe apuntar hacia el archivo .pdb o el archivo .tmf asociado para el proveedor de WPP que está intentando descodificar. Esto se puede realizar llamando a [**TdhSetDecodingParameter**](/windows/desktop/api/Tdh/nf-tdh-tdhsetdecodingparameter). De lo contrario, el motor de decodificación se retendrán en la variable de entorno TRACE \_ FORMAT \_ SEARCH \_ PATH.

### <a name="manifest-based"></a>Basado en manifiestos

TDH utiliza todos los proveedores basados en manifiestos registrados en el sistema mediante wevtutil.exe.

### <a name="tracelogging"></a>TraceLogging

Las versiones más recientes de TDH detectan y descodifican automáticamente eventos TraceLogging sin pasos adicionales.

 

 
