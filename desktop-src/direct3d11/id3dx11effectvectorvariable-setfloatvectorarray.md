---
title: Método ID3DX11EffectVectorVariable SetFloatVectorArray (D3dx11effect. h)
description: Establezca una matriz de vectores de cuatro componentes que contengan datos de punto flotante.
ms.assetid: f07edf0f-8a90-41bf-ae03-5a62a19e57e2
keywords:
- Método SetFloatVectorArray Direct3D 11
- Método SetFloatVectorArray Direct3D 11, interfaz ID3DX11EffectVectorVariable
- Interfaz ID3DX11EffectVectorVariable Direct3D 11, método SetFloatVectorArray
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.SetFloatVectorArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4f8f731dd90251848095f899bdc141bbc1d6748
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987067"
---
# <a name="id3dx11effectvectorvariablesetfloatvectorarray-method"></a><span data-ttu-id="a4de5-106">ID3DX11EffectVectorVariable:: SetFloatVectorArray (método)</span><span class="sxs-lookup"><span data-stu-id="a4de5-106">ID3DX11EffectVectorVariable::SetFloatVectorArray method</span></span>

<span data-ttu-id="a4de5-107">Establezca una matriz de vectores de cuatro componentes que contengan datos de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="a4de5-107">Set an array of four-component vectors that contain floating-point data.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4de5-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a4de5-108">Syntax</span></span>


```C++
HRESULT SetFloatVectorArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a><span data-ttu-id="a4de5-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a4de5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4de5-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="a4de5-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="a4de5-111">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="a4de5-111">Type: **float\***</span></span>

<span data-ttu-id="a4de5-112">Puntero al principio de los datos que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="a4de5-112">A pointer to the start of the data to set.</span></span>

</dd> <dt>

<span data-ttu-id="a4de5-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="a4de5-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="a4de5-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a4de5-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a4de5-115">Debe establecerse en 0; está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="a4de5-115">Must be set to 0; this is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="a4de5-116">*Recuento*</span><span class="sxs-lookup"><span data-stu-id="a4de5-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="a4de5-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a4de5-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a4de5-118">Número de elementos de matriz que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="a4de5-118">The number of array elements to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4de5-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a4de5-119">Return value</span></span>

<span data-ttu-id="a4de5-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a4de5-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a4de5-121">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="a4de5-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a4de5-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a4de5-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a4de5-123">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="a4de5-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="a4de5-124">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="a4de5-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="a4de5-125">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="a4de5-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a4de5-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4de5-126">Requirements</span></span>



| <span data-ttu-id="a4de5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4de5-127">Requirement</span></span> | <span data-ttu-id="a4de5-128">Value</span><span class="sxs-lookup"><span data-stu-id="a4de5-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4de5-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a4de5-129">Header</span></span><br/>  | <dl> <span data-ttu-id="a4de5-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4de5-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="a4de5-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a4de5-131">Library</span></span><br/> | <dl> <span data-ttu-id="a4de5-132"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="a4de5-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4de5-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="a4de5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4de5-134">ID3DX11EffectVectorVariable</span><span class="sxs-lookup"><span data-stu-id="a4de5-134">ID3DX11EffectVectorVariable</span></span>](id3dx11effectvectorvariable.md)
</dt> </dl>

 

