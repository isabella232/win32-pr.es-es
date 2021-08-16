---
description: Esta documentación es para las aplicaciones en modo de usuario que desean usar ETW. Para obtener información sobre cómo instrumentar controladores de dispositivo que se ejecutan en modo kernel, vea Seguimiento de software de WPP y Adición de seguimiento de eventos a controladores de Kernel-Mode en el kit de controladores de Windows (WDK).
ms.assetid: 3de69436-671b-46a2-8d92-4eb3af2a4233
title: Seguimiento de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 908e935d48749d80e5b2cfe237efeed5413c839157e53b489f4857c0349b4a1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070225"
---
# <a name="event-tracing"></a>Seguimiento de eventos

## <a name="purpose"></a>Propósito

Seguimiento de eventos para Windows (ETW) proporciona a los programadores de aplicaciones la capacidad de iniciar y detener sesiones de seguimiento de eventos, instrumentar una aplicación para proporcionar eventos de seguimiento y consumir eventos de seguimiento. Los eventos de seguimiento contienen un encabezado de evento y datos definidos por el proveedor que describen el estado actual de una aplicación u operación. Puede usar los eventos para depurar una aplicación y realizar análisis de capacidad y rendimiento.

Esta documentación es para las aplicaciones en modo de usuario que desean usar ETW. Para obtener información sobre cómo instrumentar controladores de dispositivo que se ejecutan en modo kernel, vea Seguimiento de software de [WPP](/windows-hardware/drivers/devtest/wpp-software-tracing) y Adición de seguimiento de eventos a controladores de [Kernel-Mode](/windows-hardware/drivers/devtest/event-tracing-for-windows--etw-) en el kit de controladores de Windows (WDK).

## <a name="where-applicable"></a>Donde sea aplicable

Use ETW cuando desee instrumentar la aplicación, registrar eventos de usuario o kernel en un archivo de registro y consumir eventos de un archivo de registro o en tiempo real.

## <a name="developer-audience"></a>Audiencia de desarrolladores

ETW está diseñado para desarrolladores de C y C++ que escriben aplicaciones en modo de usuario.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

ETW se incluye en Microsoft Windows 2000 y versiones posteriores. Para obtener información sobre qué sistemas operativos deben usar una función determinada, consulte la sección Requisitos de la documentación de la función.

## <a name="process-etw-traces-in-net-code"></a>Procesar seguimientos ETW en código .NET

Puede usar la [API TraceProcessing de .NET](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) para analizar los seguimientos de ETW de las aplicaciones y otros componentes de software. Esta API se usa internamente en Microsoft para analizar los datos ETW generados por el sistema de ingeniería Windows y también se usa para encender varias tablas [en Windows Analizador de rendimiento](/windows-hardware/test/wpt/windows-performance-analyzer). Esta API está disponible como un NuGet paquete.

Para obtener más información, consulta [este artículo](/windows/apps/trace-processing/overview).

## <a name="in-this-section"></a>En esta sección



| Tema                                                                     | Descripción                                                                        |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Novedades del seguimiento de eventos](what-s-new-in-event-tracing.md)<br/> | Nuevas características que se agregaron al seguimiento de eventos en cada versión.<br/>          |
| [Acerca del seguimiento de eventos](about-event-tracing.md)<br/>                 | Información general sobre el seguimiento de eventos.<br/>                                |
| [Uso del seguimiento de eventos](using-event-tracing.md)<br/>                 | Temas relacionados con tareas que describen cómo usar la API de ETW.<br/>               |
| [Referencia de seguimiento de eventos](event-tracing-reference.md)<br/>         | Descripciones detalladas de funciones ETW y otros elementos de programación. <br/> |



 

 

 
