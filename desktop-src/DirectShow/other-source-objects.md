---
description: Otros objetos de origen
ms.assetid: 67482227-9df6-4e89-b16f-160a0bae6609
title: Otros objetos de origen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0c76c8f6cb104e87630f178a82d613675b96723
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362374"
---
# <a name="other-source-objects"></a>Otros objetos de origen

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Además de los orígenes de audio y vídeo, [DirectShow Editing Services](directshow-editing-services.md) (DES) admite los siguientes objetos de origen.

**Imágenes fijas**

DES admite los siguientes formatos de archivo para imágenes fijas:

-   Mapa de bits (.bmp)
-   GIF (Formato de intercambio de gráficos)
-   JPEG (Grupo conjunto de expertos en fotografía)
-   Adaptador de gráficos Targa o Truevision (.tga): modo 2 (RGB sin comprimir) en formato de 16 bits, 24 bits o 32 bits.

Estos archivos se pueden usar como imágenes fijas o para crear animaciones. En el caso de los archivos de mapa de bits, JPEG y Targa, si usa el archivo como imagen fija, llame al método [**IAMTimelineSrc::SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md) para establecer la velocidad de fotogramas en cero.

**Secuencias DIB**

Dado una serie de archivos de mapa de bits, JPEG o Targa, el motor de representación puede construir una secuencia DIB. Para crear una secuencia DIB, dé a los archivos nombres secuenciales numéricamente, como Image001.bmp, Image002.bmp, Image003.bmp, y así sucesivamente. Use el primer archivo de la secuencia como origen. Establezca la velocidad de fotogramas de la secuencia llamando a [**IAMTimelineSrc::SetDefaultFPS.**](iamtimelinesrc-setdefaultfps.md) El motor de representación recorrerá las imágenes de la secuencia a la velocidad de fotogramas especificada.

Si la secuencia es demasiado corta para rellenar la duración, dada la velocidad de fotogramas, el resto de la duración es de color negro sólido. No se produce ningún error durante la representación.

**Orígenes gif**

DES admite orígenes GIF, incluidos los GIF animados y transparentes, mediante la especificación GIF89a. Con un GIF animado, a diferencia de los otros tipos de archivo, no es necesario establecer la velocidad de fotogramas. El archivo GIF especifica el retraso entre cada imagen de la animación.

Para admitir ARCHIVOS GIF transparentes, DES convierte las regiones transparentes de la imagen en rgb triplet RGB (0,0,0). A continuación, puede usar [la tecla Transición](key-transition.md) a clave en RGB(0,0,0).

DES también convierte cualquier región negra que se encuentra dentro del intervalo RGB (0–7,0–7,0–7) en el valor RGB(8,8,8),excepto para el índice de transparencia, si se encuentra en ese intervalo. Esta conversión no se puede detectar a los ojos.

**Origen de color de vídeo**

El [objeto Origen de color de](video-color-source.md) vídeo crea una imagen de vídeo continua de un color sólido. Un uso de este objeto es convertirla en una capa en una transición. Por ejemplo, úselo en un vídeo de atenuación o atenuación.

**Filtros de origen personalizados**

DES puede usar un filtro DirectShow origen como origen de escala de tiempo, si el filtro cumple las condiciones siguientes:

-   Admite búsquedas
-   Genera un formato compatible con DES. El formato se puede comprimir siempre que el sistema del usuario tenga un filtro DirectShow capaz de descodearlo.

Para usar un origen personalizado, especifique el CLSID del filtro como el GUID del subobjeto del objeto de origen. Para obtener más información, vea [Subobjects](subobjects.md). Para admitir propiedades personalizadas, implemente como **propiedades IDispatch** "put". Solo se admiten propiedades estáticas en objetos de origen; No se admiten propiedades dinámicas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con orígenes](working-with-sources.md)
</dt> </dl>

 

 



