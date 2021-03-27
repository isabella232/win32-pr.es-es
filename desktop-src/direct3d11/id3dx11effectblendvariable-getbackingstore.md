---
title: Método ID3DX11EffectBlendVariable GetBackingStore (D3dx11effect. h)
description: Obtiene un puntero a una variable de estado de mezcla.
ms.assetid: 809daaad-9bf0-48fb-ae91-f237c43db324
keywords:
- Método GetBackingStore Direct3D 11
- Método GetBackingStore Direct3D 11, interfaz ID3DX11EffectBlendVariable
- Interfaz ID3DX11EffectBlendVariable Direct3D 11, método GetBackingStore
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable.GetBackingStore
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0220481b58931edace2a5dfe7298d83f7bd1325
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280448"
---
# <a name="id3dx11effectblendvariablegetbackingstore-method"></a><span data-ttu-id="11cdd-106">ID3DX11EffectBlendVariable:: GetBackingStore (método)</span><span class="sxs-lookup"><span data-stu-id="11cdd-106">ID3DX11EffectBlendVariable::GetBackingStore method</span></span>

<span data-ttu-id="11cdd-107">Obtiene un puntero a una variable de estado de mezcla.</span><span class="sxs-lookup"><span data-stu-id="11cdd-107">Get a pointer to a blend-state variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="11cdd-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="11cdd-108">Syntax</span></span>


```C++
HRESULT GetBackingStore(
   UINT             Index,
   D3D11_BLEND_DESC *pBlendDesc
);
```



## <a name="parameters"></a><span data-ttu-id="11cdd-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="11cdd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11cdd-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="11cdd-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="11cdd-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="11cdd-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="11cdd-112">Índice en una matriz de descripciones de estado de Blend.</span><span class="sxs-lookup"><span data-stu-id="11cdd-112">Index into an array of blend-state descriptions.</span></span> <span data-ttu-id="11cdd-113">Si solo hay una variable de estado de mezcla en el efecto, use 0.</span><span class="sxs-lookup"><span data-stu-id="11cdd-113">If there is only one blend-state variable in the effect, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="11cdd-114">*pBlendDesc*</span><span class="sxs-lookup"><span data-stu-id="11cdd-114">*pBlendDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="11cdd-115">Tipo: **[ **D3D11 \_ Blend \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)\***</span><span class="sxs-lookup"><span data-stu-id="11cdd-115">Type: **[**D3D11\_BLEND\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)\***</span></span>

<span data-ttu-id="11cdd-116">Un puntero a una descripción del estado de Blend (vea [**D3D11 \_ Blend \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)).</span><span class="sxs-lookup"><span data-stu-id="11cdd-116">A pointer to a blend-state description (see [**D3D11\_BLEND\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11cdd-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="11cdd-117">Return value</span></span>

<span data-ttu-id="11cdd-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="11cdd-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="11cdd-119">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="11cdd-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="11cdd-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="11cdd-120">Remarks</span></span>

<span data-ttu-id="11cdd-121">Las variables de efecto se guardan en la memoria de la memoria auxiliar. Cuando se aplica una técnica, los valores de la memoria auxiliar se copian en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="11cdd-121">Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device.</span></span> <span data-ttu-id="11cdd-122">Los datos de la memoria auxiliar se pueden usar para volver a crear la variable cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="11cdd-122">Backing store data can used to recreate the variable when necessary.</span></span>

> [!Note]  
> <span data-ttu-id="11cdd-123">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="11cdd-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="11cdd-124">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="11cdd-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="11cdd-125">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="11cdd-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="11cdd-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11cdd-126">Requirements</span></span>



| <span data-ttu-id="11cdd-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="11cdd-127">Requirement</span></span> | <span data-ttu-id="11cdd-128">Value</span><span class="sxs-lookup"><span data-stu-id="11cdd-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11cdd-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="11cdd-129">Header</span></span><br/>  | <dl> <span data-ttu-id="11cdd-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="11cdd-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="11cdd-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="11cdd-131">Library</span></span><br/> | <dl> <span data-ttu-id="11cdd-132"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="11cdd-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11cdd-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="11cdd-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11cdd-134">ID3DX11EffectBlendVariable</span><span class="sxs-lookup"><span data-stu-id="11cdd-134">ID3DX11EffectBlendVariable</span></span>](id3dx11effectblendvariable.md)
</dt> </dl>

 

