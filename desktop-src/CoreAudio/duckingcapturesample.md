---
description: En esta aplicación de ejemplo se muestra la apertura y el cierre de secuencias de comunicación y la causa de los eventos que una aplicación puede obtener para implementar la atenuación de la secuencia.
ms.assetid: 9a2131b2-ec4a-492a-a277-bd26ec8d67e5
title: DuckingCaptureSample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 636fe39e8fa27beee14ab17548f5929d1d937b20
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907511"
---
# <a name="duckingcapturesample"></a>DuckingCaptureSample

En esta aplicación de ejemplo se muestra la apertura y el cierre de secuencias de comunicación y la causa de los eventos que una aplicación puede obtener para implementar la atenuación de la secuencia. Esta aplicación implementa un cliente de chat que usa las API de audio principales para leer los datos de audio de un dispositivo de comunicación y reproducirlos en el dispositivo de salida.

En este tema se incluyen las siguientes secciones.

-   [Descripción](#description)
-   [Requisitos](#requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Compilar el ejemplo](#building-the-sample)
-   [Ejecutar el ejemplo](#running-the-sample)
-   [Temas relacionados](#related-topics)

## <a name="description"></a>Descripción

En este ejemplo se muestran las características siguientes.

-   [MMDEVICE API](mmdevice-api.md) para la enumeración y selección de dispositivos multimedia.
-   [WASAPI](wasapi.md) para acceder al dispositivo de captura y representación de comunicaciones, las operaciones de administración de secuencias y el control de eventos de pato.
-   [API de Wave](/previous-versions//ms713499(v=vs.85)) para acceder al dispositivo de comunicaciones y capturar entradas de audio.

## <a name="requirements"></a>Requisitos



| Producto                                                        | Versión   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio 2008                                             |           |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en las siguientes ubicaciones.



| Location    | Ruta de acceso/URL                                                                                              |
|-------------|-------------------------------------------------------------------------------------------------------|
| Windows SDK | \\Archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ multimedia \\ audio \\ DuckingCaptureSample \\ ... |



 

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo DuckingCaptureSample, siga estos pasos:

1.  Abra DuckingCaptureSample. sln en Visual Studio 2008.
2.  En la ventana, seleccione la configuración de la solución de **depuración** o **versión** , seleccione el menú **compilar** en la barra de menús y seleccione la opción **compilar** . Si no abre Visual Studio desde el shell de CMD para el SDK, Visual Studio no tendrá acceso al entorno de compilación del SDK. En ese caso, el ejemplo no se compilará a menos que establezca explícitamente la variable de entorno MSSdk, que se usa en el archivo de proyecto, DuckingCaptureSample. vcproj.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

Si compila la aplicación correctamente, se genera un archivo ejecutable DuckingCaptureSample.exe. Para ejecutarlo, seleccione **iniciar depuración** o **iniciar sin depurar** en el menú **depurar** o escriba `DuckingCaptureSample` en una ventana de comandos.

DuckingCaptureSample proporciona al usuario dos implementaciones para capturar audio desde el dispositivo de consola predeterminado: WASAPI y Wave API. Para iniciar una sesión de captura, seleccione un modo y haga clic en **iniciar** en la interfaz de usuario de la aplicación. Para finalizar la sesión, haga clic en **detener**. Según el dispositivo especificado por el usuario (entrada o salida), la aplicación usa la API de MMDevice para obtener una referencia al dispositivo de comunicación de representación o captura predeterminado. Una vez que el usuario inicia una sesión de chat, la aplicación realiza las siguientes tareas:

-   Crea e inicializa un cliente de audio en modo basado en eventos.
-   Asocia el cliente con el identificador de evento que indica que los ejemplos están listos para su captura o representación.
-   Configura un cliente de captura y un cliente de representación para el transporte.
-   Crea el subproceso de chat e inicia el motor de audio.

Para capturar datos de audio, con cada paso de procesamiento, el ejemplo usa el cliente de captura para obtener la cantidad total de datos capturados que están disponibles en el búfer, leer datos del dispositivo de entrada predeterminado y liberar el paquete y hacer que el búfer esté disponible para leer el siguiente conjunto de datos capturados.

Para la representación, la aplicación determina la cantidad de datos que se ponen en cola para reproducirlos en el búfer del extremo de captura. En consecuencia, escribe en el búfer y libera el búfer como preparación para la siguiente fase de procesamiento hasta que se han escrito todos los datos. Para la representación, los marcos silenciosos se preparan para evitar que el motor de audio se ponga en proceso en el inicio. DuckingCaptureSample también muestra cómo ocultar el flujo de representación del mezclador de volumen.

Para obtener más información acerca de la característica de atenuación de flujos, consulte [uso de un dispositivo de comunicación](using-the-communication-device.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de SDK que usan las API de audio principales](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 
