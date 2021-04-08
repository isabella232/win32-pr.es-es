---
title: TraceLogging C/C++ Inicio rápido
description: En la siguiente sección se describen los pasos básicos necesarios para agregar TraceLogging al código nativo en modo de usuario.
ms.assetid: 444DA34B-7949-457D-A3EC-2F0CFBEDD1E2
ms.topic: article
ms.date: 02/20/2020
ms.openlocfilehash: 7be18feb7f372922b7e3b811cd0c9941240e18e3
ms.sourcegitcommit: 0aa1dd7577961438a1b3172f3a92fb11cbf359f1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2020
ms.locfileid: "103994997"
---
# <a name="tracelogging-cc-quick-start"></a>TraceLogging C/C++ Inicio rápido

En la siguiente sección se describen los pasos básicos necesarios para agregar TraceLogging al código nativo en modo de usuario.

## <a name="prerequisites"></a>Requisitos previos

-   Windows 10
-   Microsoft Visual Studio 2013
-   El kit de desarrollo de software (SDK) de Windows 10 es necesario para escribir un proveedor de modo de usuario
-   Windows Driver Kit (WDK) para Windows 10 es necesario para escribir un proveedor de modo kernel

> [!IMPORTANT]
> Vincule advapi32. lib para compilar estos ejemplos.

### <a name="simpletraceloggingexampleh"></a>SimpleTraceLoggingExample. h

Este encabezado de ejemplo incluye las API de TraceLogging y forward declara el identificador de proveedor que se usará para registrar eventos. Cualquier clase que desee usar TraceLogging incluirá este encabezado y podrá iniciar el registro.

```C++
#pragma once

#include <windows.h> // Defines macros used by TraceLoggingProvider.h
#include <TraceLoggingProvider.h>  // The native TraceLogging API

// Forward-declare the g_hMyComponentProvider variable that you will use for tracing in this component
TRACELOGGING_DECLARE_PROVIDER( g_hMyComponentProvider );

```

El archivo de encabezado incluye TraceLoggingProvider. h, que define la API de TraceLogging nativa. Debe incluir primero Windows. h porque define las constantes utilizadas por TraceLoggingProvider. h.

El archivo de encabezado Forward declara el identificador de proveedor `g_hMyComponentProvider` que pasará a las API de TraceLogging para registrar los eventos. Este identificador debe ser accesible para cualquier código que desee usar TraceLogging.

[**TRACELOGGING \_ Declare \_ Provider**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) es una macro que crea un `extern const TraceLoggingHProvider` identificador con el nombre proporcionado, que en el ejemplo anterior es `g_hMyComponentProvider` . Asignará la variable de identificador de proveedor real en un archivo de código.

### <a name="simpletraceloggingexamplecpp"></a>SimpleTraceLoggingExample. cpp

En el ejemplo siguiente se registra el proveedor, se registra un evento y se anula el registro del proveedor.

```C++
#include "SimpleTraceLoggingExample.h"

    // Define the GUID to use in TraceLoggingProviderRegister 
    // {3970F9cf-2c0c-4f11-b1cc-e3a1e9958833}
TRACELOGGING_DEFINE_PROVIDER(
    g_hMyComponentProvider,
    "SimpleTraceLoggingProvider",
    (0x3970f9cf, 0x2c0c, 0x4f11, 0xb1, 0xcc, 0xe3, 0xa1, 0xe9, 0x95, 0x88, 0x33));


void main()
{

    char sampleValue[] = "Sample value";

    // Register the provider
    TraceLoggingRegister(g_hMyComponentProvider);
    // Log an event
    TraceLoggingWrite(g_hMyComponentProvider, // handle to my provider
        "HelloWorldTestEvent",              // Event Name that should uniquely identify your event.
        TraceLoggingValue(sampleValue, "TestMessage")); // Field for your event in the form of (value, field name).
    // Stop TraceLogging and unregister the provider
    TraceLoggingUnregister(g_hMyComponentProvider);
}
```

En el ejemplo anterior se incluye SimpleTraceLoggingExample. h, que contiene la variable de proveedor global que utilizará el código para registrar los eventos.

La macro de [**\_ \_ proveedor de definición de TRACELOGGING**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_define_provider) asigna almacenamiento y define la variable de identificador de proveedor. El nombre de la variable que proporcione a esta macro debe coincidir con el nombre que usó en la macro [**TRACELOGGING \_ declare \_ Provider**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) en el archivo de encabezado. Este identificador seguirá siendo válido mientras esté dentro del ámbito.

### <a name="register-the-provider-handle"></a>Registrar el identificador de proveedor

Antes de poder usar el identificador de proveedor para registrar eventos, debe llamar a [**TraceLoggingRegister**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) para registrar el identificador del proveedor. Esto se hace normalmente en Main () o DLLMain (), pero se puede hacer en cualquier momento siempre que preceda cualquier intento de registrar un evento. Si registra un evento antes de registrar el identificador del proveedor, no se producirá ningún error, pero no se registrará el evento. El siguiente código del ejemplo anterior registra el identificador del proveedor.

