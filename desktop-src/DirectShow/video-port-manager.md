---
description: Administrador de puertos de vídeo
ms.assetid: d70558a5-9820-432a-b4f3-ccf7bb2a34d5
title: Administrador de puertos de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fb7a31d21592bd94579ad608fb453e2a2ec0a264d674f807b404a43f2a0bc1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903524"
---
# <a name="video-port-manager"></a>Administrador de puertos de vídeo

El filtro Administrador de puertos de vídeo (VPM) permite que el filtro de representador de mezcla de vídeo 7 (VMR-7) funcione con dispositivos de captura de vídeo o descodificadores de hardware que usan un puerto de vídeo. Un puerto de vídeo es una conexión de hardware directa al chip gráfico. Permite transferir vídeo directamente al chip gráfico sin pasar por el bus del sistema.

> [!Note]  
> El Administrador de puertos de vídeo no es compatible con VMR-9, ya que VMR-9 no admite puertos de vídeo.

 



| Etiqueta | Value |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IAMVideoDecimationProperties,**](/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties) [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IKsPropertySet,**](ikspropertyset.md) [**IQualProp,**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop) [**IVPManager**](/windows/desktop/api/Strmif/nn-strmif-ivpmanager) |
| Tipos de medios de pin de entrada                    | MEDIATYPE \_ Video, MEDIASUBTYPE \_ VPVideo o MEDIASUBTYPE \_ VPVBI, FORMAT \_ None                                                                                                                                         |
| Interfaces de pin de entrada                     | [**IKsPin,**](ikspin.md) [**IKsPropertySet,**](ikspropertyset.md) [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IPinConnection,**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Tipos de medios de pin de salida                   | MEDIATYPE \_ Video, FORMAT \_ VideoInfo2                                                                                                                                                                                 |
| Interfaces de pin de salida                    | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                                     |
| Filtrar CLSID                             | CLSID \_ VideoPortManager                                                                                                                                                                                              |
| [Mérito](merit.md)                       | PROCEDIMIENTO \_ NORMAL                                                                                                                                                                                                        |
| [Categoría de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                                        |



 

## <a name="remarks"></a>Comentarios

El Administrador de puertos de vídeo combina la funcionalidad de puerto de vídeo de [overlay Mixer Filter](overlay-mixer-filter.md) y la funcionalidad del asignador de superficie de [VBI.](vbi-surface-allocator.md) El VPM asigna puertos y superficies de vídeo, y sincroniza la captura de datos desde el puerto de vídeo. Permite la captura basada en puertos de vídeo que es independiente de la representación. Si se desea obtener una vista previa, el VPM se coordina con VMR-7 para mostrar los datos de puerto de vídeo capturados. Cuando hay un puerto de vídeo en el sistema, el filtro de captura requiere búferes adicionales para extraer datos de VBI de la secuencia de vídeo. El VPM proporciona estos búferes. Una vez que el filtro de captura ha extraído los datos de VBI, los entrega en un pin independiente a filtros como el descodificador CC. En la ilustración siguiente se muestra el VPM y sus conexiones en un gráfico de filtro.

![segmento de gráfico de filtro del administrador de puertos de vídeo](images/vpm.png)

Dvd Graph Builder agrega el VPM al gráfico de filtros automáticamente cuando se detecta un puerto de vídeo en el sistema. Una vez agregado al gráfico, el VPM usa un objeto DirectDraw proporcionado por el representador de mezcla de vídeo para asignar dos o tres superficies. Estas superficies reciben los fotogramas digitalizados del filtro de captura ascendente. En respuesta a las notificaciones de eventos en modo de usuario enviadas cuando los datos están presentes en la superficie, el VPM realiza una conmutación automática por error a una superficie fuera de pantalla proporcionada por vmr.

El hecho de que el VPM use varias superficies para sus búferes de entrada significa que requiere más VRAM que la implementación anterior DirectShow puerto de vídeo. El disco adicional de la VPM al VMR-7 requiere ancho de banda de memoria de vídeo adicional. Y como el volteo automático de hardware ya no se usa, existe un potencial teórico de fotogramas descartados, pero la evidencia empírica sugiere que esto no ocurre.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> <dt>

[**IVPManager (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-ivpmanager)
</dt> </dl>

 

 



