---
title: Método ID3DX11EffectDepthStencilVariable GetBackingStore (D3dx11effect. h)
description: Obtiene un puntero a una variable que contiene el estado de la galería de símbolos de profundidad.
ms.assetid: 6aeed5ac-f0ee-4e8c-b87b-022f58c9094c
keywords:
- Método GetBackingStore Direct3D 11
- Método GetBackingStore Direct3D 11, interfaz ID3DX11EffectDepthStencilVariable
- Interfaz ID3DX11EffectDepthStencilVariable Direct3D 11, método GetBackingStore
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable.GetBackingStore
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9335817b9c954958c97294a88291f83bf0e967d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986982"
---
# <a name="id3dx11effectdepthstencilvariablegetbackingstore-method"></a><span data-ttu-id="d41a6-106">ID3DX11EffectDepthStencilVariable:: GetBackingStore (método)</span><span class="sxs-lookup"><span data-stu-id="d41a6-106">ID3DX11EffectDepthStencilVariable::GetBackingStore method</span></span>

<span data-ttu-id="d41a6-107">Obtiene un puntero a una variable que contiene el estado de la galería de símbolos de profundidad.</span><span class="sxs-lookup"><span data-stu-id="d41a6-107">Get a pointer to a variable that contains depth-stencil state.</span></span>

## <a name="syntax"></a><span data-ttu-id="d41a6-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d41a6-108">Syntax</span></span>


```C++
HRESULT GetBackingStore(
   UINT                     Index,
   D3D11_DEPTH_STENCIL_DESC *pDepthStencilDesc
);
```



## <a name="parameters"></a><span data-ttu-id="d41a6-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d41a6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d41a6-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="d41a6-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="d41a6-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d41a6-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d41a6-112">Índice en una matriz de descripciones de estado de estarcido de profundidad.</span><span class="sxs-lookup"><span data-stu-id="d41a6-112">Index into an array of depth-stencil-state descriptions.</span></span> <span data-ttu-id="d41a6-113">Si solo hay una variable de estarcido de profundidad en el efecto, use 0.</span><span class="sxs-lookup"><span data-stu-id="d41a6-113">If there is only one depth-stencil variable in the effect, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="d41a6-114">*pDepthStencilDesc*</span><span class="sxs-lookup"><span data-stu-id="d41a6-114">*pDepthStencilDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="d41a6-115">Tipo: D3D11 de la **[ **\_ Galería de \_ símbolos \_ de profundidad**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)\***</span><span class="sxs-lookup"><span data-stu-id="d41a6-115">Type: **[**D3D11\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)\***</span></span>

<span data-ttu-id="d41a6-116">Un puntero a una descripción del estado de la galería de símbolos de profundidad (consulte [**D3D11 \_ Depth \_ estarcido \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)).</span><span class="sxs-lookup"><span data-stu-id="d41a6-116">A pointer to a depth-stencil-state description (see [**D3D11\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d41a6-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d41a6-117">Return value</span></span>

<span data-ttu-id="d41a6-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d41a6-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d41a6-119">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="d41a6-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d41a6-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d41a6-120">Remarks</span></span>

<span data-ttu-id="d41a6-121">Las variables de efecto se guardan en la memoria de la memoria auxiliar. Cuando se aplica una técnica, los valores de la memoria auxiliar se copian en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d41a6-121">Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device.</span></span> <span data-ttu-id="d41a6-122">Los datos de la memoria auxiliar se pueden usar para volver a crear la variable cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="d41a6-122">Backing store data can used to recreate the variable when necessary.</span></span>

> [!Note]  
> <span data-ttu-id="d41a6-123">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="d41a6-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="d41a6-124">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="d41a6-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="d41a6-125">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="d41a6-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d41a6-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d41a6-126">Requirements</span></span>



| <span data-ttu-id="d41a6-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="d41a6-127">Requirement</span></span> | <span data-ttu-id="d41a6-128">Value</span><span class="sxs-lookup"><span data-stu-id="d41a6-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d41a6-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d41a6-129">Header</span></span><br/>  | <dl> <span data-ttu-id="d41a6-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="d41a6-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="d41a6-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d41a6-131">Library</span></span><br/> | <dl> <span data-ttu-id="d41a6-132"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="d41a6-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d41a6-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="d41a6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d41a6-134">ID3DX11EffectDepthStencilVariable</span><span class="sxs-lookup"><span data-stu-id="d41a6-134">ID3DX11EffectDepthStencilVariable</span></span>](id3dx11effectdepthstencilvariable.md)
</dt> </dl>

 

