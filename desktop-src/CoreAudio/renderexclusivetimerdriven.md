---
description: Esta aplicación de ejemplo usa core Audio API para representar datos de audio en un dispositivo de salida especificado por el usuario. En este ejemplo se muestra el almacenamiento en búfer controlado por temporizador para un cliente de representación en modo exclusivo.
ms.assetid: 9dcfccd2-a709-4b4e-bbb3-4c68a15cce03
title: RenderExclusiveTimerDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6876c448aa7737683aff4e495416020af7def54cb01109c3d6ad2d1c26d20780
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077449"
---
# <a name="renderexclusivetimerdriven"></a>RenderExclusiveTimerDriven

Esta aplicación de ejemplo usa core Audio API para representar datos de audio en un dispositivo de salida especificado por el usuario. En este ejemplo se muestra el almacenamiento en búfer controlado por temporizador para un cliente de representación en modo exclusivo. Para una secuencia en modo exclusivo, el cliente comparte el búfer del punto de conexión con el dispositivo de audio.

En este tema se incluyen las siguientes secciones.

-   [Descripción](#description)
-   [Requisitos](#requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Compilar el ejemplo](#building-the-sample)
-   [Ver los archivos de ejemplo](#view-the-sample-files)
-   [Temas relacionados](#related-topics)

## <a name="description"></a>Descripción

En este ejemplo se muestran las siguientes características.

-   [MMDevice API para](mmdevice-api.md) la enumeración y selección de dispositivos multimedia.
-   WASAPI para operaciones de administración de flujos.

## <a name="requirements"></a>Requisitos



| Producto                                                        | Versión   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en las siguientes ubicaciones.



| Location    | Ruta de acceso o dirección URL                                                                                                    |
|-------------|-------------------------------------------------------------------------------------------------------------|
| Windows SDK | \\Archivos de \\ programa Sdk de Microsoft Windows ejemplos de audio multimedia \\ \\ v7.0 \\ \\ \\ \\ RenderExclusiveTimerDriven \\ ... |



 

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo RenderExclusiveTimerDriven, siga estos pasos:

1.  Abra el shell cmd para el SDK Windows y cambie al directorio de ejemplo RenderExclusiveTimerDriven.
2.  Ejecute el comando `start WASAPIRenderExclusiveTimerDriven.sln` en el directorio RenderExclusiveTimerDriven para abrir el proyecto WASAPIRenderExclusiveTimerDriven en la Visual Studio cliente.
3.  En la ventana, seleccione  la **configuración** de  la solución Depurar o Liberar, seleccione el menú Compilar en la barra de menús y seleccione la **opción Compilar.** Si no abre una Visual Studio desde el shell de CMD para el SDK, Visual Studio no tendrá acceso al entorno de compilación del SDK. En ese caso, el ejemplo no se compilará a menos que establezca explícitamente la variable de entorno MSSdk, que se usa en el archivo de proyecto WASAPIRenderExclusiveTimerDriven.vcproj.

## <a name="view-the-sample-files"></a>Ver los archivos de ejemplo

Si compila correctamente la aplicación de demostración, se genera WASAPIRenderExclusiveTimerDriven.exe archivo ejecutable. Para ejecutarlo, escriba `WASAPIRenderExclusiveTimerDriven` una ventana de comandos seguida de argumentos obligatorios u opcionales. En el ejemplo siguiente se muestra cómo ejecutar el ejemplo especificando la duración de reproducción en el dispositivo de consola predeterminado.

`WASAPIRenderExclusiveTimerDriven.exe -d 20 -console`

En la tabla siguiente se muestran los argumentos.

| Argumento        | Descripción                                                |
|-----------------|------------------------------------------------------------|
| -?              | Muestra ayuda.                                                |
| -H              | Muestra ayuda.                                                |
| -f              | Frecuencia de onda sinusoidal en Hz.                                 |
| -l              | Latencia de representación de audio en milisegundos.                      |
| -d              | Duración de la onda sinusoidal en segundos.                             |
| -M              | Deshabilita el uso de MMCSS.                                 |
| -console        | Use el dispositivo de consola predeterminado.                            |
| -communications | Use el dispositivo de comunicación predeterminado.                      |
| -multimedia     | Use el dispositivo multimedia predeterminado.                         |
| -endpoint       | Use el identificador de punto de conexión especificado en el valor del modificador. |



 

Si la aplicación se ejecuta sin argumentos, enumera los dispositivos disponibles y solicita al usuario que seleccione un dispositivo para la sesión de representación. Una vez que el usuario especifica un dispositivo, la aplicación representa una onda seno a 440 Hz durante 10 segundos. Estos valores se pueden modificar especificando los valores de modificador -f y -d.

RenderExclusiveTimerDriven muestra el almacenamiento en búfer controlado por temporizador. En este modo, el cliente debe esperar un período de tiempo (la mitad de la latencia, especificada por el valor del modificador -d, en milisegundos). Cuando el cliente se reactiva, a mitad del período de procesamiento, extrae el siguiente conjunto de muestras del motor. Antes de que cada procesamiento pase en el bucle de almacenamiento en búfer, el cliente debe averiguar la cantidad de datos que se representará para que los datos no sobresalan el búfer.

Los datos de audio que se reproducirán en el dispositivo especificado se pueden procesar habilitando el almacenamiento en búfer controlado por eventos. Este modo se muestra en el ejemplo RenderExclusiveTimerDriven.

Para obtener más información sobre cómo representar una secuencia, vea [Representación de una secuencia.](rendering-a-stream.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de SDK que usan las API de audio principales](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



