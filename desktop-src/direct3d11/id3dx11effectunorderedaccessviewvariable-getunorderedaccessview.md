---
title: Método ID3DX11EffectUnorderedAccessViewVariable GetUnorderedAccessView (D3dx11effect. h)
description: Obtiene una vista de acceso sin ordenar.
ms.assetid: 46f61c4f-b3ee-4058-99b9-a43ca6944fb2
keywords:
- Método GetUnorderedAccessView Direct3D 11
- Método GetUnorderedAccessView Direct3D 11, interfaz ID3DX11EffectUnorderedAccessViewVariable
- Interfaz ID3DX11EffectUnorderedAccessViewVariable Direct3D 11, método GetUnorderedAccessView
topic_type:
- apiref
api_name:
- ID3DX11EffectUnorderedAccessViewVariable.GetUnorderedAccessView
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7743d15c2380ff4e38bdcae1d38bbd8905cbccda
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998677"
---
# <a name="id3dx11effectunorderedaccessviewvariablegetunorderedaccessview-method"></a><span data-ttu-id="a6f48-106">ID3DX11EffectUnorderedAccessViewVariable:: GetUnorderedAccessView (método)</span><span class="sxs-lookup"><span data-stu-id="a6f48-106">ID3DX11EffectUnorderedAccessViewVariable::GetUnorderedAccessView method</span></span>

<span data-ttu-id="a6f48-107">Obtiene una vista de acceso sin ordenar.</span><span class="sxs-lookup"><span data-stu-id="a6f48-107">Get an unordered-access-view.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6f48-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a6f48-108">Syntax</span></span>


```C++
HRESULT GetUnorderedAccessView(
   ID3D11UnorderedAccessView **ppResource
);
```



## <a name="parameters"></a><span data-ttu-id="a6f48-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a6f48-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6f48-110">*ppResource*</span><span class="sxs-lookup"><span data-stu-id="a6f48-110">*ppResource*</span></span> 
</dt> <dd>

<span data-ttu-id="a6f48-111">Tipo: **[ **ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***</span><span class="sxs-lookup"><span data-stu-id="a6f48-111">Type: **[**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***</span></span>

<span data-ttu-id="a6f48-112">Puntero a un puntero [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) que se establecerá en la devolución.</span><span class="sxs-lookup"><span data-stu-id="a6f48-112">Pointer to an [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) pointer that will be set on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6f48-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a6f48-113">Return value</span></span>

<span data-ttu-id="a6f48-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a6f48-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a6f48-115">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="a6f48-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a6f48-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a6f48-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a6f48-117">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="a6f48-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="a6f48-118">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="a6f48-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="a6f48-119">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="a6f48-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a6f48-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6f48-120">Requirements</span></span>



| <span data-ttu-id="a6f48-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6f48-121">Requirement</span></span> | <span data-ttu-id="a6f48-122">Value</span><span class="sxs-lookup"><span data-stu-id="a6f48-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6f48-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a6f48-123">Header</span></span><br/>  | <dl> <span data-ttu-id="a6f48-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6f48-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="a6f48-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a6f48-125">Library</span></span><br/> | <dl> <span data-ttu-id="a6f48-126"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="a6f48-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6f48-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="a6f48-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6f48-128">ID3DX11EffectUnorderedAccessViewVariable</span><span class="sxs-lookup"><span data-stu-id="a6f48-128">ID3DX11EffectUnorderedAccessViewVariable</span></span>](id3dx11effectunorderedaccessviewvariable.md)
</dt> </dl>

 

 





