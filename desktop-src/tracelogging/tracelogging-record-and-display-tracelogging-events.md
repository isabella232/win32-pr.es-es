---
title: Grabar y ver eventos de TraceLogging
description: Grabe eventos de TraceLogging con la grabadora de rendimiento de Windows (WPR) y verlos con el analizador de rendimiento de Windows (WPA).
ms.assetid: 906589FA-F48D-4105-9E56-1EC8B86542FB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09be054d274fc2c2c62635cc7bf12e8cf8acdef3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904800"
---
# <a name="record-and-view-tracelogging-events"></a><span data-ttu-id="3e905-103">Grabar y ver eventos de TraceLogging</span><span class="sxs-lookup"><span data-stu-id="3e905-103">Record and View TraceLogging Events</span></span>

<span data-ttu-id="3e905-104">Grabe eventos de TraceLogging con la grabadora de rendimiento de Windows (WPR) y verlos con el analizador de rendimiento de Windows (WPA).</span><span class="sxs-lookup"><span data-stu-id="3e905-104">Record TraceLogging events with the Windows Performance Recorder (WPR) and view them with the Windows Performance Analyzer (WPA).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3e905-105">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3e905-105">Prerequisites</span></span>

-   <span data-ttu-id="3e905-106">Windows 10</span><span class="sxs-lookup"><span data-stu-id="3e905-106">Windows 10</span></span>
-   <span data-ttu-id="3e905-107">La versión de Windows 10 de la grabadora de rendimiento de Windows (WPR) y la versión de Windows 10 del analizador de rendimiento de Windows (WPA) que forma parte de Windows® Assessment and Deployment Kit (Windows ADK).</span><span class="sxs-lookup"><span data-stu-id="3e905-107">The Windows 10 version of Windows Performance Recorder (WPR), and the Windows 10 version of Windows Performance Analyzer (WPA) which is part of the Windows® Assessment and Deployment Kit (Windows ADK).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3e905-108">Los seguimientos capturados con TraceLogging deben capturarse con la versión de Windows 10 de la grabadora de rendimiento de Windows y verse con la versión de Windows 10 del analizador de rendimiento de Windows.</span><span class="sxs-lookup"><span data-stu-id="3e905-108">Traces captured with TraceLogging must be captured with the Windows 10 version of Windows Performance Recorder and viewed with the Windows 10 version of Windows Performance Analyzer.</span></span> <span data-ttu-id="3e905-109">Si no puede capturar o descodificar los eventos, compruebe que está usando la versión de Windows 10 de las herramientas.</span><span class="sxs-lookup"><span data-stu-id="3e905-109">If you are unable to capture or decode your events, verify that you are using the Windows 10 version of the tools.</span></span>

 

### <a name="1-capture-trace-data-with-wpr"></a><span data-ttu-id="3e905-110">1. capturar datos de seguimiento con WPR</span><span class="sxs-lookup"><span data-stu-id="3e905-110">1. Capture trace data with WPR</span></span>

<span data-ttu-id="3e905-111">Para capturar un seguimiento en Windows Phone, consulte capturar eventos TraceLogging en Windows Phone siguiente.</span><span class="sxs-lookup"><span data-stu-id="3e905-111">To capture a trace on Windows Phone, see Capture TraceLogging events on Windows Phone below.</span></span>

<span data-ttu-id="3e905-112">Cree un perfil de grabadora de rendimiento de Windows (. wprp) para poder usar WPR para capturar los eventos de Tracelogging.</span><span class="sxs-lookup"><span data-stu-id="3e905-112">Create a Windows Performance Recorder profile (.wprp) so that you can use WPR to capture your Tracelogging events.</span></span>

<span data-ttu-id="3e905-113">**Cree un. Archivo WPRP**</span><span class="sxs-lookup"><span data-stu-id="3e905-113">**Create a .WPRP file**</span></span>

