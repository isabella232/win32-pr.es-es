---
title: Método ID3DX11EffectVariable AsUnorderedAccessView (D3dx11effect. h)
description: Obtiene una variable de vista de acceso sin ordenar.
ms.assetid: e8b7c104-09f7-4bfb-9980-a5603550b723
keywords:
- Método AsUnorderedAccessView Direct3D 11
- Método AsUnorderedAccessView Direct3D 11, interfaz ID3DX11EffectVariable
- Interfaz ID3DX11EffectVariable Direct3D 11, método AsUnorderedAccessView
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsUnorderedAccessView
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8b9ce7dbbc99ef16ef3290ec1ba3135a8d2cb05
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821538"
---
# <a name="id3dx11effectvariableasunorderedaccessview-method"></a><span data-ttu-id="05b82-106">ID3DX11EffectVariable:: AsUnorderedAccessView (método)</span><span class="sxs-lookup"><span data-stu-id="05b82-106">ID3DX11EffectVariable::AsUnorderedAccessView method</span></span>

<span data-ttu-id="05b82-107">Obtiene una variable de vista de acceso sin ordenar.</span><span class="sxs-lookup"><span data-stu-id="05b82-107">Get an unordered-access-view variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="05b82-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="05b82-108">Syntax</span></span>


```C++
ID3DX11EffectUnorderedAccessViewVariable* AsUnorderedAccessView();
```



## <a name="parameters"></a><span data-ttu-id="05b82-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="05b82-109">Parameters</span></span>

<span data-ttu-id="05b82-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="05b82-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="05b82-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="05b82-111">Return value</span></span>

<span data-ttu-id="05b82-112">Tipo: **[ **ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="05b82-112">Type: **[**ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md)\***</span></span>

<span data-ttu-id="05b82-113">Puntero a una variable de vista de acceso sin ordenar.</span><span class="sxs-lookup"><span data-stu-id="05b82-113">A pointer to an unordered-access-view variable.</span></span> <span data-ttu-id="05b82-114">Vea [**ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md).</span><span class="sxs-lookup"><span data-stu-id="05b82-114">See [**ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="05b82-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="05b82-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="05b82-116">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="05b82-116">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="05b82-117">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="05b82-117">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="05b82-118">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="05b82-118">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="05b82-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05b82-119">Requirements</span></span>



| <span data-ttu-id="05b82-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="05b82-120">Requirement</span></span> | <span data-ttu-id="05b82-121">Value</span><span class="sxs-lookup"><span data-stu-id="05b82-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05b82-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="05b82-122">Header</span></span><br/>  | <dl> <span data-ttu-id="05b82-123"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="05b82-123"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="05b82-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="05b82-124">Library</span></span><br/> | <dl> <span data-ttu-id="05b82-125"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="05b82-125"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05b82-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="05b82-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05b82-127">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="05b82-127">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





