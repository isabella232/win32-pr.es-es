---
description: Un bloque de estado se puede usar para capturar todos los Estados de dispositivo (consulte bloques de estado guardar y restaurar estado (Direct3D 9)).
ms.assetid: e14077e4-1453-4aa3-b2de-4d3a829a819a
title: Guardar todos los Estados de los dispositivos con un StateBlock (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bfdb4f9b3a9c1e33c2e8e7f50765f1656bd59e1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686378"
---
# <a name="saving-all-device-states-with-a-stateblock-direct3d-9"></a><span data-ttu-id="e1ab4-103">Guardar todos los Estados de los dispositivos con un StateBlock (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e1ab4-103">Saving All Device States with a StateBlock (Direct3D 9)</span></span>

<span data-ttu-id="e1ab4-104">Un bloque de estado se puede usar para capturar todos los Estados de dispositivo (consulte [bloques de estado guardar y restaurar estado (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span><span class="sxs-lookup"><span data-stu-id="e1ab4-104">A state block can be used to capture all device states (see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span></span> <span data-ttu-id="e1ab4-105">Los siguientes elementos de estado se incluyen en el estado del dispositivo:</span><span class="sxs-lookup"><span data-stu-id="e1ab4-105">The following state elements are included in the device state:</span></span>

-   <span data-ttu-id="e1ab4-106">Estado del vértice (vea [guardar los Estados de los vértices con un StateBlock (Direct3D 9)](saving-vertex-states-with-a-stateblock.md)).</span><span class="sxs-lookup"><span data-stu-id="e1ab4-106">Vertex state (see [Saving Vertex States With a StateBlock (Direct3D 9)](saving-vertex-states-with-a-stateblock.md)).</span></span>
-   <span data-ttu-id="e1ab4-107">Estado de píxel (consulte [almacenamiento del estado de los píxeles con un StateBlock (Direct3D 9)](saving-pixel-states-with-a-stateblock.md)).</span><span class="sxs-lookup"><span data-stu-id="e1ab4-107">Pixel state (see [Saving Pixel State With a StateBlock (Direct3D 9)](saving-pixel-states-with-a-stateblock.md)).</span></span>
-   <span data-ttu-id="e1ab4-108">Cada textura asignada a una muestra.</span><span class="sxs-lookup"><span data-stu-id="e1ab4-108">Each texture assigned to a sampler.</span></span>
-   <span data-ttu-id="e1ab4-109">Cada textura de vértice.</span><span class="sxs-lookup"><span data-stu-id="e1ab4-109">Each vertex texture.</span></span>
-   <span data-ttu-id="e1ab4-110">Cada textura de mapa de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="e1ab4-110">Each displacement map texture.</span></span>
-   <span data-ttu-id="e1ab4-111">Paleta de textura actual.</span><span class="sxs-lookup"><span data-stu-id="e1ab4-111">The current texture palette.</span></span>
-   <span data-ttu-id="e1ab4-112">Para cada flujo de vértices: un puntero al búfer de vértices, cada argumento de [**IDirect3DDevice9:: SetStreamSource**](/windows/desktop/api)y el divisor (si existe) de [**IDirect3DDevice9:: SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq).</span><span class="sxs-lookup"><span data-stu-id="e1ab4-112">For each vertex stream: a pointer to the vertex buffer, each argument from [**IDirect3DDevice9::SetStreamSource**](/windows/desktop/api), and the divider (if any) from [**IDirect3DDevice9::SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq).</span></span>
-   <span data-ttu-id="e1ab4-113">Puntero al búfer de índice.</span><span class="sxs-lookup"><span data-stu-id="e1ab4-113">A pointer to the index buffer.</span></span>
-   <span data-ttu-id="e1ab4-114">La ventanilla.</span><span class="sxs-lookup"><span data-stu-id="e1ab4-114">The viewport.</span></span>
-   <span data-ttu-id="e1ab4-115">Rectángulo de tijeras.</span><span class="sxs-lookup"><span data-stu-id="e1ab4-115">The scissors rectangle.</span></span>
-   <span data-ttu-id="e1ab4-116">Matrices del mundo, vista y proyección.</span><span class="sxs-lookup"><span data-stu-id="e1ab4-116">The world, view, and projection matrices.</span></span>
-   <span data-ttu-id="e1ab4-117">Transformaciones de textura.</span><span class="sxs-lookup"><span data-stu-id="e1ab4-117">The texture transforms.</span></span>
-   <span data-ttu-id="e1ab4-118">Planos de recorte (si existen).</span><span class="sxs-lookup"><span data-stu-id="e1ab4-118">The clipping planes (if any).</span></span>
-   <span data-ttu-id="e1ab4-119">Material actual.</span><span class="sxs-lookup"><span data-stu-id="e1ab4-119">The current material.</span></span>

<span data-ttu-id="e1ab4-120">Para capturar todos los Estados de dispositivo con un bloque de estado, especifique D3DSBT \_ All al llamar a [**IDirect3DDevice9:: CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock).</span><span class="sxs-lookup"><span data-stu-id="e1ab4-120">To capture all device states with a state block, specify D3DSBT\_ALL when calling [**IDirect3DDevice9::CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1ab4-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e1ab4-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1ab4-122">Estado de guardado y restauración de bloques de estado</span><span class="sxs-lookup"><span data-stu-id="e1ab4-122">State Blocks Save and Restore State</span></span>](state-blocks-save-and-restore-state.md)
</dt> </dl>

 

 
