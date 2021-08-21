---
description: En este ejemplo se usan core audio API para implementar una pantalla en pantalla que muestra los cambios de volumen en el flujo de salida que se reproduce a través del dispositivo de punto de conexión de representación de audio predeterminado.
ms.assetid: 33a1e843-f7c7-4da9-a51e-83a3f0a6ac70
title: Osd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17bc0b93214cc547f0491d568abb88d696f76b494f2c562f4805f425acdcfd89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077519"
---
# <a name="osd"></a>Osd

En este ejemplo se usan core audio API para implementar una pantalla en pantalla que muestra los cambios de volumen en el flujo de salida que se reproduce a través del dispositivo de punto de conexión de representación de audio predeterminado. La pantalla en pantalla aparece cuando el usuario ajusta el nivel de volumen en el programa de control de volumen de Windows, Sndvol.exe, y desaparece después de que el nivel de volumen permanezca sin cambios durante un breve período.

Este tema contiene las secciones siguientes.

-   [Descripción](#description)
-   [Requisitos](#requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Compilar el ejemplo](#building-the-sample)
-   [Ejecución del ejemplo](#running-the-sample)
-   [Temas relacionados](#related-topics)

## <a name="description"></a>Descripción

En este ejemplo se muestran las siguientes características.

-   [MMDevice API para](mmdevice-api.md) la enumeración y selección de dispositivos multimedia.
-   Audio [EndpointVolume API](endpointvolume-api.md)

## <a name="requirements"></a>Requisitos



| Producto                                                        | Versión                |
|----------------------------------------------------------------|------------------------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows Vista o posterior |
| Visual Studio                                                  | 2005 o posterior          |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en las siguientes ubicaciones.



| Location    | Ruta de acceso o dirección URL                                                                             |
|-------------|--------------------------------------------------------------------------------------|
| Windows SDK | \\Archivos de \\ programa Sdk de Microsoft Windows ejemplos de OSD de audio multimedia \\ \\ \\ v7.0... \\ \\ \\ \\ |



 

## <a name="building-the-sample"></a>Generar el ejemplo

1.  Abra el shell de CMD para el SDK de Windows y cambie al directorio de ejemplo OSD.
2.  Ejecute el comando "start OSD.sln" en el directorio OSD para abrir el proyecto OSD en Visual Studio ventana.
3.  En la ventana, seleccione  la **configuración** de  la solución Depurar o Liberar, seleccione el menú Compilar en la barra de menús y seleccione la **opción Compilar.** Si no abre Visual Studio desde el shell de CMD para el SDK, Visual Studio tendrá acceso al entorno de compilación del SDK. En ese caso, el ejemplo no se compilará a menos que establezca explícitamente la variable de entorno MSSdk, que se usa en el archivo de proyecto OSD.vcproj.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

1.  Ejecute el archivo ejecutable OSD, OSD.exe, en Windows Vista o posterior. Tenga en cuenta que no verá un icono de bandeja del sistema ni una ventana para la aplicación, pero puede ver el proceso en ejecución mediante TaskMgr.exe.
2.  Ejecute sndvol.exe para cambiar el volumen o la exclusión mutua, o bien cambiar el volumen mediante controles de teclado o un control HID. Se muestra la interfaz de usuario osd.
3.  Para salir de la aplicación, ejecute TaskMgr.exe, resalte el OSD.exe y haga clic **en Finalizar proceso.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos del SDK que usan las API de audio principales](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