```C++
    // Define the GUID to use in TraceLoggingProviderRegister 
    // {3970F9cf-2c0c-4f11-b1cc-e3a1e9958833}
TRACELOGGING_DEFINE_PROVIDER(
    g_hMyComponentProvider,
    "SimpleTraceLoggingProvider",
    (0x3970f9cf, 0x2c0c, 0x4f11, 0xb1, 0xcc, 0xe3, 0xa1, 0xe9, 0x95, 0x88, 0x33));


void main()
{

    char sampleValue[] = "Sample value";

    // Register the provider
    TraceLoggingRegister(g_hMyComponentProvider);
```

### <a name="log-a-tracelogging-event"></a>Registrar un evento Tracelogging

Una vez registrado el proveedor, el código siguiente registra un evento simple.

```C++
    // Log an event
    TraceLoggingWrite(g_hMyComponentProvider, // handle to my provider
        "HelloWorldTestEvent",              // Event Name that should uniquely identify your event.
        TraceLoggingValue(sampleValue, "TestMessage")); // Field for your event in the form of (value, field name).
```

La macro [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) toma hasta 99 argumentos y se ejecuta como varias instrucciones. Esto significa que los valores que se registran no deben ser objetos temporales de C++. El nombre del evento se almacena en formato UTF-8. No debe utilizar caracteres insertados `null` en los nombres de evento o de otros campos. No hay ningún otro límite en los caracteres permitidos.

Cada argumento que sigue al nombre del evento debe ajustarse dentro de una [macro de contenedor TraceLogging](tracelogging-wrapper-macros.md). Si usa C++, puede usar la `TraceLoggingValue` macro de contenedor para deducir automáticamente el tipo del argumento. Si está escribiendo el controlador en C, debe usar macros de campo específicas del tipo `TraceLoggingInt32` , como, `TraceLoggingUnicodeString` , `TraceLoggingString` , etc. Las macros de contenedor TraceLogging se definen en TraceLoggingProvider. h

Además de registrar eventos individuales, también puede agrupar eventos por actividad mediante las macros [**TraceLoggingWriteActivity**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwriteactivity) o [**TraceLoggingWriteStart**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestart) / [**TraceLoggingWriteStop**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestop) que se encuentran en TraceLoggingActivity. h. Las actividades correlacionan los eventos y son útiles para los escenarios que tienen un principio y un final. Por ejemplo, puede utilizar una actividad para medir un escenario que empieza con el inicio de una aplicación, incluye el tiempo que tarda la pantalla de presentación en estar disponible y finaliza cuando la pantalla inicial de la aplicación se vuelve visible.

Las actividades capturan eventos individuales y anidan otras actividades que se producen entre el inicio y el final de esa actividad. Las actividades tienen un ámbito por proceso y se deben pasar del subproceso al subproceso para anidar correctamente los eventos multiproceso.

El ámbito de un identificador de proveedor está estrictamente limitado al módulo (archivo DLL, EXE o SYS) en el que está definido: el identificador no se debe pasar a otros archivos dll. Si se invoca una macro [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) en A.DLL mediante un identificador de proveedor definido en B.DLL, puede causar problemas. La forma más segura y eficaz de cumplir este requisito es simplemente hacer referencia directamente al identificador global del proveedor y nunca pasar el identificador del proveedor como parámetro.

### <a name="unregister-the-provider"></a>Anular el registro del proveedor

Cuando haya terminado de registrar los eventos, debe anular el registro del proveedor TraceLogging. En el código siguiente se anula el registro del proveedor.

```C++
    // Stop TraceLogging and unregister the provider
    TraceLoggingUnregister(g_hMyComponentProvider);
```

## <a name="compatibility"></a>Compatibilidad

En función de su configuración, TraceLoggingProvider. h puede ser compatible con versiones anteriores (compatible con Windows Vista o posterior), o bien se puede optimizar para versiones posteriores del sistema operativo. TraceLoggingProvider. h usa WINVER (modo de usuario) y NTDDI_VERSION (modo kernel) para determinar si debe ser compatible con versiones anteriores del sistema operativo o estar optimizado para versiones más recientes del sistema operativo.

En el modo de usuario, si incluye <Windows. h> antes de configurar WINVER, <Windows. h> establece WINVER en la versión del sistema operativo de destino predeterminada del SDK. Si WINVER se establece en 0x602 o superior, TraceLoggingProvider. h optimiza su comportamiento para Windows 8 (la aplicación no se ejecutará en versiones anteriores de Windows). Si necesita que el programa se ejecute en vista o Windows 7, asegúrese de establecer WINVER en el valor adecuado antes de incluir <Windows. h>.

Del mismo modo, si incluye <> WDM. h antes de establecer NTDDI_VERSION, <WDM. h> establece NTDDI_VERSION en un valor predeterminado. Si NTDDI_VERSION se establece en 0x06040000 o superior, TraceLoggingProvider. h optimiza su comportamiento para Windows 10 (el controlador no funcionará en versiones anteriores de Windows).

## <a name="summary-and-next-steps"></a>Resumen y pasos siguientes

Para ver cómo capturar y ver los datos de TraceLogging con las versiones internas más recientes de las herramientas de rendimiento de Windows (WPT), consulte [grabar y Mostrar eventos de TraceLogging](tracelogging-record-and-display-tracelogging-events.md).

Vea [ejemplos de C/C++ Tracelogging](tracelogging-c-cpp-tracelogging-examples.md) para obtener más ejemplos de Tracelogging de c++.

 

 




