---
description: El filtro de enganche de ejemplo proporciona una manera de recuperar ejemplos a medida que pasan por el gráfico de filtro.
ms.assetid: 3c2fb52f-2b44-449a-ae96-3cf35a0a401d
title: Filtro de enganche de ejemplo (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Sample
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 18cedd24b0ddcb8f71373641905228f8252ae4ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679025"
---
# <a name="sample-grabber-filter"></a>Filtro de enganche de ejemplo

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El filtro de enganche de ejemplo proporciona una manera de recuperar ejemplos a medida que pasan por el gráfico de filtro. Es un filtro de transformación con un PIN de entrada y un PIN de salida. Pasa todos los ejemplos de nivel inferior sin cambios, por lo que puede insertarlo en un gráfico de filtro sin modificar el flujo de datos. A continuación, la aplicación puede recuperar muestras individuales del filtro llamando a los métodos de la interfaz [**ISampleGrabber**](isamplegrabber.md) .

Si desea recuperar muestras sin representar los datos, conecte el filtro de enganche de ejemplo al filtro de [**representador nulo**](null-renderer-filter.md) .



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **ISampleGrabber**](isamplegrabber.md)                                                                       |
| Tipos de medios de anclaje de entrada                    | Cualquier tipo de medio.                                                                                                                                    |
| Interfaces de PIN de entrada                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Tipos de medios de anclaje de salida                   | Cualquier tipo de medio. Coincide con el tipo de medio de entrada.                                                                                                          |
| Interfaces de clavija de salida                    | [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Identificador CLSID                             | CLSID \_ SampleGrabber                                                                                                                               |
| CLSID de la página de propiedades                      | Ninguna página de propiedades.                                                                                                                                  |
| Executable                               | Qedit.dll                                                                                                                                          |
| [Fundament](merit.md)                       | MÉRITO \_ \_ no se \_ usa                                                                                                                                |
| [Categoría de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                      |



 

## <a name="remarks"></a>Observaciones

Para usar este filtro, agréguelo al gráfico de filtro y llame a [**ISampleGrabber:: SetMediaType**](isamplegrabber-setmediatype.md) con el tipo de medio deseado. Este método especifica el tipo de medio para las conexiones de la clavija de entrada y salida del filtro. A continuación, conecte el filtro a otros filtros del gráfico.

Si llama a [**ISampleGrabber:: SetBufferSamples**](isamplegrabber-setbuffersamples.md) con el valor **true**, el filtro almacena en búfer cada ejemplo que recibe antes de pasarlo a nivel inferior. Llame al método [**ISampleGrabber:: GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) para recuperar el contenido actual del búfer. Como alternativa, puede llamar a [**ISampleGrabber:: SetCallback**](isamplegrabber-setcallback.md) para que el filtro invoque una función de devolución de llamada cada vez que reciba un ejemplo.

El filtro tiene las siguientes limitaciones para los formatos de vídeo:

-   No admite los tipos de vídeo con orientación descendente ( **bialtura** negativa).
-   No admite la estructura de formato [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) (el tipo de formato es igual al **formato \_ VideoInfo2**).
-   Rechaza cualquier tipo de vídeo en el que el intervalo de la superficie no coincida con el ancho del vídeo.

Como resultado, el enganche de ejemplo no se conectará al representador de mezcla de vídeo (VMR) para algunos tipos de vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>QEDIT. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos de servicios de edición de DirectShow](directshow-editing-services-objects.md)
</dt> <dt>

[Usar el enganche de ejemplo](using-the-sample-grabber.md)
</dt> </dl>

 

 




