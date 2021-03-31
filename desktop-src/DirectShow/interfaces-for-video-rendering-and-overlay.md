---
description: Interfaces para la representación y superposición de vídeo
ms.assetid: e4d4e456-61fb-492b-b817-30629681e270
title: Interfaces para la representación y superposición de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cfa8a94765671e38c48418d37b929215e84b2fe
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806476"
---
# <a name="interfaces-for-video-rendering-and-overlay"></a>Interfaces para la representación y superposición de vídeo

Estas interfaces admiten el control de aplicaciones a través de la representación de vídeo. Tenga en cuenta que algunas de estas interfaces ahora están en desuso, ya que el filtro de representador de combinación de vídeo proporciona un control superior de representación y superposición.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Interfaz</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder</strong></a></td>
<td>Proporciona acceso a la información y a la configuración de los subtítulos.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamoverlayfx"><strong>IAMOverlayFX</strong></a></td>
<td>Aplique efectos superpuestos a la superficie de vídeo. (En desuso).</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties"><strong>IAMVideoDecimationProperties</strong></a></td>
<td>Controle el modo en que DirectShow escala una imagen de vídeo si la ventana de vídeo es más pequeña que el tamaño nativo del vídeo. (En desuso).</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Control/nn-control-ibasicvideo2"><strong>IBasicVideo2</strong></a></td>
<td>Establecer propiedades de vídeo.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>IDDrawExclModeVideo</strong></a></td>
<td>Representar vídeo en el modo de pantalla completa de Microsoft DirectDraw exclusivo. (En desuso).</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideocallback"><strong>IDDrawExclModeVideoCallback</strong></a></td>
<td>Interfaz de devolución de llamada para recibir notificaciones sobre los cambios en la posición, el tamaño y la visibilidad de la superposición. (En desuso).</td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-idirectdrawvideo"><strong>IDirectDrawVideo</strong></a></td>
<td>Deshabilitar las funcionalidades de DirectDraw especificadas. (En desuso).</td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/Amstream/nn-amstream-idirectdrawmediasample"><strong>IDirectDrawMediaSample</strong></a></td>
<td>Acceder a una superficie de DirectDraw asignada por el filtro de <a href="overlay-mixer-filter.md">mezclador de superposición</a> . (Desusado).</td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/Mixerocx/nn-mixerocx-imixerocx"><strong>IMixerOCX</strong></a></td>
<td>Implementado en el mezclador de superposición. Permite a los clientes sin ventanas, como los controles de® ActiveX, obtener y establecer las propiedades del rectángulo de vídeo y avisar al filtro de eventos.</td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/mixerocx/nn-mixerocx-imixerocxnotify"><strong>IMixerOCXNotify</strong></a></td>
<td>Implementado por clientes sin ventanas y llamado por el mezclador de superposición para enviar notificaciones de eventos que afectan al rectángulo de presentación de vídeo.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2"><strong>IMixerPinConfig2</strong></a></td>
<td>Establecer controles de color de vídeo en el filtro de mezclador de superposición al mezclar varias secuencias de vídeo. (En desuso).</td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a></td>
<td>Consulte un representador de vídeo para obtener información sobre el rendimiento.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Control/nn-control-ivideowindow"><strong>IVideoWindow</strong></a></td>
<td>Establecer propiedades de la ventana de vídeo.</td>
</tr>
<tr class="even">
<td><ul>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmraspectratiocontrol9"><strong>IVMRAspectRatioControl9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9"><strong>IVMRDeinterlaceControl9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9"><strong>IVMRFilterConfig9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagecompositor9"><strong>IVMRImageCompositor9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9"><strong>IVMRImagePresenter9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenterconfig9"><strong>IVMRImagePresenterConfig9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9"><strong>IVMRMixerBitmap9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9"><strong>IVMRMixerControl9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmonitorconfig9"><strong>IVMRMonitorConfig9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurface9"><strong>IVMRSurface9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9"><strong>IVMRSurfaceAllocator9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9"><strong>IVMRSurfaceAllocatorEx9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9"><strong>IVMRSurfaceAllocatorNotify9</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9"><strong>IVMRWindowlessControl9</strong></a></li>
</ul></td>
<td>Vídeo que mezcla el representador 9 interfaces.</td>
</tr>
<tr class="odd">
<td><ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmraspectratiocontrol"><strong>IVMRAspectRatioControl</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol"><strong>IVMRDeinterlaceControl</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig"><strong>IVMRFilterConfig</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagecompositor"><strong>IVMRImageCompositor</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter"><strong>IVMRImagePresenter</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenterconfig"><strong>IVMRImagePresenterConfig</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap"><strong>IVMRMixerBitmap</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol"><strong>IVMRMixerControl</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator"><strong>IVMRSurfaceAllocator</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify"><strong>IVMRSurfaceAllocatorNotify</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol"><strong>IVMRWindowlessControl</strong></a></li>
</ul></td>
<td>Vídeo en el que se combinan las interfaces del representador 7.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar el representador de mezcla de vídeo](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 



