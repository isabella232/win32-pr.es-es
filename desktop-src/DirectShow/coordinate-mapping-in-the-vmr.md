---
description: Asignación de coordenadas en vmr
ms.assetid: f0821b90-51d1-4e77-8aed-04337a3dd623
title: Asignación de coordenadas en vmr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c18b38249471e6e68e36f1b9051f51e920f62b31
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161559"
---
# <a name="coordinate-mapping-in-the-vmr"></a>Asignación de coordenadas en vmr

En esta sección se describen las cinco transformaciones que se aplican a una imagen de origen antes de que vmr la asigne a la imagen de salida final.

1.  La transformación *T(Src)* asigna el rectángulo de origen al rectángulo de destino. Estos se especifican mediante los miembros **rcSource** y **rcTarget** de la estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) o [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) en el tipo de medio. Esta asignación preprocesa la imagen de origen a medida que pasa a vmr.
2.  La transformación *T(Flag)* realiza cualquier manipulación de imágenes especificada por marcas en el ejemplo de medios. Estas incluyen transformaciones como la traducción vertical y la escala para dar cabida a las marcas de intercalación bob. La transformación entrelaza duplica el alto de la imagen y posiblemente traduce la imagen a la mitad de una línea de vídeo si está en el campo impar.
3.  La transformación *T(AR) ajusta* la imagen a píxeles cuadrados, en función de la relación de aspecto de la imagen. Para **los tipos de medios VIDEOINFOHEADER,** la relación de aspecto viene determinada por el tamaño de la imagen. Para los tipos **VIDEOINFOHEADER2,** la relación de aspecto viene determinada por los campos **dwPictAspectRatioX** y **dwPictAspectRatioY,** a menos que se establezcan las marcas AMCONTROL \_ PAD TO \_ \_ 16x9 o AMCONTROL \_ PAD TO \_ \_ 4x3. En esta transformación se supone que la configuración de visualización del monitor coincide con la relación de aspecto físico del monitor. Por ejemplo, si el usuario tiene un monitor con una relación de aspecto de 4 x 3, pero establece la pantalla en 1280 x 768 píxeles (5 x 3), la imagen no tendrá la relación de aspecto correcta.
4.  La transformación *T(Mix)* transforma la imagen dentro de la imagen de destino, usando los rectángulos normalizados especificados en los métodos [**IVMRMixerControl.**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) Los rectángulos normalizados permiten a la aplicación organizar cómo se posicionan y escalan las secuencias de origen en relación entre sí. VmR calcula la imagen de destino calculando las dimensiones máximas de todas las imágenes de origen y centrando cada una dentro de un rectángulo delimitador general. A las esquinas del rectángulo delimitador se les asigna el intervalo (0,0) a (1,1). El rectángulo delimitador se fija antes de que se ejecute el gráfico y permanece constante incluso si se agregan o eliminan secuencias. Los rectángulos de destino de cada secuencia pueden estar fuera del intervalo (0,0) a (1,1) y seguir siendo válidos.
5.  Por último, una parte de la imagen mixta se puede transformar mediante la asignación *T(Dst),* especificada por los rectángulos de origen y destino de la interfaz [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) en la VMR. Si el Allocator-Presenter se reemplaza y no se usa la interfaz **IBasicVideo,** la aplicación debe implementar la interfaz [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) y asignar las coordenadas de nuevo a un espacio lineal 2D. Las coordenadas del mouse devueltas al navegador de DVD también deben estar en este espacio. Por ejemplo, si una aplicación representa vídeo en un cubo girando, notificaría toda la pantalla para el control sin ventanas y devolvería coordenadas del mouse relativas a la pantalla.

La transformación general de la imagen de los datos de origen al representador final es:

T = T(Src) \* T(Flag)T(Ar)T(Mix) \* T(Dst)\*

donde \* indica que la imagen se podría recortar a la imagen de destino en esa fase. Tenga en cuenta que todas son transformaciones afín, por lo que vmr puede combinarlas en una sola transformación.

El inverso de la transformación es:

![transformación inversa](images/vmrmapping-t-1.png)

El factor T(Src) T(Flag) T(Ar) es relativo a la resolución de origen. En el factor T(Mix), el rectángulo de origen normalizado es relativo a la imagen corregida de aspecto. El rectángulo de destino normalizado es relativo a la resolución de salida. En el diagrama siguiente se muestran estas relaciones.

![pasos de transformación de imágenes](images/vmrmapping-transform-steps.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de VMR para DirectShow de filtros](using-the-vmr-for-directshow-filter-developers.md)
</dt> </dl>

 

 



