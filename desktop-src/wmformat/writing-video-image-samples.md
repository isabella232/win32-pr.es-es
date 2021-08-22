---
title: Escribir ejemplos de imágenes de vídeo
description: Escribir ejemplos de imágenes de vídeo
ms.assetid: 1d375186-230a-4a18-a995-b331c72a76e7
keywords:
- Formato de sistemas avanzados (ASF), escribir ejemplos de imágenes de vídeo
- ASF (formato de sistemas avanzados), escribir ejemplos de imágenes de vídeo
- imágenes de vídeo, escribir ejemplos
- streams,writing video image samples
- códecs, escribir ejemplos de imágenes de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7c05bbcc9239eede97f4ea7ca0df34004b1fb7facc0c36c8f38098c42e86fce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704825"
---
# <a name="writing-video-image-samples"></a>Escribir ejemplos de imágenes de vídeo

Una secuencia de imagen de vídeo es un vídeo que contiene una serie de imágenes fijas. Las imágenes se pueden mover dentro del marco y cada imagen se puede combinar con la siguiente. Las secuencias de imágenes de vídeo se codifican con el códec Windows Media Video 9 Image v2. El vídeo de salida es similar al creado por el códec Windows Media Video 9.

Para crear un perfil que contenga una secuencia de imagen de vídeo, empiece por enumerar los códecs de vídeo como se describe en Obtención de información de configuración de [secuencias de códecs.](getting-stream-configuration-information-from-codecs.md) Busque el códec que admite el \_ subtipo WVP2 WMMEDIASUBTYPE.

Después de establecer el perfil en el objeto de escritor, llame a [**IWMWriter::GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops) para obtener las propiedades multimedia del flujo de entrada imagen de vídeo. Obtenga el tipo de medio del objeto de propiedades multimedia llamando a [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype)y cambie el subtipo a WMMEDIASUBTYPE \_ VIDEOIMAGE. Debe establecer el ancho y el alto del vídeo en las dimensiones máximas necesarias para abarcar las imágenes que agregará a la secuencia. A continuación, llame a [**IWMMediaProps::SetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-setmediatype) con el tipo de entrada modificado. Ahora está listo para empezar a enviar ejemplos al objeto de escritor.

Cada ejemplo debe comenzar con una **estructura \_ VIDEOIMAGE \_ SAMPLE2 de WMT.** Además, los ejemplos pueden contener imágenes de mapa de bits. Una imagen solo se adjunta a una muestra para el primer fotograma en el que aparece. Todos los fotogramas adicionales que usan esa imagen solo necesitan información en la estructura . Los mapas de bits de entrada deben tener el formato RGB, 24 bits por píxel.

Los archivos de mapa de bits almacenan los datos de la imagen para que los datos de cada fila de la imagen tome un número de bytes divisible por cuatro. (Esto se denomina el paso del mapa de bits). Esto obliga al principio de cada fila de vídeo a un **límite DWORD,** lo que hace que la copia sea más eficaz. Si las filas de imagen no se pueden dividir uniformemente entre cuatro, la fila se agrega al siguiente múltiplo más alto de cuatro bytes. Al adjuntar datos de imagen, debe quitar cualquier relleno que exista al final de los datos de cada fila.

El códec Windows Media Video 9 Image v2 mantiene hasta dos imágenes en memoria a la vez. Estas imágenes se denominan imagen anterior y imagen actual. Cada imagen tiene un conjunto de miembros en la estructura **\_ VIDEOIMAGE \_ SAMPLE2 de WMT,** que dicta cómo se presenta la imagen en el marco. Puede agregar una imagen estableciendo el miembro dwControlFlags de **WMT \_ VIDEOIMAGE \_ SAMPLE2** en WMT \_ VIDEOIMAGE \_ SAMPLE INPUT \_ \_ FRAME. Cuando se pasa un marco de entrada al códec, esa imagen se convierte en la imagen actual. La imagen que era la imagen actual en el ejemplo anterior normalmente se convierte en la imagen anterior y la imagen que era la imagen anterior en el ejemplo anterior se descarta. Puede configurar el códec para conservar la imagen anterior anterior estableciendo el **miembro bKeepPrevImage** en **TRUE.** En ese caso, se descarta la imagen que era la imagen actual en el ejemplo anterior.

La composición básica de un fotograma de imagen de vídeo viene determinada por dos factores para cada imagen: región de interés y coeficiente de mezcla. La región de interés para una imagen se define mediante un punto de origen, ancho y alto. La parte de una imagen descrita por la región de interés rellena el marco de salida. Si la región de interés tiene un tamaño diferente al marco de salida, el códec cambia su tamaño. El coeficiente de mezcla de la imagen determina la mezcla de las dos imágenes. Los coeficientes de mezcla de las imágenes actuales y anteriores deben tener un total de 1,0. Por ejemplo, si **fCurrBlendCoef** se establece en 0,5 y **fPrevBlendCoef** se establece en 0,5, el marco de salida se compone de una combinación igual de las regiones de interés de ambas imágenes.

Al manipular la región de interés de una imagen, puede crear efectos de desplazamiento panorámico y zoom. Los coeficientes de mezcla le permiten atenuar (atenuar) entre imágenes. Además de estos efectos, puede usar una de las transiciones predefinidas para crear fotogramas más complejos. Las transiciones disponibles se describen en la sección [Transiciones de imágenes de](video-image-transitions.md) vídeo de esta documentación. Al usar una transición, debe configurar cada fotograma. La manera más fácil de hacerlo es crear una función que cambie incrementalmente los miembros de la estructura **\_ VIDEOIMAGE \_ SAMPLE2** de WMT para un efecto completo.

Para obtener más información sobre los valores que se establecerán para las degradaciones, vea [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2).

**Nota** Si desea incluir audio en un archivo con una secuencia de imagen de vídeo, debe usar la entrada de audio sin comprimir. Para combinar una secuencia de imagen de vídeo con una secuencia de audio comprimida existente, debe descomprimir el audio y pasar los ejemplos sin comprimir. Si pasa muestras comprimidas al escritor al escribir una secuencia de imagen de vídeo, se producirá un error, lo que provocará que las muestras se desasoyen del vídeo.

Además, los archivos de imagen de vídeo comprimidos sin secuencias de audio pueden contener varios fotogramas de vídeo muy pequeños y muy comprimidos en un único paquete asf, lo que puede dar lugar a una experiencia de reproducción deficiente en versiones anteriores de Reproductor de Windows Media. Para evitar este problema, la mejor solución es insertar una secuencia de audio silenciosa en el archivo, aunque esto también aumentará el tamaño del archivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Imagen de vídeo**](video-image.md)
</dt> <dt>

[**Escritura de archivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




