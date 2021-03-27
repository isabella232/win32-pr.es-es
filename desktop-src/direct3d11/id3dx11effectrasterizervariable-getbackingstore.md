---
title: Método ID3DX11EffectRasterizerVariable GetBackingStore (D3dx11effect. h)
description: Obtiene un puntero a una variable que contiene el estado de rasteriser.
ms.assetid: aff62a6c-bdef-49ad-9492-5db0878f632e
keywords:
- Método GetBackingStore Direct3D 11
- Método GetBackingStore Direct3D 11, interfaz ID3DX11EffectRasterizerVariable
- Interfaz ID3DX11EffectRasterizerVariable Direct3D 11, método GetBackingStore
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable.GetBackingStore
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1941ba93b69f1d07eeebaa6c1f0c9323f5c0a49e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083782"
---
# <a name="id3dx11effectrasterizervariablegetbackingstore-method"></a><span data-ttu-id="615b9-106">ID3DX11EffectRasterizerVariable:: GetBackingStore (método)</span><span class="sxs-lookup"><span data-stu-id="615b9-106">ID3DX11EffectRasterizerVariable::GetBackingStore method</span></span>

<span data-ttu-id="615b9-107">Obtiene un puntero a una variable que contiene el estado de rasteriser.</span><span class="sxs-lookup"><span data-stu-id="615b9-107">Get a pointer to a variable that contains rasteriser state.</span></span>

## <a name="syntax"></a><span data-ttu-id="615b9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="615b9-108">Syntax</span></span>


```C++
HRESULT GetBackingStore(
   UINT                  Index,
   D3D11_RASTERIZER_DESC *pRasterizerDesc
);
```



## <a name="parameters"></a><span data-ttu-id="615b9-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="615b9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="615b9-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="615b9-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="615b9-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="615b9-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="615b9-112">Índice en una matriz de descripciones de estado de rasteriser.</span><span class="sxs-lookup"><span data-stu-id="615b9-112">Index into an array of rasteriser-state descriptions.</span></span> <span data-ttu-id="615b9-113">Si solo hay una variable rasteriser en el efecto, use 0.</span><span class="sxs-lookup"><span data-stu-id="615b9-113">If there is only one rasteriser variable in the effect, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="615b9-114">*pRasterizerDesc*</span><span class="sxs-lookup"><span data-stu-id="615b9-114">*pRasterizerDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="615b9-115">Tipo: **[ **\_ \_ Descripción del rasterizador D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)\***</span><span class="sxs-lookup"><span data-stu-id="615b9-115">Type: **[**D3D11\_RASTERIZER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)\***</span></span>

<span data-ttu-id="615b9-116">Un puntero a una descripción de rasteriser-State (vea [**D3D11 de \_ rasterización de trama \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)).</span><span class="sxs-lookup"><span data-stu-id="615b9-116">A pointer to a rasteriser-state description (see [**D3D11\_RASTERIZER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="615b9-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="615b9-117">Return value</span></span>

<span data-ttu-id="615b9-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="615b9-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="615b9-119">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="615b9-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="615b9-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="615b9-120">Remarks</span></span>

<span data-ttu-id="615b9-121">Las variables de efecto se guardan en la memoria de la memoria auxiliar. Cuando se aplica una técnica, los valores de la memoria auxiliar se copian en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="615b9-121">Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device.</span></span> <span data-ttu-id="615b9-122">Los datos de la memoria auxiliar se pueden usar para volver a crear la variable cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="615b9-122">Backing store data can used to recreate the variable when necessary.</span></span>

> [!Note]  
> <span data-ttu-id="615b9-123">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="615b9-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="615b9-124">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="615b9-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="615b9-125">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="615b9-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="615b9-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="615b9-126">Requirements</span></span>



| <span data-ttu-id="615b9-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="615b9-127">Requirement</span></span> | <span data-ttu-id="615b9-128">Value</span><span class="sxs-lookup"><span data-stu-id="615b9-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="615b9-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="615b9-129">Header</span></span><br/>  | <dl> <span data-ttu-id="615b9-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="615b9-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="615b9-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="615b9-131">Library</span></span><br/> | <dl> <span data-ttu-id="615b9-132"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="615b9-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="615b9-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="615b9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="615b9-134">ID3DX11EffectRasterizerVariable</span><span class="sxs-lookup"><span data-stu-id="615b9-134">ID3DX11EffectRasterizerVariable</span></span>](id3dx11effectrasterizervariable.md)
</dt> </dl>

 

