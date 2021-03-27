---
title: Método ID3DX11EffectRasterizerVariable GetRasterizerState (D3dx11effect. h)
description: Obtiene un puntero a una interfaz de rasterizador.
ms.assetid: 4b8515e0-b79a-4572-9142-07c50a8839b8
keywords:
- Método GetRasterizerState Direct3D 11
- Método GetRasterizerState Direct3D 11, interfaz ID3DX11EffectRasterizerVariable
- Interfaz ID3DX11EffectRasterizerVariable Direct3D 11, método GetRasterizerState
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable.GetRasterizerState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 972140a8f74a3e5a6728429faddacc253aaa6c9d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987259"
---
# <a name="id3dx11effectrasterizervariablegetrasterizerstate-method"></a><span data-ttu-id="660f4-106">ID3DX11EffectRasterizerVariable:: GetRasterizerState (método)</span><span class="sxs-lookup"><span data-stu-id="660f4-106">ID3DX11EffectRasterizerVariable::GetRasterizerState method</span></span>

<span data-ttu-id="660f4-107">Obtiene un puntero a una interfaz de rasterizador.</span><span class="sxs-lookup"><span data-stu-id="660f4-107">Get a pointer to a rasterizer interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="660f4-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="660f4-108">Syntax</span></span>


```C++
HRESULT GetRasterizerState(
   UINT                  Index,
   ID3D11RasterizerState **ppRasterizerState
);
```



## <a name="parameters"></a><span data-ttu-id="660f4-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="660f4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="660f4-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="660f4-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="660f4-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="660f4-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="660f4-112">Índice en una matriz de interfaces de rasterizador.</span><span class="sxs-lookup"><span data-stu-id="660f4-112">Index into an array of rasterizer interfaces.</span></span> <span data-ttu-id="660f4-113">Si solo hay una interfaz de rasterización, use 0.</span><span class="sxs-lookup"><span data-stu-id="660f4-113">If there is only one rasterizer interface, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="660f4-114">*ppRasterizerState*</span><span class="sxs-lookup"><span data-stu-id="660f4-114">*ppRasterizerState*</span></span> 
</dt> <dd>

<span data-ttu-id="660f4-115">Tipo: **[ **ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)\*\***</span><span class="sxs-lookup"><span data-stu-id="660f4-115">Type: **[**ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)\*\***</span></span>

<span data-ttu-id="660f4-116">La dirección de un puntero a una interfaz de rasterizador (vea [**ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)).</span><span class="sxs-lookup"><span data-stu-id="660f4-116">The address of a pointer to a rasterizer interface (see [**ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="660f4-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="660f4-117">Return value</span></span>

<span data-ttu-id="660f4-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="660f4-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="660f4-119">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="660f4-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="660f4-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="660f4-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="660f4-121">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="660f4-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="660f4-122">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="660f4-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="660f4-123">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="660f4-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="660f4-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="660f4-124">Requirements</span></span>



| <span data-ttu-id="660f4-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="660f4-125">Requirement</span></span> | <span data-ttu-id="660f4-126">Value</span><span class="sxs-lookup"><span data-stu-id="660f4-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="660f4-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="660f4-127">Header</span></span><br/>  | <dl> <span data-ttu-id="660f4-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="660f4-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="660f4-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="660f4-129">Library</span></span><br/> | <dl> <span data-ttu-id="660f4-130"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="660f4-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="660f4-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="660f4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="660f4-132">ID3DX11EffectRasterizerVariable</span><span class="sxs-lookup"><span data-stu-id="660f4-132">ID3DX11EffectRasterizerVariable</span></span>](id3dx11effectrasterizervariable.md)
</dt> </dl>

 

