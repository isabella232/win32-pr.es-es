---
description: Describe cómo agregar extensiones de unidad de datos al usar codificadores de Windows Media.
ms.assetid: fdadcb85-c564-4d05-a4d7-af53a0107455
title: Uso de las extensiones de unidad de datos (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21c16053ee078f5adcd48767f53d9e6e1c0eeb02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666777"
---
# <a name="using-data-unit-extensions-microsoft-media-foundation"></a>Uso de las extensiones de unidad de datos (Microsoft Media Foundation)

Los códecs de Windows Media Audio y vídeo están diseñados para funcionar bien con el contenedor de Advanced Systems Format (ASF). ASF es el formato estructurado que se usa para archivos de Windows Media Audio (WMA) y archivos de Windows Media Video (WMV). Es un formato extensible diseñado para la transmisión de datos. Una de las características inusuales de la estructura ASF es la capacidad de adjuntar metadatos a ejemplos individuales e incrustar esos datos con los ejemplos de la secuencia de bits. Un elemento de metadatos almacenado de esta manera se denomina *extensión de unidad* de datos o *extensión de ejemplo*.

Una extensión de unidad de datos puede contener información necesaria para el codificador, el descodificador o la aplicación del reproductor. La mayoría de los tipos de extensión de unidad de datos que se implementan en la serie de códecs de Windows Media 9 contienen los datos destinados a la aplicación que descodifica y representa el medio. Por ejemplo, puede mantener los códigos de tiempo SMPTE a partir de los datos de origen agregándolos como extensiones de unidad de datos. Sin embargo, las siguientes características de códec requieren extensiones de unidad de datos:

-   [Inserción de fotogramas clave forzada](forcedkeyframeinsertion.md)
-   [Codificación de vídeo entrelazada](interlacedvideoencoding.md)
-   La dificultad para usar las extensiones de unidad de datos al obtener acceso al códec directamente es el mecanismo por el que el objeto recibe los datos de la extensión. Esto se consigue mediante los objetos del SDK de Windows Media Format mediante el uso de objetos de búfer diseñados para admitir esta característica. Se recomienda usar el SDK de Windows Media Format para activar las características de códec que requieren extensiones de unidad de datos, pero puede hacer que estas características funcionen con los objetos de códec independientes.

## <a name="passing-extended-samples-to-the-codec-objects"></a>Pasar ejemplos extendidos a los objetos Codec

El SDK de Windows Media Format usa objetos de búfer que exponen interfaces [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) . La interfaz más reciente es [**INSSBuffer4**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4). Para pasar ejemplos a un objeto codec con extensiones de unidad de datos, debe utilizar un objeto de búfer que implemente la interfaz [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) o [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) y la interfaz **INSSBuffer** . Puede usar los objetos de búfer creados por el SDK de formato de Windows Media o Microsoft Media Foundation para conseguirlo, o puede crear su propia clase de búfer que cumpla los requisitos. Para crear su propia clase de búfer, debe ajustarse a los prototipos de método de las interfaces **INSSBuffer** . Estas definiciones de interfaz se pueden encontrar en el archivo de encabezado wmsbuffer. h que se instala con el SDK de Windows Media Format.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Códecs de Windows Media](windows-media-codecs.md)
</dt> </dl>

 

 
