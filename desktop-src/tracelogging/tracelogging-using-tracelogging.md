---
title: Usar TraceLogging
description: En los temas siguientes se proporciona una guía de inicio rápido de TraceLogging para código nativo y administrado, con ejemplos.
ms.assetid: CEC57517-7A0E-45AA-85F7-F358AE51EF4A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e331f5ebec3d7eb8ce9c50d3e9d92f747bf76414
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421334"
---
# <a name="using-tracelogging"></a>Usar TraceLogging

En los temas siguientes se proporciona una guía de inicio rápido de TraceLogging para código nativo y administrado, con ejemplos.

## <a name="prerequisites"></a>Requisitos previos

-   El kit de desarrollo de software (SDK) de Windows 10 es necesario para escribir un proveedor de modo de usuario
-   El kit de controladores de Windows (WDK) es necesario para escribir un proveedor de modo kernel

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                        | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [TraceLogging C/C++ Inicio rápido](tracelogging-native-quick-start.md)<br/>                             | En la siguiente sección se describen los pasos básicos necesarios para agregar TraceLogging al código nativo en modo de usuario. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [Inicio rápido administrada de TraceLogging](tracelogging-managed-quick-start.md)<br/>                          | En la siguiente sección se describen los pasos básicos necesarios para agregar TraceLogging a código administrado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [Grabar y Mostrar eventos TraceLogging](tracelogging-record-and-display-tracelogging-events.md)<br/> | Grabe eventos de TraceLogging con la grabadora de rendimiento de Windows (WPR) y verlos con el analizador de rendimiento de Windows (WPA).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [Ejemplos de Tracelogging de C/C++](tracelogging-c-cpp-tracelogging-examples.md)<br/>                       | En este tema se incluyen ejemplos de Tracelogging de C/C++.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [Ejemplos de Tracelogging de .NET](tracelogging-net-examples.md)<br/>                                       | En este tema se incluye un ejemplo de Tracelogging de código administrado que muestra cómo registrar un evento solo cuando el nivel de detalle de la sesión es detallado y cómo registrar datos de eventos estructurados.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [Ejemplo de registro de Plataforma universal de Windows](universal-windows-platform-logging-examples.md)<br/>     | En este ejemplo se muestra cómo usar las API de registro en el espacio de nombres Windows. Foundation. Diagnostics, incluidos LoggingChannel, LoggingActivity, LoggingSession y FileLoggingSession. Estas clases están diseñadas para el registro de diagnósticos dentro de una aplicación de Windows. Estas API se agregaron en Windows 8.1. <br/> Las API LoggingChannel y LoggingActivity se han ampliado en Windows 10 para admitir la escritura de eventos complejos mediante la codificación de eventos TraceLogging.<br/> El ejemplo de registro de Plataforma universal de Windows se puede descargar desde [GitHub](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/Logging).<br/> |



 

Ejemplos de TraceLogging.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[TraceLogging para controladores y componentes de modo kernel](/windows-hardware/drivers/devtest/tracelogging-for-kernel-mode-drivers-and-components)
</dt> </dl>

 

