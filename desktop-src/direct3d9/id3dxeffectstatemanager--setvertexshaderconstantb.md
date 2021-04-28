---
description: 'Método ID3DXEffectStateManager::SetVertexShaderConstantB: una función de devolución de llamada que debe implementar un usuario para establecer una matriz de constantes booleanas del sombreador de vértices.'
ms.assetid: 25fd0c68-11b5-4401-a2f8-86075ba3fa54
title: Método ID3DXEffectStateManager::SetVertexShaderConstantB (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetVertexShaderConstantB
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 79d4972c301d7333869d68d36267186a67b37eb1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090413"
---
# <a name="id3dxeffectstatemanagersetvertexshaderconstantb-method"></a><span data-ttu-id="89f67-103">Método ID3DXEffectStateManager::SetVertexShaderConstantB</span><span class="sxs-lookup"><span data-stu-id="89f67-103">ID3DXEffectStateManager::SetVertexShaderConstantB method</span></span>

<span data-ttu-id="89f67-104">Función de devolución de llamada que debe implementar un usuario para establecer una matriz de constantes booleanas del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="89f67-104">A callback function that must be implemented by a user to set an array of vertex shader Boolean constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="89f67-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="89f67-105">Syntax</span></span>


```C++
HRESULT SetVertexShaderConstantB(
  [out]       UINT StartRegister,
  [out] const BOOL *pConstantData,
  [out]       UINT RegisterCount
);
```



## <a name="parameters"></a><span data-ttu-id="89f67-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="89f67-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89f67-107">*StartRegister* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="89f67-107">*StartRegister* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="89f67-108">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="89f67-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="89f67-109">Índice de base cero del primer registro constante.</span><span class="sxs-lookup"><span data-stu-id="89f67-109">The zero-based index of the first constant register.</span></span>

</dd> <dt>

<span data-ttu-id="89f67-110">*pConstantData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="89f67-110">*pConstantData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="89f67-111">Tipo: **const [**BOOL**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="89f67-111">Type: **const [**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="89f67-112">Matriz de constantes booleanas.</span><span class="sxs-lookup"><span data-stu-id="89f67-112">An array of Boolean constants.</span></span>

</dd> <dt>

<span data-ttu-id="89f67-113">*RegisterCount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="89f67-113">*RegisterCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="89f67-114">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="89f67-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="89f67-115">Número de registros en pConstantData.</span><span class="sxs-lookup"><span data-stu-id="89f67-115">The number of registers in pConstantData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89f67-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="89f67-116">Return value</span></span>

<span data-ttu-id="89f67-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="89f67-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="89f67-118">El método implementado por el usuario debe devolver S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="89f67-118">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="89f67-119">Si se produce un error en la devolución de llamada al establecer el estado del dispositivo, se producirá una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="89f67-119">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="89f67-120">Se producirá un error en el efecto [**durante ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="89f67-120">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="89f67-121">Se producirá un error en la llamada de estado de efecto dinámico (como [**IDirect3DDevice9::SetVertexShaderConstantB).**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb)</span><span class="sxs-lookup"><span data-stu-id="89f67-121">The dynamic effect state call (such as [**IDirect3DDevice9::SetVertexShaderConstantB**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="89f67-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89f67-122">Requirements</span></span>



| <span data-ttu-id="89f67-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="89f67-123">Requirement</span></span> | <span data-ttu-id="89f67-124">Value</span><span class="sxs-lookup"><span data-stu-id="89f67-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="89f67-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="89f67-125">Header</span></span><br/>  | <dl> <span data-ttu-id="89f67-126"><dt>D3DX9Effect.h</dt></span><span class="sxs-lookup"><span data-stu-id="89f67-126"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="89f67-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="89f67-127">Library</span></span><br/> | <dl> <span data-ttu-id="89f67-128"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="89f67-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="89f67-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="89f67-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89f67-130">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="89f67-130">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
