---
title: Compatibilidad con imágenes personalizadas para dispositivos
description: Compatibilidad con imágenes personalizadas para dispositivos
ms.assetid: 0ccc327c-e953-4348-9802-705331b574ac
keywords:
- Windows Media Player, compatibilidad con imágenes personalizadas para dispositivos
- Windows Media Player, compatibilidad con imágenes para dispositivos
- compatibilidad con imágenes personalizadas de dispositivo
- compatibilidad con imágenes personalizadas para dispositivos
- compatibilidad con imágenes para dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ffdf318df39935e844cc84919bb4d6e50cc259a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695684"
---
# <a name="custom-image-support-for-devices"></a>Compatibilidad con imágenes personalizadas para dispositivos

> [!Note]  
> En esta sección se documenta una característica de Windows Media Player 10 que está disponible al usar el sistema operativo Windows XP. Puede que no esté disponible en versiones posteriores.

 

Los fabricantes de dispositivos pueden proporcionar dos archivos de imagen especiales para personalizar el modo en que se representa un dispositivo en la interfaz de usuario de Windows Media Player 10. Estos dos archivos son:

-   DevIcon. fil. Un archivo de formato de icono de Windows que representa el hardware del dispositivo. Esta imagen se muestra en Windows Media Player 10 en cualquier lugar donde se use un icono para representar un dispositivo, como la lista de dispositivos en la característica de **sincronización** .
-   DevLogo. fil. Un archivo de formato PNG que representa el logotipo corporativo del fabricante del dispositivo. Esta imagen se muestra en Windows Media Player 10 Anywhere se usa la personalización de marca corporativa, como el cuadro de diálogo de **instalación del dispositivo** .

## <a name="general-guidelines-for-images"></a>Directrices generales para imágenes

Las siguientes directrices se aplican a la compatibilidad con imágenes personalizadas en general:

-   Esta característica es opcional. Los dispositivos que no suministran imágenes se representarán mediante imágenes predeterminadas.
-   Esta característica solo es compatible con dispositivos habilitados para MTP.
-   Para evitar cambios en los archivos, se recomienda que los archivos de imagen se almacenen en el firmware o en un medio de almacenamiento protegido, no en los archivos creados por el usuario.
-   Los archivos no se deben devolver a Windows Media Administrador de dispositivos clientes que enumeran el almacenamiento raíz del dispositivo. Además, se debe producir un error al eliminar, mover o cambiar el nombre de los archivos.
-   Si el dispositivo proporciona más de un medio de almacenamiento, el dispositivo debe devolver los archivos de imagen en respuesta a las solicitudes de apertura de archivos de cualquier medio. Se pueden devolver iconos de dispositivo diferentes de cada medio de almacenamiento.
-   En el caso de los clientes habilitados para Windows Media Administrador de dispositivos 1,2, estas imágenes tendrán prioridad sobre las propiedades de icono suministradas por los mecanismos de instalación de Windows, como las propiedades de nodo de dispositivo.
-   Las imágenes no deben contener ninguna información que requiera localización.
-   En el caso de los dispositivos de varias funciones, solo las características de reproducción de música de Windows XP usarán estas imágenes.

## <a name="creating-the-device-icon-image"></a>Crear la imagen del icono del dispositivo

El archivo de imagen del icono del dispositivo, DevIcon. fil, debe contener un archivo en formato de icono de Windows. Los [iconos de los artículos de MSDN en Win32](/previous-versions/ms997538(v=msdn.10)) describen cómo crear este tipo de archivo. En el artículo de MSDN [crear iconos de Windows XP](/previous-versions/ms997636(v=msdn.10)) se proporcionan instrucciones de estilo para los iconos de Windows XP. El archivo de imagen del icono del dispositivo incorpora doce imágenes en un único archivo, ya que proporciona cuatro tamaños diferentes con tres profundidades de color diferentes cada una.

Asegúrese de prestar especial atención a las siguientes directrices:

-   Los tamaños recomendados (en píxeles) son 16x16, 32x32, 48x48 y 256x256.
-   Las profundidades de color recomendadas son de 24 bits con canal alfa de 8 bits, de 8 bits con transparencia de 1 bit y de 4 bits con transparencia de 1 bit.
-   Use las recomendaciones de ángulo de perspectiva y sombra paralela que se describen en los artículos de MSDN mencionados anteriormente.

Una vez que haya creado el archivo de icono, simplemente cambie el nombre de DevIcon. fil.

## <a name="creating-the-corporate-logo-image"></a>Creación de la imagen de logotipo corporativo

El archivo de imagen del logotipo corporativo, DevLogo. fil, debe contener un archivo en formato PNG. Siga estas instrucciones al crear la imagen:

-   Las dimensiones máximas de la imagen son 150x32 píxeles.
-   La imagen debe admitir la combinación alfa para permitir una transición fluida entre la interfaz de usuario de Windows Media Player 10 y el logotipo.

Una vez que haya creado el archivo de logotipo corporativo, simplemente cambie el nombre de DevLogo. fil.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Reproductor de Windows Media**](windows-media-player.md)
</dt> </dl>

 

 