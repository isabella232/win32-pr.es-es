---
title: Función D3D12CalcSubresource (D3dx12. h)
description: Calcula un índice de subrecurso para una textura.
ms.assetid: 5C63A315-E21E-498B-A832-6BA2D17FF9A7
keywords:
- D3D12CalcSubresource función)
topic_type:
- apiref
api_name:
- D3D12CalcSubresource
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e872d13ba5221ad50003d789b87f65fc64821dd0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707758"
---
# <a name="d3d12calcsubresource-function"></a><span data-ttu-id="a84dd-104">D3D12CalcSubresource función)</span><span class="sxs-lookup"><span data-stu-id="a84dd-104">D3D12CalcSubresource function</span></span>

<span data-ttu-id="a84dd-105">Calcula un índice de subrecurso para una textura.</span><span class="sxs-lookup"><span data-stu-id="a84dd-105">Calculates a subresource index for a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="a84dd-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a84dd-106">Syntax</span></span>


```C++
UINT inline D3D12CalcSubresource(
   UINT MipSlice,
   UINT ArraySlice,
   UINT PlaneSlice,
   UINT MipLevels,
   UINT ArraySize
);
```



## <a name="parameters"></a><span data-ttu-id="a84dd-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a84dd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a84dd-108">*MipSlice*</span><span class="sxs-lookup"><span data-stu-id="a84dd-108">*MipSlice*</span></span> 
</dt> <dd>

<span data-ttu-id="a84dd-109">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a84dd-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a84dd-110">Índice de base cero del nivel de mipmap que se va a direccionar; 0 indica el primer nivel de mapa MIP más detallado.</span><span class="sxs-lookup"><span data-stu-id="a84dd-110">The zero-based index for the mipmap level to address; 0 indicates the first, most detailed mipmap level.</span></span>

</dd> <dt>

<span data-ttu-id="a84dd-111">*ArraySlice*</span><span class="sxs-lookup"><span data-stu-id="a84dd-111">*ArraySlice*</span></span> 
</dt> <dd>

<span data-ttu-id="a84dd-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a84dd-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a84dd-113">Índice de base cero para el nivel de matriz que se va a direccionar; Use siempre 0 para las texturas de volumen (3D).</span><span class="sxs-lookup"><span data-stu-id="a84dd-113">The zero-based index for the array level to address; always use 0 for volume (3D) textures.</span></span>

</dd> <dt>

<span data-ttu-id="a84dd-114">*PlaneSlice*</span><span class="sxs-lookup"><span data-stu-id="a84dd-114">*PlaneSlice*</span></span> 
</dt> <dd>

<span data-ttu-id="a84dd-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a84dd-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a84dd-116">Índice de base cero para el nivel de plano que se va a direccionar.</span><span class="sxs-lookup"><span data-stu-id="a84dd-116">The zero-based index for the plane level to address.</span></span>

</dd> <dt>

<span data-ttu-id="a84dd-117">*MipLevels*</span><span class="sxs-lookup"><span data-stu-id="a84dd-117">*MipLevels*</span></span> 
</dt> <dd>

<span data-ttu-id="a84dd-118">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a84dd-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a84dd-119">El número de niveles de mipmap en el recurso.</span><span class="sxs-lookup"><span data-stu-id="a84dd-119">The number of mipmap levels in the resource.</span></span>

</dd> <dt>

<span data-ttu-id="a84dd-120">*ArraySize*</span><span class="sxs-lookup"><span data-stu-id="a84dd-120">*ArraySize*</span></span> 
</dt> <dd>

<span data-ttu-id="a84dd-121">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a84dd-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a84dd-122">Número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="a84dd-122">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a84dd-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a84dd-123">Return value</span></span>

<span data-ttu-id="a84dd-124">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a84dd-124">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a84dd-125">Índice que es igual a MipSlice + (ArraySlice \* MipLevels).</span><span class="sxs-lookup"><span data-stu-id="a84dd-125">The index which equals MipSlice + (ArraySlice \* MipLevels).</span></span>

## <a name="remarks"></a><span data-ttu-id="a84dd-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a84dd-126">Remarks</span></span>

<span data-ttu-id="a84dd-127">Un búfer es un recurso no estructurado y, por tanto, se define como si contuviera un único subrecurso.</span><span class="sxs-lookup"><span data-stu-id="a84dd-127">A buffer is an unstructured resource and is therefore defined as containing a single subresource.</span></span> <span data-ttu-id="a84dd-128">Las API que toman búferes no necesitan un índice de subrecurso.</span><span class="sxs-lookup"><span data-stu-id="a84dd-128">APIs that take buffers do not need a subresource index.</span></span> <span data-ttu-id="a84dd-129">Una textura por otro lado está muy estructurada.</span><span class="sxs-lookup"><span data-stu-id="a84dd-129">A texture on the other hand is highly structured.</span></span> <span data-ttu-id="a84dd-130">Cada objeto de textura puede contener uno o más Subrecursos en función del tamaño de la matriz y el número de niveles de mipmap.</span><span class="sxs-lookup"><span data-stu-id="a84dd-130">Each texture object may contain one or more subresources depending on the size of the array and the number of mipmap levels.</span></span>

<span data-ttu-id="a84dd-131">En el caso de las texturas de volumen (3D), todos los segmentos de un nivel de mipmap determinado son un índice de un solo recurso.</span><span class="sxs-lookup"><span data-stu-id="a84dd-131">For volume (3D) textures, all slices for a given mipmap level are a single subresource index.</span></span>

## <a name="requirements"></a><span data-ttu-id="a84dd-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a84dd-132">Requirements</span></span>



| <span data-ttu-id="a84dd-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="a84dd-133">Requirement</span></span> | <span data-ttu-id="a84dd-134">Value</span><span class="sxs-lookup"><span data-stu-id="a84dd-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a84dd-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a84dd-135">Header</span></span><br/>  | <dl> <span data-ttu-id="a84dd-136"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="a84dd-136"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="a84dd-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a84dd-137">Library</span></span><br/> | <dl> <span data-ttu-id="a84dd-138"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a84dd-138"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="a84dd-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a84dd-139">DLL</span></span><br/>     | <dl> <span data-ttu-id="a84dd-140"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a84dd-140"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a84dd-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="a84dd-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a84dd-142">Funciones auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="a84dd-142">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="a84dd-143">Subrecursos</span><span class="sxs-lookup"><span data-stu-id="a84dd-143">Subresources</span></span>](subresources.md)
</dt> </dl>

 

