---
title: Método ID3DX11EffectMatrixVariable SetMatrixArray (D3dx11effect. h)
description: Establezca una matriz de matrices de punto flotante.
ms.assetid: c90d621c-7500-49c3-ab40-2d0630fc4bec
keywords:
- Método SetMatrixArray Direct3D 11
- Método SetMatrixArray Direct3D 11, interfaz ID3DX11EffectMatrixVariable
- Interfaz ID3DX11EffectMatrixVariable Direct3D 11, método SetMatrixArray
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.SetMatrixArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ffe0f6a81e0086a9afd6da9e464f09ae577dab2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987043"
---
# <a name="id3dx11effectmatrixvariablesetmatrixarray-method"></a><span data-ttu-id="923df-106">ID3DX11EffectMatrixVariable:: SetMatrixArray (método)</span><span class="sxs-lookup"><span data-stu-id="923df-106">ID3DX11EffectMatrixVariable::SetMatrixArray method</span></span>

<span data-ttu-id="923df-107">Establezca una matriz de matrices de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="923df-107">Set an array of floating-point matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="923df-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="923df-108">Syntax</span></span>


```C++
HRESULT SetMatrixArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a><span data-ttu-id="923df-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="923df-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="923df-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="923df-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="923df-111">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="923df-111">Type: **float\***</span></span>

<span data-ttu-id="923df-112">Puntero a la primera matriz.</span><span class="sxs-lookup"><span data-stu-id="923df-112">A pointer to the first matrix.</span></span>

</dd> <dt>

<span data-ttu-id="923df-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="923df-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="923df-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="923df-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="923df-115">Número de elementos de matriz que se van a omitir desde el principio de la matriz.</span><span class="sxs-lookup"><span data-stu-id="923df-115">The number of matrix elements to skip from the start of the array.</span></span>

</dd> <dt>

<span data-ttu-id="923df-116">*Recuento*</span><span class="sxs-lookup"><span data-stu-id="923df-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="923df-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="923df-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="923df-118">Número de elementos que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="923df-118">The number of elements to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="923df-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="923df-119">Return value</span></span>

<span data-ttu-id="923df-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="923df-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="923df-121">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="923df-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="923df-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="923df-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="923df-123">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="923df-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="923df-124">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="923df-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="923df-125">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="923df-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="923df-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="923df-126">Requirements</span></span>



| <span data-ttu-id="923df-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="923df-127">Requirement</span></span> | <span data-ttu-id="923df-128">Value</span><span class="sxs-lookup"><span data-stu-id="923df-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="923df-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="923df-129">Header</span></span><br/>  | <dl> <span data-ttu-id="923df-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="923df-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="923df-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="923df-131">Library</span></span><br/> | <dl> <span data-ttu-id="923df-132"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="923df-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="923df-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="923df-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="923df-134">ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="923df-134">ID3DX11EffectMatrixVariable</span></span>](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