1.  <span data-ttu-id="3e905-114">Use el siguiente ejemplo de WPRP con el ejemplo de código nativo en el [Inicio rápido de TraceLogging C/C++](tracelogging-native-quick-start.md) o el ejemplo administrado en el [Inicio rápido administrado de TraceLogging](tracelogging-managed-quick-start.md).</span><span class="sxs-lookup"><span data-stu-id="3e905-114">Use the following WPRP example with the native code example in the [TraceLogging C/C++ Quick Start](tracelogging-native-quick-start.md) or the managed example in the [TraceLogging Managed Quick Start](tracelogging-managed-quick-start.md).</span></span> <span data-ttu-id="3e905-115">Si va a registrar eventos de su propio proveedor, reemplace las `TODO` secciones por los valores adecuados para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="3e905-115">If you are logging events from your own provider, replace the `TODO` sections with the appropriate values for your provider.</span></span>

    > <span data-ttu-id="3e905-116">\[! Aún\]</span><span class="sxs-lookup"><span data-stu-id="3e905-116">\[!Important\]</span></span>  

     

    <span data-ttu-id="3e905-117">Si usa la guía de inicio rápido de C/C++ de TraceLogging, especifique el GUID del proveedor en el `Name` atributo del `<EventProvider>` elemento.</span><span class="sxs-lookup"><span data-stu-id="3e905-117">If you are using the TraceLogging C/C++ quick start, specify the provider GUID in the `Name` attribute of the `<EventProvider>` element.</span></span> <span data-ttu-id="3e905-118">Por ejemplo: `<EventProvider Id="EventProvider_SimpleTraceLoggingProvider" Name="3970F9cf-2c0c-4f11-b1cc-e3a1e9958833" />`.</span><span class="sxs-lookup"><span data-stu-id="3e905-118">For example: `<EventProvider Id="EventProvider_SimpleTraceLoggingProvider" Name="3970F9cf-2c0c-4f11-b1cc-e3a1e9958833" />`.</span></span> <span data-ttu-id="3e905-119">Si usa el inicio rápido TraceLogging administrado, especifique el nombre del proveedor precedido por ' \* ' en el `Name` atributo del `<EventProvider />` elemento.</span><span class="sxs-lookup"><span data-stu-id="3e905-119">If you are using the managed TraceLogging quick start, specify the provider name prefaced by '\*' in the `Name` attribute of the `<EventProvider />` element.</span></span> <span data-ttu-id="3e905-120">Por ejemplo, `<EventProvider Name="*SimpleTraceLoggingProvider" />`.</span><span class="sxs-lookup"><span data-stu-id="3e905-120">For example, `<EventProvider Name="*SimpleTraceLoggingProvider" />`.</span></span>

    <span data-ttu-id="3e905-121">Archivo WPRP de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="3e905-121">Sample WPRP file.</span></span>

    ```XML
    <?xml version="1.0" encoding="utf-8"?>
    <!-- TODO: 
    1. Find and replace "SimpleTraceLoggingProvider" with the name of your provider.
    2. See TODO below to update GUID for your event provider
    -->
    <WindowsPerformanceRecorder Version="1.0" Author="Microsoft Corporation" Copyright="Microsoft Corporation" Company="Microsoft Corporation">
      <Profiles>
        <EventCollector Id="EventCollector_SimpleTraceLoggingProvider" Name="SimpleTraceLoggingProvider">
          <BufferSize Value="64" />
          <Buffers Value="4" />
        </EventCollector>

        <!-- TODO: 
     1. Update Name attribute in EventProvider xml element with your provider GUID, eg: Name="3970F9cf-2c0c-4f11-b1cc-e3a1e9958833". Or
        if you specify an EventSource C# provider or call TraceLoggingRegister(...) without a GUID, use star (*) before your provider
        name, eg: Name="*MyEventSourceProvider" which will enable your provider appropriately.  
     2. This sample lists one EventProvider xml element and references it in a Profile with EventProviderId xml element. 
        For your component wprp, enable the required number of providers and fix the Profile xml element appropriately
    -->
        <EventProvider Id="EventProvider_SimpleTraceLoggingProvider" Name="*SimpleTraceLoggingProvider" />
        
        <Profile Id="SimpleTraceLoggingProvider.Verbose.File" Name="SimpleTraceLoggingProvider" Description="SimpleTraceLoggingProvider" LoggingMode="File" DetailLevel="Verbose">
          <Collectors>
            <EventCollectorId Value="EventCollector_SimpleTraceLoggingProvider">
              <EventProviders>
                <!-- TODO:
     1. Fix your EventProviderId with Value same as the Id attribute on EventProvider xml element above
    -->
                <EventProviderId Value="EventProvider_SimpleTraceLoggingProvider" />
              </EventProviders>
            </EventCollectorId>
          </Collectors>
        </Profile>

        <Profile Id="SimpleTraceLoggingProvider.Light.File" Name="SimpleTraceLoggingProvider" Description="SimpleTraceLoggingProvider" Base="SimpleTraceLoggingProvider.Verbose.File" LoggingMode="File" DetailLevel="Light" />
        <Profile Id="SimpleTraceLoggingProvider.Verbose.Memory" Name="SimpleTraceLoggingProvider" Description="SimpleTraceLoggingProvider" Base="SimpleTraceLoggingProvider.Verbose.File" LoggingMode="Memory" DetailLevel="Verbose" />
        <Profile Id="SimpleTraceLoggingProvider.Light.Memory" Name="SimpleTraceLoggingProvider" Description="SimpleTraceLoggingProvider" Base="SimpleTraceLoggingProvider.Verbose.File" LoggingMode="Memory" DetailLevel="Light" />

      </Profiles>
    </WindowsPerformanceRecorder>
    
    ```

    

