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
# <a name="directdraw-exclusive-mode"></a><span data-ttu-id="75d46-103">Modo exclusivo de DirectDraw</span><span class="sxs-lookup"><span data-stu-id="75d46-103">DirectDraw Exclusive Mode</span></span>

> [!Note]  
> <span data-ttu-id="75d46-104">Este tema se aplica solo a VMR-7.</span><span class="sxs-lookup"><span data-stu-id="75d46-104">This topic applies to the VMR-7 only.</span></span> <span data-ttu-id="75d46-105">En VMR-9, habilita el modo exclusivo proporcionando su propio asignador de modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="75d46-105">In the VMR-9, you enable exclusive mode by supplying your own exclusive mode allocator-presenter.</span></span> <span data-ttu-id="75d46-106">Esto es relativamente sencillo si usa el método [**IVMRSurfaceAllocatorNotify9:: AllocateSurfaceHelper**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) .</span><span class="sxs-lookup"><span data-stu-id="75d46-106">This is relatively straightforward if you use the [**IVMRSurfaceAllocatorNotify9::AllocateSurfaceHelper**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) method.</span></span> <span data-ttu-id="75d46-107">En el ejemplo VMR9Allocator se muestra cómo implementar un asignador personalizado.</span><span class="sxs-lookup"><span data-stu-id="75d46-107">The VMR9Allocator sample shows how to implement a custom allocator-presenter.</span></span>

 

<span data-ttu-id="75d46-108">En el modo exclusivo de DirectDraw, una aplicación toma el control exclusivo del hardware de gráficos.</span><span class="sxs-lookup"><span data-stu-id="75d46-108">In DirectDraw Exclusive Mode, an application takes exclusive control of the graphics hardware.</span></span> <span data-ttu-id="75d46-109">Esto resulta útil para aplicaciones como juegos o quizás aplicaciones de vídeo a pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="75d46-109">This is useful for applications such as games, or perhaps full-screen video applications.</span></span> <span data-ttu-id="75d46-110">Normalmente, la VMR crea los objetos de DirectDraw y establece el nivel cooperativo en normal.</span><span class="sxs-lookup"><span data-stu-id="75d46-110">Normally, the VMR creates the DirectDraw objects and sets the cooperative level to normal.</span></span> <span data-ttu-id="75d46-111">Sin embargo, para ejecutar la VMR en modo exclusivo de DirectDraw, la propia aplicación debe crear el objeto DirectDraw y la superficie principal y llamar a **SetCooperativeLevel** para especificar el modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="75d46-111">However, to run the VMR in DirectDraw Exclusive Mode, the application itself must create the DirectDraw object and the primary surface, and call **SetCooperativeLevel** to specify exclusive mode.</span></span>

<span data-ttu-id="75d46-112">La VMR tiene un asignador especial que le permite ejecutarse en modo exclusivo de DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="75d46-112">The VMR has a special allocator-presenter that enables it to run in DirectDraw Exclusive Mode.</span></span> <span data-ttu-id="75d46-113">Para configurar la VMR para usar este asignador-presentador:</span><span class="sxs-lookup"><span data-stu-id="75d46-113">To configure the VMR to use this allocator-presenter:</span></span>

1.  <span data-ttu-id="75d46-114">Cree el gráfico de filtro y agréguele el VMR mediante el método [**IFilterGraph:: addFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) .</span><span class="sxs-lookup"><span data-stu-id="75d46-114">Create the Filter Graph and add the VMR to it using the [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) method.</span></span> <span data-ttu-id="75d46-115">Para obtener un ejemplo de código, consulte [modo sin ventanas de VMR](vmr-windowless-mode.md).</span><span class="sxs-lookup"><span data-stu-id="75d46-115">For a code example, see [VMR Windowless Mode](vmr-windowless-mode.md).</span></span>
2.  <span data-ttu-id="75d46-116">Cree el asignador de modo exclusivo:</span><span class="sxs-lookup"><span data-stu-id="75d46-116">Create the Exclusive Mode allocator-presenter:</span></span>
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

    

3.  <span data-ttu-id="75d46-117">Configure el nuevo asignador-Presenter:</span><span class="sxs-lookup"><span data-stu-id="75d46-117">Configure the new allocator-presenter:</span></span>
    ```C++
    pExclModeConfig->SetXlcModeDDObjAndPrimarySurface(...);
    ```

    

4.  <span data-ttu-id="75d46-118">Conecte el nuevo asignador-Presenter a la VMR.</span><span class="sxs-lookup"><span data-stu-id="75d46-118">Plug the new allocator-presenter into the VMR.</span></span>
5.  <span data-ttu-id="75d46-119">Compile el resto del gráfico de filtro de las maneras habituales.</span><span class="sxs-lookup"><span data-stu-id="75d46-119">Build the rest of the filter graph in the usual ways.</span></span>

## <a name="related-topics"></a><span data-ttu-id="75d46-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="75d46-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75d46-121">Modos de funcionamiento de VMR</span><span class="sxs-lookup"><span data-stu-id="75d46-121">VMR Modes of Operation</span></span>](vmr-modes-of-operation.md)
</dt> </dl>

 

 



