---
title: Método ID3DX11Effect GetVariableByIndex (D3dx11effect. h)
description: Obtiene una variable por índice.
ms.assetid: af25b945-9526-45c2-8746-8b62f8166de7
keywords:
- Método GetVariableByIndex Direct3D 11
- Método GetVariableByIndex Direct3D 11, interfaz ID3DX11Effect
- Interfaz ID3DX11Effect Direct3D 11, método GetVariableByIndex
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetVariableByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd262ea0aa778f03c2d723dec99f531f3419f3be
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998616"
---
# <a name="id3dx11effectgetvariablebyindex-method"></a><span data-ttu-id="832c7-106">ID3DX11Effect:: GetVariableByIndex (método)</span><span class="sxs-lookup"><span data-stu-id="832c7-106">ID3DX11Effect::GetVariableByIndex method</span></span>

<span data-ttu-id="832c7-107">Obtiene una variable por índice.</span><span class="sxs-lookup"><span data-stu-id="832c7-107">Get a variable by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="832c7-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="832c7-108">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetVariableByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="832c7-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="832c7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="832c7-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="832c7-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="832c7-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="832c7-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="832c7-112">Un índice basado en cero.</span><span class="sxs-lookup"><span data-stu-id="832c7-112">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="832c7-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="832c7-113">Return value</span></span>

<span data-ttu-id="832c7-114">Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="832c7-114">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="832c7-115">Un puntero a un [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="832c7-115">A pointer to a [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="832c7-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="832c7-116">Remarks</span></span>

<span data-ttu-id="832c7-117">Un efecto puede contener una o más variables.</span><span class="sxs-lookup"><span data-stu-id="832c7-117">An effect may contain one or more variables.</span></span> <span data-ttu-id="832c7-118">Las variables fuera de una técnica se consideran globales para todos los efectos, las que se encuentran dentro de una técnica son locales para esa técnica.</span><span class="sxs-lookup"><span data-stu-id="832c7-118">Variables outside of a technique are considered global to all effects, those located inside of a technique are local to that technique.</span></span> <span data-ttu-id="832c7-119">Puede tener acceso a cualquier variable de efecto no estático local mediante su nombre o con un índice.</span><span class="sxs-lookup"><span data-stu-id="832c7-119">You can access any local non-static effect variable using its name or with an index.</span></span>

<span data-ttu-id="832c7-120">El método devuelve un puntero a una [**interfaz de variable de efecto**](id3dx11effectvariable.md) si no se encuentra una variable; puede llamar a [**ID3DX11Effect:: IsValid**](id3dx11effect-isvalid.md) para comprobar si el índice existe o no.</span><span class="sxs-lookup"><span data-stu-id="832c7-120">The method returns a pointer to an [**effect-variable interface**](id3dx11effectvariable.md) if a variable is not found; you can call [**ID3DX11Effect::IsValid**](id3dx11effect-isvalid.md) to verify whether or not the index exists.</span></span>

> [!Note]  
> <span data-ttu-id="832c7-121">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="832c7-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="832c7-122">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="832c7-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="832c7-123">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="832c7-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="832c7-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="832c7-124">Requirements</span></span>



| <span data-ttu-id="832c7-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="832c7-125">Requirement</span></span> | <span data-ttu-id="832c7-126">Value</span><span class="sxs-lookup"><span data-stu-id="832c7-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="832c7-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="832c7-127">Header</span></span><br/>  | <dl> <span data-ttu-id="832c7-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="832c7-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="832c7-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="832c7-129">Library</span></span><br/> | <dl> <span data-ttu-id="832c7-130"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="832c7-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="832c7-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="832c7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="832c7-132">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="832c7-132">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

