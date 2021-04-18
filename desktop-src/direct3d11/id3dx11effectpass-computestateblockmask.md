---
title: Método ID3DX11EffectPass ComputeStateBlockMask (D3dx11effect. h)
description: Generar una máscara para permitir o evitar cambios de estado.
ms.assetid: 584be931-0e22-43e6-b852-f0d2ab050bdd
keywords:
- Método ComputeStateBlockMask Direct3D 11
- Método ComputeStateBlockMask Direct3D 11, interfaz ID3DX11EffectPass
- Interfaz ID3DX11EffectPass Direct3D 11, método ComputeStateBlockMask
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.ComputeStateBlockMask
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8fc5cb32ce9e9644d7d5b62868bfa99f150cc94
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987037"
---
# <a name="id3dx11effectpasscomputestateblockmask-method"></a><span data-ttu-id="7ca1e-106">ID3DX11EffectPass:: ComputeStateBlockMask (método)</span><span class="sxs-lookup"><span data-stu-id="7ca1e-106">ID3DX11EffectPass::ComputeStateBlockMask method</span></span>

<span data-ttu-id="7ca1e-107">Generar una máscara para permitir o evitar cambios de estado.</span><span class="sxs-lookup"><span data-stu-id="7ca1e-107">Generate a mask for allowing/preventing state changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ca1e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7ca1e-108">Syntax</span></span>


```C++
HRESULT ComputeStateBlockMask(
   D3DX11_STATE_BLOCK_MASK *pStateBlockMask
);
```



## <a name="parameters"></a><span data-ttu-id="7ca1e-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7ca1e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ca1e-110">*pStateBlockMask*</span><span class="sxs-lookup"><span data-stu-id="7ca1e-110">*pStateBlockMask*</span></span> 
</dt> <dd>

<span data-ttu-id="7ca1e-111">Tipo: **[ **\_ máscara de \_ bloque \_ de estado de D3DX11**](d3dx11-state-block-mask.md)\***</span><span class="sxs-lookup"><span data-stu-id="7ca1e-111">Type: **[**D3DX11\_STATE\_BLOCK\_MASK**](d3dx11-state-block-mask.md)\***</span></span>

<span data-ttu-id="7ca1e-112">Un puntero a una máscara de bloque de estado (consulte [**D3DX11 \_ State \_ Block \_ Mask**](d3dx11-state-block-mask.md)).</span><span class="sxs-lookup"><span data-stu-id="7ca1e-112">A pointer to a state-block mask (see [**D3DX11\_STATE\_BLOCK\_MASK**](d3dx11-state-block-mask.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ca1e-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7ca1e-113">Return value</span></span>

<span data-ttu-id="7ca1e-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7ca1e-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7ca1e-115">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="7ca1e-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7ca1e-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7ca1e-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7ca1e-117">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="7ca1e-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="7ca1e-118">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="7ca1e-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="7ca1e-119">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="7ca1e-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7ca1e-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ca1e-120">Requirements</span></span>



| <span data-ttu-id="7ca1e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ca1e-121">Requirement</span></span> | <span data-ttu-id="7ca1e-122">Value</span><span class="sxs-lookup"><span data-stu-id="7ca1e-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ca1e-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7ca1e-123">Header</span></span><br/>  | <dl> <span data-ttu-id="7ca1e-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ca1e-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="7ca1e-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7ca1e-125">Library</span></span><br/> | <dl> <span data-ttu-id="7ca1e-126"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="7ca1e-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ca1e-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="7ca1e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ca1e-128">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="7ca1e-128">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

 





