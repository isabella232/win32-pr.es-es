---
description: 'Método ID3DXEffectStateManager::SetPixelShaderConstantB: una función de devolución de llamada que debe implementar un usuario para establecer una matriz de constantes booleanas del sombreador de vértices.'
ms.assetid: ad4d9beb-fd34-4574-9787-61bd3bfaaaaa
title: Método ID3DXEffectStateManager::SetPixelShaderConstantB (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetPixelShaderConstantB
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: ace60b72345c992c3f35943362f6a0958f043aba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090493"
---
# <a name="id3dxeffectstatemanagersetpixelshaderconstantb-method"></a><span data-ttu-id="00fd4-103">Método ID3DXEffectStateManager::SetPixelShaderConstantB</span><span class="sxs-lookup"><span data-stu-id="00fd4-103">ID3DXEffectStateManager::SetPixelShaderConstantB method</span></span>

<span data-ttu-id="00fd4-104">Función de devolución de llamada que debe implementar un usuario para establecer una matriz de constantes booleanas del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="00fd4-104">A callback function that must be implemented by a user to set an array of vertex shader Boolean constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="00fd4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="00fd4-105">Syntax</span></span>


```C++
HRESULT SetPixelShaderConstantB(
  [out]       UINT StartRegister,
  [out] const BOOL *pConstantData,
  [out]       UINT RegisterCount
);
```



## <a name="parameters"></a><span data-ttu-id="00fd4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="00fd4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00fd4-107">*StartRegister* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="00fd4-107">*StartRegister* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="00fd4-108">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="00fd4-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="00fd4-109">Índice de base cero del primer registro constante.</span><span class="sxs-lookup"><span data-stu-id="00fd4-109">The zero-based index of the first constant register.</span></span>

</dd> <dt>

<span data-ttu-id="00fd4-110">*pConstantData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="00fd4-110">*pConstantData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="00fd4-111">Tipo: **const [**BOOL**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="00fd4-111">Type: **const [**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="00fd4-112">Matriz de constantes booleanas.</span><span class="sxs-lookup"><span data-stu-id="00fd4-112">An array of Boolean constants.</span></span>

</dd> <dt>

<span data-ttu-id="00fd4-113">*RegisterCount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="00fd4-113">*RegisterCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="00fd4-114">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="00fd4-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="00fd4-115">Número de registros en pConstantData.</span><span class="sxs-lookup"><span data-stu-id="00fd4-115">The number of registers in pConstantData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00fd4-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="00fd4-116">Return value</span></span>

<span data-ttu-id="00fd4-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="00fd4-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="00fd4-118">El método implementado por el usuario debe devolver S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="00fd4-118">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="00fd4-119">Si se produce un error en la devolución de llamada al establecer el estado del dispositivo, se producirá una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="00fd4-119">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="00fd4-120">Se producirá un error en el efecto [**durante ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="00fd4-120">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="00fd4-121">Se producirá un error en la llamada de estado de efecto dinámico (como [**IDirect3DDevice9::SetPixelShaderConstantB).**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb)</span><span class="sxs-lookup"><span data-stu-id="00fd4-121">The dynamic effect state call (such as [**IDirect3DDevice9::SetPixelShaderConstantB**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="00fd4-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00fd4-122">Requirements</span></span>



| <span data-ttu-id="00fd4-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="00fd4-123">Requirement</span></span> | <span data-ttu-id="00fd4-124">Value</span><span class="sxs-lookup"><span data-stu-id="00fd4-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="00fd4-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="00fd4-125">Header</span></span><br/>  | <dl> <span data-ttu-id="00fd4-126"><dt>D3DX9Effect.h</dt></span><span class="sxs-lookup"><span data-stu-id="00fd4-126"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="00fd4-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="00fd4-127">Library</span></span><br/> | <dl> <span data-ttu-id="00fd4-128"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="00fd4-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="00fd4-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="00fd4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00fd4-130">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="00fd4-130">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
