---
title: Seguimiento del registro de C/C++ Inicio rápido
description: En la sección siguiente se describen los pasos básicos necesarios para agregar TraceLogging al código nativo en modo de usuario.
ms.assetid: 444DA34B-7949-457D-A3EC-2F0CFBEDD1E2
ms.topic: article
ms.date: 02/20/2020
ms.openlocfilehash: cb3734e3f314270e3d8082f5c9d25d38ce065829b94c659023950e5e2709047b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966504"
---
# <a name="tracelogging-cc-quick-start"></a>Seguimiento del registro de C/C++ Inicio rápido

En la sección siguiente se describen los pasos básicos necesarios para agregar TraceLogging al código nativo en modo de usuario.

## <a name="prerequisites"></a>Prerrequisitos

-   Windows 10
-   Microsoft Visual Studio 2013
-   Windows 10 El Kit de desarrollo de software (SDK) es necesario para escribir un proveedor en modo de usuario
-   Windows Se requiere el Kit de controladores (WDK) Windows 10 para escribir un proveedor de modo kernel

> [!IMPORTANT]
> Vincule advapi32.lib para compilar estos ejemplos.

### <a name="simpletraceloggingexampleh"></a>SimpleTraceLoggingExample.h

Este encabezado de ejemplo incluye las API traceLogging y forward declara el identificador del proveedor que se usará para registrar eventos. Cualquier clase que desee usar TraceLogging incluirá este encabezado y, a continuación, puede iniciar el registro.

```C++
#pragma once

#include <windows.h> // Defines macros used by TraceLoggingProvider.h
#include <TraceLoggingProvider.h>  // The native TraceLogging API

// Forward-declare the g_hMyComponentProvider variable that you will use for tracing in this component
TRACELOGGING_DECLARE_PROVIDER( g_hMyComponentProvider );

```

El archivo de encabezado incluye TraceLoggingProvider.h, que define la API tracelogging nativa. Primero debe incluir Windows.h porque define las constantes usadas por TraceLoggingProvider.h.

El reenvío del archivo de encabezado declara el identificador del proveedor que se pasará a las API `g_hMyComponentProvider` tracelogging para registrar eventos. Este identificador debe ser accesible para cualquier código que desee usar TraceLogging.

[**REGISTRO DE SEGUIMIENTO \_ DECLARE \_ PROVIDER**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) es una macro que crea un identificador con el nombre que se proporciona, que en `extern const TraceLoggingHProvider` el ejemplo anterior es `g_hMyComponentProvider` . Asignará la variable de identificador de proveedor real en un archivo de código.

### <a name="simpletraceloggingexamplecpp"></a>SimpleTraceLoggingExample.cpp

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

En el ejemplo anterior se incluye SimpleTraceLoggingExample.h, que contiene la variable de proveedor global que el código usará para registrar eventos.

La [**macro TRACELOGGING \_ DEFINE \_ PROVIDER**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_define_provider) asigna almacenamiento y define la variable de identificador del proveedor. El nombre de variable que proporcione a esta macro debe coincidir con el nombre que usó en la macro [**TRACELOGGING \_ DECLARE \_ PROVIDER**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) del archivo de encabezado. Este identificador seguirá siendo válido siempre que esté en el ámbito.

### <a name="register-the-provider-handle"></a>Registro del identificador del proveedor

Para poder usar el identificador del proveedor para registrar eventos, debe llamar a [**TraceLoggingRegister**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) para registrar el identificador del proveedor. Esto suele hacerse en Main() o DLLMain(), pero se puede hacer en cualquier momento, siempre que preceda a cualquier intento de registrar un evento. Si registra un evento antes de registrar el identificador del proveedor, no se producirá ningún error, pero el evento no se registrará. El código siguiente del ejemplo anterior registra el identificador del proveedor.

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

### <a name="log-a-tracelogging-event"></a>Registro de un evento de seguimiento

Una vez registrado el proveedor, el código siguiente registra un evento simple.

```C++
    // Log an event
    TraceLoggingWrite(g_hMyComponentProvider, // handle to my provider
        "HelloWorldTestEvent",              // Event Name that should uniquely identify your event.
        TraceLoggingValue(sampleValue, "TestMessage")); // Field for your event in the form of (value, field name).
```

