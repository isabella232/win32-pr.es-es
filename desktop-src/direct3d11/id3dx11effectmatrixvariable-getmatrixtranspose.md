---
title: Método ID3DX11EffectMatrixVariable GetMatrixTranspose (D3dx11effect. h)
description: Transponer y obtener una matriz de punto flotante.
ms.assetid: a261128c-d1f9-4864-b562-5fe9a69c9969
keywords:
- Método GetMatrixTranspose Direct3D 11
- Método GetMatrixTranspose Direct3D 11, interfaz ID3DX11EffectMatrixVariable
- Interfaz ID3DX11EffectMatrixVariable Direct3D 11, método GetMatrixTranspose
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.GetMatrixTranspose
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fa5c8eb8e424041a05461636d1eaf7b65c7cd4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083756"
---
# <a name="id3dx11effectmatrixvariablegetmatrixtranspose-method"></a><span data-ttu-id="daa45-106">ID3DX11EffectMatrixVariable:: GetMatrixTranspose (método)</span><span class="sxs-lookup"><span data-stu-id="daa45-106">ID3DX11EffectMatrixVariable::GetMatrixTranspose method</span></span>

<span data-ttu-id="daa45-107">Transponer y obtener una matriz de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="daa45-107">Transpose and get a floating-point matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="daa45-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="daa45-108">Syntax</span></span>


```C++
HRESULT GetMatrixTranspose(
   float *pData
);
```



## <a name="parameters"></a><span data-ttu-id="daa45-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="daa45-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="daa45-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="daa45-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="daa45-111">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="daa45-111">Type: **float\***</span></span>

<span data-ttu-id="daa45-112">Puntero al primer elemento de una matriz transpuesta.</span><span class="sxs-lookup"><span data-stu-id="daa45-112">A pointer to the first element of a transposed matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="daa45-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="daa45-113">Return value</span></span>

<span data-ttu-id="daa45-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="daa45-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="daa45-115">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="daa45-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="daa45-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="daa45-116">Remarks</span></span>

<span data-ttu-id="daa45-117">Transponer una matriz reorganizará el orden de los datos del orden de las columnas de fila al orden de las filas de columnas (o viceversa).</span><span class="sxs-lookup"><span data-stu-id="daa45-117">Transposing a matrix will rearrange the data order from row-column order to column-row order (or vice versa).</span></span>

> [!Note]  
> <span data-ttu-id="daa45-118">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="daa45-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="daa45-119">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="daa45-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="daa45-120">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="daa45-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="daa45-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="daa45-121">Requirements</span></span>



| <span data-ttu-id="daa45-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="daa45-122">Requirement</span></span> | <span data-ttu-id="daa45-123">Value</span><span class="sxs-lookup"><span data-stu-id="daa45-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="daa45-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="daa45-124">Header</span></span><br/>  | <dl> <span data-ttu-id="daa45-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="daa45-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="daa45-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="daa45-126">Library</span></span><br/> | <dl> <span data-ttu-id="daa45-127"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="daa45-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="daa45-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="daa45-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="daa45-129">ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="daa45-129">ID3DX11EffectMatrixVariable</span></span>](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

 





