---
description: La clase CBaseControlVideo implementa la interfaz IBasicVideo y controla las propiedades de vídeo de una ventana de vídeo genérica. Por lo general, un objeto CBaseControlVideo es un representador de vídeo que dibuja vídeo en una ventana de la pantalla.
ms.assetid: 16fc1b0a-e5b5-4f33-ac2b-5acff61bab81
title: CBaseControlVideo (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo
api_type:
- COM
api_location: ''
ms.openlocfilehash: e2e5962eb9d175bfbbeadd149a547f0d36fbf49f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063367"
---
# <a name="cbasecontrolvideo-class"></a>CBaseControlVideo (clase)

![Jerarquía de clases cbasecontrolvideo](images/wctrl02.png)

La **clase CBaseControlVideo** implementa la [**interfaz IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) y controla las propiedades de vídeo de una ventana de vídeo genérica. Por lo general, **un objeto CBaseControlVideo** es un representador de vídeo que dibuja vídeo en una ventana de la pantalla.

Muchas **funciones miembro CBaseControlVideo** solo requieren que el representador de vídeo esté conectado a un gráfico de filtros. Si no está conectado, las funciones miembro **devolverán VFW \_ E NOT \_ \_ CONNECTED**. Las propiedades establecidas en un representador de vídeo persisten entre conexiones sucesivas y desconexiones. Todas las aplicaciones deben asegurarse de que restablecen las propiedades del representador antes de iniciar una presentación.

Al trabajar con vídeo, la aplicación puede seleccionar una parte del vídeo que se usará. Esta parte es el rectángulo de origen que controla el objeto **CBaseControlVideo.** **CBaseControlVideo permite** a la aplicación establecer y recuperar el rectángulo de origen. Todos los rectángulos que **CBaseControlVideo** usa emplean valores de ancho y alto en lugar de los valores derecho e inferior. Cuando no se ha establecido ningún rectángulo de origen, las propiedades del rectángulo de origen devuelven el tamaño de vídeo nativo completo.



| Miembros de datos protegidos                                                                   | Descripción                                                                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| m \_ pFilter                                                                               | Puntero a un filtro de medios propietario.                                                              |
| m \_ pInterfaceLock                                                                        | Sección crítica definida externamente.                                                            |
| m \_ pPin                                                                                  | Control de los tipos de medios para la conexión.                                                      |
| Funciones de miembro                                                                         | Descripción                                                                                     |
| [**CBaseControlVideo**](cbasecontrolvideo-cbasecontrolvideo.md)                         | Construye un **objeto CBaseControlVideo.**                                                      |
| [**CopyImage**](cbasecontrolvideo-copyimage.md)                                         | Crea una copia de memoria de una imagen de vídeo.                                                         |
| [**GetImageSize**](cbasecontrolvideo-getimagesize.md)                                   | Recupera la información de tamaño de la imagen de vídeo.                                                         |
| [**SetControlVideoPin**](cbasecontrolvideo-setcontrolvideopin.md)                       | Establece el pin con el que este objeto debe sincronizarse.                                         |
| Funciones miembro reemplazables                                                             | Descripción                                                                                     |
| [**CheckSourceRect**](cbasecontrolvideo-checksourcerect.md)                             | Determina si un rectángulo de origen es válido.                                                      |
| [**CheckTargetRect**](cbasecontrolvideo-checktargetrect.md)                             | Determina si un rectángulo de destino es válido.                                                      |
| [**GetSourceRect**](cbasecontrolvideo-getsourcerect.md)                                 | Recupera el rectángulo de vídeo de origen actual (virtual puro).                                    |
| [**GetStaticImage**](cbasecontrolvideo-getstaticimage.md)                               | Devuelve la imagen actual en un búfer de memoria (virtual pura).                                    |
| [**GetTargetRect**](cbasecontrolvideo-gettargetrect.md)                                 | Recupera el rectángulo de vídeo de destino actual (virtual puro).                                    |
| [**GetVideoFormat**](cbasecontrolvideo-getvideoformat.md)                               | Recupera la estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) que contiene el formato de vídeo. |
| [**IsDefaultSourceRect**](cbasecontrolvideo-isdefaultsourcerect.md)                     | Determina si el representador usa el rectángulo de origen predeterminado (virtual puro).                |
| [**IsDefaultTargetRect**](cbasecontrolvideo-isdefaulttargetrect.md)                     | Determina si el representador usa el rectángulo de destino predeterminado (virtual puro).                |
| [**OnUpdateRectangles**](cbasecontrolvideo-onupdaterectangles.md)                       | Se llama cuando cambia el rectángulo de origen o de destino.                                             |
| [**OnVideoSizeChange**](cbasecontrolvideo-onvideosizechange.md)                         | Pasa EC \_ VIDEO SIZE CHANGED a la \_ \_ aplicación.                                             |
| [**SetDefaultSourceRect**](cbasecontrolvideo-setdefaultsourcerect.md)                   | Establece el rectángulo de vídeo de origen predeterminado (virtual puro).                                         |
| [**SetDefaultTargetRect**](cbasecontrolvideo-setdefaulttargetrect.md)                   | Establece el rectángulo de vídeo de destino predeterminado (virtual puro).                                         |
| [**SetSourceRect**](cbasecontrolvideo-setsourcerect.md)                                 | Establece el rectángulo de vídeo de origen actual (virtual puro).                                         |
| [**SetTargetRect**](cbasecontrolvideo-settargetrect.md)                                 | Establece el rectángulo de destino actual (virtual puro).                                               |
| Métodos IBasicVideo                                                                      | Descripción                                                                                     |
| [**get \_ AvgTimePerFrame**](cbasecontrolvideo-get-avgtimeperframe.md)                    | Recupera un tiempo promedio aproximado por fotograma.                                                |
| [**get \_ BitErrorRate**](cbasecontrolvideo-get-biterrorrate.md)                          | Recupera una tasa de errores de bits aproximada.                                                        |
| [**get \_ BitRate**](cbasecontrolvideo-get-bitrate.md)                                    | Recupera una velocidad de bits aproximada para el vídeo.                                                |
| [**GetCurrentImage**](cbasecontrolvideo-getcurrentimage.md)                             | Recupera una representación en memoria de la imagen actual.                                              |
| [**get \_ DestinationHeight**](cbasecontrolvideo-get-destinationheight.md)                | Recupera el alto del rectángulo de destino actual.                                           |
| [**get \_ DestinationLeft**](cbasecontrolvideo-get-destinationleft.md)                    | Recupera la coordenada izquierda del rectángulo de destino actual.                                  |
| [**GetDestinationPosition**](cbasecontrolvideo-getdestinationposition.md)               | Recupera la posición de destino actual.                                                     |
| [**get \_ DestinationTop**](cbasecontrolvideo-get-destinationtop.md)                      | Recupera la coordenada superior del rectángulo de destino actual.                                   |
| [**get \_ DestinationWidth**](cbasecontrolvideo-get-destinationwidth.md)                  | Recupera el ancho del rectángulo de destino actual.                                            |
| [**get \_ SourceHeight**](cbasecontrolvideo-get-sourceheight.md)                          | Recupera el alto del rectángulo de origen actual.                                                |
| [**get \_ SourceLeft**](cbasecontrolvideo-get-sourceleft.md)                              | Recupera la coordenada izquierda del rectángulo de origen actual.                                       |
| [**GetSourcePosition**](cbasecontrolvideo-getsourceposition.md)                         | Recupera la posición de origen actual.                                                          |
| [**get \_ SourceTop**](cbasecontrolvideo-get-sourcetop.md)                                | Recupera la coordenada superior del rectángulo de origen actual.                                        |
| [**get \_ SourceWidth**](cbasecontrolvideo-get-sourcewidth.md)                            | Recupera el ancho del rectángulo de origen actual.                                                 |
| [**get \_ VideoHeight**](cbasecontrolvideo-get-videoheight.md)                            | Recupera el alto del vídeo nativo.                                                              |
| [**GetVideoPaletteEntries**](cbasecontrolvideo-getvideopaletteentries.md)               | Recupera un intervalo de entradas de paleta para el vídeo.                                             |
| [**GetVideoSize**](cbasecontrolvideo-getvideosize.md)                                   | Recupera el ancho y alto del vídeo nativo.                                             |
| [**get \_ VideoWidth**](cbasecontrolvideo-get-videowidth.md)                              | Recupera el ancho de vídeo nativo.                                                               |
| [**IsUsingDefaultDestination**](cbasecontrolvideo-isusingdefaultdestination.md)         | Determina si el representador usa la ventana de destino predeterminada.                             |
| [**IsUsingDefaultSource**](cbasecontrolvideo-isusingdefaultsource.md)                   | Determina si el representador usa la ventana de origen predeterminada.                                  |
| [**put \_ DestinationHeight**](cbasecontrolvideo-put-destinationheight.md)                | Establece el alto del rectángulo de destino.                                                        |
| [**put \_ DestinationLeft**](cbasecontrolvideo-put-destinationleft.md)                    | Establece la coordenada izquierda del rectángulo de destino.                                               |
| [**put \_ DestinationTop**](cbasecontrolvideo-put-destinationtop.md)                      | Establece la coordenada superior del rectángulo de destino.                                                |
| [**put \_ DestinationWidth**](cbasecontrolvideo-put-destinationwidth.md)                  | Establece el ancho del rectángulo de destino.                                                         |
| [**put \_ SourceHeight**](cbasecontrolvideo-put-sourceheight.md)                          | Establece el alto del rectángulo de origen.                                                             |
| [**put \_ SourceLeft**](cbasecontrolvideo-put-sourceleft.md)                              | Establece la coordenada izquierda del rectángulo de origen.                                                    |
| [**put \_ SourceTop**](cbasecontrolvideo-put-sourcetop.md)                                | Establece la coordenada superior del rectángulo de origen.                                                     |
| [**put \_ SourceWidth**](cbasecontrolvideo-put-sourcewidth.md)                            | Establece el ancho del rectángulo de origen.                                                              |
| [**SetDefaultDestinationPosition**](cbasecontrolvideo-setdefaultdestinationposition.md) | Establece de nuevo la posición de destino predeterminada.                                                    |
| [**SetDefaultSourcePosition**](cbasecontrolvideo-setdefaultsourceposition.md)           | Establece de nuevo la posición de origen predeterminada.                                                         |
| [**SetDestinationPosition**](cbasecontrolvideo-setdestinationposition.md)               | Establece la posición del rectángulo de destino.                                                        |
| [**SetSourcePosition**](cbasecontrolvideo-setsourceposition.md)                         | Establece la posición del rectángulo de origen.                                                             |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[DirectShow Clases base](directshow-base-classes.md)
</dt> </dl>

 

 



