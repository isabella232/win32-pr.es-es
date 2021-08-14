---
description: Interfaces para los DirectShow edición de archivos
ms.assetid: e7fdb387-83b3-4fa2-9608-2f5dc95975bf
title: Interfaces para los DirectShow edición de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00e913ec6bf17a11a4b772d288b9404113cd6bdc70bf441ed20dcbc69a086f9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118397596"
---
# <a name="interfaces-for-directshow-editing-services"></a>Interfaces para los DirectShow edición de archivos

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

Esta sección contiene temas de referencia para [las interfaces DirectShow Editing Services](directshow-editing-services.md) (DES).



| Interfaz                                                  | Descripción                                                                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**IAMErrorLog**](iamerrorlog.md)                         | Proporciona un método de devolución de llamada para el registro de errores.                                                                                  |
| [**IAMSetErrorLog**](iamseterrorlog.md)                   | Establece o recupera un registro de errores.                                                                                                |
| [**IAMTimeline**](iamtimeline.md)                         | Proporciona métodos para manipular la escala de tiempo.                                                                                |
| [**IAMTimelineComp**](iamtimelinecomp.md)                 | Inserta o recupera pistas virtuales en una composición.                                                                          |
| [**IAMTimelineEffect**](iamtimelineeffect.md)             | Proporciona métodos para manipular los efectos de la escala de tiempo.                                                                            |
| [**IAMTimelineEffectable**](iamtimelineeffectable.md)     | Proporciona métodos para agregar efectos a un objeto de escala de tiempo.                                                                      |
| [**IAMTimelineGroup**](iamtimelinegroup.md)               | Establece y recupera propiedades en grupos.                                                                                       |
| [**IAMTimelineObj**](iamtimelineobj.md)                   | Proporciona métodos para manipular objetos de escala de tiempo.                                                                            |
| [**IAMTimelineSplittable**](iamtimelinesplittable.md)     | Divide un objeto de escala de tiempo.                                                                                                      |
| [**IAMTimelineSrc**](iamtimelinesrc.md)                   | Proporciona métodos para manipular y establecer propiedades en objetos de origen.                                                    |
| [**IAMTimelineTrack**](iamtimelinetrack.md)               | Proporciona métodos para manipular objetos de seguimiento.                                                                               |
| [**IAMTimelineTrans**](iamtimelinetrans.md)               | Proporciona métodos para manipular objetos de transición.                                                                          |
| [**IAMTimelineTransable**](iamtimelinetransable.md)       | Agrega transiciones a un objeto .                                                                                                 |
| [**IAMTimelineVirtualTrack**](iamtimelinevirtualtrack.md) | Proporciona métodos para trabajar con pistas virtuales.                                                                              |
| [**IDxtAlphaSetter**](idxtalphasetter.md)                 | Establece las propiedades del [efecto Alfa Setter.](alpha-setter-effect.md)                                                         |
| [**IDxtCompositor**](idxtcompositor.md)                   | Establece las propiedades de la [transición compositor.](compositor-transition.md)                                                     |
| [**IDxtXtEg**](idxtjpeg.md)                               | Establece las propiedades de la [transición de borrado de SMPTE.](smpte-wipe-transition.md)                                                     |
| [**IDxtKey**](idxtkey.md)                                 | Establece las propiedades de la [transición de](key-transition.md) clave.                                                                   |
| [**IFindCompressorCB**](ifindcompressorcb.md)             | No compatible.                                                                                                                 |
| [**IGrfCache**](igrfcache.md)                             | No compatible.                                                                                                                 |
| [**IMediaDet**](imediadet.md)                             | Recupera información sobre un archivo multimedia, como el número de secuencias y el tipo, la duración y la velocidad de fotogramas de cada secuencia. |
| [**IMediaLocator**](imedialocator.md)                     | Proporciona métodos para validar nombres de archivo.                                                                                    |
| [**IPropertySetter**](ipropertysetter.md)                 | Establece las propiedades en un efecto o transición.                                                                                    |
| [**IRenderEngine**](irenderengine.md)                     | Representa un proyecto DES mediante la construcción de un gráfico de filtros a partir de una escala de tiempo.                                                          |
| [**IRenderEngine2**](irenderengine2.md)                   | Permite que la aplicación reemplace el filtro de ajuste de tamaño de vídeo predeterminado que usa DES.                                              |
| [**Iresize**](iresize.md)                                 | Debe ser compatible con cualquier filtro de cambio de tamaño de vídeo personalizado.                                                                          |
| [**ISampleGrabber**](isamplegrabber.md)                   | Recupera ejemplos de medios individuales a medida que se mueven por el gráfico de filtro.                                                      |
| [**ISampleGrabberCB**](isamplegrabbercb.md)               | Interfaz de devolución de llamada [**para la interfaz ISampleGrabber.**](isamplegrabber.md)                                                 |
| [**ISmartRenderEngine**](ismartrenderengine.md)           | Proporciona métodos que admiten la recompresión inteligente.                                                                             |
| [**IXml2Dex**](ixml2dex.md)                               | Guarda y carga archivos de proyecto DES en lenguaje de marcado extensible (XML).                                                         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Referencia de C++ de Servicios de edición](directshow-editing-services-c---reference.md)
</dt> </dl>

 

 



