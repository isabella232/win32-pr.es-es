---
description: Una función de devolución de llamada que debe ser implementada por un usuario para establecer un sombreador de píxeles.
ms.assetid: 4124eff2-1d88-429c-b7ed-8d87155b5ddc
title: 'ID3DXEffectStateManager:: SetPixelShader (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetPixelShader
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 71a16bc267df95ed7efc1e0f74871b131e34ebe1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547998"
---
# <a name="id3dxeffectstatemanagersetpixelshader-method"></a><span data-ttu-id="dc0df-103">ID3DXEffectStateManager:: SetPixelShader (método)</span><span class="sxs-lookup"><span data-stu-id="dc0df-103">ID3DXEffectStateManager::SetPixelShader method</span></span>

<span data-ttu-id="dc0df-104">Una función de devolución de llamada que debe ser implementada por un usuario para establecer un sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="dc0df-104">A callback function that must be implemented by a user to set a pixel shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc0df-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dc0df-105">Syntax</span></span>


```C++
HRESULT SetPixelShader(
  [in] LPDIRECT3DPIXELSHADER9 pShader
);
```



## <a name="parameters"></a><span data-ttu-id="dc0df-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dc0df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc0df-107">*pShader* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dc0df-107">*pShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc0df-108">Tipo: **[ **LPDIRECT3DPIXELSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9)**</span><span class="sxs-lookup"><span data-stu-id="dc0df-108">Type: **[**LPDIRECT3DPIXELSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9)**</span></span>

<span data-ttu-id="dc0df-109">Un puntero a un objeto de sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="dc0df-109">A pointer to a pixel shader object.</span></span> <span data-ttu-id="dc0df-110">Vea [**IDirect3DPixelShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9).</span><span class="sxs-lookup"><span data-stu-id="dc0df-110">See [**IDirect3DPixelShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc0df-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dc0df-111">Return value</span></span>

<span data-ttu-id="dc0df-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dc0df-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dc0df-113">El método implementado por el usuario debe devolver S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="dc0df-113">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="dc0df-114">Si se produce un error en la devolución de llamada al establecer el estado del dispositivo, se producirá una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="dc0df-114">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="dc0df-115">Se producirá un error en el efecto durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="dc0df-115">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="dc0df-116">Se producirá un error en la llamada de estado de efecto dinámico (como [**IDirect3DDevice9:: SetPixelShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader)).</span><span class="sxs-lookup"><span data-stu-id="dc0df-116">The dynamic effect state call (such as [**IDirect3DDevice9::SetPixelShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc0df-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc0df-117">Requirements</span></span>



| <span data-ttu-id="dc0df-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc0df-118">Requirement</span></span> | <span data-ttu-id="dc0df-119">Value</span><span class="sxs-lookup"><span data-stu-id="dc0df-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc0df-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dc0df-120">Header</span></span><br/>  | <dl> <span data-ttu-id="dc0df-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc0df-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="dc0df-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dc0df-122">Library</span></span><br/> | <dl> <span data-ttu-id="dc0df-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dc0df-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="dc0df-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc0df-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc0df-125">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="dc0df-125">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
