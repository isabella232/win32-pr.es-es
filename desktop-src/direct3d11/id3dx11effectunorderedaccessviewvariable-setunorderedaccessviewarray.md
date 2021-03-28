---
title: Método ID3DX11EffectUnorderedAccessViewVariable SetUnorderedAccessViewArray (D3dx11effect. h)
description: Establezca una matriz de vistas de acceso desordenados.
ms.assetid: 12d0da06-990a-42b2-9566-cc5136f48781
keywords:
- Método SetUnorderedAccessViewArray Direct3D 11
- Método SetUnorderedAccessViewArray Direct3D 11, interfaz ID3DX11EffectUnorderedAccessViewVariable
- Interfaz ID3DX11EffectUnorderedAccessViewVariable Direct3D 11, método SetUnorderedAccessViewArray
topic_type:
- apiref
api_name:
- ID3DX11EffectUnorderedAccessViewVariable.SetUnorderedAccessViewArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 053856f294906cf56acf1f38ca90663ebcc34051
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998341"
---
# <a name="id3dx11effectunorderedaccessviewvariablesetunorderedaccessviewarray-method"></a><span data-ttu-id="8b041-106">ID3DX11EffectUnorderedAccessViewVariable:: SetUnorderedAccessViewArray (método)</span><span class="sxs-lookup"><span data-stu-id="8b041-106">ID3DX11EffectUnorderedAccessViewVariable::SetUnorderedAccessViewArray method</span></span>

<span data-ttu-id="8b041-107">Establezca una matriz de vistas de acceso desordenados.</span><span class="sxs-lookup"><span data-stu-id="8b041-107">Set an array of unordered-access-views.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b041-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8b041-108">Syntax</span></span>


```C++
HRESULT SetUnorderedAccessViewArray(
   ID3D11UnorderedAccessView **ppResources,
   UINT                      Offset,
   UINT                      Count
);
```



## <a name="parameters"></a><span data-ttu-id="8b041-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8b041-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b041-110">*ppResources*</span><span class="sxs-lookup"><span data-stu-id="8b041-110">*ppResources*</span></span> 
</dt> <dd>

<span data-ttu-id="8b041-111">Tipo: **[ **ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***</span><span class="sxs-lookup"><span data-stu-id="8b041-111">Type: **[**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***</span></span>

<span data-ttu-id="8b041-112">Matriz de punteros [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) .</span><span class="sxs-lookup"><span data-stu-id="8b041-112">An array of [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) pointers.</span></span>

</dd> <dt>

<span data-ttu-id="8b041-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="8b041-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="8b041-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8b041-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8b041-115">Índice de la primera vista de acceso sin ordenar.</span><span class="sxs-lookup"><span data-stu-id="8b041-115">Index of the first unordered-access-view.</span></span>

</dd> <dt>

<span data-ttu-id="8b041-116">*Recuento*</span><span class="sxs-lookup"><span data-stu-id="8b041-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="8b041-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8b041-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8b041-118">Número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="8b041-118">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b041-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8b041-119">Return value</span></span>

<span data-ttu-id="8b041-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8b041-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8b041-121">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="8b041-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8b041-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8b041-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8b041-123">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="8b041-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="8b041-124">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="8b041-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="8b041-125">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="8b041-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8b041-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b041-126">Requirements</span></span>



| <span data-ttu-id="8b041-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b041-127">Requirement</span></span> | <span data-ttu-id="8b041-128">Value</span><span class="sxs-lookup"><span data-stu-id="8b041-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b041-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8b041-129">Header</span></span><br/>  | <dl> <span data-ttu-id="8b041-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b041-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="8b041-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8b041-131">Library</span></span><br/> | <dl> <span data-ttu-id="8b041-132"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="8b041-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b041-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="8b041-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b041-134">ID3DX11EffectUnorderedAccessViewVariable</span><span class="sxs-lookup"><span data-stu-id="8b041-134">ID3DX11EffectUnorderedAccessViewVariable</span></span>](id3dx11effectunorderedaccessviewvariable.md)
</dt> </dl>

 

