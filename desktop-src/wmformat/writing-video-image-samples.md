---
title: Escribir ejemplos de imagen de vídeo
description: Escribir ejemplos de imagen de vídeo
ms.assetid: 1d375186-230a-4a18-a995-b331c72a76e7
keywords:
- Advanced Systems Format (ASF), escribir ejemplos de imágenes de vídeo
- ASF (formato de sistemas avanzados), escribir ejemplos de imagen de vídeo
- imágenes de vídeo, escribir ejemplos
- flujos, escribir ejemplos de imagen de vídeo
- códecs, escribir ejemplos de imagen de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fbac644d7938477ba3d2e8b21ebb6e631a47708
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104358678"
---
# <a name="writing-video-image-samples"></a>Escribir ejemplos de imagen de vídeo

Una secuencia de imágenes de vídeo es un vídeo que contiene una serie de imágenes fijas. Las imágenes pueden moverse dentro del fotograma y cada imagen puede fusionarse en el siguiente. Los flujos de imagen de vídeo se codifican con el códec Windows Media Video 9 Image V2. El vídeo de salida es similar al creado por el códec Windows Media Video 9.

Para crear un perfil que contenga una secuencia de imágenes de vídeo, empiece por enumerar los códecs de vídeo, tal como se describe en [obtención de información de configuración de flujo de códecs](getting-stream-configuration-information-from-codecs.md). Busque el códec que admite el \_ subtipo WMMEDIASUBTYPE WVP2.

Después de establecer el perfil en el objeto de escritor, llame a [**IWMWriter:: GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops) para obtener las propiedades multimedia para el flujo de entrada de la imagen de vídeo. Obtenga el tipo de medio del objeto de propiedades de medios, llamando a [**IWMMediaProps:: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype), y cambie el subtipo a WMMEDIASUBTYPE \_ videoimage. Debe establecer el ancho y el alto del vídeo en las dimensiones máximas necesarias para abarcar las imágenes que se van a agregar a la secuencia. A continuación, llame a [**IWMMediaProps:: SetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-setmediatype) con el tipo de entrada modificado. Ahora ya está listo para empezar a enviar ejemplos al objeto escritor.

Cada ejemplo debe comenzar con una estructura de **\_ \_ SAMPLE2 de imágenes WMT** . Además, los ejemplos pueden contener imágenes de mapa de bits. Una imagen solo se adjunta a un ejemplo para el primer fotograma en el que aparece. Todos los marcos adicionales que usan esa imagen solo necesitan información en la estructura. Los mapas de bits de entrada deben tener formato de RGB, 24 bits por píxel.

Los archivos de mapa de bits almacenan los datos de la imagen de modo que los datos de cada fila de la imagen contengan un número de bytes divisible por cuatro. (Esto se denomina intervalo del mapa de bits). Esto obliga al principio de cada fila de vídeo a un límite **DWORD** , lo que hace que la copia sea más eficaz. Si las filas de la imagen no son divisible en cuatro partes, la fila se rellenará hasta el siguiente múltiplo más alto de cuatro bytes. Al adjuntar datos de imagen, debe quitar cualquier relleno que exista al final de los datos de cada fila.

El códec Windows Media Video 9 Image V2 mantiene hasta dos imágenes en la memoria a la vez. Estas imágenes se denominan la imagen anterior y la imagen actual. Cada imagen tiene un conjunto de miembros de la estructura de **\_ \_ SAMPLE2 de imágenes WMT** , que dictan cómo se presenta la imagen en el fotograma. Puede Agregar una imagen estableciendo el miembro dwControlFlags de la **imagen de \_ videoimage \_ SAMPLE2 de WMT** en el \_ \_ \_ fotograma de entrada del ejemplo de imagen de videoimage \_ . Al pasar un fotograma de entrada al códec, esa imagen se convierte en la imagen actual. La imagen que era la imagen actual en el ejemplo anterior se convierte normalmente en la imagen anterior y se descarta la imagen que era la imagen anterior en el ejemplo anterior. Puede configurar el códec para conservar la imagen anterior antigua estableciendo el miembro **bKeepPrevImage** en **true**. En ese caso, se descarta la imagen que era la imagen actual en el ejemplo anterior.

La composición básica de un fotograma de imagen de vídeo viene determinada por dos factores para cada imagen: región de interés y coeficiente de mezcla. La región de interés para una imagen se define mediante un punto de origen, ancho y alto. La parte de una imagen que se describe en la región de interés rellena el fotograma de salida. Si el tamaño de la región de interés es distinto al del fotograma de salida, el códec lo cambia de tamaño. El coeficiente de fusión de la imagen determina la combinación de las dos imágenes. Los coeficientes de combinación de las imágenes actual y anterior deben ser totales de 1,0. Por ejemplo, si **fCurrBlendCoef** se establece en 0,5 y **fPrevBlendCoef** se establece en 0,5, el fotograma de salida se compone de una combinación igual de las regiones de interés de ambas imágenes.

Mediante la manipulación de la región de interés de una imagen, puede crear efectos de panorámica y zoom. Los coeficientes de Blend permiten el fundido cruzado (disolución) entre las imágenes. Además de estos efectos, puede usar una de las transiciones predefinidas para crear fotogramas más complejos. Las transiciones disponibles se describen en la sección [transiciones de imagen de vídeo](video-image-transitions.md) de esta documentación. Cuando se usa una transición, se debe configurar cada fotograma. La forma más fácil de hacerlo es crear una función que cambie incrementalmente los miembros de la estructura **de \_ \_ SAMPLE2 de imágenes WMT** para obtener un efecto completo.

Para obtener más información sobre los valores que se deben establecer para las desformaciones, vea [**WMT \_ videoimage \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2).

**Nota:** Si desea incluir audio en un archivo con una secuencia de imágenes de vídeo, debe usar la entrada de audio sin comprimir. Para combinar una secuencia de imágenes de vídeo con una secuencia de audio comprimida existente, debe descomprimir el audio y pasar los ejemplos sin comprimir. Si pasa muestras comprimidas al escritor cuando escribe una secuencia de imagen de vídeo, se producirá un error, lo que hará que se quiten los ejemplos del vídeo.

Además, los archivos de imagen de vídeo comprimidos sin secuencias de audio pueden contener varios fotogramas de vídeo muy pequeños y muy comprimidos en un único paquete ASF, lo que puede dar lugar a una mala experiencia de reproducción en versiones anteriores de Windows Media Player. Para evitar este problema, la mejor solución consiste en insertar una secuencia de audio silenciosa en el archivo, aunque también aumentará el tamaño del archivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Imagen de vídeo**](video-image.md)
</dt> <dt>

[**Escribir archivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




