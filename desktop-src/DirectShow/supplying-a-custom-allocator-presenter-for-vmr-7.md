---
description: Proporcionar un Allocator-Presenter personalizado para VMR-7
ms.assetid: 19b43c9b-2578-418f-b03b-af7c7a3a46e4
title: Proporcionar un Allocator-Presenter personalizado para VMR-7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e79f191401f990214b2551f9210fab4dfe4d43b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104571102"
---
# <a name="supplying-a-custom-allocator-presenter-for-vmr-7"></a>Proporcionar un Allocator-Presenter personalizado para VMR-7

Allocator-Presenter es responsable de asignar las superficies de DirectDraw y presentar los fotogramas de vídeo para su representación. En la gran mayoría de los escenarios, la funcionalidad del asignador predeterminado será más que suficiente para las necesidades de una aplicación. Sin embargo, al conectar un asignador personalizado, una aplicación puede obtener acceso directo a los bits de vídeo y controlar completamente el proceso de representación. La desventaja de este aumento de la eficacia es que la aplicación debe administrar la complejidad agregada de la administración de superficies de DirectDraw.

![uso de un asignador personalizado: presentador](images/custom-ap.png)

En la ilustración anterior se muestran las interfaces de comunicación utilizadas por VMR y el presentador del asignador. Un asignador personalizado que invalida toda la funcionalidad de asignación y presentación predeterminada debe implementar las interfaces [**IVMRImagePresenter**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter) y [**IVMRSurfaceAllocator**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator) y, opcionalmente, [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol).

Para reemplazar el valor predeterminado de allocator-Presenter, una aplicación llama al método [**IVMRSurfaceAllocatorNotify:: AdviseSurfaceAllocator**](/windows/desktop/api/Strmif/nf-strmif-ivmrsurfaceallocatornotify-advisesurfaceallocator) y pasa un puntero al nuevo asignador-presentador. En respuesta a esta llamada, VMR llamará al método [**IVMRSurfaceAllocator:: AdviseNotify**](/windows/desktop/api/Strmif/nf-strmif-ivmrsurfaceallocator-advisenotify) de allocator-Presenter para proporcionar el puntero a la interfaz [**IVMRSurfaceAllocatorNotify**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify) de VMR. Allocator-Presenter usará este puntero de interfaz al pasar eventos a VMR con el método [**IVMRSurfaceAllocatorNotify:: NotifyEvent**](/windows/desktop/api/Strmif/nf-strmif-ivmrsurfaceallocatornotify-notifyevent) .

Como solución alternativa, una aplicación puede usar su propio asignador-presentador y el predeterminado del asignador. En este escenario, el asignador personalizado controla solo las llamadas en las que se necesita una funcionalidad personalizada y pasa el resto de las llamadas desde la VMR hasta el asignador predeterminado. En muchos casos, solo es necesario invalidar la interfaz [**IVMRImagePresenter**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter) .

![uso de dos allocator-Presenter](images/custom-ap2.png)

Para usar un asignador personalizado y el presentador de asignador predeterminado, una aplicación llamaría primero a [**IVMRSurfaceAllocatorNotify:: AdviseSurfaceAllocator**](/windows/desktop/api/Strmif/nf-strmif-ivmrsurfaceallocatornotify-advisesurfaceallocator) para proporcionar un puntero al nuevo asignador-presentador (). Esto hace que se destruya el asignador predeterminado, por lo que la aplicación debe crear otra instancia del mismo llamando a **QueryInterface** en la VMR y solicitando la interfaz [**IVMRSurfaceAllocator**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator) . Como se muestra en la ilustración anterior, el asignador personalizado invalida los métodos de la interfaz [**IVMRImagePresenter**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter) y simplemente pasa todas las llamadas a la interfaz **IVMRSurfaceAllocator** a través de la implementación predeterminada. La ilustración también muestra la interfaz [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) que se implementa en allocator-Presenter.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Suministro de un Allocator-Presenter personalizado para VMR-9](supplying-a-custom-allocator-presenter-for-vmr-9.md)
</dt> <dt>

[Modo de reproducción no representativo de VMR (asignador personalizado)](vmr-renderless-playback-mode--custom-allocator-presenters.md)
</dt> </dl>

 

 



