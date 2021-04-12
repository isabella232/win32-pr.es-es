---
description: La interfaz ID3DXRenderToSurface se usa para generalizar el proceso de representación de las superficies.
ms.assetid: e9f2ca5e-faa3-45a8-94eb-16f354618e80
title: Interfaz ID3DXRenderToSurface (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 577e729e4e1a510dd24dc981b2b90bdca27dc0f9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362764"
---
# <a name="id3dxrendertosurface-interface"></a><span data-ttu-id="72c5d-103">Interfaz ID3DXRenderToSurface</span><span class="sxs-lookup"><span data-stu-id="72c5d-103">ID3DXRenderToSurface interface</span></span>

<span data-ttu-id="72c5d-104">La interfaz ID3DXRenderToSurface se usa para generalizar el proceso de representación de las superficies.</span><span class="sxs-lookup"><span data-stu-id="72c5d-104">The ID3DXRenderToSurface interface is used to generalize the process of rendering to surfaces.</span></span>

## <a name="members"></a><span data-ttu-id="72c5d-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="72c5d-105">Members</span></span>

<span data-ttu-id="72c5d-106">La interfaz **ID3DXRenderToSurface** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="72c5d-106">The **ID3DXRenderToSurface** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="72c5d-107">**ID3DXRenderToSurface** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="72c5d-107">**ID3DXRenderToSurface** also has these types of members:</span></span>

-   [<span data-ttu-id="72c5d-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="72c5d-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="72c5d-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="72c5d-109">Methods</span></span>

<span data-ttu-id="72c5d-110">La interfaz **ID3DXRenderToSurface** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="72c5d-110">The **ID3DXRenderToSurface** interface has these methods.</span></span>



| <span data-ttu-id="72c5d-111">Método</span><span class="sxs-lookup"><span data-stu-id="72c5d-111">Method</span></span>                                                       | <span data-ttu-id="72c5d-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="72c5d-112">Description</span></span>                                                                                                                                                                                     |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="72c5d-113">**BeginScene**</span><span class="sxs-lookup"><span data-stu-id="72c5d-113">**BeginScene**</span></span>](id3dxrendertosurface--beginscene.md)       | <span data-ttu-id="72c5d-114">Comienza una escena.</span><span class="sxs-lookup"><span data-stu-id="72c5d-114">Begins a scene.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="72c5d-115">**EndScene**</span><span class="sxs-lookup"><span data-stu-id="72c5d-115">**EndScene**</span></span>](id3dxrendertosurface--endscene.md)           | <span data-ttu-id="72c5d-116">Finaliza una escena.</span><span class="sxs-lookup"><span data-stu-id="72c5d-116">Ends a scene.</span></span><br/>                                                                                                                                                                        |
| [<span data-ttu-id="72c5d-117">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="72c5d-117">**GetDesc**</span></span>](id3dxrendertosurface--getdesc.md)             | <span data-ttu-id="72c5d-118">Recupera los parámetros de la superficie de representación.</span><span class="sxs-lookup"><span data-stu-id="72c5d-118">Retrieves the parameters of the render surface.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="72c5d-119">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="72c5d-119">**GetDevice**</span></span>](id3dxrendertosurface--getdevice.md)         | <span data-ttu-id="72c5d-120">Recupera el dispositivo Direct3D asociado a la superficie de representación.</span><span class="sxs-lookup"><span data-stu-id="72c5d-120">Retrieves the Direct3D device associated with the render surface.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="72c5d-121">**OnLostDevice**</span><span class="sxs-lookup"><span data-stu-id="72c5d-121">**OnLostDevice**</span></span>](id3dxrendertosurface--onlostdevice.md)   | <span data-ttu-id="72c5d-122">Utilice este método para liberar todas las referencias a los recursos de memoria de vídeo y eliminar todos los stateblocks.</span><span class="sxs-lookup"><span data-stu-id="72c5d-122">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="72c5d-123">Se debe llamar a este método siempre que se pierda un dispositivo o antes de restablecer un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="72c5d-123">This method should be called whenever a device is lost or before resetting a device.</span></span><br/> |
| [<span data-ttu-id="72c5d-124">**OnResetDevice**</span><span class="sxs-lookup"><span data-stu-id="72c5d-124">**OnResetDevice**</span></span>](id3dxrendertosurface--onresetdevice.md) | <span data-ttu-id="72c5d-125">Use este método para volver a adquirir recursos y guardar el estado inicial.</span><span class="sxs-lookup"><span data-stu-id="72c5d-125">Use this method to re-acquire resources and save initial state.</span></span><br/>                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="72c5d-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="72c5d-126">Remarks</span></span>

<span data-ttu-id="72c5d-127">Las superficies se pueden usar de varias maneras, como objetivos de representación, representación fuera de pantalla o representación en texturas.</span><span class="sxs-lookup"><span data-stu-id="72c5d-127">Surfaces can be used in a variety of ways including render targets, off-screen rendering, or rendering to textures.</span></span>

<span data-ttu-id="72c5d-128">Una superficie se puede configurar mediante una ventanilla independiente mediante el método [**ID3DXRenderToSurface:: BeginScene**](id3dxrendertosurface--beginscene.md) para proporcionar una vista de representación personalizada.</span><span class="sxs-lookup"><span data-stu-id="72c5d-128">A surface can be configured using a separate viewport using the [**ID3DXRenderToSurface::BeginScene**](id3dxrendertosurface--beginscene.md) method, to provide a custom render view.</span></span> <span data-ttu-id="72c5d-129">Si la superficie no es un destino de representación, se usa un destino de representación compatible y el resultado se copia en la superficie al final de la escena.</span><span class="sxs-lookup"><span data-stu-id="72c5d-129">If the surface is not a render target, a compatible render target is used, and the result is copied to the surface at the end of the scene.</span></span>

<span data-ttu-id="72c5d-130">La interfaz **ID3DXRenderToSurface** se obtiene mediante una llamada a la función [**D3DXCreateRenderToSurface**](d3dxcreaterendertosurface.md) .</span><span class="sxs-lookup"><span data-stu-id="72c5d-130">The **ID3DXRenderToSurface** interface is obtained by calling the [**D3DXCreateRenderToSurface**](d3dxcreaterendertosurface.md) function.</span></span>

<span data-ttu-id="72c5d-131">El tipo LPD3DXRENDERTOSURFACE se define como un puntero a la interfaz **ID3DXRenderToSurface** .</span><span class="sxs-lookup"><span data-stu-id="72c5d-131">The LPD3DXRENDERTOSURFACE type is defined as a pointer to the **ID3DXRenderToSurface** interface.</span></span>


```
typedef interface ID3DXRenderToSurface ID3DXRenderToSurface;
typedef interface ID3DXRenderToSurface *LPD3DXRENDERTOSURFACE;
```



## <a name="requirements"></a><span data-ttu-id="72c5d-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72c5d-132">Requirements</span></span>



| <span data-ttu-id="72c5d-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="72c5d-133">Requirement</span></span> | <span data-ttu-id="72c5d-134">Value</span><span class="sxs-lookup"><span data-stu-id="72c5d-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="72c5d-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="72c5d-135">Header</span></span><br/>  | <dl> <span data-ttu-id="72c5d-136"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="72c5d-136"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="72c5d-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="72c5d-137">Library</span></span><br/> | <dl> <span data-ttu-id="72c5d-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="72c5d-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="72c5d-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="72c5d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72c5d-140">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="72c5d-140">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
