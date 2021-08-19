---
description: Suministro de un Allocator-Presenter personalizado para VMR-9
ms.assetid: 61bb6b0d-25b5-481b-a241-74c6e421f109
title: Suministro de un Allocator-Presenter personalizado para VMR-9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21e5f87aaecf0b2e8576b60a2d0f6a8c74e60fcf0759a123015ded9136c079bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951724"
---
# <a name="supplying-a-custom-allocator-presenter-for-vmr-9"></a>Suministro de un Allocator-Presenter personalizado para VMR-9

Para usar un asignador-presentador personalizado con el filtro Representador de mezcla de vídeo 9 (VMR-9), realice los pasos siguientes:

1.  Implemente una clase que admita las interfaces [**IVMRSurfaceAllocator9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9) [**e IVMRImagePresenter9.**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9)
2.  Llame **a QueryInterface** en el filtro VMR-9 para la [**interfaz IVMRFilterConfig9.**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9)
3.  Llame al [**método IVMRFilterConfig9::SetRenderingMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) y pase la **marca VMR9Mode \_ Renderless.**
4.  **QueryInterface** en el filtro VMR-9 para la [**interfaz IVMRSurfaceAllocatorNotify9.**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9)
5.  Llame al [**método IVMRSurfaceAllocatorNotify9::AdviseSurfaceAllocator**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-advisesurfaceallocator) y pase un puntero al método [**IVMRSurfaceAllocator9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9) del asignador-presentador.
6.  Llame al método [**IVMRSurfaceAllocator9::AdviseNotify**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-advisenotify) del asignador-presentador y pase un puntero a la interfaz [**IVMRSurfaceAllocatorNotify9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9) del filtro VMR-9.
7.  En la implementación de [**IVMRSurfaceAllocator9::AdviseNotify,**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-advisenotify)llame a [**IVMRSurfaceAllocatorNotify9::SetD3DDevice**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-setd3ddevice) Pass en un puntero al dispositivo Direct3D y un identificador al monitor donde aparecerá el vídeo.
8.  En la implementación del método [**IVMRSurfaceAllocator9::InitializeDevice,**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-initializedevice) cree superficies direct3D que coincidan con los parámetros especificados en el **método InitializeDevice.** Opcionalmente, puede usar el método [**IVMRSurfaceAllocatorNotify9::AllocateSurfaceHelper**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) del filtro VMR-9 para asignar estas superficies. Almacene los punteros de superficie en una matriz.
    > [!Note]  
    > Si desea que VMR-9 dibuje los fotogramas de vídeo en una superficie de textura, agregue la marca **VMR9AllocFlag \_ TextureSurface** a la [**estructura VMR9AllocationInfo.**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9allocationinfo) Si el dispositivo no admite texturas en el formato de vídeo nativo, es posible que deba crear una superficie de textura independiente y, a continuación, copiar los fotogramas de vídeo de la superficie de vídeo a la textura.

     

9.  Durante el streaming, VMR-9 obtiene superficies del asignador-presentador mediante una llamada al método [**IVMRSurfaceAllocator9::GetSurface.**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-getsurface) VMR-9 especifica la superficie por su índice dentro de la matriz de superficie (paso 8).
10. Presente la imagen cuando VMR-9 llame al método [**IVMRImagePresenter9::P resentImage.**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrimagepresenter9-presentimage) Los parámetros incluyen un puntero a la superficie de Direct3D que contiene la imagen de vídeo.
11. Si el dispositivo Direct3D se pierde en cualquier momento, el asignador-presentador debe restaurar el dispositivo y volver a crear las superficies. Por ejemplo, el dispositivo se puede perder si cambia el modo de presentación o el usuario mueve la ventana a otro monitor. Si cambia el dispositivo Direct3D, llame al método [**IVMRSurfaceAllocatorNotify9::ChangeD3DDevice del**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-changed3ddevice) filtro VMR-9.
12. Cuando se detiene el streaming, VMR-9 llama al [**método IVMRSurfaceAllocator9::TerminateDevice.**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-terminatedevice) El asignador-presentador debe liberar todos sus recursos de Direct3D.

Hay algunas diferencias entre VMR-7 y VMR-9 en la forma en que se administran los asignadores-presentadores personalizados:

-   El método [**AllocateSurfaceHelper**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) del filtro VMR-9 está disponible para que el asignador-presentador lo use al asignar superficies. Este método hace innecesario que un asignador-presentador personalizado reenvía las llamadas al asignador-presentador predeterminado. Por este motivo, no se publica el CLSID del asignador-presentador predeterminado del filtro VMR-9.
-   A diferencia de VMR-7, VMR-9 no proporciona un asignador-presentador de modo exclusivo de DirectDraw especial. El [**método IVMRSurfaceAllocatorNotify9::AllocateSurfaceHelper**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) hace que este objeto sea innecesario.
-   En el caso del vídeo entrelazado, VMR-9 siempre desenlaza el vídeo antes de presentar la imagen. El asignador-presentador ya no es responsable de desenlazar la imagen antes de mostrarla.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modo de reproducción sin representación de VMR (asignador-presentadores personalizados)](vmr-renderless-playback-mode--custom-allocator-presenters.md)
</dt> </dl>

 

 



