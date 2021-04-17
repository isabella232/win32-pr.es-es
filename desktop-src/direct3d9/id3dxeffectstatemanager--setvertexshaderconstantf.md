---
description: Una función de devolución de llamada que debe ser implementada por un usuario para establecer una matriz de constantes de punto flotante del sombreador de vértices.
ms.assetid: 3a13040d-5d5a-4454-bf11-cda9653585c0
title: 'ID3DXEffectStateManager:: SetVertexShaderConstantF (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetVertexShaderConstantF
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 378af983e0ed7ca1709ae8bb6cfe8615a481b3f6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698322"
---
# <a name="id3dxeffectstatemanagersetvertexshaderconstantf-method"></a><span data-ttu-id="cb6ab-103">ID3DXEffectStateManager:: SetVertexShaderConstantF (método)</span><span class="sxs-lookup"><span data-stu-id="cb6ab-103">ID3DXEffectStateManager::SetVertexShaderConstantF method</span></span>

<span data-ttu-id="cb6ab-104">Una función de devolución de llamada que debe ser implementada por un usuario para establecer una matriz de constantes de punto flotante del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="cb6ab-104">A callback function that must be implemented by a user to set an array of vertex shader floating-point constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb6ab-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cb6ab-105">Syntax</span></span>


```C++
HRESULT SetVertexShaderConstantF(
  [out]       UINT  StartRegister,
  [out] const FLOAT *pConstantData,
  [out]       UINT  RegisterCount
);
```



## <a name="parameters"></a><span data-ttu-id="cb6ab-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cb6ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb6ab-107">*StartRegister* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="cb6ab-107">*StartRegister* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb6ab-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cb6ab-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cb6ab-109">Índice de base cero del primer registro constante.</span><span class="sxs-lookup"><span data-stu-id="cb6ab-109">The zero-based index of the first constant register.</span></span>

</dd> <dt>

<span data-ttu-id="cb6ab-110">*pConstantData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="cb6ab-110">*pConstantData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb6ab-111">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="cb6ab-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="cb6ab-112">Matriz de constantes de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="cb6ab-112">An array of floating-point constants.</span></span>

</dd> <dt>

<span data-ttu-id="cb6ab-113">*RegisterCount* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="cb6ab-113">*RegisterCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb6ab-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cb6ab-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cb6ab-115">El número de registros en pConstantData.</span><span class="sxs-lookup"><span data-stu-id="cb6ab-115">The number of registers in pConstantData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb6ab-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cb6ab-116">Return value</span></span>

<span data-ttu-id="cb6ab-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cb6ab-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cb6ab-118">El método implementado por el usuario debe devolver S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="cb6ab-118">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="cb6ab-119">Si se produce un error en la devolución de llamada al establecer el estado del dispositivo, se producirá una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="cb6ab-119">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="cb6ab-120">Se producirá un error en el efecto durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="cb6ab-120">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="cb6ab-121">Se producirá un error en la llamada de estado de efecto dinámico (como [**IDirect3DDevice9:: SetVertexShaderConstantF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf)).</span><span class="sxs-lookup"><span data-stu-id="cb6ab-121">The dynamic effect state call (such as [**IDirect3DDevice9::SetVertexShaderConstantF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb6ab-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb6ab-122">Requirements</span></span>



| <span data-ttu-id="cb6ab-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb6ab-123">Requirement</span></span> | <span data-ttu-id="cb6ab-124">Value</span><span class="sxs-lookup"><span data-stu-id="cb6ab-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb6ab-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cb6ab-125">Header</span></span><br/>  | <dl> <span data-ttu-id="cb6ab-126"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb6ab-126"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="cb6ab-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cb6ab-127">Library</span></span><br/> | <dl> <span data-ttu-id="cb6ab-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cb6ab-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="cb6ab-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb6ab-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb6ab-130">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="cb6ab-130">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
