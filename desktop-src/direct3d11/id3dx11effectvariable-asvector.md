---
title: Método asvector ID3DX11EffectVariable (D3dx11effect. h)
description: Obtiene una variable de vector.
ms.assetid: 995bd9f3-1417-4048-9a23-4dcb3864c77d
keywords:
- Método asvector de Direct3D 11
- Método asvector de Direct3D 11, interfaz ID3DX11EffectVariable
- Interfaz ID3DX11EffectVariable Direct3D 11, método asvector
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsVector
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8df994536c818461b0307cdee726e704aaaf8a43
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998713"
---
# <a name="id3dx11effectvariableasvector-method"></a><span data-ttu-id="253e6-106">ID3DX11EffectVariable:: asvector (método)</span><span class="sxs-lookup"><span data-stu-id="253e6-106">ID3DX11EffectVariable::AsVector method</span></span>

<span data-ttu-id="253e6-107">Obtiene una variable de vector.</span><span class="sxs-lookup"><span data-stu-id="253e6-107">Get a vector variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="253e6-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="253e6-108">Syntax</span></span>


```C++
ID3DX11EffectVectorVariable* AsVector();
```



## <a name="parameters"></a><span data-ttu-id="253e6-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="253e6-109">Parameters</span></span>

<span data-ttu-id="253e6-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="253e6-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="253e6-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="253e6-111">Return value</span></span>

<span data-ttu-id="253e6-112">Tipo: **[ **ID3DX11EffectVectorVariable**](id3dx11effectvectorvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="253e6-112">Type: **[**ID3DX11EffectVectorVariable**](id3dx11effectvectorvariable.md)\***</span></span>

<span data-ttu-id="253e6-113">Puntero a una variable de vector.</span><span class="sxs-lookup"><span data-stu-id="253e6-113">A pointer to a vector variable.</span></span> <span data-ttu-id="253e6-114">Vea [**ID3DX11EffectVectorVariable**](id3dx11effectvectorvariable.md).</span><span class="sxs-lookup"><span data-stu-id="253e6-114">See [**ID3DX11EffectVectorVariable**](id3dx11effectvectorvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="253e6-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="253e6-115">Remarks</span></span>

<span data-ttu-id="253e6-116">Asvector devuelve una versión de la variable de efecto que se ha especializado en una variable de vector.</span><span class="sxs-lookup"><span data-stu-id="253e6-116">AsVector returns a version of the effect variable that has been specialized to a vector variable.</span></span> <span data-ttu-id="253e6-117">De forma similar a una conversión, esta especialización devolverá un objeto no válido si la variable de efecto no contiene datos vectoriales.</span><span class="sxs-lookup"><span data-stu-id="253e6-117">Similar to a cast, this specialization will return an invalid object if the effect variable does not contain vector data.</span></span>

<span data-ttu-id="253e6-118">Las aplicaciones pueden probar la validez del objeto devuelto mediante una llamada a [**IsValid**](id3dx11effectvariable-isvalid.md).</span><span class="sxs-lookup"><span data-stu-id="253e6-118">Applications can test the returned object for validity by calling [**IsValid**](id3dx11effectvariable-isvalid.md).</span></span>

> [!Note]  
> <span data-ttu-id="253e6-119">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="253e6-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="253e6-120">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="253e6-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="253e6-121">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="253e6-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="253e6-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="253e6-122">Requirements</span></span>



| <span data-ttu-id="253e6-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="253e6-123">Requirement</span></span> | <span data-ttu-id="253e6-124">Value</span><span class="sxs-lookup"><span data-stu-id="253e6-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="253e6-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="253e6-125">Header</span></span><br/>  | <dl> <span data-ttu-id="253e6-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="253e6-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="253e6-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="253e6-127">Library</span></span><br/> | <dl> <span data-ttu-id="253e6-128"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="253e6-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="253e6-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="253e6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="253e6-130">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="253e6-130">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





