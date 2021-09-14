---
description: Modo exclusivo de DirectDraw
ms.assetid: 3ef4f267-4dc2-421b-ade4-6b1efa364733
title: Modo exclusivo de DirectDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e5b04bae9c3221a4acee9900c5f19ba4e9b0d54
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061701"
---
# <a name="directdraw-exclusive-mode"></a>Modo exclusivo de DirectDraw

> [!Note]  
> Este tema solo se aplica a VMR-7. En VMR-9, se habilita el modo exclusivo mediante el suministro de su propio asignador-presentador en modo exclusivo. Esto es relativamente sencillo si usa el [**método IVMRSurfaceAllocatorNotify9::AllocateSurfaceHelper.**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) En el ejemplo VMR9Allocator se muestra cómo implementar un asignador-presentador personalizado.

 

En el modo exclusivo de DirectDraw, una aplicación toma el control exclusivo del hardware gráfico. Esto es útil para aplicaciones como juegos o, quizás, aplicaciones de vídeo de pantalla completa. Normalmente, el VMR crea los objetos DirectDraw y establece el nivel de cooperación en normal. Sin embargo, para ejecutar vmr en el modo exclusivo de DirectDraw, la propia aplicación debe crear el objeto DirectDraw y la superficie principal, y llamar a **SetCooperativeLevel** para especificar el modo exclusivo.

VmR tiene un asignador-presentador especial que le permite ejecutarse en el modo exclusivo de DirectDraw. Para configurar vmr para usar este asignador-presentador:

1.  Cree el Graph filtro y agrégréle el VMR mediante el [**método IFilterGraph::AddFilter.**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) Para obtener un ejemplo de código, consulte [Modo sin ventanas de VMR.](vmr-windowless-mode.md)
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

    

4.  Conecte el nuevo asignador-presentador al VMR.
5.  Compile el resto del gráfico de filtros de las maneras habituales.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modos de funcionamiento de VMR](vmr-modes-of-operation.md)
</dt> </dl>

 

 



