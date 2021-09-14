---
description: Esta aplicación de ejemplo muestra cómo abrir y cerrar secuencias de comunicación y provocar eventos de afijo que una aplicación puede obtener para implementar la atenuación de secuencias.
ms.assetid: 9a2131b2-ec4a-492a-a277-bd26ec8d67e5
title: DuckingCaptureSample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 636fe39e8fa27beee14ab17548f5929d1d937b20
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165018"
---
# <a name="duckingcapturesample"></a>DuckingCaptureSample

Esta aplicación de ejemplo muestra cómo abrir y cerrar secuencias de comunicación y provocar eventos de afijo que una aplicación puede obtener para implementar la atenuación de secuencias. Esta aplicación implementa un cliente de chat que usa Core Audio API para leer datos de audio de un dispositivo de comunicación y reproducirlo en el dispositivo de salida.

En este tema se incluyen las siguientes secciones.

-   [Descripción](#description)
-   [Requisitos](#requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Compilar el ejemplo](#building-the-sample)
-   [Ejecución del ejemplo](#running-the-sample)
-   [Temas relacionados](#related-topics)

## <a name="description"></a>Descripción

En este ejemplo se muestran las siguientes características.

-   [MMDevice API para](mmdevice-api.md) la enumeración y selección de dispositivos multimedia.
-   [WASAPI para](wasapi.md) acceder a la captura de comunicaciones y representar el dispositivo, las operaciones de administración de flujos y el control de eventos de afijo.
-   [API wave para acceder](/previous-versions//ms713499(v=vs.85)) al dispositivo de comunicaciones y capturar entradas de audio.

## <a name="requirements"></a>Requisitos



| Producto                                                        | Versión   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio 2008                                             |           |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en las siguientes ubicaciones.



| Location    | Ruta de acceso o dirección URL                                                                                              |
|-------------|-------------------------------------------------------------------------------------------------------|
| Windows SDK | \\Archivos de \\ programa Sdk de Microsoft Windows ejemplos de audio multimedia \\ \\ v7.0CaptureSample... \\ \\ \\ \\ \\ |



 

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo DesanchamientoCaptureSample, siga estos pasos:

1.  Abra el archivo DuckingCaptureSample.sln en Visual Studio 2008.
2.  En la ventana, seleccione  la **configuración** de  la solución Depurar o Liberar, seleccione el menú Compilar en la barra de menús y seleccione la **opción Compilar.** Si no abre Visual Studio shell de CMD para el SDK, Visual Studio tendrá acceso al entorno de compilación del SDK. En ese caso, el ejemplo no se compilará a menos que establezca explícitamente la variable de entorno MSSdk, que se usa en el archivo de proyecto, DuckingCaptureSample.vcproj.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

Si compila la aplicación correctamente, se genera un archivo ejecutable, DuckingCaptureSample.exe, . Para ejecutarlo, seleccione **Iniciar depuración** **o** Iniciar sin depurar en el menú **Depurar** o escriba en una ventana de `DuckingCaptureSample` comandos.

La clase DuckingCaptureSample proporciona al usuario dos implementaciones para capturar audio desde el dispositivo de consola predeterminado: WASAPI y Wave API. Para iniciar una sesión de captura, seleccione un modo y haga clic **en Iniciar en** la interfaz de usuario de la aplicación. Para finalizar la sesión, haga clic en **Detener**. En función del dispositivo especificado por el usuario (entrada o salida), la aplicación usa MMDevice API para obtener una referencia al dispositivo de comunicación de representación o captura predeterminado. Una vez que el usuario inicia una sesión de chat, la aplicación realiza las siguientes tareas:

-   Crea e inicializa un cliente de audio en modo controlado por eventos.
-   Asocia el cliente al identificador de eventos que indica que las muestras están listas para la captura o representación.
-   Configura un cliente de captura y un cliente de representación para el transporte.
-   Crea el subproceso de chat e inicia el motor de audio.

Para capturar datos de audio, con cada paso de procesamiento, el ejemplo usa el cliente de captura para obtener la cantidad total de datos capturados que están disponibles en el búfer, leer datos del dispositivo de entrada predeterminado y liberar el paquete y hacer que el búfer esté disponible para leer el siguiente conjunto de datos capturados.

Para la representación, la aplicación determina la cantidad de datos que se ponen en cola para reproducirse en el búfer del punto de conexión de captura. En consecuencia, escribe en el búfer y libera el búfer como preparación para el siguiente paso de procesamiento hasta que se han escrito todos los datos. Para la representación, los fotogramas silenciosos se inscriben previamente para evitar que el motor de audio se desajuste al iniciarse. HideingCaptureSample también muestra cómo ocultar la secuencia de representación del mezclador de volúmenes.

Para obtener más información sobre la característica de atenuación de secuencias, consulte [Uso de un dispositivo de comunicación.](using-the-communication-device.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos del SDK que usan las API de audio principales](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 
