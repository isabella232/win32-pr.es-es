---
title: Método ID3DX11EffectVectorVariable GetFloatVectorArray (D3dx11effect. h)
description: Obtiene una matriz de vectores de cuatro componentes que contienen datos de punto flotante.
ms.assetid: 30ecbd97-c16d-4ea9-b7d9-364887f42a04
keywords:
- Método GetFloatVectorArray Direct3D 11
- Método GetFloatVectorArray Direct3D 11, interfaz ID3DX11EffectVectorVariable
- Interfaz ID3DX11EffectVectorVariable Direct3D 11, método GetFloatVectorArray
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.GetFloatVectorArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18a4c53b884c623ca3d11fb4a9a44660ce21d8a8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987073"
---
# <a name="id3dx11effectvectorvariablegetfloatvectorarray-method"></a><span data-ttu-id="a7cac-106">ID3DX11EffectVectorVariable:: GetFloatVectorArray (método)</span><span class="sxs-lookup"><span data-stu-id="a7cac-106">ID3DX11EffectVectorVariable::GetFloatVectorArray method</span></span>

<span data-ttu-id="a7cac-107">Obtiene una matriz de vectores de cuatro componentes que contienen datos de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="a7cac-107">Get an array of four-component vectors that contain floating-point data.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7cac-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a7cac-108">Syntax</span></span>


```C++
HRESULT GetFloatVectorArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a><span data-ttu-id="a7cac-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a7cac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7cac-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="a7cac-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="a7cac-111">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="a7cac-111">Type: **float\***</span></span>

<span data-ttu-id="a7cac-112">Puntero al principio de los datos que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="a7cac-112">A pointer to the start of the data to set.</span></span>

</dd> <dt>

<span data-ttu-id="a7cac-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="a7cac-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="a7cac-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a7cac-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a7cac-115">Debe establecerse en 0; está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="a7cac-115">Must be set to 0; this is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="a7cac-116">*Recuento*</span><span class="sxs-lookup"><span data-stu-id="a7cac-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="a7cac-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a7cac-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a7cac-118">Número de elementos de matriz que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="a7cac-118">The number of array elements to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7cac-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a7cac-119">Return value</span></span>

<span data-ttu-id="a7cac-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a7cac-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a7cac-121">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="a7cac-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a7cac-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a7cac-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a7cac-123">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="a7cac-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="a7cac-124">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="a7cac-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="a7cac-125">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="a7cac-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a7cac-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7cac-126">Requirements</span></span>



| <span data-ttu-id="a7cac-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7cac-127">Requirement</span></span> | <span data-ttu-id="a7cac-128">Value</span><span class="sxs-lookup"><span data-stu-id="a7cac-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7cac-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a7cac-129">Header</span></span><br/>  | <dl> <span data-ttu-id="a7cac-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7cac-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="a7cac-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a7cac-131">Library</span></span><br/> | <dl> <span data-ttu-id="a7cac-132"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="a7cac-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7cac-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="a7cac-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7cac-134">ID3DX11EffectVectorVariable</span><span class="sxs-lookup"><span data-stu-id="a7cac-134">ID3DX11EffectVectorVariable</span></span>](id3dx11effectvectorvariable.md)
</dt> </dl>

 

