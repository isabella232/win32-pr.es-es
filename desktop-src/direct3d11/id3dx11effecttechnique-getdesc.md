---
title: Método ID3DX11EffectTechnique GetDesc (D3dx11effect. h)
description: Obtener una descripción de la técnica.
ms.assetid: ed82d873-0540-4aa8-ac0f-198852b886ad
keywords:
- Método GetDesc Direct3D 11
- Método GetDesc Direct3D 11, interfaz ID3DX11EffectTechnique
- Interfaz ID3DX11EffectTechnique Direct3D 11, método GetDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b847bd8381ec7d190931c04e5940f713676ff0b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998353"
---
# <a name="id3dx11effecttechniquegetdesc-method"></a><span data-ttu-id="4b97f-106">ID3DX11EffectTechnique:: GetDesc (método)</span><span class="sxs-lookup"><span data-stu-id="4b97f-106">ID3DX11EffectTechnique::GetDesc method</span></span>

<span data-ttu-id="4b97f-107">Obtener una descripción de la técnica.</span><span class="sxs-lookup"><span data-stu-id="4b97f-107">Get a technique description.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b97f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4b97f-108">Syntax</span></span>


```C++
HRESULT GetDesc(
   D3DX11_TECHNIQUE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="4b97f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4b97f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b97f-110">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="4b97f-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="4b97f-111">Tipo: **[ **D3DX11 \_ técnica \_ DESC**](d3dx11-technique-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="4b97f-111">Type: **[**D3DX11\_TECHNIQUE\_DESC**](d3dx11-technique-desc.md)\***</span></span>

<span data-ttu-id="4b97f-112">Un puntero a una descripción de la técnica (vea [**D3DX11 ( \_ técnica) \_ DESC**](d3dx11-technique-desc.md)).</span><span class="sxs-lookup"><span data-stu-id="4b97f-112">A pointer to a technique description (see [**D3DX11\_TECHNIQUE\_DESC**](d3dx11-technique-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b97f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4b97f-113">Return value</span></span>

<span data-ttu-id="4b97f-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4b97f-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4b97f-115">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="4b97f-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4b97f-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4b97f-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4b97f-117">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="4b97f-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="4b97f-118">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="4b97f-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="4b97f-119">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="4b97f-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4b97f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b97f-120">Requirements</span></span>



| <span data-ttu-id="4b97f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b97f-121">Requirement</span></span> | <span data-ttu-id="4b97f-122">Value</span><span class="sxs-lookup"><span data-stu-id="4b97f-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b97f-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4b97f-123">Header</span></span><br/>  | <dl> <span data-ttu-id="4b97f-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b97f-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="4b97f-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4b97f-125">Library</span></span><br/> | <dl> <span data-ttu-id="4b97f-126"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="4b97f-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b97f-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="4b97f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b97f-128">ID3DX11EffectTechnique</span><span class="sxs-lookup"><span data-stu-id="4b97f-128">ID3DX11EffectTechnique</span></span>](id3dx11effecttechnique.md)
</dt> </dl>

 

 





