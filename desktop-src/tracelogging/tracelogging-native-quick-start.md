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
# <a name="tracelogging-cc-quick-start"></a><span data-ttu-id="e1992-103">TraceLogging C/C++ Inicio rápido</span><span class="sxs-lookup"><span data-stu-id="e1992-103">TraceLogging C/C++ Quick Start</span></span>

<span data-ttu-id="e1992-104">En la siguiente sección se describen los pasos básicos necesarios para agregar TraceLogging al código nativo en modo de usuario.</span><span class="sxs-lookup"><span data-stu-id="e1992-104">The following section describes the basic steps required to add TraceLogging to native user-mode code.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e1992-105">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e1992-105">Prerequisites</span></span>

-   <span data-ttu-id="e1992-106">Windows 10</span><span class="sxs-lookup"><span data-stu-id="e1992-106">Windows 10</span></span>
-   <span data-ttu-id="e1992-107">Microsoft Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="e1992-107">Microsoft Visual Studio 2013</span></span>
-   <span data-ttu-id="e1992-108">El kit de desarrollo de software (SDK) de Windows 10 es necesario para escribir un proveedor de modo de usuario</span><span class="sxs-lookup"><span data-stu-id="e1992-108">Windows 10 Software Development Kit (SDK) is required to write a user-mode provider</span></span>
-   <span data-ttu-id="e1992-109">Windows Driver Kit (WDK) para Windows 10 es necesario para escribir un proveedor de modo kernel</span><span class="sxs-lookup"><span data-stu-id="e1992-109">Windows Driver Kit (WDK) for Windows 10 is required to write a kernel-mode provider</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e1992-110">Vincule advapi32. lib para compilar estos ejemplos.</span><span class="sxs-lookup"><span data-stu-id="e1992-110">Link advapi32.lib in order to compile these examples.</span></span>

### <a name="simpletraceloggingexampleh"></a><span data-ttu-id="e1992-111">SimpleTraceLoggingExample. h</span><span class="sxs-lookup"><span data-stu-id="e1992-111">SimpleTraceLoggingExample.h</span></span>

<span data-ttu-id="e1992-112">Este encabezado de ejemplo incluye las API de TraceLogging y forward declara el identificador de proveedor que se usará para registrar eventos.</span><span class="sxs-lookup"><span data-stu-id="e1992-112">This example header includes the TraceLogging APIs and forward declares the provider handle that will be used to log events.</span></span> <span data-ttu-id="e1992-113">Cualquier clase que desee usar TraceLogging incluirá este encabezado y podrá iniciar el registro.</span><span class="sxs-lookup"><span data-stu-id="e1992-113">Any class that wishes to use TraceLogging will include this header and can then start logging.</span></span>

```C++
#pragma once

#include <windows.h> // Defines macros used by TraceLoggingProvider.h
#include <TraceLoggingProvider.h>  // The native TraceLogging API

// Forward-declare the g_hMyComponentProvider variable that you will use for tracing in this component
TRACELOGGING_DECLARE_PROVIDER( g_hMyComponentProvider );

```

<span data-ttu-id="e1992-114">El archivo de encabezado incluye TraceLoggingProvider. h, que define la API de TraceLogging nativa.</span><span class="sxs-lookup"><span data-stu-id="e1992-114">The header file includes TraceLoggingProvider.h which defines the native TraceLogging API.</span></span> <span data-ttu-id="e1992-115">Debe incluir primero Windows. h porque define las constantes utilizadas por TraceLoggingProvider. h.</span><span class="sxs-lookup"><span data-stu-id="e1992-115">You must include Windows.h first because it defines constants used by TraceLoggingProvider.h.</span></span>

<span data-ttu-id="e1992-116">El archivo de encabezado Forward declara el identificador de proveedor `g_hMyComponentProvider` que pasará a las API de TraceLogging para registrar los eventos.</span><span class="sxs-lookup"><span data-stu-id="e1992-116">The header file forward declares the provider handle `g_hMyComponentProvider` that you will pass to the TraceLogging APIs to log events.</span></span> <span data-ttu-id="e1992-117">Este identificador debe ser accesible para cualquier código que desee usar TraceLogging.</span><span class="sxs-lookup"><span data-stu-id="e1992-117">This handle needs to be accessible to any code that wishes to use TraceLogging.</span></span>

