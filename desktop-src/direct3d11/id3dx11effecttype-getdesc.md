---
title: Método ID3DX11EffectType GetDesc (D3dx11effect. h)
description: Obtiene una descripción del tipo de efecto.
ms.assetid: 08a8a1b6-fe2d-431b-a0e4-d628f0ceb1a0
keywords:
- Método GetDesc Direct3D 11
- Método GetDesc Direct3D 11, interfaz ID3DX11EffectType
- Interfaz ID3DX11EffectType Direct3D 11, método GetDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c1ee52e4c6628c00b0155e5bd3081b6c4fd8c46
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998719"
---
# <a name="id3dx11effecttypegetdesc-method"></a><span data-ttu-id="c5aa8-106">ID3DX11EffectType:: GetDesc (método)</span><span class="sxs-lookup"><span data-stu-id="c5aa8-106">ID3DX11EffectType::GetDesc method</span></span>

<span data-ttu-id="c5aa8-107">Obtiene una descripción del tipo de efecto.</span><span class="sxs-lookup"><span data-stu-id="c5aa8-107">Get an effect-type description.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5aa8-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c5aa8-108">Syntax</span></span>


```C++
HRESULT GetDesc(
   D3DX11_EFFECT_TYPE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="c5aa8-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c5aa8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5aa8-110">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="c5aa8-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="c5aa8-111">Tipo: **[ **efecto de D3DX11 \_ \_ tipo \_ DESC**](d3dx11-effect-type-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="c5aa8-111">Type: **[**D3DX11\_EFFECT\_TYPE\_DESC**](d3dx11-effect-type-desc.md)\***</span></span>

<span data-ttu-id="c5aa8-112">Puntero a una descripción de tipo de efecto.</span><span class="sxs-lookup"><span data-stu-id="c5aa8-112">A pointer to an effect-type description.</span></span> <span data-ttu-id="c5aa8-113">Consulte [**D3DX11 \_ Effect \_ Type \_ DESC**](d3dx11-effect-type-desc.md).</span><span class="sxs-lookup"><span data-stu-id="c5aa8-113">See [**D3DX11\_EFFECT\_TYPE\_DESC**](d3dx11-effect-type-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5aa8-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c5aa8-114">Return value</span></span>

<span data-ttu-id="c5aa8-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c5aa8-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c5aa8-116">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="c5aa8-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c5aa8-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c5aa8-117">Remarks</span></span>

<span data-ttu-id="c5aa8-118">La descripción de la variable de efecto contiene datos sobre el nombre, las anotaciones, la semántica, las marcas y el desplazamiento del búfer del tipo de efecto.</span><span class="sxs-lookup"><span data-stu-id="c5aa8-118">The effect-variable description contains data about the name, annotations, semantic, flags and buffer offset of the effect type.</span></span>

> [!Note]  
> <span data-ttu-id="c5aa8-119">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="c5aa8-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="c5aa8-120">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="c5aa8-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="c5aa8-121">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="c5aa8-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c5aa8-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5aa8-122">Requirements</span></span>



| <span data-ttu-id="c5aa8-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5aa8-123">Requirement</span></span> | <span data-ttu-id="c5aa8-124">Value</span><span class="sxs-lookup"><span data-stu-id="c5aa8-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5aa8-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c5aa8-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c5aa8-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5aa8-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="c5aa8-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c5aa8-127">Library</span></span><br/> | <dl> <span data-ttu-id="c5aa8-128"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="c5aa8-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5aa8-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5aa8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5aa8-130">ID3DX11EffectType</span><span class="sxs-lookup"><span data-stu-id="c5aa8-130">ID3DX11EffectType</span></span>](id3dx11effecttype.md)
</dt> </dl>

 

 





