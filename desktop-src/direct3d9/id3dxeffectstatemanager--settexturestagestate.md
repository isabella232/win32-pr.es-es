---
description: Función de devolución de llamada que debe ser implementada por un usuario para establecer el estado de la fase de textura.
ms.assetid: cc86a483-ccf0-400d-b14d-ab55a3cf4b98
title: 'ID3DXEffectStateManager:: SetTextureStageState (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetTextureStageState
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 937fd3f2b89dc093d9dceb9441f53d6be2cb06b5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105678831"
---
# <a name="id3dxeffectstatemanagersettexturestagestate-method"></a><span data-ttu-id="b05a3-103">ID3DXEffectStateManager:: SetTextureStageState (método)</span><span class="sxs-lookup"><span data-stu-id="b05a3-103">ID3DXEffectStateManager::SetTextureStageState method</span></span>

<span data-ttu-id="b05a3-104">Función de devolución de llamada que debe ser implementada por un usuario para establecer el estado de la fase de textura.</span><span class="sxs-lookup"><span data-stu-id="b05a3-104">A callback function that must be implemented by a user to set the texture stage state.</span></span>

## <a name="syntax"></a><span data-ttu-id="b05a3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b05a3-105">Syntax</span></span>


```C++
HRESULT SetTextureStageState(
  [in] DWORD                    Stage,
  [in] D3DTEXTURESTAGESTATETYPE Type,
  [in] DWORD                    Value
);
```



## <a name="parameters"></a><span data-ttu-id="b05a3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b05a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b05a3-107">*Stage* \[in\]</span><span class="sxs-lookup"><span data-stu-id="b05a3-107">*Stage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b05a3-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b05a3-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b05a3-109">Fase a la que se asigna la textura.</span><span class="sxs-lookup"><span data-stu-id="b05a3-109">The stage that the texture is assigned to.</span></span> <span data-ttu-id="b05a3-110">Este es el valor de índice en [**IDirect3DDevice9:: SetTexture**](/windows/desktop/api) o [**IDirect3DDevice9:: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate).</span><span class="sxs-lookup"><span data-stu-id="b05a3-110">This is the index value in [**IDirect3DDevice9::SetTexture**](/windows/desktop/api) or [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate).</span></span>

</dd> <dt>

<span data-ttu-id="b05a3-111">*Tipo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="b05a3-111">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b05a3-112">Tipo: **[ **D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)**</span><span class="sxs-lookup"><span data-stu-id="b05a3-112">Type: **[**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)**</span></span>

<span data-ttu-id="b05a3-113">Define el tipo de operación que realizará una fase de textura.</span><span class="sxs-lookup"><span data-stu-id="b05a3-113">Defines the type of operation that a texture stage will perform.</span></span> <span data-ttu-id="b05a3-114">Vea [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md).</span><span class="sxs-lookup"><span data-stu-id="b05a3-114">See [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="b05a3-115">*Valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="b05a3-115">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b05a3-116">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b05a3-116">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b05a3-117">Puede ser una operación ([**D3DTEXTUREOP**](./d3dtextureop.md)) o un valor de argumento ([D3DTA](d3dta.md)), en función de lo que se elija para el tipo.</span><span class="sxs-lookup"><span data-stu-id="b05a3-117">Can be either an operation ([**D3DTEXTUREOP**](./d3dtextureop.md)) or an argument value ([D3DTA](d3dta.md)), depending on what is chosen for Type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b05a3-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b05a3-118">Return value</span></span>

<span data-ttu-id="b05a3-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b05a3-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b05a3-120">El método implementado por el usuario debe devolver S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="b05a3-120">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="b05a3-121">Si se produce un error en la devolución de llamada al establecer el estado del dispositivo, se producirá una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="b05a3-121">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="b05a3-122">Se producirá un error en el efecto durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="b05a3-122">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="b05a3-123">Se producirá un error en la llamada de estado de efecto dinámico (como [**IDirect3DDevice9:: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)).</span><span class="sxs-lookup"><span data-stu-id="b05a3-123">The dynamic effect state call (such as [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="b05a3-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b05a3-124">Requirements</span></span>



| <span data-ttu-id="b05a3-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b05a3-125">Requirement</span></span> | <span data-ttu-id="b05a3-126">Value</span><span class="sxs-lookup"><span data-stu-id="b05a3-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b05a3-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b05a3-127">Header</span></span><br/>  | <dl> <span data-ttu-id="b05a3-128"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b05a3-128"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="b05a3-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b05a3-129">Library</span></span><br/> | <dl> <span data-ttu-id="b05a3-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b05a3-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b05a3-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="b05a3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b05a3-132">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="b05a3-132">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
