---
description: La clase CBaseControlVideo implementa la interfaz IBasicVideo y controla las propiedades de vídeo de una ventana de vídeo genérica. Por lo general, un objeto CBaseControlVideo es un representador de vídeo que dibuja vídeo en una ventana de la pantalla.
ms.assetid: 16fc1b0a-e5b5-4f33-ac2b-5acff61bab81
title: Clase CBaseControlVideo
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
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495412"
---
# <a name="cbasecontrolvideo-class"></a>Clase CBaseControlVideo

![jerarquía de clases cbasecontrolvideo](images/wctrl02.png)

La clase **CBaseControlVideo** implementa la interfaz [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) y controla las propiedades de vídeo de una ventana de vídeo genérica. Por lo general, un objeto **CBaseControlVideo** es un representador de vídeo que dibuja vídeo en una ventana de la pantalla.

Muchas funciones miembro de **CBaseControlVideo** solo requieren que el representador de vídeo esté conectado a un gráfico de filtro. Si no está conectado, las funciones miembro devolverán **VFW \_ E \_ not \_ Connected**. Las propiedades establecidas en un representador de vídeo se conservan entre las conexiones sucesivas y las desconexiones. Todas las aplicaciones deben asegurarse de que restablecen las propiedades del representador antes de iniciar una presentación.

Al trabajar con vídeo, la aplicación puede seleccionar una parte del vídeo que se va a usar. Esta parte es el rectángulo de origen que controla el objeto **CBaseControlVideo** . **CBaseControlVideo** permite que la aplicación establezca y recupere el rectángulo de origen. Todos los rectángulos que usa **CBaseControlVideo** emplean los valores de ancho y alto en lugar de los valores de derecha e inferior. Cuando no se ha establecido ningún rectángulo de origen, las propiedades del rectángulo de origen devuelven el tamaño de vídeo completo y nativo.