La [**macro TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) toma hasta 99 argumentos y se ejecuta como varias instrucciones. Esto significa que los valores que se registran no deben ser objetos temporales de C++. El nombre del evento se almacena en formato UTF-8. No debe usar caracteres `null` incrustados en el evento ni en otros nombres de campo. No hay otros límites en los caracteres permitidos.

Cada argumento que sigue al nombre del evento se debe encapsular dentro de una [macro de contenedor tracelogging](tracelogging-wrapper-macros.md). Si usa C++, puede usar la macro contenedora para deducir automáticamente `TraceLoggingValue` el tipo del argumento. Si escribe el controlador en C, debe usar macros de campo específicas del tipo, como `TraceLoggingInt32` , `TraceLoggingUnicodeString` , , `TraceLoggingString` etc. Las macros de contenedor TraceLogging se definen en TraceLoggingProvider.h

Además de registrar eventos únicos, también puede agrupar eventos por actividad mediante las macros [**TraceLoggingWriteActivity**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwriteactivity) o [**TraceLoggingWriteStart**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestart) / [**TraceLoggingWriteStop**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestop) que se encuentran en TraceLoggingActivity.h. Las actividades correlacionan eventos y son útiles para escenarios que tienen un principio y un final. Por ejemplo, puede usar una actividad para medir un escenario que comienza con el inicio de una aplicación, incluye el tiempo que tarda en estar disponible la pantalla de presentación y finaliza cuando la pantalla inicial de la aplicación se vuelve visible.

Las actividades capturan eventos únicos y anidan otras actividades que se producen entre el inicio y el final de esa actividad. Las actividades tienen ámbito por proceso y se deben pasar de subproceso a subproceso para anidar correctamente eventos multiproceso.

El ámbito de un identificador de proveedor está estrictamente limitado al módulo (archivo DLL, EXE o SYS) en el que se define: el identificador no debe pasarse a otros archivos DLL. Si se invoca una macro [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) en A.DLL mediante un identificador de proveedor definido en B.DLL, puede causar problemas. La manera más segura y eficaz de cumplir este requisito es simplemente hacer referencia directamente al identificador del proveedor global y nunca pasar el identificador del proveedor como parámetro.

### <a name="unregister-the-provider"></a>Anulación del registro del proveedor

Cuando haya terminado de registrar eventos, debe anular el registro del proveedor traceLogging. El código siguiente anula el registro del proveedor.

```C++
    // Stop TraceLogging and unregister the provider
    TraceLoggingUnregister(g_hMyComponentProvider);
```

## <a name="compatibility"></a>Compatibilidad

En función de su configuración, TraceLoggingProvider.h puede ser compatible con versiones anteriores (compatibles con Windows Vista o versiones posteriores) o puede optimizarse para versiones posteriores del sistema operativo. TraceLoggingProvider.h usa WINVER (modo de usuario) y NTDDI_VERSION (modo kernel) para determinar si debe ser compatible con versiones anteriores del sistema operativo o estar optimizada para versiones más recientes del sistema operativo.

Para el modo de usuario, si incluye <windows.h> antes de establecer WINVER, <windows.h> establece WINVER en la versión predeterminada del sistema operativo de destino del SDK. Si WINVER está establecido en 0x602 o superior, TraceLoggingProvider.h optimiza su comportamiento para Windows 8 (la aplicación no se ejecutará en versiones anteriores de Windows). Si necesita que el programa se ejecute en Vista o Windows 7, asegúrese de establecer WINVER en el valor adecuado antes de incluir <windows.h>.

Del mismo modo, si incluye <wdm.h> antes de establecer NTDDI_VERSION, <wdm.h> establece NTDDI_VERSION en un valor predeterminado. Si NTDDI_VERSION se establece en 0x06040000 o superior, TraceLoggingProvider.h optimiza su comportamiento para Windows 10 (el controlador no funcionará en versiones anteriores de Windows).

## <a name="summary-and-next-steps"></a>Resumen y pasos siguientes

Para ver cómo capturar y ver los datos de TraceLogging con las versiones internas más recientes de Windows Performance Tools (WPT), vea [Record and Display TraceLogging Events](tracelogging-record-and-display-tracelogging-events.md).

Vea [C/C++ Tracelogging Examples (Ejemplos](tracelogging-c-cpp-tracelogging-examples.md) de registro de seguimiento de C/C++) para obtener más ejemplos de seguimiento de C++.

 

 




