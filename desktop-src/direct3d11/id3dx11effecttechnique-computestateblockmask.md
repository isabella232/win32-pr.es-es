---
title: Método ID3DX11EffectTechnique ComputeStateBlockMask (D3dx11effect. h)
description: Calcule una máscara de bloque de estado para permitir o impedir los cambios de estado.
ms.assetid: 4fd6061d-6ca5-4e3f-b031-fae98f3de057
keywords:
- Método ComputeStateBlockMask Direct3D 11
- Método ComputeStateBlockMask Direct3D 11, interfaz ID3DX11EffectTechnique
- Interfaz ID3DX11EffectTechnique Direct3D 11, método ComputeStateBlockMask
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.ComputeStateBlockMask
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d15a159c15f35d530559b4ad6d84dd815e5964a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280265"
---
# <a name="id3dx11effecttechniquecomputestateblockmask-method"></a><span data-ttu-id="0d894-106">ID3DX11EffectTechnique:: ComputeStateBlockMask (método)</span><span class="sxs-lookup"><span data-stu-id="0d894-106">ID3DX11EffectTechnique::ComputeStateBlockMask method</span></span>

<span data-ttu-id="0d894-107">Calcule una máscara de bloque de estado para permitir o impedir los cambios de estado.</span><span class="sxs-lookup"><span data-stu-id="0d894-107">Compute a state-block mask to allow/prevent state changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d894-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0d894-108">Syntax</span></span>


```C++
HRESULT ComputeStateBlockMask(
   D3DX11_STATE_BLOCK_MASK *pStateBlockMask
);
```



## <a name="parameters"></a><span data-ttu-id="0d894-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0d894-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d894-110">*pStateBlockMask*</span><span class="sxs-lookup"><span data-stu-id="0d894-110">*pStateBlockMask*</span></span> 
</dt> <dd>

<span data-ttu-id="0d894-111">Tipo: **[ **\_ máscara de \_ bloque \_ de estado de D3DX11**](d3dx11-state-block-mask.md)\***</span><span class="sxs-lookup"><span data-stu-id="0d894-111">Type: **[**D3DX11\_STATE\_BLOCK\_MASK**](d3dx11-state-block-mask.md)\***</span></span>

<span data-ttu-id="0d894-112">Un puntero a una máscara de bloque de estado (consulte [**D3DX11 \_ State \_ Block \_ Mask**](d3dx11-state-block-mask.md)).</span><span class="sxs-lookup"><span data-stu-id="0d894-112">A pointer to a state-block mask (see [**D3DX11\_STATE\_BLOCK\_MASK**](d3dx11-state-block-mask.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d894-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0d894-113">Return value</span></span>

<span data-ttu-id="0d894-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0d894-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0d894-115">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="0d894-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0d894-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0d894-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0d894-117">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="0d894-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="0d894-118">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="0d894-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="0d894-119">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="0d894-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0d894-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d894-120">Requirements</span></span>



| <span data-ttu-id="0d894-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d894-121">Requirement</span></span> | <span data-ttu-id="0d894-122">Value</span><span class="sxs-lookup"><span data-stu-id="0d894-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d894-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0d894-123">Header</span></span><br/>  | <dl> <span data-ttu-id="0d894-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d894-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="0d894-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0d894-125">Library</span></span><br/> | <dl> <span data-ttu-id="0d894-126"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="0d894-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d894-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="0d894-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d894-128">ID3DX11EffectTechnique</span><span class="sxs-lookup"><span data-stu-id="0d894-128">ID3DX11EffectTechnique</span></span>](id3dx11effecttechnique.md)
</dt> </dl>

 

 





