---
description: Función de devolución de llamada que debe ser implementada por un usuario para establecer el estado de representación.
ms.assetid: a5a27e30-c141-44a4-b8d4-38c1d6076b2a
title: 'ID3DXEffectStateManager:: SetRenderState (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetRenderState
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 111ab8ff379d5b095500101674fc45b6a2b31bc1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718302"
---
# <a name="id3dxeffectstatemanagersetrenderstate-method"></a><span data-ttu-id="a334a-103">ID3DXEffectStateManager:: SetRenderState (método)</span><span class="sxs-lookup"><span data-stu-id="a334a-103">ID3DXEffectStateManager::SetRenderState method</span></span>

<span data-ttu-id="a334a-104">Función de devolución de llamada que debe ser implementada por un usuario para establecer el estado de representación.</span><span class="sxs-lookup"><span data-stu-id="a334a-104">A callback function that must be implemented by a user to set render state.</span></span>

## <a name="syntax"></a><span data-ttu-id="a334a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a334a-105">Syntax</span></span>


```C++
HRESULT SetRenderState(
  [in] D3DRENDERSTATETYPE State,
  [in] DWORD              Value
);
```



## <a name="parameters"></a><span data-ttu-id="a334a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a334a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a334a-107">*Estado* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="a334a-107">*State* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a334a-108">Tipo: **[ **D3DRENDERSTATETYPE**](./d3drenderstatetype.md)**</span><span class="sxs-lookup"><span data-stu-id="a334a-108">Type: **[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)**</span></span>

<span data-ttu-id="a334a-109">Estado de representación que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="a334a-109">The render state to set.</span></span> [<span data-ttu-id="a334a-110">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="a334a-110">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)

</dd> <dt>

<span data-ttu-id="a334a-111">*Valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="a334a-111">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a334a-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a334a-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a334a-113">Valor de estado de representación.</span><span class="sxs-lookup"><span data-stu-id="a334a-113">The render state value.</span></span> <span data-ttu-id="a334a-114">Consulte [Estados de efectos (Direct3D 9)](effect-states.md).</span><span class="sxs-lookup"><span data-stu-id="a334a-114">See [Effect States (Direct3D 9)](effect-states.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a334a-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a334a-115">Return value</span></span>

<span data-ttu-id="a334a-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a334a-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a334a-117">El método implementado por el usuario debe devolver S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="a334a-117">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="a334a-118">Si se produce un error en la devolución de llamada al establecer el estado del dispositivo, se producirá una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="a334a-118">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="a334a-119">Se producirá un error en el efecto durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="a334a-119">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="a334a-120">Se producirá un error en la llamada de estado de efecto dinámico (como [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)).</span><span class="sxs-lookup"><span data-stu-id="a334a-120">The dynamic effect state call (such as [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="a334a-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a334a-121">Requirements</span></span>



| <span data-ttu-id="a334a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a334a-122">Requirement</span></span> | <span data-ttu-id="a334a-123">Value</span><span class="sxs-lookup"><span data-stu-id="a334a-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a334a-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a334a-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a334a-125"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="a334a-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="a334a-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a334a-126">Library</span></span><br/> | <dl> <span data-ttu-id="a334a-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a334a-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a334a-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="a334a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a334a-129">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="a334a-129">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
