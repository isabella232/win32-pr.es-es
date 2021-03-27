---
description: Seguimiento de eventos para Windows (ETW) es una herramienta de seguimiento de nivel de kernel eficaz que permite registrar eventos definidos por el kernel o la aplicación en un archivo de registro.
ms.assetid: 0eaa7bd3-8537-483a-b0d6-db3b790a6f3d
title: Acerca del seguimiento de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a2f13284cec1d9300c23241fafe154f277f72a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001299"
---
# <a name="about-event-tracing"></a>Acerca del seguimiento de eventos

Seguimiento de eventos para Windows (ETW) es una herramienta de seguimiento de nivel de kernel eficaz que permite registrar eventos definidos por el kernel o la aplicación en un archivo de registro. Puede consumir los eventos en tiempo real o desde un archivo de registro y usarlos para depurar una aplicación o para determinar dónde se producen los problemas de rendimiento en la aplicación.

ETW le permite habilitar o deshabilitar el seguimiento de eventos de forma dinámica, lo que le permite realizar un seguimiento detallado en un entorno de producción sin necesidad de reiniciar el equipo o la aplicación.

La API de seguimiento de eventos se divide en tres componentes distintos:

-   [Controladores](#controllers), que inician y detienen una sesión de seguimiento de eventos y habilitan proveedores
-   [Proveedores](#providers), que proporcionan los eventos
-   [Consumidores](#consumers), que consumen los eventos

En el diagrama siguiente se muestra el modelo de seguimiento de eventos.

![modelo de seguimiento de eventos](images/etdiag2.png)

## <a name="controllers"></a>Controladores

Los controladores son aplicaciones que definen el tamaño y la ubicación del archivo de registro, inician y detienen [sesiones de seguimiento de eventos](event-tracing-sessions.md), habilitan proveedores para que puedan registrar eventos en la sesión, administrar el tamaño del grupo de búferes y obtener estadísticas de ejecución para las sesiones. Las estadísticas de la sesión incluyen el número de búferes utilizados, el número de búferes entregados y el número de eventos y búferes perdidos. 

Para obtener más información, vea [controlar las sesiones de seguimiento de eventos](controlling-event-tracing-sessions.md).

## <a name="providers"></a>Proveedores

Los proveedores son aplicaciones que contienen instrumentación de seguimiento de eventos. Después de que un proveedor se registra a sí mismo, un controlador puede habilitar o deshabilitar el seguimiento de eventos en el proveedor. El proveedor define su interpretación de que está habilitada o deshabilitada. Normalmente, un proveedor habilitado genera eventos, mientras que un proveedor deshabilitado no lo hace. Esto le permite agregar seguimiento de eventos a la aplicación sin necesidad de que genere eventos en todo momento. 

Aunque el modelo ETW separa el controlador y el proveedor en aplicaciones independientes, una aplicación puede incluir ambos componentes.

Para obtener más información, vea [proporcionar eventos](providing-events.md).

### <a name="types-of-providers"></a>Tipos de proveedores

Hay cuatro tipos principales de proveedores: proveedores de MOF (clásico), proveedores de WPP, proveedores basados en manifiestos y proveedores de TraceLogging. Debe usar un proveedor basado en manifiesto o un proveedor TraceLogging si está escribiendo aplicaciones para Windows Vista o posterior que no necesitan admitir sistemas heredados.

#### <a name="mof-classic-providers"></a>Proveedores de MOF (clásico):

-   Utilice las funciones [RegisterTraceGuids](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) y [TraceEvent](/windows/win32/api/evntrace/nf-evntrace-traceevent) para registrar y escribir eventos.
-   Use las clases MOF para definir eventos para que los consumidores sepan cómo consumirlos.
-   Solo se puede habilitar en una sesión de seguimiento cada vez.

#### <a name="wpp-providers"></a>Proveedores WPP:

-   Utilice las funciones [RegisterTraceGuids](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) y [TraceEvent](/windows/win32/api/evntrace/nf-evntrace-traceevent) para registrar y escribir eventos.
-   Tienen archivos TMF asociados (compilados en un archivo binario. pdb) que contiene información de descodificación que se deduce del análisis del preprocesador de la instrumentación WPP en el código fuente.
-   Solo se puede habilitar en una sesión de seguimiento cada vez.

#### <a name="manifest-based-providers"></a>Proveedores basados en manifiestos:

-   Use [EventRegister](/windows/desktop/api/Evntprov/nf-evntprov-eventregister) y [EventWrite](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) para registrar y escribir eventos.
-   Use un manifiesto para definir eventos para que los consumidores sepan cómo consumirlos.
-   Puede habilitarse hasta ocho sesiones de seguimiento simultáneamente.

#### <a name="tracelogging-providers"></a>Proveedores de [TraceLogging](/windows/desktop/tracelogging/trace-logging-about) :

-   Use [TraceLoggingRegister](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) y [TraceLoggingWrite](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) para registrar y escribir eventos.
-   Use eventos autodescriptivos para que los propios eventos contengan toda la información necesaria para consumirlos.
-   Puede habilitarse hasta ocho sesiones de seguimiento simultáneamente.

Todos los proveedores de eventos usan fundamentalmente la familia de API de seguimiento de eventos ([TraceEvent](/windows/win32/api/evntrace/nf-evntrace-traceevent) para tecnologías heredadas y [EventWrite](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) / [EventWriteEx](/windows/desktop/api/Evntprov/nf-evntprov-eventwriteex) para las versiones más recientes). Los proveedores de eventos solo se diferencian en los tipos de campo que almacenan en cargas de eventos y donde almacenan la información de descodificación de eventos asociada.

## <a name="consumers"></a>Consumidores

Los consumidores son aplicaciones que seleccionan una o varias sesiones de seguimiento de eventos como origen de eventos. Un consumidor puede solicitar eventos de varias sesiones de seguimiento de eventos simultáneamente. el sistema entrega los eventos en orden cronológico. Los consumidores pueden recibir eventos almacenados en archivos de registro o desde sesiones que entregan eventos en tiempo real. Al procesar eventos, un consumidor puede especificar las horas de inicio y finalización, y solo se entregarán los eventos que se produzcan en el período de tiempo especificado. 

Para obtener más información, consulte [consumo de eventos](consuming-events.md).

## <a name="missing-events"></a>Eventos que faltan

Perfmon, diagnóstico del sistema y otras herramientas del sistema pueden notificar los eventos que faltan en el registro de eventos e indicar que la configuración del seguimiento de eventos para Windows (ETW) puede no ser óptima. Los eventos se pueden perder por una serie de motivos:

-   El tamaño total del evento es mayor que 64 KB. Esto incluye el encabezado ETW más los datos o la carga. Un usuario no tiene control sobre estos eventos que faltan, ya que la aplicación configura el tamaño del evento.

-   El tamaño del búfer de ETW es menor que el tamaño total del evento. Un usuario no tiene control sobre estos eventos que faltan, ya que el tamaño del evento lo configura la aplicación que registra los eventos.

-   Para el registro en tiempo real, el consumidor en tiempo real no está consumiendo eventos lo suficientemente rápido o no está presente por completo y, a continuación, se está llenando el archivo de copia de seguridad. Esto puede producirse si el servicio registro de eventos se detiene y se inicia cuando se registran eventos. Un usuario no tiene control sobre estos eventos que faltan.

-   Al registrar en un archivo, el disco es demasiado lento para mantenerse al día de la tasa de registro.

Por cualquiera de estos motivos, informe de estos problemas al proveedor de la aplicación o servicio que está generando los eventos. Estos problemas solo los puede solucionar el desarrollador de la aplicación o el servicio que registra los eventos. Si se notifican los eventos que faltan en el servicio registro de eventos, esto puede indicar un problema con la configuración del servicio registro de eventos. El usuario puede tener una capacidad limitada para aumentar el espacio en disco máximo que usará el servicio registro de eventos, lo que puede reducir el número de eventos que faltan.

 

 
