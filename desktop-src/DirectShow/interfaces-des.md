---
description: Interfaces para servicios de edición de DirectShow
ms.assetid: e7fdb387-83b3-4fa2-9608-2f5dc95975bf
title: Interfaces para servicios de edición de DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dba286a340693407287ed370ed401ac6b039593c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806482"
---
# <a name="interfaces-for-directshow-editing-services"></a>Interfaces para servicios de edición de DirectShow

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

Esta sección contiene temas de referencia para las interfaces de [servicios de edición de DirectShow](directshow-editing-services.md) (des).



| Interfaz                                                  | Descripción                                                                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**IAMErrorLog**](iamerrorlog.md)                         | Proporciona un método de devolución de llamada para el registro de errores.                                                                                  |
| [**IAMSetErrorLog**](iamseterrorlog.md)                   | Establece o recupera un registro de errores.                                                                                                |
| [**IAMTimeline**](iamtimeline.md)                         | Proporciona métodos para manipular la escala de tiempo.                                                                                |
| [**IAMTimelineComp**](iamtimelinecomp.md)                 | Inserta o recupera pistas virtuales en una composición.                                                                          |
| [**IAMTimelineEffect**](iamtimelineeffect.md)             | Proporciona métodos para manipular los efectos de la escala de tiempo.                                                                            |
| [**IAMTimelineEffectable**](iamtimelineeffectable.md)     | Proporciona métodos para agregar efectos a un objeto Timeline.                                                                      |
| [**IAMTimelineGroup**](iamtimelinegroup.md)               | Establece y recupera propiedades en grupos.                                                                                       |
| [**IAMTimelineObj**](iamtimelineobj.md)                   | Proporciona métodos para manipular objetos Timeline.                                                                            |
| [**IAMTimelineSplittable**](iamtimelinesplittable.md)     | Divide un objeto Timeline.                                                                                                      |
| [**IAMTimelineSrc**](iamtimelinesrc.md)                   | Proporciona métodos para manipular y establecer las propiedades de los objetos de origen.                                                    |
| [**IAMTimelineTrack**](iamtimelinetrack.md)               | Proporciona métodos para manipular objetos de seguimiento.                                                                               |
| [**IAMTimelineTrans**](iamtimelinetrans.md)               | Proporciona métodos para manipular objetos de transición.                                                                          |
| [**IAMTimelineTransable**](iamtimelinetransable.md)       | Agrega transiciones a un objeto.                                                                                                 |
| [**IAMTimelineVirtualTrack**](iamtimelinevirtualtrack.md) | Proporciona métodos para trabajar con pistas virtuales.                                                                              |
| [**IDxtAlphaSetter**](idxtalphasetter.md)                 | Establece propiedades en el efecto del [establecedor alfa](alpha-setter-effect.md) .                                                         |
| [**IDxtCompositor**](idxtcompositor.md)                   | Establece las propiedades de la transición del [compositor](compositor-transition.md) .                                                     |
| [**IDxtJpeg**](idxtjpeg.md)                               | Establece las propiedades de la transición de [borrado de SMPTE](smpte-wipe-transition.md) .                                                     |
| [**IDxtKey**](idxtkey.md)                                 | Establece las propiedades de la transición de la [clave](key-transition.md) .                                                                   |
| [**IFindCompressorCB**](ifindcompressorcb.md)             | No se admite.                                                                                                                 |
| [**IGrfCache**](igrfcache.md)                             | No se admite.                                                                                                                 |
| [**IMediaDet**](imediadet.md)                             | Recupera información sobre un archivo multimedia, como el número de flujos y el tipo, la duración y la velocidad de fotogramas de cada flujo. |
| [**IMediaLocator**](imedialocator.md)                     | Proporciona métodos para validar nombres de archivo.                                                                                    |
| [**IPropertySetter**](ipropertysetter.md)                 | Establece las propiedades de un efecto o una transición.                                                                                    |
| [**IRenderEngine**](irenderengine.md)                     | Representa un proyecto DES mediante la creación de un gráfico de filtro a partir de una escala de tiempo.                                                          |
| [**IRenderEngine2**](irenderengine2.md)                   | Permite que la aplicación Reemplace el filtro de cambio de tamaño de vídeo predeterminado que usa DES.                                              |
| [**IResize**](iresize.md)                                 | Debe ser compatible con cualquier filtro de tamaño de vídeo personalizado.                                                                          |
| [**ISampleGrabber**](isamplegrabber.md)                   | Recupera ejemplos de medios individuales a medida que se mueven por el gráfico de filtro.                                                      |
| [**ISampleGrabberCB**](isamplegrabbercb.md)               | Interfaz de devolución de llamada para la interfaz [**ISampleGrabber**](isamplegrabber.md) .                                                 |
| [**ISmartRenderEngine**](ismartrenderengine.md)           | Proporciona métodos que admiten la recompresión inteligente.                                                                             |
| [**IXml2Dex**](ixml2dex.md)                               | Guarda y carga archivos del proyecto DES en lenguaje de marcado extensible (XML).                                                         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de C++ de los servicios de edición de DirectShow](directshow-editing-services-c---reference.md)
</dt> </dl>

 

 



