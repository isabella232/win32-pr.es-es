---
title: Método ID3DX11EffectMatrixVariable GetMatrix (D3dx11effect. h)
description: Obtiene una matriz.
ms.assetid: 1d0b20f2-6e43-414d-a161-65ce13bef1e0
keywords:
- Método GetMatrix Direct3D 11
- Método GetMatrix Direct3D 11, interfaz ID3DX11EffectMatrixVariable
- Interfaz ID3DX11EffectMatrixVariable Direct3D 11, método GetMatrix
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.GetMatrix
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a14c2f196c4072d7f81a75045fe4703bf51ea338
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083757"
---
# <a name="id3dx11effectmatrixvariablegetmatrix-method"></a><span data-ttu-id="30f64-106">ID3DX11EffectMatrixVariable:: GetMatrix (método)</span><span class="sxs-lookup"><span data-stu-id="30f64-106">ID3DX11EffectMatrixVariable::GetMatrix method</span></span>

<span data-ttu-id="30f64-107">Obtiene una matriz.</span><span class="sxs-lookup"><span data-stu-id="30f64-107">Get a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="30f64-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="30f64-108">Syntax</span></span>


```C++
HRESULT GetMatrix(
   float *pData
);
```



## <a name="parameters"></a><span data-ttu-id="30f64-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="30f64-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30f64-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="30f64-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="30f64-111">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="30f64-111">Type: **float\***</span></span>

<span data-ttu-id="30f64-112">Puntero al primer elemento de una matriz.</span><span class="sxs-lookup"><span data-stu-id="30f64-112">A pointer to the first element in a matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30f64-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="30f64-113">Return value</span></span>

<span data-ttu-id="30f64-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="30f64-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="30f64-115">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="30f64-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="30f64-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="30f64-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="30f64-117">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="30f64-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="30f64-118">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="30f64-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="30f64-119">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="30f64-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="30f64-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30f64-120">Requirements</span></span>



| <span data-ttu-id="30f64-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="30f64-121">Requirement</span></span> | <span data-ttu-id="30f64-122">Value</span><span class="sxs-lookup"><span data-stu-id="30f64-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30f64-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="30f64-123">Header</span></span><br/>  | <dl> <span data-ttu-id="30f64-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="30f64-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="30f64-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="30f64-125">Library</span></span><br/> | <dl> <span data-ttu-id="30f64-126"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="30f64-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30f64-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="30f64-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30f64-128">ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="30f64-128">ID3DX11EffectMatrixVariable</span></span>](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

 





