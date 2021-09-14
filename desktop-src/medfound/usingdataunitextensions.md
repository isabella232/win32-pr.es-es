---
description: Describe cómo agregar extensiones de unidad de datos al usar Windows codificadores multimedia.
ms.assetid: fdadcb85-c564-4d05-a4d7-af53a0107455
title: Uso de extensiones de unidad de datos (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21c16053ee078f5adcd48767f53d9e6e1c0eeb02
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363674"
---
# <a name="using-data-unit-extensions-microsoft-media-foundation"></a>Uso de extensiones de unidad de datos (Microsoft Media Foundation)

Los códecs Windows media audio y vídeo están diseñados para funcionar bien con el contenedor de formato de sistemas avanzados (ASF). ASF es el formato estructurado que se usa para Windows archivos de Audio multimedia (WMA) y Windows media video (WMV). Es un formato extensible diseñado para el streaming de datos. Una de las características inusuales de la estructura de ASF es la capacidad de adjuntar metadatos a muestras individuales e insertar los datos con los ejemplos en el flujo de bits. Un elemento de metadatos almacenado de esta manera se denomina extensión de *unidad de datos* o extensión de *ejemplo*.

Una extensión de unidad de datos puede contener información necesaria para el codificador, el descodificador o la aplicación de reproductor. La mayoría de los tipos de extensión de unidad de datos que se implementan en los códecs de la serie Windows Media 9 contienen datos destinados a la aplicación que descodifica y representa los medios. Por ejemplo, puede mantener códigos de tiempo SMPTE a partir de datos de origen agregándolos como extensiones de unidad de datos. Sin embargo, las siguientes características de códec requieren extensiones de unidad de datos:

-   [Inserción forzada de fotogramas clave](forcedkeyframeinsertion.md)
-   [Codificación de vídeo entrelazada](interlacedvideoencoding.md)
-   La dificultad de usar extensiones de unidad de datos al acceder directamente al códec es el mecanismo por el que el objeto recibe los datos de extensión. Esto lo logran los objetos del SDK Windows Media Format mediante objetos de búfer diseñados para admitir esta característica. Se recomienda usar el SDK de formato multimedia de Windows para activar las características de códec que requieren extensiones de unidad de datos, pero puede hacer que estas características funcionen con los objetos de códec independientes.

## <a name="passing-extended-samples-to-the-codec-objects"></a>Pasar ejemplos extendidos a los objetos de códec

El SDK Windows Media Format usa objetos de búfer que exponen [**interfaces INSSBuffer.**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) La interfaz más reciente es [**INSSBuffer4.**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4) Para pasar ejemplos a un objeto de códec con extensiones de unidad de datos, debe usar un objeto de búfer que implemente la interfaz [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) o [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) y la **interfaz INSSBuffer.** Puede usar objetos de búfer creados por el SDK de formato multimedia de Windows o Microsoft Media Foundation para ello, o bien puede crear su propia clase de búfer que cumpla los requisitos. Para crear su propia clase de búfer, debe cumplir los prototipos de método para las **interfaces INSSBuffer.** Estas definiciones de interfaz se pueden encontrar en el archivo de encabezado wmsbuffer.h que se instala con el SDK Windows Media Format.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Códecs de Windows Media](windows-media-codecs.md)
</dt> </dl>

 

 
