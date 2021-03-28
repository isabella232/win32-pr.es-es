---
title: Método asrasterizador ID3DX11EffectVariable (D3dx11effect. h)
description: Obtiene una variable de rasterizador.
ms.assetid: 6a55d067-f527-4a1b-a4d4-a6d1719aebe7
keywords:
- Método asrasterizador de Direct3D 11
- Método asrasterizador Direct3D 11, ID3DX11EffectVariable (interfaz)
- Interfaz ID3DX11EffectVariable Direct3D 11, método asrasterizador
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsRasterizer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cbe4edc1b1195a9d449b37897f0875b1f35aae3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998784"
---
# <a name="id3dx11effectvariableasrasterizer-method"></a><span data-ttu-id="01556-106">ID3DX11EffectVariable:: asrasterizador (método)</span><span class="sxs-lookup"><span data-stu-id="01556-106">ID3DX11EffectVariable::AsRasterizer method</span></span>

<span data-ttu-id="01556-107">Obtiene una variable de rasterizador.</span><span class="sxs-lookup"><span data-stu-id="01556-107">Get a rasterizer variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="01556-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="01556-108">Syntax</span></span>


```C++
ID3DX11EffectRasterizerVariable* AsRasterizer();
```



## <a name="parameters"></a><span data-ttu-id="01556-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="01556-109">Parameters</span></span>

<span data-ttu-id="01556-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="01556-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="01556-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="01556-111">Return value</span></span>

<span data-ttu-id="01556-112">Tipo: **[ **ID3DX11EffectRasterizerVariable**](id3dx11effectrasterizervariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="01556-112">Type: **[**ID3DX11EffectRasterizerVariable**](id3dx11effectrasterizervariable.md)\***</span></span>

<span data-ttu-id="01556-113">Puntero a una variable de rasterizador.</span><span class="sxs-lookup"><span data-stu-id="01556-113">A pointer to a rasterizer variable.</span></span> <span data-ttu-id="01556-114">Vea [**ID3DX11EffectRasterizerVariable**](id3dx11effectrasterizervariable.md).</span><span class="sxs-lookup"><span data-stu-id="01556-114">See [**ID3DX11EffectRasterizerVariable**](id3dx11effectrasterizervariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="01556-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="01556-115">Remarks</span></span>

<span data-ttu-id="01556-116">Asrasterizador devuelve una versión de la variable de efecto que se ha especializado en una variable de rasterizador.</span><span class="sxs-lookup"><span data-stu-id="01556-116">AsRasterizer returns a version of the effect variable that has been specialized to a rasterizer variable.</span></span> <span data-ttu-id="01556-117">De forma similar a una conversión, esta especialización devolverá un objeto no válido si la variable de efecto no contiene datos de rasterizador.</span><span class="sxs-lookup"><span data-stu-id="01556-117">Similar to a cast, this specialization will return an invalid object if the effect variable does not contain rasterizer data.</span></span>

<span data-ttu-id="01556-118">Las aplicaciones pueden probar la validez del objeto devuelto mediante una llamada a [**IsValid**](id3dx11effectvariable-isvalid.md).</span><span class="sxs-lookup"><span data-stu-id="01556-118">Applications can test the returned object for validity by calling [**IsValid**](id3dx11effectvariable-isvalid.md).</span></span>

> [!Note]  
> <span data-ttu-id="01556-119">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="01556-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="01556-120">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="01556-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="01556-121">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="01556-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="01556-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01556-122">Requirements</span></span>



| <span data-ttu-id="01556-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="01556-123">Requirement</span></span> | <span data-ttu-id="01556-124">Value</span><span class="sxs-lookup"><span data-stu-id="01556-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01556-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="01556-125">Header</span></span><br/>  | <dl> <span data-ttu-id="01556-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="01556-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="01556-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="01556-127">Library</span></span><br/> | <dl> <span data-ttu-id="01556-128"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="01556-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01556-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="01556-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01556-130">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="01556-130">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





