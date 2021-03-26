---
title: Método ID3DX11EffectSamplerVariable GetBackingStore (D3dx11effect. h)
description: Obtiene un puntero a una variable que contiene el estado de muestra.
ms.assetid: b188fb86-f54b-481e-9110-7b8af70ff303
keywords:
- Método GetBackingStore Direct3D 11
- Método GetBackingStore Direct3D 11, interfaz ID3DX11EffectSamplerVariable
- Interfaz ID3DX11EffectSamplerVariable Direct3D 11, método GetBackingStore
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable.GetBackingStore
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03f2d6ac3035d1dd2fd3aee8950135d7b4481862
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362672"
---
# <a name="id3dx11effectsamplervariablegetbackingstore-method"></a><span data-ttu-id="5c2e6-106">ID3DX11EffectSamplerVariable:: GetBackingStore (método)</span><span class="sxs-lookup"><span data-stu-id="5c2e6-106">ID3DX11EffectSamplerVariable::GetBackingStore method</span></span>

<span data-ttu-id="5c2e6-107">Obtiene un puntero a una variable que contiene el estado de muestra.</span><span class="sxs-lookup"><span data-stu-id="5c2e6-107">Get a pointer to a variable that contains sampler state.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c2e6-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5c2e6-108">Syntax</span></span>


```C++
HRESULT GetBackingStore(
   UINT               Index,
   D3D11_SAMPLER_DESC *pSamplerDesc
);
```



## <a name="parameters"></a><span data-ttu-id="5c2e6-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5c2e6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c2e6-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="5c2e6-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="5c2e6-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5c2e6-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5c2e6-112">Índice en una matriz de descripciones de muestra.</span><span class="sxs-lookup"><span data-stu-id="5c2e6-112">Index into an array of sampler descriptions.</span></span> <span data-ttu-id="5c2e6-113">Si solo hay una variable de muestrario en el efecto, use 0.</span><span class="sxs-lookup"><span data-stu-id="5c2e6-113">If there is only one sampler variable in the effect, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="5c2e6-114">*pSamplerDesc*</span><span class="sxs-lookup"><span data-stu-id="5c2e6-114">*pSamplerDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="5c2e6-115">Tipo: **[ **D3D11 \_ muestra \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)\***</span><span class="sxs-lookup"><span data-stu-id="5c2e6-115">Type: **[**D3D11\_SAMPLER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)\***</span></span>

<span data-ttu-id="5c2e6-116">Un puntero a una descripción de muestra (vea [**D3D11 \_ muestra \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)).</span><span class="sxs-lookup"><span data-stu-id="5c2e6-116">A pointer to a sampler description (see [**D3D11\_SAMPLER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c2e6-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5c2e6-117">Return value</span></span>

<span data-ttu-id="5c2e6-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5c2e6-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5c2e6-119">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="5c2e6-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5c2e6-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5c2e6-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5c2e6-121">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="5c2e6-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="5c2e6-122">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="5c2e6-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="5c2e6-123">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="5c2e6-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5c2e6-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c2e6-124">Requirements</span></span>



| <span data-ttu-id="5c2e6-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c2e6-125">Requirement</span></span> | <span data-ttu-id="5c2e6-126">Value</span><span class="sxs-lookup"><span data-stu-id="5c2e6-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c2e6-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5c2e6-127">Header</span></span><br/>  | <dl> <span data-ttu-id="5c2e6-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c2e6-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="5c2e6-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5c2e6-129">Library</span></span><br/> | <dl> <span data-ttu-id="5c2e6-130"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="5c2e6-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c2e6-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="5c2e6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c2e6-132">ID3DX11EffectSamplerVariable</span><span class="sxs-lookup"><span data-stu-id="5c2e6-132">ID3DX11EffectSamplerVariable</span></span>](id3dx11effectsamplervariable.md)
</dt> </dl>

 

