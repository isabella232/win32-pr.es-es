---
description: Esta aplicación de ejemplo, que muestra el almacenamiento en búfer controlado por eventos, usa las API de audio principal para representar datos de audio en un dispositivo de salida especificado por el usuario.
ms.assetid: 3a2e3fa6-2d6a-4ab0-a531-d1c968458e96
title: RenderExclusiveEventDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75553496219d0a4ddaf6685089de802e034f94cb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164837"
---
# <a name="renderexclusiveeventdriven"></a>RenderExclusiveEventDriven

Esta aplicación de ejemplo usa core Audio API para representar datos de audio en un dispositivo de salida especificado por el usuario. En este ejemplo se muestra el almacenamiento en búfer controlado por eventos para un cliente de representación en modo exclusivo. Para una secuencia en modo exclusivo, el cliente comparte el búfer del punto de conexión con el dispositivo de audio.

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



| Location    | Ruta de acceso o dirección URL                                                                                                    |
|-------------|-------------------------------------------------------------------------------------------------------------|
| Windows SDK | \\Archivos de \\ programa Sdk de Microsoft Windows ejemplos de audio multimedia \\ \\ v7.0 \\ \\ \\ \\ RenderExclusiveEventDriven \\ ... |



 

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo RenderExclusiveEventDriven, siga estos pasos:

1.  Abra el shell de CMD para el SDK Windows y cambie al directorio de ejemplo RenderExclusiveEventDriven.
2.  Ejecute el comando en el directorio RenderExclusiveEventDriven para abrir el `start WASAPIRenderExclusiveEventDriven.sln` proyecto WASAPIRenderExclusiveEventDriven en la Visual Studio cliente.
3.  En la ventana, seleccione  la **configuración** de  la solución Depurar o Liberar, seleccione el menú Compilar en la barra de menús y seleccione la **opción Compilar.** Si no abre una Visual Studio desde el shell de CMD para el SDK, Visual Studio no tendrá acceso al entorno de compilación del SDK. En ese caso, el ejemplo no se compilará a menos que establezca explícitamente la variable de entorno MSSdk, que se usa en el archivo de proyecto WASAPIRenderExclusiveEventDriven.vcproj.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

Si compila correctamente la aplicación de demostración, se genera WASAPIRenderExclusiveEventDriven.exe archivo ejecutable. Para ejecutarlo, escriba `WASAPIRenderExclusiveEventDriven` una ventana de comandos seguida de argumentos obligatorios u opcionales. En el ejemplo siguiente se muestra cómo ejecutar el ejemplo especificando la duración de reproducción en el dispositivo multimedia predeterminado.

`WASAPIRenderExclusiveEventDriven.exe -d 20 -multimedia`

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

El ejemplo RenderExclusiveEventDriven muestra el almacenamiento en búfer controlado por eventos. En el ejemplo se muestra cómo:

-   Cree una instancia de un cliente de audio, configúrelo para que se ejecute en modo exclusivo y habilite el almacenamiento en búfer controlado por eventos estableciendo la marca **\_ \_ EVENTCALLBACK AUDCLNT STREAMFLAGS** en la llamada a [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).
-   Asocie el cliente con los ejemplos que están listos para representarse proporcionando un identificador de eventos al sistema mediante una llamada al [**método IAudioClient::SetEventHandle.**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle)
-   Cree un subproceso de representación para procesar ejemplos del motor de audio.
-   Alinee los búferes correctamente en un límite de 128 bytes antes de enviarlos al dispositivo. Esto se hace ajustando la periodicidad del motor.
-   Compruebe el formato de combinación del punto de conexión del dispositivo para determinar si se pueden representar las muestras. Si el dispositivo no admite el formato de combinación, los datos se convierten a PCM.
-   Controle el cambio de flujo.

Una vez que se inicia la sesión de representación y se inicia la secuencia, el motor de audio señala el identificador de eventos proporcionado para notificar al cliente cada vez que un búfer está listo para que el cliente lo procese. Los datos de audio también se pueden procesar en un bucle controlado por temporizador. Este modo se muestra en el [ejemplo RenderExclusiveTimerDriven.](renderexclusivetimerdriven.md)

Para obtener más información sobre cómo representar una secuencia, vea [Representación de una secuencia.](rendering-a-stream.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de SDK que usan las API de audio principales](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