| Miembros de datos protegidos                                                                   | Descripción                                                                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| m \_ pFilter                                                                               | Puntero a un filtro multimedia propietario.                                                              |
| m \_ pInterfaceLock                                                                        | Sección crítica definida externamente.                                                            |
| m \_ pPin                                                                                  | Control de los tipos de medios para la conexión.                                                      |
| Funciones de miembro                                                                         | Descripción                                                                                     |
| [**CBaseControlVideo**](cbasecontrolvideo-cbasecontrolvideo.md)                         | Construye un objeto **CBaseControlVideo** .                                                      |
| [**CopyImage**](cbasecontrolvideo-copyimage.md)                                         | Crea una copia de la memoria de una imagen de vídeo.                                                         |
| [**GetImageSize**](cbasecontrolvideo-getimagesize.md)                                   | Recupera información de tamaño de imagen de vídeo.                                                         |
| [**SetControlVideoPin**](cbasecontrolvideo-setcontrolvideopin.md)                       | Establece el pin con el que debe sincronizarse este objeto.                                         |
| Funciones miembro reemplazables                                                             | Descripción                                                                                     |
| [**CheckSourceRect**](cbasecontrolvideo-checksourcerect.md)                             | Determina si un rectángulo de origen es válido.                                                      |
| [**CheckTargetRect**](cbasecontrolvideo-checktargetrect.md)                             | Determina si un rectángulo de destino es válido.                                                      |
| [**GetSourceRect**](cbasecontrolvideo-getsourcerect.md)                                 | Recupera el rectángulo de vídeo de origen actual (virtual puro).                                    |
| [**GetStaticImage**](cbasecontrolvideo-getstaticimage.md)                               | Devuelve la imagen actual en un búfer de memoria (virtual puro).                                    |
| [**GetTargetRect**](cbasecontrolvideo-gettargetrect.md)                                 | Recupera el rectángulo de vídeo de destino actual (virtual puro).                                    |
| [**GetVideoFormat**](cbasecontrolvideo-getvideoformat.md)                               | Recupera la estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) que contiene el formato de vídeo. |
| [**IsDefaultSourceRect**](cbasecontrolvideo-isdefaultsourcerect.md)                     | Determina si el representador usa el rectángulo de origen predeterminado (virtual puro).                |
| [**IsDefaultTargetRect**](cbasecontrolvideo-isdefaulttargetrect.md)                     | Determina si el representador usa el rectángulo de destino predeterminado (virtual puro).                |
| [**OnUpdateRectangles**](cbasecontrolvideo-onupdaterectangles.md)                       | Se le llama cuando cambia el rectángulo de origen o de destino.                                             |
| [**OnVideoSizeChange**](cbasecontrolvideo-onvideosizechange.md)                         | Pasa \_ \_ el tamaño de vídeo EC \_ cambiado a la aplicación.                                             |
| [**SetDefaultSourceRect**](cbasecontrolvideo-setdefaultsourcerect.md)                   | Establece el rectángulo de vídeo de origen predeterminado (virtual puro).                                         |
| [**SetDefaultTargetRect**](cbasecontrolvideo-setdefaulttargetrect.md)                   | Establece el rectángulo de vídeo de destino predeterminado (virtual puro).                                         |
| [**SetSourceRect**](cbasecontrolvideo-setsourcerect.md)                                 | Establece el rectángulo de vídeo de origen actual (virtual puro).                                         |
| [**SetTargetRect**](cbasecontrolvideo-settargetrect.md)                                 | Establece el rectángulo de destino actual (virtual puro).                                               |
| Métodos IBasicVideo                                                                      | Descripción                                                                                     |
| [**obtener \_ AvgTimePerFrame**](cbasecontrolvideo-get-avgtimeperframe.md)                    | Recupera un promedio aproximado de tiempo por fotograma.                                                |
| [**obtener \_ BitErrorRate**](cbasecontrolvideo-get-biterrorrate.md)                          | Recupera una tasa de errores de bits aproximada.                                                        |
| [**obtener \_ velocidad de bits**](cbasecontrolvideo-get-bitrate.md)                                    | Recupera una velocidad de bits aproximada para el vídeo.                                                |
| [**GetCurrentImage**](cbasecontrolvideo-getcurrentimage.md)                             | Recupera una representación de memoria de la imagen actual.                                              |
| [**obtener \_ DestinationHeight**](cbasecontrolvideo-get-destinationheight.md)                | Recupera el alto del rectángulo de destino actual.                                           |
| [**obtener \_ DestinationLeft**](cbasecontrolvideo-get-destinationleft.md)                    | Recupera la coordenada izquierda del rectángulo de destino actual.                                  |
| [**GetDestinationPosition**](cbasecontrolvideo-getdestinationposition.md)               | Recupera la posición de destino actual.                                                     |
| [**obtener \_ DestinationTop**](cbasecontrolvideo-get-destinationtop.md)                      | Recupera la coordenada superior del rectángulo de destino actual.                                   |
| [**obtener \_ DestinationWidth**](cbasecontrolvideo-get-destinationwidth.md)                  | Recupera el ancho del rectángulo de destino actual.                                            |
| [**obtener \_ SourceHeight**](cbasecontrolvideo-get-sourceheight.md)                          | Recupera el alto del rectángulo de origen actual.                                                |
| [**obtener \_ SourceLeft**](cbasecontrolvideo-get-sourceleft.md)                              | Recupera la coordenada izquierda del rectángulo de origen actual.                                       |
| [**GetSourcePosition**](cbasecontrolvideo-getsourceposition.md)                         | Recupera la posición de origen actual.                                                          |
| [**obtener \_ SourceTop**](cbasecontrolvideo-get-sourcetop.md)                                | Recupera la coordenada superior del rectángulo de origen actual.                                        |
| [**obtener \_ SourceWidth**](cbasecontrolvideo-get-sourcewidth.md)                            | Recupera el ancho del rectángulo de origen actual.                                                 |
| [**obtención de un \_ Videoalto**](cbasecontrolvideo-get-videoheight.md)                            | Recupera el alto de vídeo nativo.                                                              |
| [**GetVideoPaletteEntries**](cbasecontrolvideo-getvideopaletteentries.md)               | Recupera un intervalo de entradas de la paleta del vídeo.                                             |
| [**GetVideoSize**](cbasecontrolvideo-getvideosize.md)                                   | Recupera el ancho y el alto del vídeo nativo.                                             |
| [**obtener el \_ ancho de Videobyte**](cbasecontrolvideo-get-videowidth.md)                              | Recupera el ancho de vídeo nativo.                                                               |
| [**IsUsingDefaultDestination**](cbasecontrolvideo-isusingdefaultdestination.md)         | Determina si el representador está utilizando la ventana de destino predeterminada.                             |
| [**IsUsingDefaultSource**](cbasecontrolvideo-isusingdefaultsource.md)                   | Determina si el representador está utilizando la ventana de código fuente predeterminada.                                  |
| [**Put \_ DestinationHeight**](cbasecontrolvideo-put-destinationheight.md)                | Establece el alto del rectángulo de destino.                                                        |
| [**Put \_ DestinationLeft**](cbasecontrolvideo-put-destinationleft.md)                    | Establece la coordenada izquierda del rectángulo de destino.                                               |
| [**Put \_ DestinationTop**](cbasecontrolvideo-put-destinationtop.md)                      | Establece la coordenada superior del rectángulo de destino.                                                |
| [**Put \_ DestinationWidth**](cbasecontrolvideo-put-destinationwidth.md)                  | Establece el ancho del rectángulo de destino.                                                         |
| [**Put \_ SourceHeight**](cbasecontrolvideo-put-sourceheight.md)                          | Establece el alto del rectángulo de origen.                                                             |
| [**Put \_ SourceLeft**](cbasecontrolvideo-put-sourceleft.md)                              | Establece la coordenada izquierda del rectángulo de origen.                                                    |
| [**Put \_ SourceTop**](cbasecontrolvideo-put-sourcetop.md)                                | Establece la coordenada superior del rectángulo de origen.                                                     |
| [**Put \_ SourceWidth**](cbasecontrolvideo-put-sourcewidth.md)                            | Establece el ancho del rectángulo de origen.                                                              |
| [**SetDefaultDestinationPosition**](cbasecontrolvideo-setdefaultdestinationposition.md) | Vuelve a establecer la posición de destino predeterminada.                                                    |
| [**SetDefaultSourcePosition**](cbasecontrolvideo-setdefaultsourceposition.md)           | Vuelve a establecer la posición de origen predeterminada.                                                         |
| [**SetDestinationPosition**](cbasecontrolvideo-setdestinationposition.md)               | Establece la posición del rectángulo de destino.                                                        |
| [**SetSourcePosition**](cbasecontrolvideo-setsourceposition.md)                         | Establece la posición del rectángulo de origen.                                                             |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases base de DirectShow](directshow-base-classes.md)
</dt> </dl>

 

 



