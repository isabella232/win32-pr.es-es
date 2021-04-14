---
description: Esta aplicación de ejemplo usa las API de audio principales para cambiar el volumen del dispositivo, según lo especificado por el usuario.
ms.assetid: 2597f3b1-5339-4fd4-9938-39ff917626b4
title: EndpointVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e89efe89035ec272c68c6a9289672a249616e23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496372"
---
# <a name="endpointvolume"></a>EndpointVolume

Esta aplicación de ejemplo usa las API de audio principales para cambiar el volumen del dispositivo, según lo especificado por el usuario.

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
-   [ENDPOINTVOLUME API](endpointvolume-api.md) para controlar los niveles de volumen del punto de conexión del dispositivo.

## <a name="requirements"></a>Requisitos



| Producto                                                        | Versión   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en las siguientes ubicaciones.



| Location    | Ruta de acceso/URL                                                                                        |
|-------------|-------------------------------------------------------------------------------------------------|
| Windows SDK | \\Archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ multimedia \\ audio \\ EndpointVolume \\ ... |



 

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo x, siga estos pasos:

Para compilar el ejemplo EndpointVolumeChanger, siga estos pasos:

1.  Abra el shell de CMD para el Windows SDK y cambie al directorio de ejemplo EndpointVolume.
2.  Ejecute el comando `start EndpointVolumeChanger.sln` en el directorio EndpointVolume para abrir el proyecto EndpointVolumeChanger en la ventana de Visual Studio.
3.  En la ventana, seleccione la configuración de la solución de **depuración** o **versión** , seleccione el menú **compilar** en la barra de menús y seleccione la opción **compilar** . Si no abre Visual Studio desde el shell de CMD para el SDK, Visual Studio no tendrá acceso al entorno de compilación del SDK. En ese caso, el ejemplo no se compilará a menos que establezca explícitamente la variable de entorno MSSdk, que se usa en el archivo de proyecto, WASAPIEndpointVolume. vcproj.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

Si compila la aplicación de demostración correctamente, se genera un archivo ejecutable EndpointVolumeChanger.exe. Para ejecutarlo, escriba `EndpointVolumeChanger` en una ventana de comandos seguida de los argumentos obligatorios u opcionales. En el ejemplo siguiente se muestra cómo alternar el valor de silenciar en el dispositivo de consola predeterminado.

`EndpointVolumeChanger.exe -console -m`

En la tabla siguiente se muestran los argumentos.

| Argumento        | Descripción                                                         |
|-----------------|---------------------------------------------------------------------|
| -?              | Muestra la ayuda.                                                         |
| -H              | Muestra la ayuda.                                                         |
| -+              | Incrementa el nivel de volumen en el dispositivo de punto de conexión de audio en un solo paso. . |
| -arriba             | Incrementa el nivel de volumen en el dispositivo de punto de conexión de audio en un solo paso.   |
| --              | Disminuye el nivel de volumen en el dispositivo de punto de conexión de audio en un solo paso.   |
| -abajo           | Disminuye el nivel de volumen en el dispositivo de punto de conexión de audio en un solo paso.   |
| -v              | Establece el nivel de volumen maestro en el dispositivo de punto de conexión de audio.          |
| -consola        | Use el dispositivo de consola predeterminado.                                     |
| -comunicaciones | Use el dispositivo de comunicación predeterminado.                               |
| -multimedia     | Use el dispositivo multimedia predeterminado.                                  |
| -punto de conexión       | Use el identificador de extremo especificado en el valor del modificador.          |



 

Si la aplicación se ejecuta sin argumentos, enumera los dispositivos disponibles y solicita al usuario que seleccione un dispositivo. Una vez que el usuario especifica el dispositivo, la aplicación muestra la configuración actual del volumen del punto de conexión. El volumen se puede controlar mediante los modificadores descritos en la tabla anterior.

Para obtener más información sobre el control de los niveles de volumen de los dispositivos de punto de conexión de audio, consulte [ENDPOINTVOLUME API](endpointvolume-api.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de SDK que usan las API de audio principales](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



