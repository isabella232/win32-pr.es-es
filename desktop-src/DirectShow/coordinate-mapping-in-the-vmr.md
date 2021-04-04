---
description: Asignación de coordenadas en VMR
ms.assetid: f0821b90-51d1-4e77-8aed-04337a3dd623
title: Asignación de coordenadas en VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c18b38249471e6e68e36f1b9051f51e920f62b31
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906462"
---
# <a name="coordinate-mapping-in-the-vmr"></a>Asignación de coordenadas en VMR

En esta sección se describen las cinco transformaciones que se aplican a una imagen de origen antes de que la VMR la asigne a la imagen de salida final.

1.  La transformación *T (src)* asigna el rectángulo de origen al rectángulo de destino. Se especifican mediante los miembros **rcSource** y **rcTarget** de la estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) o [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) en el tipo de medio. Esta asignación preprocesa la imagen de origen a medida que se pasa a la VMR.
2.  La transformación *T (marca)* realiza las manipulaciones de imagen especificadas por marcas en el ejemplo multimedia. Estas transformaciones incluyen, por ejemplo, la traslación vertical y la escala para dar cabida a las marcas de entrelazado Bob. La transformación entrelazada duplica el alto de la imagen y posiblemente traduce la imagen en la mitad de una línea de vídeo si está en el campo impar.
3.  La transformación *T (ar)* ajusta la imagen a píxeles cuadrados, en función de la relación de aspecto de la imagen. En el caso de los tipos de medios **VIDEOINFOHEADER** , la relación de aspecto viene determinada por el tamaño de la imagen. En el caso de los tipos **VIDEOINFOHEADER2** , la relación de aspecto viene determinada por los campos **dwPictAspectRatioX** y **dwPictAspectRatioY** , a menos que \_ se establezca el panel AMCONTROL \_ en \_ 16x9 o el \_ Panel AMCONTROL \_ en \_ marcas 4x3. Esta transformación supone que la configuración de pantalla del monitor coincide con la relación de aspecto física del monitor. Por ejemplo, si el usuario tiene un monitor con una relación de aspecto de 4 x 3, pero establece la presentación en 1280 x 768 píxeles (5 x 3), la imagen no tendrá la relación de aspecto correcta.
4.  Las transformaciones *T (Mix)* de transformación sitúan la imagen dentro de la imagen de destino, utilizando los rectángulos normalizados especificados en los métodos [**IVMRMixerControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) . Los rectángulos normalizados permiten que la aplicación organice el modo en que los flujos de origen se colocan y escalan entre sí. VMR calcula la imagen de destino al calcular las dimensiones máximas de todas las imágenes de origen y centrar cada una dentro de un rectángulo delimitador global. A las esquinas del rectángulo delimitador se les asigna el intervalo (0,0) a (1,1). El rectángulo delimitador se fija antes de que se ejecute el gráfico y permanece constante incluso si se agregan o eliminan secuencias. Los rectángulos de destino para cada flujo pueden estar fuera del intervalo (0,0) a (1,1) y seguir siendo válidos.
5.  Por último, una parte de la imagen mixta se puede transformar mediante la asignación *T (DST)*, especificada por los rectángulos de origen y de destino en la interfaz [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) de VMR. Si se reemplaza el Allocator-Presenter y no se utiliza la interfaz **IBasicVideo** , la aplicación debe implementar la interfaz [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) y volver a asignar las coordenadas a un espacio lineal 2D. Las coordenadas del mouse que se devuelven al navegador de DVD también deben estar en este espacio. Por ejemplo, si una aplicación representa el vídeo en un cubo giratorio, notificaría toda la presentación del control sin ventana y devolverá las coordenadas del mouse con respecto a la pantalla.

La transformación de imagen general de los datos de origen al representador final es:

T = T (src) t (marca) t (ar) t (Mix) t ( \* \* horario de verano)\*

donde \* indica que la imagen se podría recortar en la imagen de destino en esa fase. Tenga en cuenta que se trata de todas las transformaciones afines, por lo que la VMR puede combinarlas en una única transformación.

El inverso de la transformación es:

![transformación inversa](images/vmrmapping-t-1.png)

El factor T (src) T (marca) t (ar) es relativo a la resolución del origen. En el factor T (Mix), el rectángulo de origen normalizado es relativo a la imagen con corrección de aspecto. El rectángulo de destino normalizado es relativo a la resolución de salida. En el diagrama siguiente se muestran estas relaciones.

![pasos de la transformación de imagen](images/vmrmapping-transform-steps.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar la VMR para desarrolladores de filtros de DirectShow](using-the-vmr-for-directshow-filter-developers.md)
</dt> </dl>

 

 



