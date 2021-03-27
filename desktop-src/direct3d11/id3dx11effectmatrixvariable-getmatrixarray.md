---
title: Método ID3DX11EffectMatrixVariable GetMatrixArray (D3dx11effect. h)
description: Obtiene una matriz de matrices.
ms.assetid: a7598687-a11c-41ad-9fb6-2c16d12f5edc
keywords:
- Método GetMatrixArray Direct3D 11
- Método GetMatrixArray Direct3D 11, interfaz ID3DX11EffectMatrixVariable
- Interfaz ID3DX11EffectMatrixVariable Direct3D 11, método GetMatrixArray
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.GetMatrixArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d4a339bf6918868473966b6d79bcbe6b6aa3eaa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003880"
---
# <a name="id3dx11effectmatrixvariablegetmatrixarray-method"></a><span data-ttu-id="7f9b8-106">ID3DX11EffectMatrixVariable:: GetMatrixArray (método)</span><span class="sxs-lookup"><span data-stu-id="7f9b8-106">ID3DX11EffectMatrixVariable::GetMatrixArray method</span></span>

<span data-ttu-id="7f9b8-107">Obtiene una matriz de matrices.</span><span class="sxs-lookup"><span data-stu-id="7f9b8-107">Get an array of matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f9b8-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7f9b8-108">Syntax</span></span>


```C++
HRESULT GetMatrixArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a><span data-ttu-id="7f9b8-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7f9b8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f9b8-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="7f9b8-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="7f9b8-111">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="7f9b8-111">Type: **float\***</span></span>

<span data-ttu-id="7f9b8-112">Puntero al primer elemento de la primera matriz de una matriz de matrices.</span><span class="sxs-lookup"><span data-stu-id="7f9b8-112">A pointer to the first element of the first matrix in an array of matrices.</span></span>

</dd> <dt>

<span data-ttu-id="7f9b8-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="7f9b8-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="7f9b8-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7f9b8-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="7f9b8-115">Desplazamiento (en número de matrices) entre el inicio de la matriz y la primera matriz devuelta.</span><span class="sxs-lookup"><span data-stu-id="7f9b8-115">The offset (in number of matrices) between the start of the array and the first matrix returned.</span></span>

</dd> <dt>

<span data-ttu-id="7f9b8-116">*Recuento*</span><span class="sxs-lookup"><span data-stu-id="7f9b8-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="7f9b8-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7f9b8-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="7f9b8-118">Número de matrices de la matriz devuelta.</span><span class="sxs-lookup"><span data-stu-id="7f9b8-118">The number of matrices in the returned array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f9b8-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7f9b8-119">Return value</span></span>

<span data-ttu-id="7f9b8-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7f9b8-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7f9b8-121">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="7f9b8-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7f9b8-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7f9b8-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7f9b8-123">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="7f9b8-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="7f9b8-124">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="7f9b8-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="7f9b8-125">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="7f9b8-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7f9b8-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f9b8-126">Requirements</span></span>



| <span data-ttu-id="7f9b8-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f9b8-127">Requirement</span></span> | <span data-ttu-id="7f9b8-128">Value</span><span class="sxs-lookup"><span data-stu-id="7f9b8-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f9b8-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7f9b8-129">Header</span></span><br/>  | <dl> <span data-ttu-id="7f9b8-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f9b8-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="7f9b8-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7f9b8-131">Library</span></span><br/> | <dl> <span data-ttu-id="7f9b8-132"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="7f9b8-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f9b8-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="7f9b8-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f9b8-134">ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="7f9b8-134">ID3DX11EffectMatrixVariable</span></span>](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

