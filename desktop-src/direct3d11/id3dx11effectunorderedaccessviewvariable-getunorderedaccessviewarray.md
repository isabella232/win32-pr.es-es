---
title: Método ID3DX11EffectUnorderedAccessViewVariable GetUnorderedAccessViewArray (D3dx11effect. h)
description: Obtiene una matriz de vistas de acceso desordenados.
ms.assetid: 38f838bb-cdcb-43c2-8b98-a188f479e93d
keywords:
- Método GetUnorderedAccessViewArray Direct3D 11
- Método GetUnorderedAccessViewArray Direct3D 11, interfaz ID3DX11EffectUnorderedAccessViewVariable
- Interfaz ID3DX11EffectUnorderedAccessViewVariable Direct3D 11, método GetUnorderedAccessViewArray
topic_type:
- apiref
api_name:
- ID3DX11EffectUnorderedAccessViewVariable.GetUnorderedAccessViewArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c264b5652287676d0792027f4f0ea8921bdb92f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280395"
---
# <a name="id3dx11effectunorderedaccessviewvariablegetunorderedaccessviewarray-method"></a><span data-ttu-id="ed5f9-106">ID3DX11EffectUnorderedAccessViewVariable:: GetUnorderedAccessViewArray (método)</span><span class="sxs-lookup"><span data-stu-id="ed5f9-106">ID3DX11EffectUnorderedAccessViewVariable::GetUnorderedAccessViewArray method</span></span>

<span data-ttu-id="ed5f9-107">Obtiene una matriz de vistas de acceso desordenados.</span><span class="sxs-lookup"><span data-stu-id="ed5f9-107">Get an array of unordered-access-views.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed5f9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ed5f9-108">Syntax</span></span>


```C++
HRESULT GetUnorderedAccessViewArray(
   ID3D11UnorderedAccessView **ppResources,
   UINT                      Offset,
   UINT                      Count
);
```



## <a name="parameters"></a><span data-ttu-id="ed5f9-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ed5f9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed5f9-110">*ppResources*</span><span class="sxs-lookup"><span data-stu-id="ed5f9-110">*ppResources*</span></span> 
</dt> <dd>

<span data-ttu-id="ed5f9-111">Tipo: **[ **ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***</span><span class="sxs-lookup"><span data-stu-id="ed5f9-111">Type: **[**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***</span></span>

<span data-ttu-id="ed5f9-112">Puntero a un puntero [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) que se establecerá en la matriz UAV en la devolución.</span><span class="sxs-lookup"><span data-stu-id="ed5f9-112">Pointer to an [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) pointer that will be set to the UAV array on return.</span></span>

</dd> <dt>

<span data-ttu-id="ed5f9-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="ed5f9-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="ed5f9-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ed5f9-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ed5f9-115">Índice de la primera interfaz.</span><span class="sxs-lookup"><span data-stu-id="ed5f9-115">Index of the first interface.</span></span>

</dd> <dt>

<span data-ttu-id="ed5f9-116">*Recuento*</span><span class="sxs-lookup"><span data-stu-id="ed5f9-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="ed5f9-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ed5f9-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ed5f9-118">Número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="ed5f9-118">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed5f9-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ed5f9-119">Return value</span></span>

<span data-ttu-id="ed5f9-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ed5f9-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ed5f9-121">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="ed5f9-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ed5f9-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ed5f9-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ed5f9-123">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="ed5f9-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="ed5f9-124">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="ed5f9-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="ed5f9-125">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="ed5f9-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ed5f9-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed5f9-126">Requirements</span></span>



| <span data-ttu-id="ed5f9-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed5f9-127">Requirement</span></span> | <span data-ttu-id="ed5f9-128">Value</span><span class="sxs-lookup"><span data-stu-id="ed5f9-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed5f9-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ed5f9-129">Header</span></span><br/>  | <dl> <span data-ttu-id="ed5f9-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed5f9-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="ed5f9-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ed5f9-131">Library</span></span><br/> | <dl> <span data-ttu-id="ed5f9-132"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="ed5f9-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed5f9-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed5f9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed5f9-134">ID3DX11EffectUnorderedAccessViewVariable</span><span class="sxs-lookup"><span data-stu-id="ed5f9-134">ID3DX11EffectUnorderedAccessViewVariable</span></span>](id3dx11effectunorderedaccessviewvariable.md)
</dt> </dl>

 

