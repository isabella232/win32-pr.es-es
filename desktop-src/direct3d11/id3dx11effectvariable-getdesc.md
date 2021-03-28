---
title: Método ID3DX11EffectVariable GetDesc (D3dx11effect. h)
description: Obtener una descripción.
ms.assetid: bf6339d7-8eb0-44da-893e-c805309a3cd3
keywords:
- Método GetDesc Direct3D 11
- Método GetDesc Direct3D 11, interfaz ID3DX11EffectVariable
- Interfaz ID3DX11EffectVariable Direct3D 11, método GetDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1625b9d72b3ff4afe1880b48125d244da1f68844
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998754"
---
# <a name="id3dx11effectvariablegetdesc-method"></a><span data-ttu-id="5d39c-106">ID3DX11EffectVariable:: GetDesc (método)</span><span class="sxs-lookup"><span data-stu-id="5d39c-106">ID3DX11EffectVariable::GetDesc method</span></span>

<span data-ttu-id="5d39c-107">Obtener una descripción.</span><span class="sxs-lookup"><span data-stu-id="5d39c-107">Get a description.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d39c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5d39c-108">Syntax</span></span>


```C++
HRESULT GetDesc(
   D3DX11_EFFECT_VARIABLE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="5d39c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5d39c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d39c-110">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="5d39c-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="5d39c-111">Tipo: **[ **D3DX11 \_ efecto \_ \_ DESC de variable**](d3dx11-effect-variable-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="5d39c-111">Type: **[**D3DX11\_EFFECT\_VARIABLE\_DESC**](d3dx11-effect-variable-desc.md)\***</span></span>

<span data-ttu-id="5d39c-112">Un puntero a una descripción de variable de efecto (consulte [**D3DX11 \_ Effect \_ variable \_ DESC**](d3dx11-effect-variable-desc.md)).</span><span class="sxs-lookup"><span data-stu-id="5d39c-112">A pointer to an effect-variable description (see [**D3DX11\_EFFECT\_VARIABLE\_DESC**](d3dx11-effect-variable-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d39c-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5d39c-113">Return value</span></span>

<span data-ttu-id="5d39c-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5d39c-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5d39c-115">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="5d39c-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5d39c-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5d39c-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5d39c-117">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="5d39c-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="5d39c-118">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="5d39c-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="5d39c-119">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="5d39c-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5d39c-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d39c-120">Requirements</span></span>



| <span data-ttu-id="5d39c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d39c-121">Requirement</span></span> | <span data-ttu-id="5d39c-122">Value</span><span class="sxs-lookup"><span data-stu-id="5d39c-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d39c-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5d39c-123">Header</span></span><br/>  | <dl> <span data-ttu-id="5d39c-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d39c-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="5d39c-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5d39c-125">Library</span></span><br/> | <dl> <span data-ttu-id="5d39c-126"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="5d39c-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d39c-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="5d39c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d39c-128">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="5d39c-128">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