2.  <span data-ttu-id="3e905-122">Guarde el archivo con un. Extensión de nombre de archivo WPRP.</span><span class="sxs-lookup"><span data-stu-id="3e905-122">Save the file with a .WPRP file name extension.</span></span>
3.  <span data-ttu-id="3e905-123">Inicie la captura mediante la ventana del símbolo del sistema con permisos elevados (ejecutar como administrador).</span><span class="sxs-lookup"><span data-stu-id="3e905-123">Start the capture using WPR from an elevated (run as Administrator) Command Prompt window.</span></span>

    <span data-ttu-id="3e905-124">**<path to wpr>\\wpr.exe-Start GeneralProfile-Start TraceLoggingProvider. wprp**</span><span class="sxs-lookup"><span data-stu-id="3e905-124">**<path to wpr>\\wpr.exe -start GeneralProfile -start TraceLoggingProvider.wprp**</span></span>

    > <span data-ttu-id="3e905-125">\[! Tip\]</span><span class="sxs-lookup"><span data-stu-id="3e905-125">\[!Tip\]</span></span>  
    > <span data-ttu-id="3e905-126">En lo que respecta a la generación de perfiles general, también puede agregar **– Start GeneralProfile** a la línea de comandos wpr.exe para capturar eventos del sistema junto con los eventos del proveedor.</span><span class="sxs-lookup"><span data-stu-id="3e905-126">For general profiling purposes, you can also add **–start GeneralProfile** to the wpr.exe command line to capture system events along with the events from your provider.</span></span> <span data-ttu-id="3e905-127">Si solo desea recopilar los eventos, omita **-Start GeneralProfile**.</span><span class="sxs-lookup"><span data-stu-id="3e905-127">If you only want to gather your events, omit **-start GeneralProfile**.</span></span>

     

4.  <span data-ttu-id="3e905-128">Ejecute la aplicación que contiene los eventos.</span><span class="sxs-lookup"><span data-stu-id="3e905-128">Run the application that contains your events.</span></span>
5.  <span data-ttu-id="3e905-129">Detenga la captura de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="3e905-129">Stop the trace capture.</span></span>

    <span data-ttu-id="3e905-130">**<path to wpr>\\wpr.exe-STOP TraceCaptureFile. ETL Description**</span><span class="sxs-lookup"><span data-stu-id="3e905-130">**<path to wpr>\\wpr.exe -stop TraceCaptureFile.etl description**</span></span>

    > <span data-ttu-id="3e905-131">\[! Tip\]</span><span class="sxs-lookup"><span data-stu-id="3e905-131">\[!Tip\]</span></span>  
    > <span data-ttu-id="3e905-132">Si agregó **– Start GeneralProfile** para recopilar eventos del sistema, agregue **-Stop GeneralProfile** a la **wpr.exe** línea de comandos anterior.</span><span class="sxs-lookup"><span data-stu-id="3e905-132">If you added **–start GeneralProfile** to gather system events, add **-stop GeneralProfile** to the **wpr.exe** command line above.</span></span>

     

