---
description: Una función de devolución de llamada que debe ser implementada por un usuario para establecer una matriz de constantes booleanas del sombreador de vértices.
ms.assetid: 25fd0c68-11b5-4401-a2f8-86075ba3fa54
title: 'ID3DXEffectStateManager:: SetVertexShaderConstantB (método) (D3DX9Effect. h)'
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
ms.openlocfilehash: 1eaf68f27d477aee36bd7773488f34bad29db61d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698300"
---
# <a name="id3dxeffectstatemanagersetvertexshaderconstantb-method"></a><span data-ttu-id="832c8-103">ID3DXEffectStateManager:: SetVertexShaderConstantB (método)</span><span class="sxs-lookup"><span data-stu-id="832c8-103">ID3DXEffectStateManager::SetVertexShaderConstantB method</span></span>

<span data-ttu-id="832c8-104">Una función de devolución de llamada que debe ser implementada por un usuario para establecer una matriz de constantes booleanas del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="832c8-104">A callback function that must be implemented by a user to set an array of vertex shader Boolean constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="832c8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="832c8-105">Syntax</span></span>


```C++
HRESULT SetVertexShaderConstantB(
  [out]       UINT StartRegister,
  [out] const BOOL *pConstantData,
  [out]       UINT RegisterCount
);
```



## <a name="parameters"></a><span data-ttu-id="832c8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="832c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="832c8-107">*StartRegister* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="832c8-107">*StartRegister* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="832c8-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="832c8-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="832c8-109">Índice de base cero del primer registro constante.</span><span class="sxs-lookup"><span data-stu-id="832c8-109">The zero-based index of the first constant register.</span></span>

</dd> <dt>

<span data-ttu-id="832c8-110">*pConstantData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="832c8-110">*pConstantData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="832c8-111">Tipo: **const [**bool**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="832c8-111">Type: **const [**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="832c8-112">Matriz de constantes booleanas.</span><span class="sxs-lookup"><span data-stu-id="832c8-112">An array of Boolean constants.</span></span>

</dd> <dt>

<span data-ttu-id="832c8-113">*RegisterCount* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="832c8-113">*RegisterCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="832c8-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="832c8-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="832c8-115">El número de registros en pConstantData.</span><span class="sxs-lookup"><span data-stu-id="832c8-115">The number of registers in pConstantData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="832c8-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="832c8-116">Return value</span></span>

<span data-ttu-id="832c8-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="832c8-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="832c8-118">El método implementado por el usuario debe devolver S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="832c8-118">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="832c8-119">Si se produce un error en la devolución de llamada al establecer el estado del dispositivo, se producirá una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="832c8-119">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="832c8-120">Se producirá un error en el efecto durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="832c8-120">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="832c8-121">Se producirá un error en la llamada de estado de efecto dinámico (como [**IDirect3DDevice9:: SetVertexShaderConstantB**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb)).</span><span class="sxs-lookup"><span data-stu-id="832c8-121">The dynamic effect state call (such as [**IDirect3DDevice9::SetVertexShaderConstantB**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="832c8-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="832c8-122">Requirements</span></span>



| <span data-ttu-id="832c8-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="832c8-123">Requirement</span></span> | <span data-ttu-id="832c8-124">Value</span><span class="sxs-lookup"><span data-stu-id="832c8-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="832c8-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="832c8-125">Header</span></span><br/>  | <dl> <span data-ttu-id="832c8-126"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="832c8-126"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="832c8-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="832c8-127">Library</span></span><br/> | <dl> <span data-ttu-id="832c8-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="832c8-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="832c8-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="832c8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="832c8-130">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="832c8-130">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
