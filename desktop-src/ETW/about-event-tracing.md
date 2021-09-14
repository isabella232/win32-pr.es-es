---
description: Seguimiento de eventos para Windows (ETW) es una eficaz instalación de seguimiento de nivel de kernel que permite registrar eventos de kernel o definidos por la aplicación en un archivo de registro.
ms.assetid: 0eaa7bd3-8537-483a-b0d6-db3b790a6f3d
title: Acerca del seguimiento de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a2f13284cec1d9300c23241fafe154f277f72a3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063169"
---
# <a name="about-event-tracing"></a>Acerca del seguimiento de eventos

Seguimiento de eventos para Windows (ETW) es una eficaz instalación de seguimiento de nivel de kernel que permite registrar eventos de kernel o definidos por la aplicación en un archivo de registro. Puede consumir los eventos en tiempo real o desde un archivo de registro y usarlos para depurar una aplicación o para determinar dónde se producen problemas de rendimiento en la aplicación.

ETW permite habilitar o deshabilitar el seguimiento de eventos dinámicamente, lo que le permite realizar un seguimiento detallado en un entorno de producción sin necesidad de reiniciar el equipo o la aplicación.

Event Tracing API se divide en tres componentes distintos:

-   [Controladores](#controllers), que inician y detienen una sesión de seguimiento de eventos y habilitan proveedores
-   [Proveedores](#providers), que proporcionan los eventos
-   [Consumidores](#consumers), que consumen los eventos

En el diagrama siguiente se muestra el modelo de seguimiento de eventos.

![modelo de seguimiento de eventos](images/etdiag2.png)

## <a name="controllers"></a>Controladores

Los controladores son aplicaciones que definen el tamaño y la ubicación del archivo de registro, inician y detienen las sesiones de seguimiento de [eventos,](event-tracing-sessions.md)habilitan los proveedores para que puedan registrar eventos en la sesión, administrar el tamaño del grupo de búferes y obtener estadísticas de ejecución para las sesiones. Las estadísticas de sesión incluyen el número de búferes usados, el número de búferes entregados y el número de eventos y búferes perdidos. 

Para obtener más información, vea [Controlar sesiones de seguimiento de eventos.](controlling-event-tracing-sessions.md)

## <a name="providers"></a>Proveedores

Los proveedores son aplicaciones que contienen instrumentación de seguimiento de eventos. Una vez que un proveedor se registra a sí mismo, un controlador puede habilitar o deshabilitar el seguimiento de eventos en el proveedor. El proveedor define su interpretación de que se habilita o deshabilita. Por lo general, un proveedor habilitado genera eventos, mientras que un proveedor deshabilitado no lo hace. Esto le permite agregar el seguimiento de eventos a la aplicación sin necesidad de que genere eventos todo el tiempo. 

Aunque el modelo ETW separa el controlador y el proveedor en aplicaciones independientes, una aplicación puede incluir ambos componentes.

Para obtener más información, vea [Proporcionar eventos](providing-events.md).

### <a name="types-of-providers"></a>Tipos de proveedores

Hay cuatro tipos principales de proveedores: proveedores de MOF (clásico), proveedores de WPP, proveedores basados en manifiestos y proveedores de seguimiento. Debe usar un proveedor basado en manifiestos o un proveedor de seguimiento si está escribiendo aplicaciones para Windows Vista o posterior que no necesitan admitir sistemas heredados.

#### <a name="mof-classic-providers"></a>Proveedores de MOF (clásico):

-   Use las [funciones RegisterTraceGuids](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) y [TraceEvent](/windows/win32/api/evntrace/nf-evntrace-traceevent) para registrar y escribir eventos.
-   Use clases MOF para definir eventos para que los consumidores sepan cómo consumirlos.
-   Solo se puede habilitar una sesión de seguimiento a la vez.

#### <a name="wpp-providers"></a>Proveedores de WPP:

-   Use las [funciones RegisterTraceGuids](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) y [TraceEvent](/windows/win32/api/evntrace/nf-evntrace-traceevent) para registrar y escribir eventos.
-   Tener asociados archivos TMF (compilados en el archivo .pdb de un archivo binario) que contienen información de codificación inferida del examen del preprocesador de la instrumentación de WPP en el código fuente.
-   Solo se puede habilitar una sesión de seguimiento a la vez.

#### <a name="manifest-based-providers"></a>Proveedores basados en manifiestos:

-   Use [EventRegister](/windows/desktop/api/Evntprov/nf-evntprov-eventregister) y [EventWrite para](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) registrar y escribir eventos.
-   Use un manifiesto para definir eventos para que los consumidores sepan cómo consumirlos.
-   Puede habilitarse mediante hasta ocho sesiones de seguimiento simultáneamente.

#### <a name="tracelogging-providers"></a>[Proveedores de seguimiento de](/windows/desktop/tracelogging/trace-logging-about) registros:

-   Use [TraceLoggingRegister y](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) [TraceLoggingWrite para](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) registrar y escribir eventos.
-   Use eventos autodescriptos para que los propios eventos contengan toda la información necesaria para consumirlos.
-   Puede habilitarse mediante hasta ocho sesiones de seguimiento simultáneamente.

Todos los proveedores de eventos usan fundamentalmente la familia de API de Seguimiento de eventos[(TraceEvent](/windows/win32/api/evntrace/nf-evntrace-traceevent) para tecnologías heredadas y [EventWrite](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) / [EventWriteEx](/windows/desktop/api/Evntprov/nf-evntprov-eventwriteex) para las más recientes). Los proveedores de eventos simplemente difieren en qué tipos de campo almacenan en cargas de eventos y dónde almacenan la información de codificación de eventos asociada.

## <a name="consumers"></a>Consumidores

Los consumidores son aplicaciones que seleccionan una o varias sesiones de seguimiento de eventos como origen de eventos. Un consumidor puede solicitar eventos de varias sesiones de seguimiento de eventos simultáneamente; el sistema entrega los eventos en orden cronológico. Los consumidores pueden recibir eventos almacenados en archivos de registro o desde sesiones que entregan eventos en tiempo real. Al procesar eventos, un consumidor puede especificar las horas de inicio y finalización, y solo se entregarán los eventos que se produzcan en el período de tiempo especificado. 

Para obtener más información, [vea Consumo de eventos](consuming-events.md).

## <a name="missing-events"></a>Eventos que faltan

Perfmon, Diagnósticos del sistema y otras herramientas del sistema pueden informar sobre eventos que faltan en el registro de eventos e indicar que la configuración de Seguimiento de eventos para Windows (ETW) puede no ser óptima. Los eventos se pueden perder por varios motivos:

-   El tamaño total del evento es mayor que 64 K. Esto incluye el encabezado ETW más los datos o la carga. Un usuario no tiene control sobre estos eventos que faltan, ya que la aplicación configura el tamaño del evento.

-   El tamaño del búfer ETW es menor que el tamaño total del evento. Un usuario no tiene control sobre estos eventos que faltan, ya que la aplicación que registra los eventos configura el tamaño del evento.

-   Para el registro en tiempo real, el consumidor en tiempo real no está consumiendo eventos lo suficientemente rápido o no está presente por completo y, a continuación, el archivo de copia de seguridad se está rellenando. Esto puede producirse si el servicio de registro de eventos se detiene e inicia cuando se registran eventos. Un usuario no tiene control sobre estos eventos que faltan.

-   Al registrar en un archivo, el disco es demasiado lento para mantenerse al día con la tasa de registro.

Por cualquiera de estos motivos, informe de estos problemas al proveedor de la aplicación o servicio que genera los eventos. Estos problemas solo los puede solucionar el desarrollador de la aplicación o el servicio que registra los eventos. Si los eventos que faltan se notifican en el servicio de registro de eventos, esto puede indicar un problema con la configuración del servicio de registro de eventos. El usuario puede tener una capacidad limitada para aumentar el espacio máximo en disco que usará el servicio de registro de eventos, lo que puede reducir el número de eventos que faltan.

 

 
