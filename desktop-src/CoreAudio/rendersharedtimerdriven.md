---
description: Esta aplicación de ejemplo, que muestra el almacenamiento en búfer controlado por temporizador, usa las API de audio principal para representar datos de audio en un dispositivo de salida especificado por el usuario.
ms.assetid: eae7d896-77ef-4340-bd77-1f3333166987
title: RenderSharedTimerDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37aace64636ff132006c3059f7e056c4312322d4b1b8f52c07c71e07c2186de5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984885"
---
# <a name="rendersharedtimerdriven"></a>RenderSharedTimerDriven

Esta aplicación de ejemplo usa core Audio API para representar datos de audio en un dispositivo de salida especificado por el usuario. En este ejemplo se muestra el almacenamiento en búfer controlado por temporizador para un cliente de representación en modo compartido. Para una secuencia en modo compartido, el cliente comparte el búfer del punto de conexión con el motor de audio.

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
-   WASAPI para operaciones de administración de flujos.

## <a name="requirements"></a>Requisitos



| Producto                                                        | Versión   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en las siguientes ubicaciones.



| Ubicación    | Ruta de acceso o dirección URL                                                                                                 |
|-------------|----------------------------------------------------------------------------------------------------------|
| Windows SDK | \\Archivos de \\ programa Sdk de Microsoft Windows ejemplos de audio multimedia \\ \\ v7.0 \\ \\ \\ \\ RenderSharedTimerDriven \\ ... |



 

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo RenderSharedTimerDriven, siga estos pasos:

1.  Abra el shell de CMD para Windows SDK y cambie al directorio de ejemplo RenderSharedTimerDriven.
2.  Ejecute el comando en el directorio `start WASAPIRenderSharedTimerDriven.sln` RenderSharedTimerDriven para abrir el proyecto WASAPIRenderSharedTimerDriven en la Visual Studio cliente.
3.  En la ventana, seleccione  la **configuración** de  la solución Depurar o Liberar, seleccione el menú Compilar en la barra de menús y seleccione la **opción Compilar.** Si no abre una Visual Studio desde el shell de CMD para el SDK, Visual Studio no tendrá acceso al entorno de compilación del SDK. En ese caso, el ejemplo no se compilará a menos que establezca explícitamente la variable de entorno MSSdk, que se usa en el archivo de proyecto WASAPIRenderSharedTimerDriven.vcproj.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

Si compila correctamente la aplicación de demostración, se genera WASAPIRenderSharedTimerDriven.exe archivo ejecutable. Para ejecutarlo, escriba `WASAPIRenderSharedTimerDriven` una ventana de comandos seguida de argumentos obligatorios u opcionales. En el ejemplo siguiente se muestra cómo ejecutar el ejemplo especificando la duración de reproducción en el dispositivo multimedia predeterminado.

`WASAPIRenderSharedTimerDriven.exe -d 20 -multimedia`

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

RenderSharedTimerDriven muestra el almacenamiento en búfer controlado por temporizador. En este modo, el cliente debe esperar un período de tiempo (la mitad de la latencia, especificada por el valor del modificador -d, en milisegundos). Cuando el cliente se reactiva, a mitad del período de procesamiento, extrae el siguiente conjunto de muestras del motor. Antes de que cada procesamiento pase en el bucle de almacenamiento en búfer, el cliente debe averiguar la cantidad de datos que se representará para que los datos no sobresalan el búfer.

Los datos de audio que se reproducirán en el dispositivo especificado se pueden procesar habilitando el almacenamiento en búfer controlado por eventos. Este modo se muestra en el ejemplo [RenderSharedEventDriven.](rendersharedeventdriven.md)

Para obtener más información sobre cómo representar una secuencia, vea [Representación de una secuencia.](rendering-a-stream.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de SDK que usan las API de audio principales](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



