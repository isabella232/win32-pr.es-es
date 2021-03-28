---
title: Operaciones disponibles en grupos de iconos
description: En esta sección se enumeran las operaciones que se pueden realizar en grupos de mosaicos.
ms.assetid: 69CF182B-9161-43B7-89A5-0468E1BBD6B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a6c9ec58e6c9197f107f47cd7fe3513f43030c0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104271268"
---
# <a name="operations-available-on-tile-pools"></a><span data-ttu-id="f21f9-103">Operaciones disponibles en grupos de iconos</span><span class="sxs-lookup"><span data-stu-id="f21f9-103">Operations available on tile pools</span></span>

<span data-ttu-id="f21f9-104">En esta sección se enumeran las operaciones que se pueden realizar en grupos de mosaicos.</span><span class="sxs-lookup"><span data-stu-id="f21f9-104">This section lists operations that you can perform on tile pools.</span></span>

-   <span data-ttu-id="f21f9-105">La duración de los grupos de mosaicos funciona como cualquier otro recurso de Direct3D, respaldado por el recuento de referencias, incluido en este caso el seguimiento de las asignaciones de los recursos en mosaico.</span><span class="sxs-lookup"><span data-stu-id="f21f9-105">The lifetime of tile pools works like any other Direct3D Resource, backed by reference counting, including in this case tracking of mappings from tiled resources.</span></span> <span data-ttu-id="f21f9-106">Cuando la aplicación ya no hace referencia a un grupo de mosaicos y las asignaciones de icono a la memoria han desaparecido y los accesos a la unidad de procesamiento de gráficos (GPU) se han completado, el sistema operativo desasignará el grupo de mosaicos.</span><span class="sxs-lookup"><span data-stu-id="f21f9-106">When the application no longer references a tile pool and any tile mappings to the memory are gone and graphics processing unit (GPU) accesses completed, the operating system will deallocate the tile pool.</span></span>
-   <span data-ttu-id="f21f9-107">Las API relacionadas con el uso compartido de Surface y la sincronización funcionan para los grupos de mosaicos (pero no directamente en los recursos en mosaico).</span><span class="sxs-lookup"><span data-stu-id="f21f9-107">APIs related to surface sharing and synchronization work for tile pools (but not directly on tiled resources).</span></span> <span data-ttu-id="f21f9-108">De forma similar al comportamiento de los grupos de mosaicos ofrecidos, los comandos de Direct3D que tienen acceso a los recursos en mosaico que apuntan a un grupo de mosaicos se quitan si el grupo de mosaicos se ha compartido y está adquirido actualmente por otro dispositivo y proceso.</span><span class="sxs-lookup"><span data-stu-id="f21f9-108">Similar to the behavior for offered tile pools, Direct3D commands that access tiled resources that point to a tile pool are dropped if the tile pool has been shared and is currently acquired by another device and process.</span></span>
-   <span data-ttu-id="f21f9-109">[**ID3D11DeviceContext2:: ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) (operación)</span><span class="sxs-lookup"><span data-stu-id="f21f9-109">[**ID3D11DeviceContext2::ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) operation</span></span>
-   <span data-ttu-id="f21f9-110">Operaciones [**IDXGIDevice2:: OfferResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources) y [**ReclaimResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-reclaimresources) : estas API para producir temporalmente la memoria para el sistema operan en todo el grupo de mosaicos (y no están disponibles para recursos individuales en mosaico).</span><span class="sxs-lookup"><span data-stu-id="f21f9-110">[**IDXGIDevice2::OfferResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources) and [**ReclaimResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-reclaimresources) operations - These APIs for yielding memory temporarily to the system operate on the entire tile pool (and aren't available for individual tiled resources).</span></span> <span data-ttu-id="f21f9-111">Si un recurso en mosaico apunta a un icono de un grupo de mosaicos ofrecido, el recurso en mosaico se comporta como si se hubiera ofrecido (por ejemplo, el tiempo de ejecución quita los comandos que hacen referencia a él).</span><span class="sxs-lookup"><span data-stu-id="f21f9-111">If a tiled resource points to a tile in an offered tile pool, the tiled resource behaves as if it is offered (for example, the runtime drops commands that reference it).</span></span>

<span data-ttu-id="f21f9-112">Los datos no se pueden copiar directamente a y desde la memoria del grupo de mosaicos.</span><span class="sxs-lookup"><span data-stu-id="f21f9-112">Data can't be copied to and from tile pool memory directly.</span></span> <span data-ttu-id="f21f9-113">Los accesos a la memoria siempre se realizan a través de recursos en mosaico.</span><span class="sxs-lookup"><span data-stu-id="f21f9-113">Accesses to the memory are always done through tiled resources.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f21f9-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f21f9-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f21f9-115">Crear recursos en mosaico</span><span class="sxs-lookup"><span data-stu-id="f21f9-115">Creating tiled resources</span></span>](creating-tiled-resources.md)
</dt> </dl>

 

 