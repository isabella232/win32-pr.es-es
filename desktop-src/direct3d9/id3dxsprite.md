---
description: La interfaz ID3DXSprite proporciona un conjunto de métodos que simplifican el proceso de dibujar sprites mediante Microsoft Direct3D.
ms.assetid: ccf34fac-91a7-4734-bc62-aedaf4d66522
title: Interfaz ID3DXSprite (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3703132cd8a0f7744119d9b8cb5d9d48f260094c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914753"
---
# <a name="id3dxsprite-interface"></a><span data-ttu-id="b711a-103">Interfaz ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="b711a-103">ID3DXSprite interface</span></span>

<span data-ttu-id="b711a-104">La interfaz ID3DXSprite proporciona un conjunto de métodos que simplifican el proceso de dibujar sprites mediante Microsoft Direct3D.</span><span class="sxs-lookup"><span data-stu-id="b711a-104">The ID3DXSprite interface provides a set of methods that simplify the process of drawing sprites using Microsoft Direct3D.</span></span>

## <a name="members"></a><span data-ttu-id="b711a-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="b711a-105">Members</span></span>

<span data-ttu-id="b711a-106">La interfaz **ID3DXSprite** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b711a-106">The **ID3DXSprite** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b711a-107">**ID3DXSprite** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b711a-107">**ID3DXSprite** also has these types of members:</span></span>

-   [<span data-ttu-id="b711a-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="b711a-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b711a-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="b711a-109">Methods</span></span>

<span data-ttu-id="b711a-110">La interfaz **ID3DXSprite** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="b711a-110">The **ID3DXSprite** interface has these methods.</span></span>



| <span data-ttu-id="b711a-111">Método</span><span class="sxs-lookup"><span data-stu-id="b711a-111">Method</span></span>                                                | <span data-ttu-id="b711a-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="b711a-112">Description</span></span>                                                                                                                                                                                                                  |
|:------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b711a-113">**Comenzar**</span><span class="sxs-lookup"><span data-stu-id="b711a-113">**Begin**</span></span>](id3dxsprite--begin.md)                   | <span data-ttu-id="b711a-114">Prepara un dispositivo para dibujar sprites.</span><span class="sxs-lookup"><span data-stu-id="b711a-114">Prepares a device for drawing sprites.</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="b711a-115">**Dibujar**</span><span class="sxs-lookup"><span data-stu-id="b711a-115">**Draw**</span></span>](id3dxsprite--draw.md)                     | <span data-ttu-id="b711a-116">Agrega un objeto Sprite a la lista de objetos Sprite por lotes.</span><span class="sxs-lookup"><span data-stu-id="b711a-116">Adds a sprite to the list of batched sprites.</span></span><br/>                                                                                                                                                                     |
| [<span data-ttu-id="b711a-117">**Fin**</span><span class="sxs-lookup"><span data-stu-id="b711a-117">**End**</span></span>](id3dxsprite--end.md)                       | <span data-ttu-id="b711a-118">Llama a [**ID3DXSprite:: Flush**](id3dxsprite--flush.md) y restaura el estado del dispositivo al modo en que se encontraba antes de que se llamara a [**ID3DXSprite:: Begin**](id3dxsprite--begin.md) .</span><span class="sxs-lookup"><span data-stu-id="b711a-118">Calls [**ID3DXSprite::Flush**](id3dxsprite--flush.md) and restores the device state to how it was before [**ID3DXSprite::Begin**](id3dxsprite--begin.md) was called.</span></span><br/>                                            |
| [<span data-ttu-id="b711a-119">**Vaciar**</span><span class="sxs-lookup"><span data-stu-id="b711a-119">**Flush**</span></span>](id3dxsprite--flush.md)                   | <span data-ttu-id="b711a-120">Obliga a que todos los sprites por lotes se envíen al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b711a-120">Forces all batched sprites to be submitted to the device.</span></span> <span data-ttu-id="b711a-121">Los Estados de los dispositivos permanecen tal como estaban después de la última llamada a [**ID3DXSprite:: Begin**](id3dxsprite--begin.md).</span><span class="sxs-lookup"><span data-stu-id="b711a-121">Device states remain as they were after the last call to [**ID3DXSprite::Begin**](id3dxsprite--begin.md).</span></span> <span data-ttu-id="b711a-122">A continuación, se borra la lista de sprites por lotes.</span><span class="sxs-lookup"><span data-stu-id="b711a-122">The list of batched sprites is then cleared.</span></span><br/> |
| [<span data-ttu-id="b711a-123">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="b711a-123">**GetDevice**</span></span>](id3dxsprite--getdevice.md)           | <span data-ttu-id="b711a-124">Recupera el dispositivo asociado al objeto Sprite.</span><span class="sxs-lookup"><span data-stu-id="b711a-124">Retrieves the device associated with the sprite object.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="b711a-125">**GetTransform**</span><span class="sxs-lookup"><span data-stu-id="b711a-125">**GetTransform**</span></span>](id3dxsprite--gettransform.md)     | <span data-ttu-id="b711a-126">Obtiene la transformación de Sprite.</span><span class="sxs-lookup"><span data-stu-id="b711a-126">Gets the sprite transform.</span></span><br/>                                                                                                                                                                                        |
| [<span data-ttu-id="b711a-127">**OnLostDevice**</span><span class="sxs-lookup"><span data-stu-id="b711a-127">**OnLostDevice**</span></span>](id3dxsprite--onlostdevice.md)     | <span data-ttu-id="b711a-128">Utilice este método para liberar todas las referencias a los recursos de memoria de vídeo y eliminar todos los stateblocks.</span><span class="sxs-lookup"><span data-stu-id="b711a-128">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="b711a-129">Se debe llamar a este método siempre que se pierda un dispositivo o antes de restablecer un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b711a-129">This method should be called whenever a device is lost or before resetting a device.</span></span><br/>                              |
| [<span data-ttu-id="b711a-130">**OnResetDevice**</span><span class="sxs-lookup"><span data-stu-id="b711a-130">**OnResetDevice**</span></span>](id3dxsprite--onresetdevice.md)   | <span data-ttu-id="b711a-131">Use este método para volver a adquirir recursos y guardar el estado inicial.</span><span class="sxs-lookup"><span data-stu-id="b711a-131">Use this method to re-acquire resources and save initial state.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="b711a-132">**SetTransform**</span><span class="sxs-lookup"><span data-stu-id="b711a-132">**SetTransform**</span></span>](id3dxsprite--settransform.md)     | <span data-ttu-id="b711a-133">Establece la transformación de Sprite.</span><span class="sxs-lookup"><span data-stu-id="b711a-133">Sets the sprite transform.</span></span><br/>                                                                                                                                                                                        |
| [<span data-ttu-id="b711a-134">**SetWorldViewLH**</span><span class="sxs-lookup"><span data-stu-id="b711a-134">**SetWorldViewLH**</span></span>](id3dxsprite--setworldviewlh.md) | <span data-ttu-id="b711a-135">Establece la transformación de vista universal que se entrega a la izquierda de un objeto Sprite.</span><span class="sxs-lookup"><span data-stu-id="b711a-135">Sets the left-handed world-view transform for a sprite.</span></span> <span data-ttu-id="b711a-136">Se requiere una llamada a este método antes de la cartelera o la ordenación de los sprites.</span><span class="sxs-lookup"><span data-stu-id="b711a-136">A call to this method is required before billboarding or sorting sprites.</span></span><br/>                                                                                 |
| [<span data-ttu-id="b711a-137">**SetWorldViewRH**</span><span class="sxs-lookup"><span data-stu-id="b711a-137">**SetWorldViewRH**</span></span>](id3dxsprite--setworldviewrh.md) | <span data-ttu-id="b711a-138">Establece la transformación de vista mundial de la mano derecha para un Sprite.</span><span class="sxs-lookup"><span data-stu-id="b711a-138">Sets the right-handed world-view transform for a sprite.</span></span> <span data-ttu-id="b711a-139">Se requiere una llamada a este método antes de la cartelera o la ordenación de los sprites.</span><span class="sxs-lookup"><span data-stu-id="b711a-139">A call to this method is required before billboarding or sorting sprites.</span></span><br/>                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="b711a-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b711a-140">Remarks</span></span>

