---
title: Uso de TraceLogging
description: En los temas siguientes se proporciona un inicio rápido de TraceLogging para código nativo y administrado, con ejemplos.
ms.assetid: CEC57517-7A0E-45AA-85F7-F358AE51EF4A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e331f5ebec3d7eb8ce9c50d3e9d92f747bf76414
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362871"
---
# <a name="using-tracelogging"></a>Uso de TraceLogging

En los temas siguientes se proporciona un inicio rápido de TraceLogging para código nativo y administrado, con ejemplos.

## <a name="prerequisites"></a>Prerrequisitos

-   Windows 10 El Kit de desarrollo de software (SDK) es necesario para escribir un proveedor de modo de usuario
-   Windows Driver Kit (WDK) es necesario para escribir un proveedor de modo kernel

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                        | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Seguimiento de C/C++ Inicio rápido](tracelogging-native-quick-start.md)<br/>                             | En la sección siguiente se describen los pasos básicos necesarios para agregar TraceLogging al código nativo en modo de usuario. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [Seguimiento de registros administrados Inicio rápido](tracelogging-managed-quick-start.md)<br/>                          | En la sección siguiente se describen los pasos básicos necesarios para agregar TraceLogging al código administrado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [Registrar y mostrar eventos de seguimiento](tracelogging-record-and-display-tracelogging-events.md)<br/> | Registre los eventos tracelogging con Windows Performance Recorder (WPR) y véalos con Windows Analizador de rendimiento (WPA).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [Ejemplos de seguimiento de C/C++](tracelogging-c-cpp-tracelogging-examples.md)<br/>                       | Este tema contiene ejemplos de seguimiento de C/C++.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [Ejemplos de seguimiento de .NET](tracelogging-net-examples.md)<br/>                                       | Este tema contiene un ejemplo de seguimiento de código administrado que muestra cómo registrar un evento solo cuando el nivel de detalle de la sesión es detallado y cómo registrar datos de eventos estructurados.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [Ejemplo Windows registro de plataforma universal](universal-windows-platform-logging-examples.md)<br/>     | En este ejemplo se muestra cómo usar las API de registro en el Windows. Espacio de nombres Foundation.Diagnostics, incluidos LoggingChannel, LoggingActivity, LoggingSession y FileLoggingSession. Estas clases están diseñadas para el registro de diagnóstico dentro de una Windows aplicación. Estas API se agregaron en Windows 8.1. <br/> Las API LoggingChannel y LoggingActivity se han ampliado en Windows 10 para admitir la escritura de eventos complejos mediante la codificación de eventos TraceLogging.<br/> El ejemplo de registro Windows plataforma universal se puede descargar desde [GitHub](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/Logging).<br/> |



 

Ejemplos de seguimiento de registros.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Seguimiento de controladores y componentes en modo kernel](/windows-hardware/drivers/devtest/tracelogging-for-kernel-mode-drivers-and-components)
</dt> </dl>

 

