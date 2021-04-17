---
description: Suministro de un Allocator-Presenter personalizado para VMR-9
ms.assetid: 61bb6b0d-25b5-481b-a241-74c6e421f109
title: Suministro de un Allocator-Presenter personalizado para VMR-9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f004e119fc1cbfc167c2130852a4f59700706fcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678431"
---
# <a name="supplying-a-custom-allocator-presenter-for-vmr-9"></a>Suministro de un Allocator-Presenter personalizado para VMR-9

Para usar un asignador personalizado con el filtro de mezclador de vídeo 9 (VMR-9), realice los pasos siguientes:

1.  Implemente una clase que admita las interfaces [**IVMRSurfaceAllocator9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9) y [**IVMRImagePresenter9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9) .
2.  Llame a **QueryInterface** en el filtro VMR-9 para la interfaz [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) .
3.  Llame al método [**IVMRFilterConfig9:: SetRenderingMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) y pase la marca **sin \_ representación VMR9Mode** .
4.  **QueryInterface** en el filtro VMR-9 para la interfaz [**IVMRSurfaceAllocatorNotify9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9) .
5.  Llame al método [**IVMRSurfaceAllocatorNotify9:: AdviseSurfaceAllocator**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-advisesurfaceallocator) y pase un puntero al método [**IVMRSurfaceAllocator9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9) de la persona que presenta el asignador.
6.  Llame al método [**IVMRSurfaceAllocator9:: AdviseNotify**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-advisenotify) de allocator-Presenter y pase un puntero a la interfaz [**IVMRSURFACEALLOCATORNOTIFY9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9) del filtro VMR-9.
7.  En la implementación de [**IVMRSurfaceAllocator9:: AdviseNotify**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-advisenotify), llame a [**IVMRSurfaceAllocatorNotify9:: SetD3DDevice**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-setd3ddevice) pase un puntero al dispositivo Direct3D y un identificador al monitor en el que aparecerá el vídeo.
8.  En la implementación del método [**IVMRSurfaceAllocator9:: InitializeDevice**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-initializedevice) , cree superficies de Direct3D que coincidan con los parámetros proporcionados en el método **InitializeDevice** . Opcionalmente, puede usar el método [**IVMRSurfaceAllocatorNotify9:: AllocateSurfaceHelper**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) del filtro VMR-9 para asignar estas superficies. Almacenar los punteros de superficie en una matriz.
    > [!Note]  
    > Si desea que VMR-9 dibuje los fotogramas de vídeo en una superficie de textura, agregue la marca **VMR9AllocFlag \_ TextureSurface** a la estructura [**VMR9AllocationInfo**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9allocationinfo) . Si el dispositivo no admite texturas en el formato de vídeo nativo, es posible que tenga que crear una superficie de textura independiente y, a continuación, copiar los fotogramas de vídeo de la superficie de vídeo a la textura.

     

9.  Durante el streaming, VMR-9 obtiene las superficies del asignador-Presenter llamando al método [**IVMRSurfaceAllocator9:: GetSurface**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-getsurface) . VMR-9 especifica la superficie por su índice dentro de la matriz de la superficie (paso 8).
10. Presente la imagen cuando VMR-9 llama al método [**IVMRImagePresenter9::P resentimage**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrimagepresenter9-presentimage) . Los parámetros incluyen un puntero a la superficie de Direct3D que contiene la imagen de vídeo.
11. Si el dispositivo Direct3D se pierde en cualquier momento, el asignador debe restaurar el dispositivo y volver a crear las superficies. Por ejemplo, se puede perder el dispositivo si cambia el modo de presentación o si el usuario mueve la ventana a otro monitor. Si el dispositivo Direct3D cambia, llame al método [**IVMRSurfaceAllocatorNotify9:: ChangeD3DDevice**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-changed3ddevice) del filtro VMR-9.
12. Cuando se detiene el streaming, VMR-9 llama al método [**IVMRSurfaceAllocator9:: TerminateDevice**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-terminatedevice) . Allocator-Presenter debe liberar todos sus recursos de Direct3D.

Hay algunas diferencias entre la VMR-7 y la VMR-9 en la forma en que se administran los presentadores personalizados:

-   El método [**AllocateSurfaceHelper**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) del filtro VMR-9 está disponible para que lo use el presentador del asignador cuando se asignan superficies. Este método hace que resulte innecesario que un asignador personalizado reenvíe las llamadas al asignador predeterminado. Por esta razón, el CLSID del asignador predeterminado del filtro VMR-9 no se publica.
-   A diferencia de la de VMR-7, el modelo VMR-9 no proporciona un asignador de modo exclusivo de DirectDraw (el presentador). El método [**IVMRSurfaceAllocatorNotify9:: AllocateSurfaceHelper**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) hace que este objeto sea innecesario.
-   En el caso del vídeo entrelazado, VMR-9 siempre anula el entrelazado del vídeo antes de presentar la imagen. Allocator-Presenter ya no es responsable de quitar el entrelazado de la imagen antes de mostrarla.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modo de reproducción no representativo de VMR (asignador personalizado)](vmr-renderless-playback-mode--custom-allocator-presenters.md)
</dt> </dl>

 

 



