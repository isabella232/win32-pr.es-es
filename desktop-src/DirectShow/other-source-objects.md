---
description: Otros objetos de origen
ms.assetid: 67482227-9df6-4e89-b16f-160a0bae6609
title: Otros objetos de origen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0c76c8f6cb104e87630f178a82d613675b96723
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806439"
---
# <a name="other-source-objects"></a>Otros objetos de origen

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Además de los orígenes de vídeo y audio, el [servicio de edición de DirectShow](directshow-editing-services.md) (des) admite los siguientes objetos de origen.

**Imágenes fijas**

DES admite los siguientes formatos de archivo para imágenes fijas:

-   Mapa de bits (.bmp)
-   GIF (formato de intercambio de gráficos)
-   JPEG (grupo de expertos fotográficos Unidos)
-   Adaptador de gráficos Targa o Truevision (. TGA): modo 2 (RGB sin comprimir) en formato de 16 bits, 24, bits o 32 bits.

Estos archivos se pueden usar como imágenes fijas o para crear animaciones. En el caso de los archivos Bitmap, JPEG y Targa, si usa el archivo como imagen fija, llame al método [**IAMTimelineSrc:: SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md) para establecer la velocidad de fotogramas en cero.

**Secuencias DIB**

Dado una serie de archivos de mapa de bits, JPEG o Targa, el motor de representación puede construir una secuencia DIB. Para crear una secuencia DIB, asigne a los archivos nombres secuenciales numéricos, como Image001.bmp, Image002.bmp, Image003.bmp, etc. Use el primer archivo de la secuencia como origen. Establezca la velocidad de fotogramas para la secuencia mediante una llamada a [**IAMTimelineSrc:: SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md). El motor de representación recorre las imágenes de la secuencia a la velocidad de fotogramas especificada.

Si la secuencia es demasiado corta para rellenar la duración, dada la velocidad de fotogramas, el resto de la duración es el negro sólido. No se produce ningún error durante la representación.

**Orígenes GIF**

DES admite orígenes GIF, incluidos los GIF animados y transparentes, mediante la especificación GIF89a. Con un GIF animado, a diferencia de los demás tipos de archivo, no es necesario establecer la velocidad de fotogramas. El archivo GIF especifica el retraso entre cada imagen de la animación.

Para admitir archivos GIF transparentes, DES convierte las regiones transparentes de la imagen en el triple Triple RGB (0,0). Después, puede usar la [transición de clave](key-transition.md) a la clave en RGB (0,0).

DES también convierte las regiones negras que se encuentran dentro del intervalo RGB (0 – 7, 0 – 7, 0 – 7) al valor RGB (8, 8, 8), excepto para el índice de transparencia, si está en ese intervalo. Esta conversión no se detecta en el ojo.

**Origen de color de vídeo**

El objeto de [origen de color de vídeo](video-color-source.md) crea una imagen de vídeo continua de un color sólido. Un uso para este objeto es convertirlo en una capa en una transición. Por ejemplo, úselo en un fundido de vídeo o fundido de salida.

**Filtros de origen personalizados**

DES puede usar un filtro de origen de DirectShow como origen de la escala de tiempo, si el filtro cumple las siguientes condiciones:

-   Admite búsquedas
-   Genera un formato compatible con DES. El formato se puede comprimir siempre que el sistema del usuario tenga un filtro DirectShow capaz de descodificarlo.

Para usar un origen personalizado, especifique el CLSID del filtro como el GUID del subobjeto del objeto de origen. Para obtener más información, vea [subobjects](subobjects.md). Para admitir propiedades personalizadas, impleméntelo como propiedades "put" de **IDispatch** . Solo se admiten propiedades estáticas en objetos de origen; no se admiten las propiedades dinámicas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con orígenes](working-with-sources.md)
</dt> </dl>

 

 



