---
description: Modo exclusivo de DirectDraw
ms.assetid: 3ef4f267-4dc2-421b-ade4-6b1efa364733
title: Modo exclusivo de DirectDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e5b04bae9c3221a4acee9900c5f19ba4e9b0d54
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677203"
---
# <a name="directdraw-exclusive-mode"></a>Modo exclusivo de DirectDraw

> [!Note]  
> Este tema se aplica solo a VMR-7. En VMR-9, habilita el modo exclusivo proporcionando su propio asignador de modo exclusivo. Esto es relativamente sencillo si usa el método [**IVMRSurfaceAllocatorNotify9:: AllocateSurfaceHelper**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) . En el ejemplo VMR9Allocator se muestra cómo implementar un asignador personalizado.

 

En el modo exclusivo de DirectDraw, una aplicación toma el control exclusivo del hardware de gráficos. Esto resulta útil para aplicaciones como juegos o quizás aplicaciones de vídeo a pantalla completa. Normalmente, la VMR crea los objetos de DirectDraw y establece el nivel cooperativo en normal. Sin embargo, para ejecutar la VMR en modo exclusivo de DirectDraw, la propia aplicación debe crear el objeto DirectDraw y la superficie principal y llamar a **SetCooperativeLevel** para especificar el modo exclusivo.

La VMR tiene un asignador especial que le permite ejecutarse en modo exclusivo de DirectDraw. Para configurar la VMR para usar este asignador-presentador:

1.  Cree el gráfico de filtro y agréguele el VMR mediante el método [**IFilterGraph:: addFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) . Para obtener un ejemplo de código, consulte [modo sin ventanas de VMR](vmr-windowless-mode.md).
2.  Cree el asignador de modo exclusivo:
    ```C++
    IVMRImagePresenterExclModeConfig* pExclModeConfig;
    CoCreateInstance(
            CLSID_AllocPresenterDDXclMode,
            NULL,
            CLSCTX_INPROC_SERVER,
            IID_IVMRImagePresenterExclModeConfig,
            (void**)&pExclModeConfig
            );
    ```

    

3.  Configure el nuevo asignador-Presenter:
    ```C++
    pExclModeConfig->SetXlcModeDDObjAndPrimarySurface(...);
    ```

    

4.  Conecte el nuevo asignador-Presenter a la VMR.
5.  Compile el resto del gráfico de filtro de las maneras habituales.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modos de funcionamiento de VMR](vmr-modes-of-operation.md)
</dt> </dl>

 

 



