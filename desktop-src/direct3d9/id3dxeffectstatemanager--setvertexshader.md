---
description: Una función de devolución de llamada que debe ser implementada por un usuario para establecer un sombreador de vértices.
ms.assetid: 8f3d3be3-c073-441d-a318-6d2cd5e7aca5
title: 'ID3DXEffectStateManager:: SetVertexShader (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetVertexShader
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 9fd25158f2aa6ab0a22d6226e8e709c3b498b0e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914777"
---
# <a name="id3dxeffectstatemanagersetvertexshader-method"></a><span data-ttu-id="e70a1-103">ID3DXEffectStateManager:: SetVertexShader (método)</span><span class="sxs-lookup"><span data-stu-id="e70a1-103">ID3DXEffectStateManager::SetVertexShader method</span></span>

<span data-ttu-id="e70a1-104">Una función de devolución de llamada que debe ser implementada por un usuario para establecer un sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="e70a1-104">A callback function that must be implemented by a user to set a vertex shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="e70a1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e70a1-105">Syntax</span></span>


```C++
HRESULT SetVertexShader(
  [in] LPDIRECT3DVERTEXSHADER9 pShader
);
```



## <a name="parameters"></a><span data-ttu-id="e70a1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e70a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e70a1-107">*pShader* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e70a1-107">*pShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e70a1-108">Tipo: **[ **LPDIRECT3DVERTEXSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9)**</span><span class="sxs-lookup"><span data-stu-id="e70a1-108">Type: **[**LPDIRECT3DVERTEXSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9)**</span></span>

<span data-ttu-id="e70a1-109">Un puntero a un objeto de sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="e70a1-109">A pointer to a vertex shader object.</span></span> <span data-ttu-id="e70a1-110">Vea [**IDirect3DVertexShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9).</span><span class="sxs-lookup"><span data-stu-id="e70a1-110">See [**IDirect3DVertexShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e70a1-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e70a1-111">Return value</span></span>

<span data-ttu-id="e70a1-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e70a1-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e70a1-113">El método implementado por el usuario debe devolver S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="e70a1-113">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="e70a1-114">Si se produce un error en la devolución de llamada al establecer el estado del dispositivo, se producirá una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="e70a1-114">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="e70a1-115">Se producirá un error en el efecto durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="e70a1-115">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="e70a1-116">Se producirá un error en la llamada de estado de efecto dinámico (como [**IDirect3DDevice9:: SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader)).</span><span class="sxs-lookup"><span data-stu-id="e70a1-116">The dynamic effect state call (such as [**IDirect3DDevice9::SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="e70a1-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e70a1-117">Requirements</span></span>



| <span data-ttu-id="e70a1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e70a1-118">Requirement</span></span> | <span data-ttu-id="e70a1-119">Value</span><span class="sxs-lookup"><span data-stu-id="e70a1-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e70a1-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e70a1-120">Header</span></span><br/>  | <dl> <span data-ttu-id="e70a1-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e70a1-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="e70a1-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e70a1-122">Library</span></span><br/> | <dl> <span data-ttu-id="e70a1-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e70a1-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e70a1-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="e70a1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e70a1-125">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="e70a1-125">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
