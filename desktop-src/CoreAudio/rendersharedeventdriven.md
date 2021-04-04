---
description: Esta aplicación de ejemplo usa las API de audio principales para representar datos de audio en un dispositivo de salida, especificado por el usuario.
ms.assetid: 92e644be-df8b-415d-ac8e-c0c30c85f844
title: RenderSharedEventDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9901896b962717ed72fd36d022eef9510d7cb916
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907317"
---
# <a name="rendersharedeventdriven"></a>RenderSharedEventDriven

Esta aplicación de ejemplo usa las API de audio principales para representar datos de audio en un dispositivo de salida, especificado por el usuario. Este ejemplo muestra el almacenamiento en búfer basado en eventos para un cliente de representación en modo compartido. En el caso de una secuencia en modo compartido, el cliente comparte el búfer del extremo con el motor de audio.

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
-   WASAPI para las operaciones de administración de secuencias.

## <a name="requirements"></a>Requisitos



| Producto                                                        | Versión   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en las siguientes ubicaciones.



| Location    | Ruta de acceso/URL                                                                                                 |
|-------------|----------------------------------------------------------------------------------------------------------|
| Windows SDK | \\Archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ multimedia \\ audio \\ RenderSharedEventDriven \\ ... |



 

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo RenderSharedEventDriven, siga estos pasos:

1.  Abra el shell de CMD para el Windows SDK y cambie al directorio de ejemplo RenderSharedEventDriven.
2.  Ejecute el comando `start WASAPIRenderSharedEventDriven.sln` en el directorio RenderSharedEventDriven para abrir el proyecto WASAPIRenderSharedEventDriven en la ventana de Visual Studio.
3.  En la ventana, seleccione la configuración de la solución de **depuración** o **versión** , seleccione el menú **compilar** en la barra de menús y seleccione la opción **compilar** . Si no abre Visual Studio desde el shell de CMD para el SDK, Visual Studio no tendrá acceso al entorno de compilación del SDK. En ese caso, el ejemplo no se compilará a menos que establezca explícitamente la variable de entorno MSSdk, que se usa en el archivo de proyecto, WASAPIRenderSharedEventDriven. vcproj.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

Si compila la aplicación de demostración correctamente, se genera un archivo ejecutable WASAPIRenderSharedEventDriven.exe. Para ejecutarlo, escriba `WASAPIRenderSharedEventDriven` en una ventana de comandos seguida de los argumentos obligatorios u opcionales. En el ejemplo siguiente se muestra cómo ejecutar el ejemplo especificando la duración de la reproducción en el dispositivo multimedia predeterminado.

`WASAPIRenderSharedEventDriven.exe -d 20 -multimedia`

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

RenderSharedEventDriven muestra el almacenamiento en búfer basado en eventos. En el ejemplo se muestra cómo:

-   Cree una instancia de un cliente de audio, configúrela para que se ejecute en modo exclusivo y habilite el almacenamiento en búfer basado en eventos estableciendo la marca **\_ \_ EVENTCALLBACK STREAMFLAGS AUDCLNT** en la llamada a [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).
-   Asocie el cliente a los ejemplos que estén listos para ser representados proporcionando un identificador de evento al sistema llamando al método [**IAudioClient:: SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) .
-   Cree un subproceso de representación para procesar los ejemplos del motor de audio.
-   Compruebe el formato de combinación del punto de conexión del dispositivo para determinar si se pueden representar los ejemplos. Si el dispositivo no admite el formato de combinación, los datos se convierten en PCM.
-   Controlar el cambio de flujo.

Una vez iniciada la sesión de representación y iniciada la secuencia, el motor de audio señala el identificador de eventos proporcionado para notificar al cliente cada vez que un búfer está listo para que lo procese el cliente. Los datos de audio también se pueden procesar en un bucle controlado por temporizador. Este modo se muestra en el ejemplo [RenderSharedTimerDriven](rendersharedtimerdriven.md) .

Para obtener más información sobre la representación de una secuencia, vea [representar un flujo](rendering-a-stream.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de SDK que usan las API de audio principales](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



