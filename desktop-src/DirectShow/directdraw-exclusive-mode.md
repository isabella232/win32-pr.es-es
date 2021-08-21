---
description: Modo exclusivo de DirectDraw
ms.assetid: 3ef4f267-4dc2-421b-ade4-6b1efa364733
title: Modo exclusivo de DirectDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09199e04a221299676c21fbc2876af4b8149943a743101d34893d5563ed42482
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016192"
---
# <a name="directdraw-exclusive-mode"></a>Modo exclusivo de DirectDraw

> [!Note]  
> Este tema solo se aplica a VMR-7. En VMR-9, puede habilitar el modo exclusivo mediante el suministro de su propio asignador-presentador en modo exclusivo. Esto es relativamente sencillo si usa el [**método IVMRSurfaceAllocatorNotify9::AllocateSurfaceHelper.**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) El ejemplo VMR9Allocator muestra cómo implementar un asignador-presentador personalizado.

 

En el modo exclusivo de DirectDraw, una aplicación toma el control exclusivo del hardware gráfico. Esto es útil para aplicaciones como juegos o quizás aplicaciones de vídeo de pantalla completa. Normalmente, vmr crea los objetos DirectDraw y establece el nivel de cooperación en normal. Sin embargo, para ejecutar vmr en el modo exclusivo de DirectDraw, la propia aplicación debe crear el objeto DirectDraw y la superficie principal y llamar a **SetCooperativeLevel** para especificar el modo exclusivo.

VmR tiene un asignador-presentador especial que le permite ejecutarse en modo exclusivo de DirectDraw. Para configurar vmr para usar este asignador-presentador:

1.  Cree el filtro Graph y agrégrele la VMR mediante el [**método IFilterGraph::AddFilter.**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) Para obtener un ejemplo de código, vea [Modo sin ventanas de VMR.](vmr-windowless-mode.md)
2.  Cree el asignador-presentador de modo exclusivo:
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

    

3.  Configure el nuevo asignador-presentador:
    ```C++
    pExclModeConfig->SetXlcModeDDObjAndPrimarySurface(...);
    ```

    

4.  Conecte el nuevo asignador-presentador a vmr.
5.  Compile el resto del gráfico de filtros de las maneras habituales.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modos de funcionamiento de VMR](vmr-modes-of-operation.md)
</dt> </dl>

 

 



