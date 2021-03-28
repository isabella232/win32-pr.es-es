---
description: Esta documentación es para las aplicaciones de modo de usuario que desean usar ETW. Para obtener información acerca de la instrumentación de controladores de dispositivos que se ejecutan en el modo kernel, consulte seguimiento de software WPP y agregar seguimiento de eventos a controladores de Kernel-Mode en el kit de controladores de Windows (WDK).
ms.assetid: 3de69436-671b-46a2-8d92-4eb3af2a4233
title: Seguimiento de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9802635fffddfea79c979534771605af13949d69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361464"
---
# <a name="event-tracing"></a>Seguimiento de eventos

## <a name="purpose"></a>Propósito

Seguimiento de eventos para Windows (ETW) proporciona a los programadores de aplicaciones la capacidad de iniciar y detener sesiones de seguimiento de eventos, instrumentar una aplicación para proporcionar eventos de seguimiento y consumir eventos de seguimiento. Los eventos de seguimiento contienen un encabezado de evento y datos definidos por el proveedor que describen el estado actual de una aplicación u operación. Puede usar los eventos para depurar una aplicación y realizar análisis de rendimiento y capacidad.

Esta documentación es para las aplicaciones de modo de usuario que desean usar ETW. Para obtener información acerca de la instrumentación de controladores de dispositivos que se ejecutan en el modo kernel, consulte [seguimiento de software WPP](/windows-hardware/drivers/devtest/wpp-software-tracing) y [Agregar seguimiento de eventos a controladores de Kernel-Mode](/windows-hardware/drivers/devtest/event-tracing-for-windows--etw-) en el kit de controladores de Windows (WDK).

## <a name="where-applicable"></a>Donde sea aplicable

Use ETW cuando desee instrumentar la aplicación, registrar eventos de usuario o de kernel en un archivo de registro y consumir eventos de un archivo de registro o en tiempo real.

## <a name="developer-audience"></a>Audiencia de desarrolladores

ETW está diseñado para desarrolladores de C y C++ que escriben aplicaciones en modo usuario.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

ETW se incluye en Microsoft Windows 2000 y versiones posteriores. Para obtener información acerca de los sistemas operativos necesarios para usar una función determinada, consulte la sección de requisitos de la documentación de la función.

## <a name="process-etw-traces-in-net-code"></a>Procesar seguimientos de ETW en código .NET

Puede usar la [API TraceProcessing de .net](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) para analizar seguimientos de ETW para las aplicaciones y otros componentes de software. Esta API se usa internamente en Microsoft para analizar los datos de ETW generados por Windows Engineering System y también se usa para potenciar varias tablas en el [analizador de rendimiento de Windows](/windows-hardware/test/wpt/windows-performance-analyzer). Esta API está disponible como un paquete NuGet.

Para obtener más información, consulte [este artículo](/windows/apps/trace-processing/overview).

## <a name="in-this-section"></a>En esta sección



| Tema                                                                     | Descripción                                                                        |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Novedades del seguimiento de eventos](what-s-new-in-event-tracing.md)<br/> | Nuevas características que se agregaron al seguimiento de eventos en cada versión.<br/>          |
| [Acerca del seguimiento de eventos](about-event-tracing.md)<br/>                 | Información general sobre el seguimiento de eventos.<br/>                                |
| [Usar el seguimiento de eventos](using-event-tracing.md)<br/>                 | Temas relacionados con tareas que describen cómo usar la API ETW.<br/>               |
| [Referencia de seguimiento de eventos](event-tracing-reference.md)<br/>         | Descripciones detalladas de las funciones ETW y otros elementos de programación. <br/> |



 

 

 
