---
title: Registrar y ver eventos de seguimiento
description: Registre los eventos tracelogging con Windows Performance Recorder (WPR) y véalos con Windows Analizador de rendimiento (WPA).
ms.assetid: 906589FA-F48D-4105-9E56-1EC8B86542FB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25c77c1a1759988252f57c1ec54dca77cffaa21832878ead6ba8a827df3329fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966549"
---
# <a name="record-and-view-tracelogging-events"></a>Registrar y ver eventos de seguimiento

Registre los eventos tracelogging con Windows Performance Recorder (WPR) y véalos con Windows Analizador de rendimiento (WPA).

## <a name="prerequisites"></a>Requisitos previos

-   Windows 10
-   La versión Windows 10 de Windows Performance Recorder (WPR) y la versión Windows 10 de Windows Analizador de rendimiento (WPA) que forma parte del kit de evaluación e implementación de Windows® (Windows ADK).

> [!IMPORTANT]
> Los seguimientos capturados con TraceLogging deben capturarse con la versión Windows 10 de Windows Performance Recorder y visualizarse con la versión Windows 10 de Windows Analizador de rendimiento. Si no puede capturar o descodificar los eventos, compruebe que está usando la Windows 10 de las herramientas.

 

### <a name="1-capture-trace-data-with-wpr"></a>1. Captura de datos de seguimiento con WPR

Para capturar un seguimiento en Windows Phone, vea Capturar eventos tracelogging en Windows Phone a continuación.

Cree un Windows de grabadora de rendimiento (.wprp) para que pueda usar WPR para capturar los eventos de seguimiento.

**Cree un . Archivo WPRP**

1.  Use el siguiente ejemplo de WPRP con el ejemplo de código nativo en el Inicio rápido [C/C++](tracelogging-native-quick-start.md) de TraceLogging o el ejemplo administrado en la instancia administrada de [TraceLogging Inicio rápido](tracelogging-managed-quick-start.md). Si va a registrar eventos de su propio proveedor, reemplace las secciones `TODO` por los valores adecuados para el proveedor.

    > \[! Importante\]  

     

    Si usa el inicio rápido tracelogging de C/C++, especifique el GUID del proveedor en `Name` el atributo del elemento `<EventProvider>` . Por ejemplo: `<EventProvider Id="EventProvider_SimpleTraceLoggingProvider" Name="3970F9cf-2c0c-4f11-b1cc-e3a1e9958833" />`. Si usa el inicio rápido tracelogging administrado, especifique el nombre del proveedor precedido por ' ' en el \* `Name` atributo del elemento `<EventProvider />` . Por ejemplo, `<EventProvider Name="*SimpleTraceLoggingProvider" />`.

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

    

2.  Guarde el archivo con un . Extensión de nombre de archivo WPRP.
3.  Inicie la captura mediante WPR desde una ventana del símbolo del sistema con privilegios elevados (ejecutar como administrador).

    **<path to wpr>\\wpr.exe -start GeneralProfile -start TraceLoggingProvider.wprp**

    > \[! Propina\]  
    > Para fines generales de generación de perfiles, también puede agregar **–start GeneralProfile** a la línea de comandos de wpr.exe para capturar eventos del sistema junto con los eventos del proveedor. Si solo desea recopilar los eventos, omita **-start GeneralProfile**.

     

4.  Ejecute la aplicación que contiene los eventos.
5.  Detenga la captura de seguimiento.

    **<path to wpr>\\wpr.exe -stop TraceCaptureFile.etl description**

    > \[! Propina\]  
    > Si ha agregado **–start GeneralProfile para** recopilar eventos del sistema, agregue **-stop GeneralProfile** a lawpr.exe **línea** de comandos anterior.

     

### <a name="2-capture-tracelogging-events-on-windows-phone"></a>2. Capturar eventos tracelogging en Windows Phone

<span id="capturephone"></span><span id="CAPTUREPHONE"></span>

1.  Inicie tracelog para capturar eventos del proveedor.

    **cmdd tracelog -start test -f c: \\ test.etl \# -guid providerguid**

2.  Ejecute el escenario de prueba para registrar eventos.
3.  Detenga la captura de seguimiento.

    **cmdd tracelog -stop test**

4.  Combine los resultados de seguimiento del sistema con los resultados de seguimiento.

    **cmdd xperf -merge c: \\ test.etl c: \\ testmerged.etl**

5.  Recupere el archivo de registro combinado.

    **getd c: \\ testmerged.etl**

### <a name="3-view-tracelogging-data-using-windows-performance-analyzer"></a>3. Vea los datos de TraceLogging mediante Windows Analizador de rendimiento.

WPA es actualmente el único visor que puede usar para ver los archivos de seguimiento de seguimiento (.etl).

1.  Inicie WPA.

    **<path to wpr>\\wpa.exe traceLoggingResults.etl**

2.  Cargue el archivo de seguimiento (.etl) que especificó en el wpa.exe anterior, por ejemplo, traceLoggingResults.etl.
3.  Ver los eventos del proveedor. En el Explorador de Graph WPA, expanda **Actividad del sistema**.
4.  Haga doble clic en el **panel Eventos** genéricos para ver los eventos en el **panel** Análisis.

    ![expandir eventos genéricos](images/expandsystemactivity.png)

5.  En el panel Análisis, busque los eventos del proveedor para comprobar que TraceLogging funciona.

    En la **columna Nombre del proveedor** de la tabla **Eventos** genéricos, busque y seleccione la fila con el nombre del proveedor.

    Si tiene varios proveedores para ordenar, haga clic en el encabezado de columna para ordenar por nombre de columna, lo que puede facilitar la búsqueda del proveedor.

    Cuando encuentre el proveedor, haga clic con el botón derecho en el nombre y seleccione **Filtrar por Selección.**

    ![selección de filtro al proveedor](images/filtertoselection.png)

    El evento de SimpleTraceLoggingProvider y su valor aparecerá en el panel inferior de la ventana Análisis. Expanda el nombre del proveedor para ver los eventos.

    ![ver el evento desde simpletraceloggingprovider](images/eventview.png)

    Para obtener más información sobre el uso de WPA, [vea Windows Analizador de rendimiento](/previous-versions/windows/it-pro/windows-8.1-and-8/hh448170(v=win.10)).

## <a name="summary-and-next-steps"></a>Resumen y pasos siguientes

El proceso de grabación y visualización de eventos ETW mediante WPR y WPA se aplica igualmente bien a los eventos tracelogging.

Vea [Ejemplos de seguimiento de C/C++ para](tracelogging-c-cpp-tracelogging-examples.md) obtener ejemplos de seguimiento adicionales.

 

 