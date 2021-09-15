---
title: Compatibilidad con imágenes personalizadas para dispositivos
description: Compatibilidad con imágenes personalizadas para dispositivos
ms.assetid: 0ccc327c-e953-4348-9802-705331b574ac
keywords:
- Reproductor de Windows Media, compatibilidad con imágenes personalizadas para dispositivos
- Reproductor de Windows Media,compatibilidad con imágenes para dispositivos
- compatibilidad con imágenes personalizadas de dispositivo
- compatibilidad con imágenes personalizadas para dispositivos
- Compatibilidad con imágenes para dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ffdf318df39935e844cc84919bb4d6e50cc259a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127258927"
---
# <a name="custom-image-support-for-devices"></a>Compatibilidad con imágenes personalizadas para dispositivos

> [!Note]  
> En esta sección se documenta una característica de Reproductor de Windows Media 10 que está disponible cuando se usa el Windows operativo XP. Es posible que no esté disponible en versiones posteriores.

 

Los fabricantes de dispositivos pueden proporcionar dos archivos de imagen especiales para personalizar la forma en que se representa un dispositivo en Reproductor de Windows Media interfaz de usuario 10. Estos dos archivos son:

-   DevIcon.fil. Un Windows de formato de icono que representa el hardware del dispositivo. Esta imagen se muestra en Reproductor de Windows Media 10 en cualquier lugar donde se usa un icono para representar un dispositivo, como la lista de dispositivos en la **característica Sincronización.**
-   DevLogo.fil. Un archivo de formato PNG que representa el logotipo corporativo del fabricante del dispositivo. Esta imagen se muestra en Reproductor de Windows Media 10 en cualquier lugar en el que se usa la personal de marca corporativa, como el cuadro **de diálogo Configuración del** dispositivo.

## <a name="general-guidelines-for-images"></a>Directrices generales para imágenes

Las siguientes directrices se aplican a la compatibilidad con imágenes personalizadas en general:

-   Esta característica es opcional. Los dispositivos que no proporcionen imágenes se representarán mediante imágenes predeterminadas.
-   Esta característica solo es compatible con dispositivos habilitados para MTP.
-   Para evitar cambios en los archivos, se recomienda almacenar los archivos de imagen en firmware o en un medio de almacenamiento protegido, no con archivos creados por el usuario.
-   Los archivos no deben devolverse a Windows de Administrador de dispositivos que enumeran el almacenamiento raíz del dispositivo. Además, se producirá un error al eliminar, mover o cambiar el nombre de los archivos.
-   Si el dispositivo proporciona más de un medio de almacenamiento, el dispositivo debe devolver los archivos de imagen en respuesta a las solicitudes abiertas de archivos desde cualquier medio. Se pueden devolver iconos de dispositivo diferentes desde cada medio de almacenamiento.
-   Para los Windows habilitados para Administrador de dispositivos Media Administrador de dispositivos 1.2, estas imágenes tendrán prioridad sobre las propiedades de icono proporcionadas por los mecanismos de configuración de Windows, como las propiedades del nodo de dispositivo.
-   Las imágenes no deben contener ninguna información que requiera localización.
-   En el caso de los dispositivos con varias funciones, solo las características de reproducción de música Windows XP usarán estas imágenes.

## <a name="creating-the-device-icon-image"></a>Creación de la imagen de icono de dispositivo

El archivo de imagen del icono de dispositivo, DevIcon.fil, debe contener un archivo en Windows de icono. En el artículo de MSDN [Iconos de Win32](/previous-versions/ms997538(v=msdn.10)) se describe cómo crear este tipo de archivo. En el artículo de MSDN [Creating Windows XP Icons (Creación](/previous-versions/ms997636(v=msdn.10)) de iconos de WINDOWS XP) se proporcionan directrices de estilo para Windows XP. El archivo de imagen de icono de dispositivo incorpora doce imágenes en un único archivo proporcionando cuatro tamaños diferentes con tres profundidades de color diferentes cada una.

Asegúrese de prestar especial atención a las siguientes directrices:

-   Los tamaños recomendados (en píxeles) son 16 x 16, 32 x 32, 48 x 48 y 256 x 256.
-   Las profundidades de color recomendadas son de 24 bits con canal alfa de 8 bits, 8 bits con transparencia de 1 bit y 4 bits con transparencia de 1 bit.
-   Use las recomendaciones de ángulo de perspectiva y sombra paralela descritas en los artículos de MSDN mencionados anteriormente.

Una vez que haya creado el archivo de icono, simplemente cámbiele el nombre DevIcon.fil.

## <a name="creating-the-corporate-logo-image"></a>Creación de la imagen de logotipo corporativo

El archivo de imagen del logotipo corporativo, DevLogo.fil, debe contener un archivo en formato PNG. Use las siguientes directrices al crear la imagen:

-   Las dimensiones máximas de la imagen son de 150 x 32 píxeles.
-   La imagen debe admitir la combinación alfa para permitir una transición fluida entre la interfaz de usuario Reproductor de Windows Media 10 y el logotipo.

Una vez que haya creado el archivo de logotipo corporativo, simplemente cambie su nombre a DevLogo.fil.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Reproductor de Windows Media**](windows-media-player.md)
</dt> </dl>

 

 