<span data-ttu-id="e1992-118">[**TRACELOGGING \_ Declare \_ Provider**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) es una macro que crea un `extern const TraceLoggingHProvider` identificador con el nombre proporcionado, que en el ejemplo anterior es `g_hMyComponentProvider` .</span><span class="sxs-lookup"><span data-stu-id="e1992-118">[**TRACELOGGING\_DECLARE\_PROVIDER**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) is a macro that creates an `extern const TraceLoggingHProvider` handle using the name that you provide, which in the example above is `g_hMyComponentProvider`.</span></span> <span data-ttu-id="e1992-119">Asignará la variable de identificador de proveedor real en un archivo de código.</span><span class="sxs-lookup"><span data-stu-id="e1992-119">You will allocate the actual provider handle variable in a code file.</span></span>

### <a name="simpletraceloggingexamplecpp"></a><span data-ttu-id="e1992-120">SimpleTraceLoggingExample. cpp</span><span class="sxs-lookup"><span data-stu-id="e1992-120">SimpleTraceLoggingExample.cpp</span></span>

<span data-ttu-id="e1992-121">En el ejemplo siguiente se registra el proveedor, se registra un evento y se anula el registro del proveedor.</span><span class="sxs-lookup"><span data-stu-id="e1992-121">The following example registers the provider, logs an event, and unregisters the provider.</span></span>

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

<span data-ttu-id="e1992-122">En el ejemplo anterior se incluye SimpleTraceLoggingExample. h, que contiene la variable de proveedor global que utilizará el código para registrar los eventos.</span><span class="sxs-lookup"><span data-stu-id="e1992-122">The example above includes SimpleTraceLoggingExample.h which contains the global provider variable that your code will use to log events.</span></span>

<span data-ttu-id="e1992-123">La macro de [**\_ \_ proveedor de definición de TRACELOGGING**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_define_provider) asigna almacenamiento y define la variable de identificador de proveedor.</span><span class="sxs-lookup"><span data-stu-id="e1992-123">The [**TRACELOGGING\_DEFINE\_PROVIDER**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_define_provider) macro allocates storage and defines the provider handle variable.</span></span> <span data-ttu-id="e1992-124">El nombre de la variable que proporcione a esta macro debe coincidir con el nombre que usó en la macro [**TRACELOGGING \_ declare \_ Provider**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) en el archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="e1992-124">The variable name that you provide to this macro must match the name you used in the [**TRACELOGGING\_DECLARE\_PROVIDER**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogging_declare_provider) macro in your header file.</span></span> <span data-ttu-id="e1992-125">Este identificador seguirá siendo válido mientras esté dentro del ámbito.</span><span class="sxs-lookup"><span data-stu-id="e1992-125">This handle will remain valid as long as it is in scope.</span></span>

### <a name="register-the-provider-handle"></a><span data-ttu-id="e1992-126">Registrar el identificador de proveedor</span><span class="sxs-lookup"><span data-stu-id="e1992-126">Register the provider handle</span></span>

<span data-ttu-id="e1992-127">Antes de poder usar el identificador de proveedor para registrar eventos, debe llamar a [**TraceLoggingRegister**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) para registrar el identificador del proveedor.</span><span class="sxs-lookup"><span data-stu-id="e1992-127">Before you can use the provider handle to log events you must call [**TraceLoggingRegister**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) to register your provider handle.</span></span> <span data-ttu-id="e1992-128">Esto se hace normalmente en Main () o DLLMain (), pero se puede hacer en cualquier momento siempre que preceda cualquier intento de registrar un evento.</span><span class="sxs-lookup"><span data-stu-id="e1992-128">This is typically done in Main() or DLLMain() but can be done at any time as long as it precedes any attempt to log an event.</span></span> <span data-ttu-id="e1992-129">Si registra un evento antes de registrar el identificador del proveedor, no se producirá ningún error, pero no se registrará el evento.</span><span class="sxs-lookup"><span data-stu-id="e1992-129">If you log an event before registering the provider handle, no error will occur but the event will not be logged.</span></span> <span data-ttu-id="e1992-130">El siguiente código del ejemplo anterior registra el identificador del proveedor.</span><span class="sxs-lookup"><span data-stu-id="e1992-130">The following code from the example above registers the provider handle.</span></span>

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