<span data-ttu-id="b711a-141">La interfaz **ID3DXSprite** se obtiene mediante una llamada a la función [**D3DXCreateSprite**](d3dxcreatesprite.md) .</span><span class="sxs-lookup"><span data-stu-id="b711a-141">The **ID3DXSprite** interface is obtained by calling the [**D3DXCreateSprite**](d3dxcreatesprite.md) function.</span></span>

<span data-ttu-id="b711a-142">Normalmente, la aplicación llama a [**ID3DXSprite:: Begin**](id3dxsprite--begin.md), que permite controlar el estado de representación del dispositivo, la combinación alfa y la transformación y ordenación de sprites.</span><span class="sxs-lookup"><span data-stu-id="b711a-142">The application typically first calls [**ID3DXSprite::Begin**](id3dxsprite--begin.md), which allows control over the device render state, alpha blending, and sprite transformation and sorting.</span></span> <span data-ttu-id="b711a-143">A continuación, para que se muestre cada Sprite, llame a [**ID3DXSprite::D RAW**](id3dxsprite--draw.md).</span><span class="sxs-lookup"><span data-stu-id="b711a-143">Then for each sprite to be displayed, call [**ID3DXSprite::Draw**](id3dxsprite--draw.md).</span></span> <span data-ttu-id="b711a-144">**ID3DXSprite:** se puede llamar a:D RAW repetidamente para almacenar cualquier número de objetos Sprite.</span><span class="sxs-lookup"><span data-stu-id="b711a-144">**ID3DXSprite::Draw** can be called repeatedly to store any number of sprites.</span></span> <span data-ttu-id="b711a-145">Para mostrar los sprites por lotes en el dispositivo, llame a [**ID3DXSprite:: end**](id3dxsprite--end.md) o [**ID3DXSprite:: Flush**](id3dxsprite--flush.md).</span><span class="sxs-lookup"><span data-stu-id="b711a-145">To display the batched sprites to the device, call [**ID3DXSprite::End**](id3dxsprite--end.md) or [**ID3DXSprite::Flush**](id3dxsprite--flush.md).</span></span>

<span data-ttu-id="b711a-146">El tipo LPD3DXSPRITE se define como un puntero a la interfaz **ID3DXSprite** .</span><span class="sxs-lookup"><span data-stu-id="b711a-146">The LPD3DXSPRITE type is defined as a pointer to the **ID3DXSprite** interface.</span></span>


```
typedef interface ID3DXSprite ID3DXSprite;
typedef interface ID3DXSprite *LPD3DXSPRITE;
```



## <a name="requirements"></a><span data-ttu-id="b711a-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b711a-147">Requirements</span></span>



| <span data-ttu-id="b711a-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="b711a-148">Requirement</span></span> | <span data-ttu-id="b711a-149">Value</span><span class="sxs-lookup"><span data-stu-id="b711a-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b711a-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b711a-150">Header</span></span><br/>  | <dl> <span data-ttu-id="b711a-151"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="b711a-151"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="b711a-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b711a-152">Library</span></span><br/> | <dl> <span data-ttu-id="b711a-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b711a-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b711a-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="b711a-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b711a-155">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="b711a-155">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
