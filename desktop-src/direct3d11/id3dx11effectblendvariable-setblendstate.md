---
title: Método ID3DX11EffectBlendVariable SetBlendState (D3dx11effect. h)
description: Establece el estado de fusión de un efecto.
ms.assetid: 46100721-65a3-46de-aa22-3e7e2fb7b960
keywords:
- Método SetBlendState Direct3D 11
- Método SetBlendState Direct3D 11, interfaz ID3DX11EffectBlendVariable
- Interfaz ID3DX11EffectBlendVariable Direct3D 11, método SetBlendState
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable.SetBlendState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ce781f29c521df7b81821cb19a56e6fd3999310
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821311"
---
# <a name="id3dx11effectblendvariablesetblendstate-method"></a><span data-ttu-id="66d35-106">ID3DX11EffectBlendVariable:: SetBlendState (método)</span><span class="sxs-lookup"><span data-stu-id="66d35-106">ID3DX11EffectBlendVariable::SetBlendState method</span></span>

<span data-ttu-id="66d35-107">Establece el estado de fusión de un efecto.</span><span class="sxs-lookup"><span data-stu-id="66d35-107">Sets an effect's blend-state.</span></span>

## <a name="syntax"></a><span data-ttu-id="66d35-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="66d35-108">Syntax</span></span>


```C++
HRESULT SetBlendState(
   UINT             Index,
   ID3D11BlendState *pBlendState
);
```



## <a name="parameters"></a><span data-ttu-id="66d35-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="66d35-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66d35-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="66d35-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="66d35-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="66d35-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="66d35-112">Índice en una matriz de interfaces de estado de mezcla.</span><span class="sxs-lookup"><span data-stu-id="66d35-112">Index into an array of blend-state interfaces.</span></span> <span data-ttu-id="66d35-113">Si solo hay una interfaz de estado de mezcla, use 0.</span><span class="sxs-lookup"><span data-stu-id="66d35-113">If there is only one blend-state interface, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="66d35-114">*pBlendState*</span><span class="sxs-lookup"><span data-stu-id="66d35-114">*pBlendState*</span></span> 
</dt> <dd>

<span data-ttu-id="66d35-115">Tipo: **[ **ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)\***</span><span class="sxs-lookup"><span data-stu-id="66d35-115">Type: **[**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)\***</span></span>

<span data-ttu-id="66d35-116">Puntero a una interfaz [**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate) que contiene el estado de combinación que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="66d35-116">A pointer to an [**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate) interface containing the blend-state to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66d35-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="66d35-117">Return value</span></span>

<span data-ttu-id="66d35-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="66d35-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="66d35-119">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="66d35-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="66d35-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="66d35-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="66d35-121">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="66d35-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="66d35-122">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="66d35-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="66d35-123">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="66d35-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="66d35-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66d35-124">Requirements</span></span>



| <span data-ttu-id="66d35-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="66d35-125">Requirement</span></span> | <span data-ttu-id="66d35-126">Value</span><span class="sxs-lookup"><span data-stu-id="66d35-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66d35-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="66d35-127">Header</span></span><br/>  | <dl> <span data-ttu-id="66d35-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="66d35-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="66d35-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="66d35-129">Library</span></span><br/> | <dl> <span data-ttu-id="66d35-130"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="66d35-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66d35-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="66d35-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66d35-132">ID3DX11EffectBlendVariable</span><span class="sxs-lookup"><span data-stu-id="66d35-132">ID3DX11EffectBlendVariable</span></span>](id3dx11effectblendvariable.md)
</dt> </dl>

 