### <a name="log-a-tracelogging-event"></a><span data-ttu-id="e1992-131">Registrar un evento Tracelogging</span><span class="sxs-lookup"><span data-stu-id="e1992-131">Log a Tracelogging event</span></span>

<span data-ttu-id="e1992-132">Una vez registrado el proveedor, el código siguiente registra un evento simple.</span><span class="sxs-lookup"><span data-stu-id="e1992-132">After the provider is registered, the following code logs a simple event.</span></span>

```C++
    // Log an event
    TraceLoggingWrite(g_hMyComponentProvider, // handle to my provider
        "HelloWorldTestEvent",              // Event Name that should uniquely identify your event.
        TraceLoggingValue(sampleValue, "TestMessage")); // Field for your event in the form of (value, field name).
```

<span data-ttu-id="e1992-133">La macro [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) toma hasta 99 argumentos y se ejecuta como varias instrucciones.</span><span class="sxs-lookup"><span data-stu-id="e1992-133">The [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) macro takes up to ninety-nine arguments and executes as several statements.</span></span> <span data-ttu-id="e1992-134">Esto significa que los valores que se registran no deben ser objetos temporales de C++.</span><span class="sxs-lookup"><span data-stu-id="e1992-134">This means that the values being logged should not be C++ temporary objects.</span></span> <span data-ttu-id="e1992-135">El nombre del evento se almacena en formato UTF-8.</span><span class="sxs-lookup"><span data-stu-id="e1992-135">The event name is stored in UTF-8 format.</span></span> <span data-ttu-id="e1992-136">No debe utilizar caracteres insertados `null` en los nombres de evento o de otros campos.</span><span class="sxs-lookup"><span data-stu-id="e1992-136">You must not use embedded `null` characters in the event or other field names.</span></span> <span data-ttu-id="e1992-137">No hay ningún otro límite en los caracteres permitidos.</span><span class="sxs-lookup"><span data-stu-id="e1992-137">There are no other limits on permitted characters.</span></span>

<span data-ttu-id="e1992-138">Cada argumento que sigue al nombre del evento debe ajustarse dentro de una [macro de contenedor TraceLogging](tracelogging-wrapper-macros.md).</span><span class="sxs-lookup"><span data-stu-id="e1992-138">Each argument following the event name must be wrapped inside of a [TraceLogging Wrapper Macro](tracelogging-wrapper-macros.md).</span></span> <span data-ttu-id="e1992-139">Si usa C++, puede usar la `TraceLoggingValue` macro de contenedor para deducir automáticamente el tipo del argumento.</span><span class="sxs-lookup"><span data-stu-id="e1992-139">If you are using C++, you can use the `TraceLoggingValue` wrapper macro to automatically infer the type of the argument.</span></span> <span data-ttu-id="e1992-140">Si está escribiendo el controlador en C, debe usar macros de campo específicas del tipo `TraceLoggingInt32` , como, `TraceLoggingUnicodeString` , `TraceLoggingString` , etc. Las macros de contenedor TraceLogging se definen en TraceLoggingProvider. h</span><span class="sxs-lookup"><span data-stu-id="e1992-140">If you are writing your driver in C, you must use type-specific field macros such as `TraceLoggingInt32`, `TraceLoggingUnicodeString`, `TraceLoggingString`, etc. The TraceLogging wrapper macros are defined in TraceLoggingProvider.h</span></span>

