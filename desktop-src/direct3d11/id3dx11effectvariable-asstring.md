---
title: Método AsString ID3DX11EffectVariable (D3dx11effect. h)
description: Obtiene una variable de cadena.
ms.assetid: 60f8a730-bf95-4577-9259-7348d479ac3d
keywords:
- AsString (método) Direct3D 11
- AsString (método) Direct3D 11, ID3DX11EffectVariable (interfaz)
- Interfaz ID3DX11EffectVariable Direct3D 11, AsString (método)
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsString
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73092dcd27b5651ad6205fa05bcbb13cc1f86116
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362828"
---
# <a name="id3dx11effectvariableasstring-method"></a><span data-ttu-id="d3c62-106">ID3DX11EffectVariable:: AsString (método)</span><span class="sxs-lookup"><span data-stu-id="d3c62-106">ID3DX11EffectVariable::AsString method</span></span>

<span data-ttu-id="d3c62-107">Obtiene una variable de cadena.</span><span class="sxs-lookup"><span data-stu-id="d3c62-107">Get a string variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3c62-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d3c62-108">Syntax</span></span>


```C++
ID3DX11EffectStringVariable* AsString();
```



## <a name="parameters"></a><span data-ttu-id="d3c62-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d3c62-109">Parameters</span></span>

<span data-ttu-id="d3c62-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="d3c62-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d3c62-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d3c62-111">Return value</span></span>

<span data-ttu-id="d3c62-112">Tipo: **[ **ID3DX11EffectStringVariable**](id3dx11effectstringvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="d3c62-112">Type: **[**ID3DX11EffectStringVariable**](id3dx11effectstringvariable.md)\***</span></span>

<span data-ttu-id="d3c62-113">Puntero a una variable de cadena.</span><span class="sxs-lookup"><span data-stu-id="d3c62-113">A pointer to a string variable.</span></span> <span data-ttu-id="d3c62-114">Vea [**ID3DX11EffectStringVariable**](id3dx11effectstringvariable.md).</span><span class="sxs-lookup"><span data-stu-id="d3c62-114">See [**ID3DX11EffectStringVariable**](id3dx11effectstringvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d3c62-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d3c62-115">Remarks</span></span>

<span data-ttu-id="d3c62-116">AsString devuelve una versión de la variable de efecto que se ha especializado en una variable de cadena.</span><span class="sxs-lookup"><span data-stu-id="d3c62-116">AsString returns a version of the effect variable that has been specialized to a string variable.</span></span> <span data-ttu-id="d3c62-117">De forma similar a una conversión, esta especialización devolverá un objeto no válido si la variable de efecto no contiene datos de cadena.</span><span class="sxs-lookup"><span data-stu-id="d3c62-117">Similar to a cast, this specialization will return an invalid object if the effect variable does not contain string data.</span></span>

<span data-ttu-id="d3c62-118">Las aplicaciones pueden probar la validez del objeto devuelto mediante una llamada a [**IsValid**](id3dx11effectvariable-isvalid.md).</span><span class="sxs-lookup"><span data-stu-id="d3c62-118">Applications can test the returned object for validity by calling [**IsValid**](id3dx11effectvariable-isvalid.md).</span></span>

> [!Note]  
> <span data-ttu-id="d3c62-119">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="d3c62-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="d3c62-120">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="d3c62-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="d3c62-121">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="d3c62-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d3c62-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3c62-122">Requirements</span></span>



| <span data-ttu-id="d3c62-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3c62-123">Requirement</span></span> | <span data-ttu-id="d3c62-124">Value</span><span class="sxs-lookup"><span data-stu-id="d3c62-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3c62-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d3c62-125">Header</span></span><br/>  | <dl> <span data-ttu-id="d3c62-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3c62-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="d3c62-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d3c62-127">Library</span></span><br/> | <dl> <span data-ttu-id="d3c62-128"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="d3c62-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3c62-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="d3c62-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3c62-130">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="d3c62-130">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





