---
description: Esta aplicación de ejemplo usa core Audio API para capturar datos de audio de un dispositivo de entrada especificado por el usuario y los escribe en un archivo .wav con nombre único en el directorio actual. En este ejemplo se muestra el almacenamiento en búfer controlado por temporizador.
ms.assetid: 06124b99-89b3-4dfa-b989-a54746ecd697
title: CaptureSharedTimerDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b635462767f22d3e31fe6deaa79b5c00911b378b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165122"
---
# <a name="capturesharedtimerdriven"></a>CaptureSharedTimerDriven

Esta aplicación de ejemplo usa core Audio API para capturar datos de audio de un dispositivo de entrada especificado por el usuario y los escribe en un archivo .wav con nombre único en el directorio actual. En este ejemplo se muestra el almacenamiento en búfer controlado por temporizador.

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
-   [WASAPI para](wasapi.md) operaciones de administración de flujos.

## <a name="requirements"></a>Requisitos



| Producto                                                        | Versión   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en las siguientes ubicaciones.



| Location    | Ruta de acceso o dirección URL                                                                                                  |
|-------------|-----------------------------------------------------------------------------------------------------------|
| Windows SDK | \\Archivos de programa Sdk de Microsoft Windows archivos de audio multimedia de ejemplo \\ \\ \\ v7.0 \\ \\ \\ \\ CaptureSharedTimerDriven \\ ... |



 

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo CaptureSharedTimerDriven, siga estos pasos:

1.  Abra el shell de CMD para Windows SDK y cambie al directorio de ejemplo CaptureSharedTimerDriven.
2.  Ejecute el comando en el directorio CaptureSharedTimerDriven para abrir el proyecto `start WASAPICaptureSharedTimerDriven.sln` WASAPICaptureSharedTimerDriven en la Visual Studio anterior.
3.  En la ventana, seleccione  la **configuración** de  la solución Depurar o Liberar, seleccione el menú Compilar en la barra de menús y seleccione la **opción Compilar.** Si no abre Visual Studio shell de CMD para el SDK, Visual Studio tendrá acceso al entorno de compilación del SDK. En ese caso, el ejemplo no se compilará a menos que establezca explícitamente la variable de entorno MSSdk, que se usa en el archivo de proyecto WASAPICaptureSharedTimerDriven.vcproj.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

Si compila correctamente la aplicación de demostración, se genera WASAPICaptureSharedTimerDriven.exe archivo ejecutable. Para ejecutarlo, escriba `WASAPICaptureSharedTimerDriven` una ventana de comandos seguida de argumentos obligatorios u opcionales. En el ejemplo siguiente se muestra cómo ejecutar el ejemplo especificando la duración de la captura en el dispositivo multimedia predeterminado.

`WASAPICaptureSharedTimerDriven.exe -d 20 -multimedia`

En la tabla siguiente se muestran los argumentos.

| Argumento        | Descripción                                                |
|-----------------|------------------------------------------------------------|
| -?              | Muestra ayuda.                                                |
| -H              | Muestra ayuda.                                                |
| -l              | Latencia de captura de audio en milisegundos.                     |
| -d              | Duración de la captura de audio en segundos.                         |
| -M              | Deshabilita el uso de MMCSS.                                 |
| -console        | Use el dispositivo de consola predeterminado.                            |
| -communications | Use el dispositivo de comunicación predeterminado.                      |
| -multimedia     | Use el dispositivo multimedia predeterminado.                         |
| -endpoint       | Use el identificador de punto de conexión especificado en el valor del modificador. |



 

Si la aplicación se ejecuta sin argumentos, enumera los dispositivos disponibles y solicita al usuario que seleccione un dispositivo para la sesión de captura. La consola predeterminada, la comunicación y los dispositivos multimedia aparecen seguidos de los dispositivos y los identificadores de punto de conexión. Si no se especifica ninguna duración, la secuencia de audio del dispositivo especificado se captura durante 10 segundos. La aplicación escribe los datos capturados en un archivo .wav con nombre único.

CaptureSharedTimerDriven muestra el almacenamiento en búfer controlado por temporizador. En este modo, el cliente debe esperar un período de tiempo (la mitad de la latencia, especificada por el valor del modificador -d, en milisegundos). Cuando el cliente se reactiva, a mitad del período de procesamiento, extrae el siguiente conjunto de muestras del motor. Antes de que cada procesamiento pase en el bucle de almacenamiento en búfer, el cliente debe averiguar la cantidad de datos de captura disponibles para que los datos no supere el búfer de captura. Los datos de audio que se capturan desde el dispositivo especificado se pueden procesar habilitando el almacenamiento en búfer controlado por eventos. Este modo se muestra en el [ejemplo CaptureSharedEventDriven.](capturesharedeventdriven.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos del SDK que usan las API de audio principales](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



