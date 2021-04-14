---
description: Esta aplicación de ejemplo utiliza las API de audio principales para representar datos de audio en un dispositivo de salida especificado por el usuario. Este ejemplo muestra el almacenamiento en búfer basado en temporizador para un cliente de representación en modo exclusivo.
ms.assetid: 9dcfccd2-a709-4b4e-bbb3-4c68a15cce03
title: RenderExclusiveTimerDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb6145f65de3de9425f7ba2f023a669ec0b57a3c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496366"
---
# <a name="renderexclusivetimerdriven"></a>RenderExclusiveTimerDriven

Esta aplicación de ejemplo utiliza las API de audio principales para representar datos de audio en un dispositivo de salida especificado por el usuario. Este ejemplo muestra el almacenamiento en búfer basado en temporizador para un cliente de representación en modo exclusivo. En el caso de una secuencia en modo exclusivo, el cliente comparte el búfer del extremo con el dispositivo de audio.

En este tema se incluyen las siguientes secciones.

-   [Descripción](#description)
-   [Requisitos](#requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Compilar el ejemplo](#building-the-sample)
-   [Ver los archivos de ejemplo](#view-the-sample-files)
-   [Temas relacionados](#related-topics)

## <a name="description"></a>Descripción

En este ejemplo se muestran las características siguientes.

-   [MMDEVICE API](mmdevice-api.md) para la enumeración y selección de dispositivos multimedia.
-   WASAPI para las operaciones de administración de secuencias.

## <a name="requirements"></a>Requisitos



| Producto                                                        | Versión   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en las siguientes ubicaciones.



| Location    | Ruta de acceso/URL                                                                                                    |
|-------------|-------------------------------------------------------------------------------------------------------------|
| Windows SDK | \\Archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ multimedia \\ audio \\ RenderExclusiveTimerDriven \\ ... |



 

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo RenderExclusiveTimerDriven, siga estos pasos:

1.  Abra el shell de CMD para el Windows SDK y cambie al directorio de ejemplo RenderExclusiveTimerDriven.
2.  Ejecute el comando `start WASAPIRenderExclusiveTimerDriven.sln` en el directorio RenderExclusiveTimerDriven para abrir el proyecto WASAPIRenderExclusiveTimerDriven en la ventana de Visual Studio.
3.  En la ventana, seleccione la configuración de la solución de **depuración** o **versión** , seleccione el menú **compilar** en la barra de menús y seleccione la opción **compilar** . Si no abre Visual Studio desde el shell de CMD para el SDK, Visual Studio no tendrá acceso al entorno de compilación del SDK. En ese caso, el ejemplo no se compilará a menos que establezca explícitamente la variable de entorno MSSdk, que se usa en el archivo de proyecto, WASAPIRenderExclusiveTimerDriven. vcproj.

## <a name="view-the-sample-files"></a>Ver los archivos de ejemplo

Si compila la aplicación de demostración correctamente, se genera un archivo ejecutable WASAPIRenderExclusiveTimerDriven.exe. Para ejecutarlo, escriba `WASAPIRenderExclusiveTimerDriven` en una ventana de comandos seguida de los argumentos obligatorios u opcionales. En el ejemplo siguiente se muestra cómo ejecutar el ejemplo mediante un que especifica la duración de la reproducción en el dispositivo de consola predeterminado.

`WASAPIRenderExclusiveTimerDriven.exe -d 20 -console`

En la tabla siguiente se muestran los argumentos.

| Argumento        | Descripción                                                |
|-----------------|------------------------------------------------------------|
| -?              | Muestra la ayuda.                                                |
| -H              | Muestra la ayuda.                                                |
| -f              | Frecuencia de onda sinusoidal en Hz.                                 |
| -l              | Latencia de representación de audio en milisegundos.                      |
| -d              | Duración de onda sinusoidal en segundos.                             |
| -M              | Deshabilita el uso de MMCSS.                                 |
| -consola        | Use el dispositivo de consola predeterminado.                            |
| -comunicaciones | Use el dispositivo de comunicación predeterminado.                      |
| -multimedia     | Use el dispositivo multimedia predeterminado.                         |
| -punto de conexión       | Use el identificador de extremo especificado en el valor del modificador. |



 

Si la aplicación se ejecuta sin argumentos, enumera los dispositivos disponibles y solicita al usuario que seleccione un dispositivo para la sesión de representación. Una vez que el usuario especifica un dispositivo, la aplicación representa una onda sinusoidal en 440 Hz durante 10 segundos. Estos valores se pueden modificar especificando los valores de modificador-f y-d.

RenderExclusiveTimerDriven muestra el almacenamiento en búfer basado en temporizador. En este modo, el cliente debe esperar durante un período de tiempo (la mitad de la latencia, especificada por el valor del modificador-d, en milisegundos). Cuando el cliente se reactiva, a mitad del período de procesamiento, extrae el siguiente conjunto de ejemplos del motor. Antes de cada paso de procesamiento en el bucle de almacenamiento en búfer, el cliente debe averiguar la cantidad de datos que se van a representar para que los datos no desbordan el búfer.

Los datos de audio que se van a reproducir en el dispositivo especificado se pueden procesar habilitando el almacenamiento en búfer basado en eventos. Este modo se muestra en el ejemplo RenderExclusiveTimerDriven.

Para obtener más información sobre la representación de una secuencia, vea [representar un flujo](rendering-a-stream.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de SDK que usan las API de audio principales](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



