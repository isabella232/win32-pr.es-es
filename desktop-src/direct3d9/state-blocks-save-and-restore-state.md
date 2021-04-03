---
description: Un bloque de estado es un grupo de Estados de dispositivo.
ms.assetid: 6b1917a8-8685-40c3-983d-6bd2fed95642
title: Estado de guardado y restauración de bloques de estado (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c8f19d6409e0dc9c40f1d4c7711440a0dc09fe2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997634"
---
# <a name="state-blocks-save-and-restore-state-direct3d-9"></a><span data-ttu-id="4ebe5-103">Estado de guardado y restauración de bloques de estado (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4ebe5-103">State Blocks Save and Restore State (Direct3D 9)</span></span>

<span data-ttu-id="4ebe5-104">Un bloque de estado es un grupo de Estados de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4ebe5-104">A state block is a group of device states.</span></span> <span data-ttu-id="4ebe5-105">El estado del dispositivo se compone del estado de representación, el estado del vértice, el estado del píxel o todo lo anterior.</span><span class="sxs-lookup"><span data-stu-id="4ebe5-105">Device state is made up of render state, vertex state, pixel state, or all of the above.</span></span> <span data-ttu-id="4ebe5-106">Un bloque de estado contiene una instantánea del estado actual de un dispositivo o puede crear un bloque de estado que registre cada cambio de estado que realiza la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4ebe5-106">A state block contains a snapshot of a device's current state, or you can create a state block that records each state change that your application makes.</span></span>

## <a name="capture-a-block-of-state"></a><span data-ttu-id="4ebe5-107">Captura de un bloque de estado</span><span class="sxs-lookup"><span data-stu-id="4ebe5-107">Capture a Block of State</span></span>

<span data-ttu-id="4ebe5-108">Elija el tipo de estado que desea capturar y cree un bloque de estado similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="4ebe5-108">Choose the type of state that you want to capture, and create a state block like this:</span></span>


```
IDirect3DStateBlock9* pStateBlock = NULL;
pd3dDevice->CreateStateBlock( D3DSBT_ALL, &pStateBlock );
```



<span data-ttu-id="4ebe5-109">[**IDirect3DDevice9:: CreateStateBlock**](/windows/desktop/api) crea un bloque de estado y captura automáticamente el estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4ebe5-109">[**IDirect3DDevice9::CreateStateBlock**](/windows/desktop/api) creates a state block, and automatically captures the device state.</span></span> <span data-ttu-id="4ebe5-110">El estado del dispositivo se especifica mediante el tipo de bloque de estado en el primer argumento.</span><span class="sxs-lookup"><span data-stu-id="4ebe5-110">The device state is specified by the state block type in the first argument.</span></span> <span data-ttu-id="4ebe5-111">Este estado puede ser uno de los siguientes: todo el estado del dispositivo (vea [guardar todos los Estados de los dispositivos con un StateBlock (Direct3D 9)](saving-all-device-states-with-a-stateblock.md)), todo el estado de los píxeles (vea [guardar el estado de los píxeles con un StateBlock (Direct3D 9)](saving-pixel-states-with-a-stateblock.md)) o todo el estado del vértice (vea [guardar los Estados de los vértices con un StateBlock (Direct3D 9)](saving-vertex-states-with-a-stateblock.md)).</span><span class="sxs-lookup"><span data-stu-id="4ebe5-111">This state can be one of the following: all device state (see [Saving All Device States with a StateBlock (Direct3D 9)](saving-all-device-states-with-a-stateblock.md)), all pixel state (see [Saving Pixel State With a StateBlock (Direct3D 9)](saving-pixel-states-with-a-stateblock.md)), or all vertex state (see [Saving Vertex States With a StateBlock (Direct3D 9)](saving-vertex-states-with-a-stateblock.md)).</span></span>

<span data-ttu-id="4ebe5-112">El sistema de efectos usa un bloque de estado para guardar el estado.</span><span class="sxs-lookup"><span data-stu-id="4ebe5-112">The effect system uses a state block to save state.</span></span> <span data-ttu-id="4ebe5-113">Después de llamar a [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) , se crea un bloque de estado y se captura el estado.</span><span class="sxs-lookup"><span data-stu-id="4ebe5-113">After [**ID3DXEffect::Begin**](id3dxeffect--begin.md) is called, a state block is created and state is captured.</span></span> <span data-ttu-id="4ebe5-114">Cuando se llama a [**ID3DXEffect:: end**](id3dxeffect--end.md) , el estado del bloque de estado se vuelve a aplicar al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4ebe5-114">When [**ID3DXEffect::End**](id3dxeffect--end.md) is called, the state block state is reapplied to the device.</span></span>

## <a name="capture-individual-states"></a><span data-ttu-id="4ebe5-115">Capturar Estados individuales</span><span class="sxs-lookup"><span data-stu-id="4ebe5-115">Capture Individual States</span></span>

<span data-ttu-id="4ebe5-116">Para guardar una secuencia de estado personalizada, ajuste el estado que desea guardar en un par [**IDirect3DDevice9:: BeginStateBlock**](/windows/desktop/api) y [**IDirect3DDevice9:: EndStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endstateblock) .</span><span class="sxs-lookup"><span data-stu-id="4ebe5-116">To save a custom state sequence, wrap the state that you want to save in a [**IDirect3DDevice9::BeginStateBlock**](/windows/desktop/api) and [**IDirect3DDevice9::EndStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endstateblock) pair.</span></span> <span data-ttu-id="4ebe5-117">BeginStateBlock indica al dispositivo actual que configure un bloque de estado y le agregue todos los cambios de estado que se producen hasta que se llama a EndStateBlock.</span><span class="sxs-lookup"><span data-stu-id="4ebe5-117">BeginStateBlock tells the current device to set up a state block and add to it every state change that occurs until EndStateBlock is called.</span></span> <span data-ttu-id="4ebe5-118">Este es un ejemplo:</span><span class="sxs-lookup"><span data-stu-id="4ebe5-118">Here's an example:</span></span>


```
IDirect3DStateBlock9* pStateBlock = NULL;
pd3dDevice->BeginStateBlock();
pd3dDevice->SetRenderState ( D3DRS_ZENABLE, true );
pd3dDevice->EndStateBlock( &pStateBlock );
```



<span data-ttu-id="4ebe5-119">Esto guardará cualquier número de cambios de estado en cualquier secuencia en un stateblock personalizado.</span><span class="sxs-lookup"><span data-stu-id="4ebe5-119">This will save any number of state changes in any sequence to a custom stateblock.</span></span> <span data-ttu-id="4ebe5-120">Más adelante, cuando quiera usar stateblock para restablecer el estado del dispositivo, llame a [**IDirect3DStateBlock9:: Apply**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dstateblock9-apply).</span><span class="sxs-lookup"><span data-stu-id="4ebe5-120">Later, when you want to use the stateblock to reset the device state, call [**IDirect3DStateBlock9::Apply**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dstateblock9-apply).</span></span> <span data-ttu-id="4ebe5-121">Esto sobrescribirá solo el estado del dispositivo capturado en el bloque de estado.</span><span class="sxs-lookup"><span data-stu-id="4ebe5-121">This will overwrite only the device state that has been captured in the state block.</span></span> <span data-ttu-id="4ebe5-122">No se cambiará ningún otro estado de dispositivo que no se haya capturado con el stateblock personalizado.</span><span class="sxs-lookup"><span data-stu-id="4ebe5-122">Any other device state that was not captured with the custom stateblock will not be changed.</span></span> <span data-ttu-id="4ebe5-123">Una vez más, como el objeto stateblock es una interfaz, tendrá que liberarlo cuando haya terminado.</span><span class="sxs-lookup"><span data-stu-id="4ebe5-123">Once again, since the stateblock object is an interface, you will need to release it when you are done with it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4ebe5-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4ebe5-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ebe5-125">Estados (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4ebe5-125">States (Direct3D 9)</span></span>](states.md)
</dt> </dl>

 

 
