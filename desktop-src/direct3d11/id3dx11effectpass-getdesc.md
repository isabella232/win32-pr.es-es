---
title: Método ID3DX11EffectPass GetDesc (D3dx11effect. h)
description: Obtener una descripción del paso.
ms.assetid: 423766be-96b2-4038-834e-34125789e8b1
keywords:
- Método GetDesc Direct3D 11
- Método GetDesc Direct3D 11, interfaz ID3DX11EffectPass
- Interfaz ID3DX11EffectPass Direct3D 11, método GetDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a85a8c08faa100ecb3987a1a1421613d9c448b8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362648"
---
# <a name="id3dx11effectpassgetdesc-method"></a><span data-ttu-id="3a6e7-106">ID3DX11EffectPass:: GetDesc (método)</span><span class="sxs-lookup"><span data-stu-id="3a6e7-106">ID3DX11EffectPass::GetDesc method</span></span>

<span data-ttu-id="3a6e7-107">Obtener una descripción del paso.</span><span class="sxs-lookup"><span data-stu-id="3a6e7-107">Get a pass description.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a6e7-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3a6e7-108">Syntax</span></span>


```C++
HRESULT GetDesc(
   D3DX11_PASS_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="3a6e7-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3a6e7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a6e7-110">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="3a6e7-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="3a6e7-111">Tipo: **[ **D3DX11 \_ Pass \_ DESC**](d3dx11-pass-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="3a6e7-111">Type: **[**D3DX11\_PASS\_DESC**](d3dx11-pass-desc.md)\***</span></span>

<span data-ttu-id="3a6e7-112">Un puntero a una descripción de paso (vea [**D3DX11 \_ Pass \_ DESC**](d3dx11-pass-desc.md)).</span><span class="sxs-lookup"><span data-stu-id="3a6e7-112">A pointer to a pass description (see [**D3DX11\_PASS\_DESC**](d3dx11-pass-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a6e7-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3a6e7-113">Return value</span></span>

<span data-ttu-id="3a6e7-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3a6e7-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3a6e7-115">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="3a6e7-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3a6e7-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3a6e7-116">Remarks</span></span>

<span data-ttu-id="3a6e7-117">Un paso es un bloque de código que establece los sombreadores y el estado de representación (que, a su vez, establece búferes de constantes, muestras y texturas).</span><span class="sxs-lookup"><span data-stu-id="3a6e7-117">A pass is a block of code that sets render state and shaders (which in turn sets constant buffers, samplers and textures).</span></span> <span data-ttu-id="3a6e7-118">Una técnica de efecto contiene una o varias fases.</span><span class="sxs-lookup"><span data-stu-id="3a6e7-118">An effect technique contains one or more passes.</span></span>

> [!Note]  
> <span data-ttu-id="3a6e7-119">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="3a6e7-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="3a6e7-120">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="3a6e7-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="3a6e7-121">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="3a6e7-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3a6e7-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a6e7-122">Requirements</span></span>



| <span data-ttu-id="3a6e7-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a6e7-123">Requirement</span></span> | <span data-ttu-id="3a6e7-124">Value</span><span class="sxs-lookup"><span data-stu-id="3a6e7-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a6e7-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3a6e7-125">Header</span></span><br/>  | <dl> <span data-ttu-id="3a6e7-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a6e7-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="3a6e7-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3a6e7-127">Library</span></span><br/> | <dl> <span data-ttu-id="3a6e7-128"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="3a6e7-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a6e7-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="3a6e7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a6e7-130">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="3a6e7-130">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

 





