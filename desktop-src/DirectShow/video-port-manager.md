---
description: Administrador de puertos de vídeo
ms.assetid: d70558a5-9820-432a-b4f3-ccf7bb2a34d5
title: Administrador de puertos de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7ca884ff009584ef2904387d872733ddf8d53dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911054"
---
# <a name="video-port-manager"></a>Administrador de puertos de vídeo

El filtro del administrador de puertos de vídeo (VPM) permite que el filtro de representador de combinación de vídeo 7 (VMR-7) funcione con dispositivos de captura de vídeo o descodificadores de hardware que usan un puerto de vídeo. Un puerto de vídeo es una conexión de hardware directa con el chip de gráficos. Permite que el vídeo se transfiera directamente al chip de gráficos sin pasar por el bus del sistema.

> [!Note]  
> El administrador de puertos de vídeo no es compatible con VMR-9, ya que VMR-9 no admite puertos de vídeo.

 



|                                          |                                                                                                                                                                                                                      |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IAMVideoDecimationProperties**](/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IKsPropertySet**](ikspropertyset.md), [**IQualProp**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop), [**IVPManager**](/windows/desktop/api/Strmif/nn-strmif-ivpmanager) |
| Tipos de medios de anclaje de entrada                    | MEDIATYPE \_ video, MEDIASUBTYPE \_ VPVIDEO o MEDIASUBTYPE \_ VPVBI, format \_ None                                                                                                                                         |
| Interfaces de PIN de entrada                     | [**IKsPin**](ikspin.md), [**IKsPropertySet**](ikspropertyset.md), [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Tipos de medios de anclaje de salida                   | \_Vídeo de MEDIATYPE, formato \_ VideoInfo2                                                                                                                                                                                 |
| Interfaces de clavija de salida                    | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                                     |
| Identificador CLSID                             | CLSID \_ VideoPortManager                                                                                                                                                                                              |
| [Fundament](merit.md)                       | MÉRITO \_ normal                                                                                                                                                                                                        |
| [Categoría de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                                        |



 

## <a name="remarks"></a>Observaciones

El administrador de puertos de vídeo combina la funcionalidad de puerto de vídeo del [filtro de mezclador de superposición](overlay-mixer-filter.md) y la funcionalidad del [asignador de superficie de VBI](vbi-surface-allocator.md). VPM asigna puertos y superficies de vídeo y sincroniza la captura de datos desde el puerto de vídeo. Permite la captura basada en el puerto de vídeo que es independiente de la representación. Si desea obtener una vista previa, el VPM se coordina con el VMR-7 para mostrar los datos del puerto de vídeo capturado. Cuando un puerto de vídeo está presente en el sistema, el filtro de captura requiere búferes adicionales para extraer datos de VBI del flujo de vídeo. Estos búferes son proporcionados por VPM. Una vez que el filtro de captura ha extraído los datos de VBI, los entrega en un PIN independiente a los filtros como el descodificador de CC. En la ilustración siguiente se muestra el VPM y sus conexiones en un gráfico de filtro.

![segmento del gráfico de filtro del administrador de puertos de vídeo](images/vpm.png)

El generador de gráficos de DVD agrega el VPM al gráfico de filtros automáticamente cuando se detecta un puerto de vídeo en el sistema. Una vez agregado al gráfico, VPM usa un objeto DirectDraw proporcionado por el representador de mezcla de vídeo para asignar dos o tres superficies. Estas superficies reciben los fotogramas digitalizados del filtro de captura ascendente. En respuesta a las notificaciones de eventos de modo de usuario que se envían cuando los datos están presentes en la superficie, el VPM realiza una operación de ajuste automático en una superficie fuera de la vista proporcionada por VMR.

El hecho de que VPM use varias superficies para sus búferes de entrada significa que requiere más de VRAM que la implementación anterior del puerto de vídeo de DirectShow. La blit adicional desde VPM a VMR-7 requiere más ancho de banda de memoria de vídeo. Además, puesto que el volteo automático de hardware no se usa más, existe un potencial teórico para los fotogramas descartados, pero la evidencia empírica sugiere que esto no se produce.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> <dt>

[**Interfaz IVPManager**](/windows/desktop/api/Strmif/nn-strmif-ivpmanager)
</dt> </dl>

 

 