<span data-ttu-id="e1992-141">Además de registrar eventos individuales, también puede agrupar eventos por actividad mediante las macros [**TraceLoggingWriteActivity**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwriteactivity) o [**TraceLoggingWriteStart**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestart) / [**TraceLoggingWriteStop**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestop) que se encuentran en TraceLoggingActivity. h.</span><span class="sxs-lookup"><span data-stu-id="e1992-141">In addition to logging single events you can also group events by activity by using the [**TraceLoggingWriteActivity**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwriteactivity) or [**TraceLoggingWriteStart**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestart)/[**TraceLoggingWriteStop**](/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestop) macros found in TraceLoggingActivity.h.</span></span> <span data-ttu-id="e1992-142">Las actividades correlacionan los eventos y son útiles para los escenarios que tienen un principio y un final.</span><span class="sxs-lookup"><span data-stu-id="e1992-142">Activities correlate events and are useful for scenarios that have a beginning and an end.</span></span> <span data-ttu-id="e1992-143">Por ejemplo, puede utilizar una actividad para medir un escenario que empieza con el inicio de una aplicación, incluye el tiempo que tarda la pantalla de presentación en estar disponible y finaliza cuando la pantalla inicial de la aplicación se vuelve visible.</span><span class="sxs-lookup"><span data-stu-id="e1992-143">For example, you might use an activity to measure a scenario that starts with the launch of an application, includes the time it takes for the splash screen becomes available, and ends when the initial screen of the application becomes visible.</span></span>

<span data-ttu-id="e1992-144">Las actividades capturan eventos individuales y anidan otras actividades que se producen entre el inicio y el final de esa actividad.</span><span class="sxs-lookup"><span data-stu-id="e1992-144">Activities capture single events and nest other activities that occur between the start and end of that activity.</span></span> <span data-ttu-id="e1992-145">Las actividades tienen un ámbito por proceso y se deben pasar del subproceso al subproceso para anidar correctamente los eventos multiproceso.</span><span class="sxs-lookup"><span data-stu-id="e1992-145">Activities have per-process scope and must be passed from thread to thread to properly nest multi-threaded events.</span></span>

<span data-ttu-id="e1992-146">El ámbito de un identificador de proveedor está estrictamente limitado al módulo (archivo DLL, EXE o SYS) en el que está definido: el identificador no se debe pasar a otros archivos dll.</span><span class="sxs-lookup"><span data-stu-id="e1992-146">The scope of a provider handle is strictly limited to the module (DLL, EXE, or SYS file) in which it is defined – the handle should not be passed to other DLLs.</span></span> <span data-ttu-id="e1992-147">Si se invoca una macro [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) en A.DLL mediante un identificador de proveedor definido en B.DLL, puede causar problemas.</span><span class="sxs-lookup"><span data-stu-id="e1992-147">If a [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) macro is invoked in A.DLL using a provider handle defined in B.DLL, it may cause problems.</span></span> <span data-ttu-id="e1992-148">La forma más segura y eficaz de cumplir este requisito es simplemente hacer referencia directamente al identificador global del proveedor y nunca pasar el identificador del proveedor como parámetro.</span><span class="sxs-lookup"><span data-stu-id="e1992-148">The safest and most efficient way to meet this requirement is to just always directly reference the global provider handle and never pass the provider handle as a parameter.</span></span>

### <a name="unregister-the-provider"></a><span data-ttu-id="e1992-149">Anular el registro del proveedor</span><span class="sxs-lookup"><span data-stu-id="e1992-149">Unregister the provider</span></span>

<span data-ttu-id="e1992-150">Cuando haya terminado de registrar los eventos, debe anular el registro del proveedor TraceLogging.</span><span class="sxs-lookup"><span data-stu-id="e1992-150">When you are finished logging events you must unregister the TraceLogging provider.</span></span> <span data-ttu-id="e1992-151">En el código siguiente se anula el registro del proveedor.</span><span class="sxs-lookup"><span data-stu-id="e1992-151">The following code unregisters the provider.</span></span>

```C++
    // Stop TraceLogging and unregister the provider
    TraceLoggingUnregister(g_hMyComponentProvider);
```

## <a name="compatibility"></a><span data-ttu-id="e1992-152">Compatibilidad</span><span class="sxs-lookup"><span data-stu-id="e1992-152">Compatibility</span></span>

