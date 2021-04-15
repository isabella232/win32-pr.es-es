---
title: Método ID3DX11EffectVariable AsConstantBuffer (D3dx11effect. h)
description: Obtiene un búfer de constantes. | Método ID3DX11EffectVariable AsConstantBuffer (D3dx11effect. h)
ms.assetid: b8d8b43c-4626-43b6-8a49-8ffa7cb48427
keywords:
- Método AsConstantBuffer Direct3D 11
- Método AsConstantBuffer Direct3D 11, interfaz ID3DX11EffectVariable
- Interfaz ID3DX11EffectVariable Direct3D 11, método AsConstantBuffer
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee4caca60216df0c04a773da22150dbc6f7be717
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998431"
---
# <a name="id3dx11effectvariableasconstantbuffer-method"></a><span data-ttu-id="a0fb8-107">ID3DX11EffectVariable:: AsConstantBuffer (método)</span><span class="sxs-lookup"><span data-stu-id="a0fb8-107">ID3DX11EffectVariable::AsConstantBuffer method</span></span>

<span data-ttu-id="a0fb8-108">Obtiene un búfer de constantes.</span><span class="sxs-lookup"><span data-stu-id="a0fb8-108">Get a constant buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0fb8-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a0fb8-109">Syntax</span></span>


```C++
ID3DX11EffectConstantBuffer* AsConstantBuffer();
```



## <a name="parameters"></a><span data-ttu-id="a0fb8-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a0fb8-110">Parameters</span></span>

<span data-ttu-id="a0fb8-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="a0fb8-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a0fb8-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a0fb8-112">Return value</span></span>

<span data-ttu-id="a0fb8-113">Tipo: **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="a0fb8-113">Type: **[**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span></span>

<span data-ttu-id="a0fb8-114">Un puntero a un búfer de constantes.</span><span class="sxs-lookup"><span data-stu-id="a0fb8-114">A pointer to a constant buffer.</span></span> <span data-ttu-id="a0fb8-115">Vea [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="a0fb8-115">See [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a0fb8-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a0fb8-116">Remarks</span></span>

<span data-ttu-id="a0fb8-117">AsConstantBuffer devuelve una versión de la variable de efecto que se ha especializado en un búfer de constantes.</span><span class="sxs-lookup"><span data-stu-id="a0fb8-117">AsConstantBuffer returns a version of the effect variable that has been specialized to a constant buffer.</span></span> <span data-ttu-id="a0fb8-118">De forma similar a una conversión, esta especialización devolverá un objeto no válido si la variable de efecto no contiene datos de búfer de constantes.</span><span class="sxs-lookup"><span data-stu-id="a0fb8-118">Similar to a cast, this specialization will return an invalid object if the effect variable does not contain constant buffer data.</span></span>

<span data-ttu-id="a0fb8-119">Las aplicaciones pueden probar la validez del objeto devuelto mediante una llamada a [**IsValid**](id3dx11effectvariable-isvalid.md).</span><span class="sxs-lookup"><span data-stu-id="a0fb8-119">Applications can test the returned object for validity by calling [**IsValid**](id3dx11effectvariable-isvalid.md).</span></span>

> [!Note]  
> <span data-ttu-id="a0fb8-120">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="a0fb8-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="a0fb8-121">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="a0fb8-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="a0fb8-122">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="a0fb8-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a0fb8-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0fb8-123">Requirements</span></span>



| <span data-ttu-id="a0fb8-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0fb8-124">Requirement</span></span> | <span data-ttu-id="a0fb8-125">Value</span><span class="sxs-lookup"><span data-stu-id="a0fb8-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0fb8-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a0fb8-126">Header</span></span><br/>  | <dl> <span data-ttu-id="a0fb8-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0fb8-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="a0fb8-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a0fb8-128">Library</span></span><br/> | <dl> <span data-ttu-id="a0fb8-129"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="a0fb8-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0fb8-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="a0fb8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0fb8-131">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="a0fb8-131">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





