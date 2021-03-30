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
# <a name="record-and-view-tracelogging-events"></a>Grabar y ver eventos de TraceLogging

Grabe eventos de TraceLogging con la grabadora de rendimiento de Windows (WPR) y verlos con el analizador de rendimiento de Windows (WPA).

## <a name="prerequisites"></a>Requisitos previos

-   Windows 10
-   La versión de Windows 10 de la grabadora de rendimiento de Windows (WPR) y la versión de Windows 10 del analizador de rendimiento de Windows (WPA) que forma parte de Windows® Assessment and Deployment Kit (Windows ADK).

> [!IMPORTANT]
> Los seguimientos capturados con TraceLogging deben capturarse con la versión de Windows 10 de la grabadora de rendimiento de Windows y verse con la versión de Windows 10 del analizador de rendimiento de Windows. Si no puede capturar o descodificar los eventos, compruebe que está usando la versión de Windows 10 de las herramientas.

 

### <a name="1-capture-trace-data-with-wpr"></a>1. capturar datos de seguimiento con WPR

Para capturar un seguimiento en Windows Phone, consulte capturar eventos TraceLogging en Windows Phone siguiente.

Cree un perfil de grabadora de rendimiento de Windows (. wprp) para poder usar WPR para capturar los eventos de Tracelogging.

**Cree un. Archivo WPRP**

1.  Use el siguiente ejemplo de WPRP con el ejemplo de código nativo en el [Inicio rápido de TraceLogging C/C++](tracelogging-native-quick-start.md) o el ejemplo administrado en el [Inicio rápido administrado de TraceLogging](tracelogging-managed-quick-start.md). Si va a registrar eventos de su propio proveedor, reemplace las `TODO` secciones por los valores adecuados para el proveedor.

    > \[! Aún\]  

     

    Si usa la guía de inicio rápido de C/C++ de TraceLogging, especifique el GUID del proveedor en el `Name` atributo del `<EventProvider>` elemento. Por ejemplo: `<EventProvider Id="EventProvider_SimpleTraceLoggingProvider" Name="3970F9cf-2c0c-4f11-b1cc-e3a1e9958833" />`. Si usa el inicio rápido TraceLogging administrado, especifique el nombre del proveedor precedido por ' \* ' en el `Name` atributo del `<EventProvider />` elemento. Por ejemplo, `<EventProvider Name="*SimpleTraceLoggingProvider" />`.

    Archivo WPRP de ejemplo.

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

    

2.  Guarde el archivo con un. Extensión de nombre de archivo WPRP.
3.  Inicie la captura mediante la ventana del símbolo del sistema con permisos elevados (ejecutar como administrador).

    **<path to wpr>\\wpr.exe-Start GeneralProfile-Start TraceLoggingProvider. wprp**

    > \[! Tip\]  
    > En lo que respecta a la generación de perfiles general, también puede agregar **– Start GeneralProfile** a la línea de comandos wpr.exe para capturar eventos del sistema junto con los eventos del proveedor. Si solo desea recopilar los eventos, omita **-Start GeneralProfile**.

     

4.  Ejecute la aplicación que contiene los eventos.
5.  Detenga la captura de seguimiento.

    **<path to wpr>\\wpr.exe-STOP TraceCaptureFile. ETL Description**

    > \[! Tip\]  
    > Si agregó **– Start GeneralProfile** para recopilar eventos del sistema, agregue **-Stop GeneralProfile** a la **wpr.exe** línea de comandos anterior.

     

### <a name="2-capture-tracelogging-events-on-windows-phone"></a>2. capturar eventos TraceLogging en Windows Phone

<span id="capturephone"></span><span id="CAPTUREPHONE"></span>

1.  Inicie tracelog para capturar eventos del proveedor.

    **cmdd tracelog-Start test-f c: \\ Test. ETL-GUID \# providerguid**

2.  Ejecute el escenario de prueba para registrar eventos.
3.  Detener captura de seguimiento.

    **cmdd tracelog-detener prueba**

4.  Combinar los resultados del seguimiento del sistema con los resultados del seguimiento.

    **cmdd xperf-Merge c: \\ Test. ETL c: \\ testmerged. ETL**

5.  Recupere el archivo de registro combinado.

    **GetD c: \\ testmerged. ETL**

### <a name="3-view-tracelogging-data-using-windows-performance-analyzer"></a>3. ver los datos de TraceLogging con el analizador de rendimiento de Windows.

WPA es actualmente el único visor que se puede usar para ver los archivos de seguimiento de TraceLogging (. ETL).

1.  Inicie WPA.

    **<path to wpr>\\wpa.exe traceLoggingResults. ETL**

2.  Cargue el archivo de seguimiento (. ETL) que especificó en el comando wpa.exe anterior, por ejemplo, traceLoggingResults. ETL.
3.  Vea los eventos del proveedor. En el explorador de gráficos de WPA, expanda **actividad del sistema**.
4.  Haga doble clic en el panel **eventos genéricos** para ver los eventos en el panel **análisis** .

    ![expandir eventos genéricos](images/expandsystemactivity.png)

5.  En el panel análisis, busque los eventos de su proveedor para comprobar que TraceLogging funciona.

    En la columna **nombre del proveedor** de la tabla **eventos genéricos** , busque y seleccione la fila con el nombre del proveedor.

    Si tiene varios proveedores para ordenar, haga clic en el encabezado de columna para ordenar por nombre de columna, lo que puede facilitar la búsqueda de su proveedor.

    Cuando encuentre el proveedor, haga clic con el botón derecho en el nombre y seleccione **filtro para** seleccionar.

    ![filtrar la selección al proveedor](images/filtertoselection.png)

    El evento para SimpleTraceLoggingProvider y su valor aparecerán en el panel inferior de la ventana de análisis. Expanda el nombre del proveedor para ver los eventos.

    ![ver el evento desde simpletraceloggingprovider](images/eventview.png)

    Para obtener más información acerca del uso de WPA, consulte [analizador de rendimiento de Windows](/previous-versions/windows/it-pro/windows-8.1-and-8/hh448170(v=win.10)).

## <a name="summary-and-next-steps"></a>Resumen y pasos siguientes

El proceso de grabación y visualización de eventos ETW mediante WPR y WPA se aplica igualmente a los eventos TraceLogging.

Vea [ejemplos de C/C++ Tracelogging](tracelogging-c-cpp-tracelogging-examples.md) para obtener ejemplos adicionales de Tracelogging.

 

 