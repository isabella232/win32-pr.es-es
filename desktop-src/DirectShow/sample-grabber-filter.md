---
description: El filtro Sample Grabber proporciona una manera de recuperar muestras a medida que pasan por el gráfico de filtros.
ms.assetid: 3c2fb52f-2b44-449a-ae96-3cf35a0a401d
title: Sample Grabber Filter (Qedit.h)
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
ms.openlocfilehash: 286348ec102a93697aa413ecfd1886879e7361b54eca48276b5e868be78eee03
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633515"
---
# <a name="sample-grabber-filter"></a>Filtro de captura de ejemplo

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El filtro Sample Grabber proporciona una manera de recuperar muestras a medida que pasan por el gráfico de filtros. Es un filtro de transformación con un pin de entrada y un pin de salida. Pasa todos los ejemplos de nivel inferior sin modificar, por lo que puede insertarlo en un gráfico de filtro sin modificar el flujo de datos. A continuación, la aplicación puede recuperar ejemplos individuales del filtro llamando a métodos en la [**interfaz ISampleGrabber.**](isamplegrabber.md)

Si desea recuperar ejemplos sin representar los datos, conecte el filtro Sample Grabber al [**filtro Representador**](null-renderer-filter.md) null.



| Etiqueta | Valor |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **ISampleGrabber**](isamplegrabber.md)                                                                       |
| Tipos de medios de pin de entrada                    | Cualquier tipo de medio.                                                                                                                                    |
| Interfaces de pin de entrada                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Tipos de medios de pin de salida                   | Cualquier tipo de medio. Coincide con el tipo de medio de entrada.                                                                                                          |
| Interfaces de pin de salida                    | [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Filtrar CLSID                             | CLSID \_ SampleGrabber                                                                                                                               |
| CLSID de la página de propiedades                      | No hay ninguna página de propiedades.                                                                                                                                  |
| Executable                               | Qedit.dll                                                                                                                                          |
| [Mérito](merit.md)                       | NO USE EL VALOR DE NO \_ \_ \_ USE.                                                                                                                                |
| [Categoría de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                      |



 

## <a name="remarks"></a>Comentarios

Para usar este filtro, agrégolo al gráfico de filtros y llame a [**ISampleGrabber::SetMediaType**](isamplegrabber-setmediatype.md) con el tipo de medio deseado. Este método especifica el tipo de medio para las conexiones de pin de entrada y salida del filtro. A continuación, conecte el filtro a otros filtros del gráfico.

Si llama a [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md) con el valor **TRUE**, el filtro almacena en búfer cada muestra que recibe antes de pasarlo de nivel inferior. Llame al [**método ISampleGrabber::GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) para recuperar el contenido actual del búfer. Como alternativa, puede llamar a [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md) para que el filtro invoque una función de devolución de llamada cada vez que reciba un ejemplo.

El filtro tiene las siguientes limitaciones para los formatos de vídeo:

-   No admite tipos de vídeo con orientación de arriba abajo **(biHeight negativo).**
-   No admite la estructura de formato [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) (tipo de formato igual a **FORMAT \_ VideoInfo2).**
-   Rechaza cualquier tipo de vídeo en el que el paso de superficie no coincida con el ancho del vídeo.

Como resultado, Sample Grabber no se conectará al representador de mezcla de vídeo (VMR) para algunos tipos de vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Qedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[DirectShow Edición de objetos de servicios](directshow-editing-services-objects.md)
</dt> <dt>

[Uso de Sample Grabber](using-the-sample-grabber.md)
</dt> </dl>

 

 




