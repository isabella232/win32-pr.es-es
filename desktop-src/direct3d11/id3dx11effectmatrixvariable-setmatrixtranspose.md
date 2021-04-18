---
title: Método ID3DX11EffectMatrixVariable SetMatrixTranspose (D3dx11effect. h)
description: Transponer y establecer una matriz de punto flotante.
ms.assetid: 228546c9-0141-4e17-bc8f-bff7201825d7
keywords:
- Método SetMatrixTranspose Direct3D 11
- Método SetMatrixTranspose Direct3D 11, interfaz ID3DX11EffectMatrixVariable
- Interfaz ID3DX11EffectMatrixVariable Direct3D 11, método SetMatrixTranspose
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.SetMatrixTranspose
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5daf77b6e2e9578dcbc6c9cfe80f57b149097c32
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986934"
---
# <a name="id3dx11effectmatrixvariablesetmatrixtranspose-method"></a><span data-ttu-id="b959c-106">ID3DX11EffectMatrixVariable:: SetMatrixTranspose (método)</span><span class="sxs-lookup"><span data-stu-id="b959c-106">ID3DX11EffectMatrixVariable::SetMatrixTranspose method</span></span>

<span data-ttu-id="b959c-107">Transponer y establecer una matriz de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="b959c-107">Transpose and set a floating-point matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="b959c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b959c-108">Syntax</span></span>


```C++
HRESULT SetMatrixTranspose(
   float *pData
);
```



## <a name="parameters"></a><span data-ttu-id="b959c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b959c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b959c-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="b959c-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="b959c-111">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="b959c-111">Type: **float\***</span></span>

<span data-ttu-id="b959c-112">Puntero al primer elemento de una matriz.</span><span class="sxs-lookup"><span data-stu-id="b959c-112">A pointer to the first element of a matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b959c-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b959c-113">Return value</span></span>

<span data-ttu-id="b959c-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b959c-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b959c-115">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="b959c-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b959c-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b959c-116">Remarks</span></span>

<span data-ttu-id="b959c-117">Transponer una matriz reorganizará el orden de los datos del orden de las columnas de fila al orden de las filas de columnas (o viceversa).</span><span class="sxs-lookup"><span data-stu-id="b959c-117">Transposing a matrix will rearrange the data order from row-column order to column-row order (or vice versa).</span></span>

> [!Note]  
> <span data-ttu-id="b959c-118">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="b959c-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="b959c-119">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="b959c-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="b959c-120">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="b959c-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b959c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b959c-121">Requirements</span></span>



| <span data-ttu-id="b959c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b959c-122">Requirement</span></span> | <span data-ttu-id="b959c-123">Value</span><span class="sxs-lookup"><span data-stu-id="b959c-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b959c-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b959c-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b959c-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b959c-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="b959c-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b959c-126">Library</span></span><br/> | <dl> <span data-ttu-id="b959c-127"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="b959c-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b959c-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="b959c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b959c-129">ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="b959c-129">ID3DX11EffectMatrixVariable</span></span>](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

 