<span data-ttu-id="e1992-153">En función de su configuración, TraceLoggingProvider. h puede ser compatible con versiones anteriores (compatible con Windows Vista o posterior), o bien se puede optimizar para versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e1992-153">Depending on its configuration, TraceLoggingProvider.h can be backwards-compatible (compatible with Windows Vista or later), or can be optimized for later OS versions.</span></span> <span data-ttu-id="e1992-154">TraceLoggingProvider. h usa WINVER (modo de usuario) y NTDDI_VERSION (modo kernel) para determinar si debe ser compatible con versiones anteriores del sistema operativo o estar optimizado para versiones más recientes del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e1992-154">TraceLoggingProvider.h uses WINVER (user mode) and NTDDI_VERSION (kernel mode) to determine whether it should be compatible with earlier OS versions or be optimized for newer OS versions.</span></span>

<span data-ttu-id="e1992-155">En el modo de usuario, si incluye <Windows. h> antes de configurar WINVER, <Windows. h> establece WINVER en la versión del sistema operativo de destino predeterminada del SDK.</span><span class="sxs-lookup"><span data-stu-id="e1992-155">For user-mode, if you include <windows.h> before setting WINVER, <windows.h> sets WINVER to the SDK's default target OS version.</span></span> <span data-ttu-id="e1992-156">Si WINVER se establece en 0x602 o superior, TraceLoggingProvider. h optimiza su comportamiento para Windows 8 (la aplicación no se ejecutará en versiones anteriores de Windows).</span><span class="sxs-lookup"><span data-stu-id="e1992-156">If WINVER is set to 0x602 or higher, TraceLoggingProvider.h optimizes its behavior for Windows 8 (your app will not run on earlier versions of Windows).</span></span> <span data-ttu-id="e1992-157">Si necesita que el programa se ejecute en vista o Windows 7, asegúrese de establecer WINVER en el valor adecuado antes de incluir <Windows. h>.</span><span class="sxs-lookup"><span data-stu-id="e1992-157">If you need your program to run on Vista or Windows 7, be sure to set WINVER to the appropriate value before including <windows.h>.</span></span>

<span data-ttu-id="e1992-158">Del mismo modo, si incluye <> WDM. h antes de establecer NTDDI_VERSION, <WDM. h> establece NTDDI_VERSION en un valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="e1992-158">Similarly, if you include <wdm.h> before setting NTDDI_VERSION, <wdm.h> sets NTDDI_VERSION to a default value.</span></span> <span data-ttu-id="e1992-159">Si NTDDI_VERSION se establece en 0x06040000 o superior, TraceLoggingProvider. h optimiza su comportamiento para Windows 10 (el controlador no funcionará en versiones anteriores de Windows).</span><span class="sxs-lookup"><span data-stu-id="e1992-159">If NTDDI_VERSION is set to 0x06040000 or higher, TraceLoggingProvider.h optimizes its behavior for Windows 10 (your driver will not work on earlier versions of Windows).</span></span>

## <a name="summary-and-next-steps"></a><span data-ttu-id="e1992-160">Resumen y pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="e1992-160">Summary and next steps</span></span>

<span data-ttu-id="e1992-161">Para ver cómo capturar y ver los datos de TraceLogging con las versiones internas más recientes de las herramientas de rendimiento de Windows (WPT), consulte [grabar y Mostrar eventos de TraceLogging](tracelogging-record-and-display-tracelogging-events.md).</span><span class="sxs-lookup"><span data-stu-id="e1992-161">To see how to capture and view TraceLogging data using the latest internal versions of the Windows Performance Tools (WPT), see [Record and Display TraceLogging Events](tracelogging-record-and-display-tracelogging-events.md).</span></span>

<span data-ttu-id="e1992-162">Vea [ejemplos de C/C++ Tracelogging](tracelogging-c-cpp-tracelogging-examples.md) para obtener más ejemplos de Tracelogging de c++.</span><span class="sxs-lookup"><span data-stu-id="e1992-162">See [C/C++ Tracelogging Examples](tracelogging-c-cpp-tracelogging-examples.md) for more C++ TraceLogging examples.</span></span>

 

 




