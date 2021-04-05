---
description: En este ejemplo se usan las API de audio principales para implementar una pantalla en pantalla que muestra los cambios de volumen en el flujo de salida que se reproduce a través del dispositivo de extremo de representación de audio predeterminado.
ms.assetid: 33a1e843-f7c7-4da9-a51e-83a3f0a6ac70
title: Feature
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89c4c04daf5d2dd333a25150821a831695e06a06
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080224"
---
# <a name="osd"></a>Feature

En este ejemplo se usan las API de audio principales para implementar una pantalla en pantalla que muestra los cambios de volumen en el flujo de salida que se reproduce a través del dispositivo de extremo de representación de audio predeterminado. La presentación en pantalla aparece cuando el usuario ajusta el nivel de volumen en el programa de control de volumen de Windows, Sndvol.exe, y desaparece después de que el nivel de volumen permanezca inalterado durante un breve período de tiempo.

Este tema contiene las siguientes secciones.

-   [Descripción](#description)
-   [Requisitos](#requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Compilar el ejemplo](#building-the-sample)
-   [Ejecutar el ejemplo](#running-the-sample)
-   [Temas relacionados](#related-topics)

## <a name="description"></a>Descripción

En este ejemplo se muestran las características siguientes.

-   [MMDEVICE API](mmdevice-api.md) para la enumeración y selección de dispositivos multimedia.
-   API de audio [EndpointVolume](endpointvolume-api.md)

## <a name="requirements"></a>Requisitos



| Producto                                                        | Versión                |
|----------------------------------------------------------------|------------------------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows Vista o posterior |
| Visual Studio                                                  | 2005 o posterior          |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en las siguientes ubicaciones.



| Location    | Ruta de acceso/URL                                                                             |
|-------------|--------------------------------------------------------------------------------------|
| Windows SDK | \\Archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ multimedia \\ audio \\ OSD \\ ... |



 

## <a name="building-the-sample"></a>Generar el ejemplo

1.  Abra el shell de CMD para el Windows SDK y cambie al directorio de ejemplo OSD.
2.  Ejecute el comando "Start OSD. sln" en el directorio OSD para abrir el proyecto OSD en la ventana de Visual Studio.
3.  En la ventana, seleccione la configuración de la solución de **depuración** o **versión** , seleccione el menú **compilar** en la barra de menús y seleccione la opción **compilar** . Si no abre Visual Studio desde el shell de CMD para el SDK, Visual Studio no tendrá acceso al entorno de compilación del SDK. En ese caso, el ejemplo no se compilará a menos que establezca explícitamente la variable de entorno MSSdk, que se usa en el archivo de proyecto, OSD. vcproj.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

1.  Ejecute el archivo ejecutable OSD, OSD.exe, en Windows Vista o posterior. Tenga en cuenta que no verá un icono de la bandeja del sistema o una ventana de la aplicación, pero puede ver el proceso en ejecución mediante TaskMgr.exe.
2.  Ejecute sndvol.exe para cambiar el volumen o silenciar, o bien cambie el volumen mediante controles de teclado o un control HID. Se muestra la interfaz de usuario OSD.
3.  Para salir de la aplicación, ejecute TaskMgr.exe, resalte el proceso de OSD.exe y haga clic en **Finalizar proceso**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de SDK que usan las API de audio principales](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



