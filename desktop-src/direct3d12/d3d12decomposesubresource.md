---
title: Función D3D12DecomposeSubresource (D3dx12.h)
description: Genera el segmento MIP, el segmento de matriz y el segmento de plano que se corresponden con el índice del subrecurso especificado.
ms.assetid: 89FAD7C5-E732-4E74-AC2F-DEECD6ADDA7D
keywords:
- D3D12DecomposeSubresource función)
topic_type:
- apiref
api_name:
- D3D12DecomposeSubresource
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec147833ee94969880865f679d40a198e0b22852
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717589"
---
# <a name="d3d12decomposesubresource-function"></a><span data-ttu-id="e99f2-104">D3D12DecomposeSubresource función)</span><span class="sxs-lookup"><span data-stu-id="e99f2-104">D3D12DecomposeSubresource function</span></span>

<span data-ttu-id="e99f2-105">Genera el segmento MIP, el segmento de matriz y el segmento de plano que se corresponden con el índice del subrecurso especificado.</span><span class="sxs-lookup"><span data-stu-id="e99f2-105">Outputs the mip slice, array slice, and plane slice that correspond to the specified subresource index.</span></span>

## <a name="syntax"></a><span data-ttu-id="e99f2-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e99f2-106">Syntax</span></span>


```C++
void inline D3D12DecomposeSubresource(
        UINT Subresource,
        UINT MipLevels,
        UINT ArraySize,
  _Out_ T    &MipSlice,
  _Out_ U    &ArraySlice,
  _Out_ V    &PlaneSlice
);
```



## <a name="parameters"></a><span data-ttu-id="e99f2-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e99f2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e99f2-108">*Subrecurso*</span><span class="sxs-lookup"><span data-stu-id="e99f2-108">*Subresource*</span></span> 
</dt> <dd>

<span data-ttu-id="e99f2-109">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e99f2-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e99f2-110">Índice del subrecurso.</span><span class="sxs-lookup"><span data-stu-id="e99f2-110">The index of the subresource.</span></span>

</dd> <dt>

<span data-ttu-id="e99f2-111">*MipLevels*</span><span class="sxs-lookup"><span data-stu-id="e99f2-111">*MipLevels*</span></span> 
</dt> <dd>

<span data-ttu-id="e99f2-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e99f2-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e99f2-113">Número máximo de niveles de mipmap en el subrecurso.</span><span class="sxs-lookup"><span data-stu-id="e99f2-113">The maximum number of mipmap levels in the subresource.</span></span>

</dd> <dt>

<span data-ttu-id="e99f2-114">*ArraySize*</span><span class="sxs-lookup"><span data-stu-id="e99f2-114">*ArraySize*</span></span> 
</dt> <dd>

<span data-ttu-id="e99f2-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e99f2-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e99f2-116">Número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="e99f2-116">The number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="e99f2-117">*MipSlice* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="e99f2-117">*MipSlice* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="e99f2-118">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="e99f2-118">Type: **T**</span></span>

<span data-ttu-id="e99f2-119">Genera el segmento de MIP que corresponde al índice de subrecurso dado.</span><span class="sxs-lookup"><span data-stu-id="e99f2-119">Outputs the mip slice that corresponds to the given subresource index.</span></span>

</dd> <dt>

<span data-ttu-id="e99f2-120">*ArraySlice* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="e99f2-120">*ArraySlice* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="e99f2-121">Tipo: **U**</span><span class="sxs-lookup"><span data-stu-id="e99f2-121">Type: **U**</span></span>

<span data-ttu-id="e99f2-122">Genera el segmento de la matriz que corresponde al índice del subrecurso dado.</span><span class="sxs-lookup"><span data-stu-id="e99f2-122">Outputs the array slice that corresponds to the given subresource index.</span></span>

</dd> <dt>

<span data-ttu-id="e99f2-123">*PlaneSlice* \[ out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="e99f2-123">*PlaneSlice* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="e99f2-124">Tipo: **V**</span><span class="sxs-lookup"><span data-stu-id="e99f2-124">Type: **V**</span></span>

<span data-ttu-id="e99f2-125">Genera el segmento del plano que corresponde al índice del subrecurso dado.</span><span class="sxs-lookup"><span data-stu-id="e99f2-125">Outputs the plane slice that corresponds to the given subresource index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e99f2-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e99f2-126">Return value</span></span>

<span data-ttu-id="e99f2-127">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e99f2-127">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e99f2-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e99f2-128">Remarks</span></span>

<span data-ttu-id="e99f2-129">Esta función determina qué segmento MIP, segmento de matriz y segmento de plano corresponden a un índice de subrecurso dado.</span><span class="sxs-lookup"><span data-stu-id="e99f2-129">This function determines which mip slice, array slice, and plane slice correspond to a given subresource index.</span></span> <span data-ttu-id="e99f2-130">Se trata de una utilidad útil, aunque es específica de C++.</span><span class="sxs-lookup"><span data-stu-id="e99f2-130">This is a useful utility, though it is C++ specific.</span></span>

<span data-ttu-id="e99f2-131">Esta función se declara como sigue, con los parámetros hace plantilla de C++ para los tipos **T**, **U** y **V**:</span><span class="sxs-lookup"><span data-stu-id="e99f2-131">This function is declared as follows, with C++ templatized parameters for types **T**, **U**, and **V**:</span></span>


```c++
template <typename T, typename U, typename V>
inline void D3D12DecomposeSubresource( UINT Subresource, UINT MipLevels, UINT ArraySize, _Out_ T& MipSlice, _Out_ U& ArraySlice, _Out_ V& PlaneSlice )
{
    MipSlice = static_cast<T>(Subresource % MipLevels);
    ArraySlice = static_cast<U>((Subresource / MipLevels) % ArraySize);
    PlaneSlice = static_cast<V>(Subresource / (MipLevels * ArraySize));
}
```



## <a name="requirements"></a><span data-ttu-id="e99f2-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e99f2-132">Requirements</span></span>



| <span data-ttu-id="e99f2-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="e99f2-133">Requirement</span></span> | <span data-ttu-id="e99f2-134">Value</span><span class="sxs-lookup"><span data-stu-id="e99f2-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e99f2-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e99f2-135">Header</span></span><br/>  | <dl> <span data-ttu-id="e99f2-136"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="e99f2-136"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="e99f2-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e99f2-137">Library</span></span><br/> | <dl> <span data-ttu-id="e99f2-138"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e99f2-138"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="e99f2-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e99f2-139">DLL</span></span><br/>     | <dl> <span data-ttu-id="e99f2-140"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e99f2-140"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e99f2-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="e99f2-141">See also</span></span>

[<span data-ttu-id="e99f2-142">Funciones auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="e99f2-142">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)

[<span data-ttu-id="e99f2-143">Subrecursos</span><span class="sxs-lookup"><span data-stu-id="e99f2-143">Subresources</span></span>](subresources.md)