### <a name="2-capture-tracelogging-events-on-windows-phone"></a><span data-ttu-id="3e905-133">2. capturar eventos TraceLogging en Windows Phone</span><span class="sxs-lookup"><span data-stu-id="3e905-133">2. Capture TraceLogging events on Windows Phone</span></span>

<span id="capturephone"></span><span id="CAPTUREPHONE"></span>

1.  <span data-ttu-id="3e905-134">Inicie tracelog para capturar eventos del proveedor.</span><span class="sxs-lookup"><span data-stu-id="3e905-134">Start tracelog to capture events from your provider.</span></span>

    <span data-ttu-id="3e905-135">**cmdd tracelog-Start test-f c: \\ Test. ETL-GUID \# providerguid**</span><span class="sxs-lookup"><span data-stu-id="3e905-135">**cmdd tracelog -start test -f c:\\test.etl -guid \#providerguid**</span></span>

2.  <span data-ttu-id="3e905-136">Ejecute el escenario de prueba para registrar eventos.</span><span class="sxs-lookup"><span data-stu-id="3e905-136">Run your test scenario to log events.</span></span>
3.  <span data-ttu-id="3e905-137">Detener captura de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="3e905-137">Stop trace capture.</span></span>

    <span data-ttu-id="3e905-138">**cmdd tracelog-detener prueba**</span><span class="sxs-lookup"><span data-stu-id="3e905-138">**cmdd tracelog -stop test**</span></span>

4.  <span data-ttu-id="3e905-139">Combinar los resultados del seguimiento del sistema con los resultados del seguimiento.</span><span class="sxs-lookup"><span data-stu-id="3e905-139">Merge the system trace results with your trace results.</span></span>

    <span data-ttu-id="3e905-140">**cmdd xperf-Merge c: \\ Test. ETL c: \\ testmerged. ETL**</span><span class="sxs-lookup"><span data-stu-id="3e905-140">**cmdd xperf -merge c:\\test.etl c:\\testmerged.etl**</span></span>

5.  <span data-ttu-id="3e905-141">Recupere el archivo de registro combinado.</span><span class="sxs-lookup"><span data-stu-id="3e905-141">Retrieve the merged log file.</span></span>

    <span data-ttu-id="3e905-142">**GetD c: \\ testmerged. ETL**</span><span class="sxs-lookup"><span data-stu-id="3e905-142">**getd c:\\testmerged.etl**</span></span>

### <a name="3-view-tracelogging-data-using-windows-performance-analyzer"></a><span data-ttu-id="3e905-143">3. ver los datos de TraceLogging con el analizador de rendimiento de Windows.</span><span class="sxs-lookup"><span data-stu-id="3e905-143">3. View TraceLogging data using Windows Performance Analyzer.</span></span>

<span data-ttu-id="3e905-144">WPA es actualmente el único visor que se puede usar para ver los archivos de seguimiento de TraceLogging (. ETL).</span><span class="sxs-lookup"><span data-stu-id="3e905-144">WPA is currently the only viewer you can use to view TraceLogging trace (.etl) files.</span></span>

1.  <span data-ttu-id="3e905-145">Inicie WPA.</span><span class="sxs-lookup"><span data-stu-id="3e905-145">Start WPA.</span></span>

    <span data-ttu-id="3e905-146">**<path to wpr>\\wpa.exe traceLoggingResults. ETL**</span><span class="sxs-lookup"><span data-stu-id="3e905-146">**<path to wpr>\\wpa.exe traceLoggingResults.etl**</span></span>

