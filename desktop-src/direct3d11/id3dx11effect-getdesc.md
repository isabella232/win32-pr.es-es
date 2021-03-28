---
title: Método ID3DX11Effect GetDesc (D3dx11effect. h)
description: Obtiene una descripción de efecto.
ms.assetid: ca684786-c813-48d1-acad-e78aafd1c0db
keywords:
- Método GetDesc Direct3D 11
- Método GetDesc Direct3D 11, interfaz ID3DX11Effect
- Interfaz ID3DX11Effect Direct3D 11, método GetDesc
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 587cde43ec2d9136bab5884691c99321d1492835
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998634"
---
# <a name="id3dx11effectgetdesc-method"></a><span data-ttu-id="8ee5f-106">ID3DX11Effect:: GetDesc (método)</span><span class="sxs-lookup"><span data-stu-id="8ee5f-106">ID3DX11Effect::GetDesc method</span></span>

<span data-ttu-id="8ee5f-107">Obtiene una descripción de efecto.</span><span class="sxs-lookup"><span data-stu-id="8ee5f-107">Get an effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ee5f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8ee5f-108">Syntax</span></span>


```C++
HRESULT GetDesc(
   D3DX11_EFFECT_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="8ee5f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8ee5f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ee5f-110">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="8ee5f-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="8ee5f-111">Tipo: **[ **D3DX11 \_ efecto \_ DESC**](d3dx11-effect-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="8ee5f-111">Type: **[**D3DX11\_EFFECT\_DESC**](d3dx11-effect-desc.md)\***</span></span>

<span data-ttu-id="8ee5f-112">Un puntero a una descripción de efecto (vea [**D3DX11 \_ Effect \_ DESC**](d3dx11-effect-desc.md)).</span><span class="sxs-lookup"><span data-stu-id="8ee5f-112">A pointer to an effect description (see [**D3DX11\_EFFECT\_DESC**](d3dx11-effect-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ee5f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8ee5f-113">Return value</span></span>

<span data-ttu-id="8ee5f-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8ee5f-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8ee5f-115">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="8ee5f-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8ee5f-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8ee5f-116">Remarks</span></span>

<span data-ttu-id="8ee5f-117">Una descripción de efecto contiene información básica sobre un efecto, como las técnicas que contiene y los recursos de búfer de constantes que requiere.</span><span class="sxs-lookup"><span data-stu-id="8ee5f-117">An effect description contains basic information about an effect such as the techniques it contains and the constant buffer resources it requires.</span></span>

> [!Note]  
> <span data-ttu-id="8ee5f-118">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="8ee5f-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="8ee5f-119">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="8ee5f-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="8ee5f-120">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="8ee5f-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8ee5f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ee5f-121">Requirements</span></span>



| <span data-ttu-id="8ee5f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ee5f-122">Requirement</span></span> | <span data-ttu-id="8ee5f-123">Value</span><span class="sxs-lookup"><span data-stu-id="8ee5f-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ee5f-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8ee5f-124">Header</span></span><br/>  | <dl> <span data-ttu-id="8ee5f-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ee5f-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="8ee5f-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8ee5f-126">Library</span></span><br/> | <dl> <span data-ttu-id="8ee5f-127"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="8ee5f-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ee5f-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ee5f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ee5f-129">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="8ee5f-129">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

 





