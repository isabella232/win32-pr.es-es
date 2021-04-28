---
description: 'Método ID3DXEffectStateManager::SetPixelShaderConstantF: una función de devolución de llamada que debe implementar un usuario para establecer una matriz de constantes de punto flotante del sombreador de vértices.'
ms.assetid: db87ca8c-2539-4d80-854c-25b114a7e7e0
title: Método ID3DXEffectStateManager::SetPixelShaderConstantF (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetPixelShaderConstantF
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f73963e98d4951eaf2905cc5da6eab3a6409f220
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090463"
---
# <a name="id3dxeffectstatemanagersetpixelshaderconstantf-method"></a><span data-ttu-id="875a2-103">Método ID3DXEffectStateManager::SetPixelShaderConstantF</span><span class="sxs-lookup"><span data-stu-id="875a2-103">ID3DXEffectStateManager::SetPixelShaderConstantF method</span></span>

<span data-ttu-id="875a2-104">Función de devolución de llamada que debe implementar un usuario para establecer una matriz de constantes de punto flotante del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="875a2-104">A callback function that must be implemented by a user to set an array of vertex shader floating-point constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="875a2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="875a2-105">Syntax</span></span>


```C++
HRESULT SetPixelShaderConstantF(
  [out]       UINT  StartRegister,
  [out] const FLOAT *pConstantData,
  [out]       UINT  RegisterCount
);
```



## <a name="parameters"></a><span data-ttu-id="875a2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="875a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="875a2-107">*StartRegister* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="875a2-107">*StartRegister* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="875a2-108">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="875a2-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="875a2-109">Índice de base cero del primer registro constante.</span><span class="sxs-lookup"><span data-stu-id="875a2-109">The zero-based index of the first constant register.</span></span>

</dd> <dt>

<span data-ttu-id="875a2-110">*pConstantData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="875a2-110">*pConstantData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="875a2-111">Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="875a2-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="875a2-112">Matriz de constantes de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="875a2-112">An array of floating-point constants.</span></span>

</dd> <dt>

<span data-ttu-id="875a2-113">*RegisterCount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="875a2-113">*RegisterCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="875a2-114">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="875a2-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="875a2-115">Número de registros en pConstantData.</span><span class="sxs-lookup"><span data-stu-id="875a2-115">The number of registers in pConstantData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="875a2-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="875a2-116">Return value</span></span>

<span data-ttu-id="875a2-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="875a2-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="875a2-118">El método implementado por el usuario debe devolver S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="875a2-118">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="875a2-119">Si se produce un error en la devolución de llamada al establecer el estado del dispositivo, se producirá una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="875a2-119">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="875a2-120">Se producirá un error en el efecto [**durante ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="875a2-120">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="875a2-121">Se producirá un error en la llamada de estado de efecto dinámico (como [**IDirect3DDevice9::SetPixelShaderConstantF).**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf)</span><span class="sxs-lookup"><span data-stu-id="875a2-121">The dynamic effect state call (such as [**IDirect3DDevice9::SetPixelShaderConstantF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="875a2-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="875a2-122">Requirements</span></span>



| <span data-ttu-id="875a2-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="875a2-123">Requirement</span></span> | <span data-ttu-id="875a2-124">Value</span><span class="sxs-lookup"><span data-stu-id="875a2-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="875a2-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="875a2-125">Header</span></span><br/>  | <dl> <span data-ttu-id="875a2-126"><dt>D3DX9Effect.h</dt></span><span class="sxs-lookup"><span data-stu-id="875a2-126"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="875a2-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="875a2-127">Library</span></span><br/> | <dl> <span data-ttu-id="875a2-128"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="875a2-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="875a2-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="875a2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="875a2-130">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="875a2-130">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
