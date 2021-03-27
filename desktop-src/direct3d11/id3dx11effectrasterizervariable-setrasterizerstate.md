---
title: Método ID3DX11EffectRasterizerVariable SetRasterizerState (D3dx11effect. h)
description: Establece el estado del rasterizador.
ms.assetid: b2cd93fb-77bb-4a39-b686-7b8f683c9172
keywords:
- Método SetRasterizerState Direct3D 11
- Método SetRasterizerState Direct3D 11, interfaz ID3DX11EffectRasterizerVariable
- Interfaz ID3DX11EffectRasterizerVariable Direct3D 11, método SetRasterizerState
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable.SetRasterizerState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c1f44df653339f274207bfa4283fc8470c8844f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280522"
---
# <a name="id3dx11effectrasterizervariablesetrasterizerstate-method"></a><span data-ttu-id="704a1-106">ID3DX11EffectRasterizerVariable:: SetRasterizerState (método)</span><span class="sxs-lookup"><span data-stu-id="704a1-106">ID3DX11EffectRasterizerVariable::SetRasterizerState method</span></span>

<span data-ttu-id="704a1-107">Establece el estado del rasterizador.</span><span class="sxs-lookup"><span data-stu-id="704a1-107">Sets the rasterizer state.</span></span>

## <a name="syntax"></a><span data-ttu-id="704a1-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="704a1-108">Syntax</span></span>


```C++
HRESULT SetRasterizerState(
   UINT                  Index,
   ID3D11RasterizerState *pRasterizerState
);
```



## <a name="parameters"></a><span data-ttu-id="704a1-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="704a1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="704a1-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="704a1-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="704a1-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="704a1-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="704a1-112">Índice en una matriz de interfaces de rasterizador.</span><span class="sxs-lookup"><span data-stu-id="704a1-112">Index into an array of rasterizer interfaces.</span></span> <span data-ttu-id="704a1-113">Si solo hay una interfaz de rasterización, use 0.</span><span class="sxs-lookup"><span data-stu-id="704a1-113">If there is only one rasterizer interface, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="704a1-114">*pRasterizerState*</span><span class="sxs-lookup"><span data-stu-id="704a1-114">*pRasterizerState*</span></span> 
</dt> <dd>

<span data-ttu-id="704a1-115">Tipo: **[ **ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)\***</span><span class="sxs-lookup"><span data-stu-id="704a1-115">Type: **[**ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)\***</span></span>

<span data-ttu-id="704a1-116">Puntero a una interfaz [**ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate) .</span><span class="sxs-lookup"><span data-stu-id="704a1-116">Pointer to an [**ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="704a1-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="704a1-117">Return value</span></span>

<span data-ttu-id="704a1-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="704a1-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="704a1-119">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="704a1-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="704a1-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="704a1-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="704a1-121">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="704a1-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="704a1-122">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="704a1-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="704a1-123">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="704a1-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="704a1-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="704a1-124">Requirements</span></span>



| <span data-ttu-id="704a1-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="704a1-125">Requirement</span></span> | <span data-ttu-id="704a1-126">Value</span><span class="sxs-lookup"><span data-stu-id="704a1-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="704a1-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="704a1-127">Header</span></span><br/>  | <dl> <span data-ttu-id="704a1-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="704a1-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="704a1-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="704a1-129">Library</span></span><br/> | <dl> <span data-ttu-id="704a1-130"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="704a1-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="704a1-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="704a1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="704a1-132">ID3DX11EffectRasterizerVariable</span><span class="sxs-lookup"><span data-stu-id="704a1-132">ID3DX11EffectRasterizerVariable</span></span>](id3dx11effectrasterizervariable.md)
</dt> </dl>

 

