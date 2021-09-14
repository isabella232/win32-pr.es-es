---
description: Esta aplicación de ejemplo usa las API de audio principal para cambiar el volumen del dispositivo, según lo especificado por el usuario.
ms.assetid: 2597f3b1-5339-4fd4-9938-39ff917626b4
title: EndpointVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e89efe89035ec272c68c6a9289672a249616e23
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164993"
---
# <a name="endpointvolume"></a>EndpointVolume

Esta aplicación de ejemplo usa las API de audio principal para cambiar el volumen del dispositivo, según lo especificado por el usuario.

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
-   [EndpointVolume API para](endpointvolume-api.md) controlar los niveles de volumen del punto de conexión del dispositivo.

## <a name="requirements"></a>Requisitos



| Producto                                                        | Versión   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en las siguientes ubicaciones.



| Location    | Ruta de acceso o dirección URL                                                                                        |
|-------------|-------------------------------------------------------------------------------------------------|
| Windows SDK | \\Archivos de \\ programa Sdk de Microsoft Windows ejemplos de audio multimedia \\ \\ v7.0 \\ \\ \\ \\ EndpointVolume \\ ... |



 

## <a name="building-the-sample"></a>Generar el ejemplo

Para compilar el ejemplo x, siga estos pasos:

Para compilar el ejemplo EndpointVolumeChanger, siga estos pasos:

1.  Abra el shell de CMD para Windows SDK y cambie al directorio de ejemplo EndpointVolume.
2.  Ejecute el comando en el directorio EndpointVolume para abrir el proyecto `start EndpointVolumeChanger.sln` EndpointVolumeChanger en Visual Studio ventana.
3.  En la ventana, seleccione  la **configuración** de  la solución Depurar o Liberar, seleccione el menú Compilar en la barra de menús y seleccione la **opción Compilar.** Si no abre una Visual Studio desde el shell de CMD para el SDK, Visual Studio no tendrá acceso al entorno de compilación del SDK. En ese caso, el ejemplo no se compilará a menos que establezca explícitamente la variable de entorno MSSdk, que se usa en el archivo de proyecto WASAPIEndpointVolume.vcproj.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

Si compila correctamente la aplicación de demostración, se genera EndpointVolumeChanger.exe archivo ejecutable. Para ejecutarlo, escriba `EndpointVolumeChanger` una ventana de comandos seguida de argumentos obligatorios u opcionales. En el ejemplo siguiente se muestra cómo alternar la configuración de exclusión mutua en el dispositivo de consola predeterminado.

`EndpointVolumeChanger.exe -console -m`

En la tabla siguiente se muestran los argumentos.

| Argumento        | Descripción                                                         |
|-----------------|---------------------------------------------------------------------|
| -?              | Muestra ayuda.                                                         |
| -H              | Muestra ayuda.                                                         |
| -+              | Incrementa el nivel de volumen en el dispositivo de punto de conexión de audio en un paso. . |
| -up             | Incrementa el nivel de volumen en el dispositivo de punto de conexión de audio en un paso.   |
| --              | Disminuye el nivel de volumen en el dispositivo de punto de conexión de audio en un paso.   |
| -down           | Disminuye el nivel de volumen en el dispositivo de punto de conexión de audio en un paso.   |
| -v              | Establece el nivel de volumen maestro en el dispositivo de punto de conexión de audio.          |
| -console        | Use el dispositivo de consola predeterminado.                                     |
| -communications | Use el dispositivo de comunicación predeterminado.                               |
| -multimedia     | Use el dispositivo multimedia predeterminado.                                  |
| -endpoint       | Use el identificador de punto de conexión especificado en el valor del modificador.          |



 

Si la aplicación se ejecuta sin argumentos, enumera los dispositivos disponibles y solicita al usuario que seleccione un dispositivo. Una vez que el usuario especifica el dispositivo, la aplicación muestra la configuración del volumen actual para el punto de conexión. El volumen se puede controlar mediante los modificadores descritos en la tabla anterior.

Para obtener más información sobre cómo controlar los niveles de volumen de los dispositivos de punto de conexión de audio, vea [EndpointVolume API](endpointvolume-api.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de SDK que usan las API de audio principales](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