2.  <span data-ttu-id="3e905-147">Cargue el archivo de seguimiento (. ETL) que especificó en el comando wpa.exe anterior, por ejemplo, traceLoggingResults. ETL.</span><span class="sxs-lookup"><span data-stu-id="3e905-147">Load the trace (.etl) file that you specified in the wpa.exe command above, e.g. traceLoggingResults.etl.</span></span>
3.  <span data-ttu-id="3e905-148">Vea los eventos del proveedor.</span><span class="sxs-lookup"><span data-stu-id="3e905-148">View your provider events.</span></span> <span data-ttu-id="3e905-149">En el explorador de gráficos de WPA, expanda **actividad del sistema**.</span><span class="sxs-lookup"><span data-stu-id="3e905-149">In the WPA Graph Explorer, expand **System Activity**.</span></span>
4.  <span data-ttu-id="3e905-150">Haga doble clic en el panel **eventos genéricos** para ver los eventos en el panel **análisis** .</span><span class="sxs-lookup"><span data-stu-id="3e905-150">Double-click in the **Generic Events** pane to view the events in the **Analysis** pane.</span></span>

    ![expandir eventos genéricos](images/expandsystemactivity.png)

5.  <span data-ttu-id="3e905-152">En el panel análisis, busque los eventos de su proveedor para comprobar que TraceLogging funciona.</span><span class="sxs-lookup"><span data-stu-id="3e905-152">In the Analysis pane, locate the events from your provider to verify that TraceLogging is working.</span></span>

    <span data-ttu-id="3e905-153">En la columna **nombre del proveedor** de la tabla **eventos genéricos** , busque y seleccione la fila con el nombre del proveedor.</span><span class="sxs-lookup"><span data-stu-id="3e905-153">In the **Provider Name** column of the **Generic Events** table, find and select the row with your provider name.</span></span>

    <span data-ttu-id="3e905-154">Si tiene varios proveedores para ordenar, haga clic en el encabezado de columna para ordenar por nombre de columna, lo que puede facilitar la búsqueda de su proveedor.</span><span class="sxs-lookup"><span data-stu-id="3e905-154">If you have multiple providers to sort through, click the column header to sort by column name which may make it easier to find your provider.</span></span>

    <span data-ttu-id="3e905-155">Cuando encuentre el proveedor, haga clic con el botón derecho en el nombre y seleccione **filtro para** seleccionar.</span><span class="sxs-lookup"><span data-stu-id="3e905-155">When you find your provider, right click on the name and select **Filter to Selection**.</span></span>

    ![filtrar la selección al proveedor](images/filtertoselection.png)

    <span data-ttu-id="3e905-157">El evento para SimpleTraceLoggingProvider y su valor aparecerán en el panel inferior de la ventana de análisis.</span><span class="sxs-lookup"><span data-stu-id="3e905-157">The event for the SimpleTraceLoggingProvider and its value will appear in the bottom pane of the Analysis window.</span></span> <span data-ttu-id="3e905-158">Expanda el nombre del proveedor para ver los eventos.</span><span class="sxs-lookup"><span data-stu-id="3e905-158">Expand the provider name to see the events.</span></span>

    ![ver el evento desde simpletraceloggingprovider](images/eventview.png)

    <span data-ttu-id="3e905-160">Para obtener más información acerca del uso de WPA, consulte [analizador de rendimiento de Windows](/previous-versions/windows/it-pro/windows-8.1-and-8/hh448170(v=win.10)).</span><span class="sxs-lookup"><span data-stu-id="3e905-160">For more information about using WPA, see [Windows Performance Analyzer](/previous-versions/windows/it-pro/windows-8.1-and-8/hh448170(v=win.10)).</span></span>

## <a name="summary-and-next-steps"></a><span data-ttu-id="3e905-161">Resumen y pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="3e905-161">Summary and next steps</span></span>

<span data-ttu-id="3e905-162">El proceso de grabación y visualización de eventos ETW mediante WPR y WPA se aplica igualmente a los eventos TraceLogging.</span><span class="sxs-lookup"><span data-stu-id="3e905-162">The process for recording and viewing ETW events using WPR and WPA apply equally well to TraceLogging events.</span></span>

<span data-ttu-id="3e905-163">Vea [ejemplos de C/C++ Tracelogging](tracelogging-c-cpp-tracelogging-examples.md) para obtener ejemplos adicionales de Tracelogging.</span><span class="sxs-lookup"><span data-stu-id="3e905-163">See [C/C++ Tracelogging Examples](tracelogging-c-cpp-tracelogging-examples.md) for additional TraceLogging examples.</span></span>

 

 