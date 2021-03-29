---
title: Método ID3DX11EffectConstantBuffer GetTextureBuffer (D3dx11effect. h)
description: Obtiene un búfer de textura.
ms.assetid: 8d09e67c-358e-49ee-8ca4-e1f548b52c3a
keywords:
- Método GetTextureBuffer Direct3D 11
- Método GetTextureBuffer Direct3D 11, interfaz ID3DX11EffectConstantBuffer
- Interfaz ID3DX11EffectConstantBuffer Direct3D 11, método GetTextureBuffer
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer.GetTextureBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d03000338c725e71096e57715a49a70b4347b358
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987150"
---
# <a name="id3dx11effectconstantbuffergettexturebuffer-method"></a><span data-ttu-id="4cc25-106">ID3DX11EffectConstantBuffer:: GetTextureBuffer (método)</span><span class="sxs-lookup"><span data-stu-id="4cc25-106">ID3DX11EffectConstantBuffer::GetTextureBuffer method</span></span>

<span data-ttu-id="4cc25-107">Obtiene un búfer de textura.</span><span class="sxs-lookup"><span data-stu-id="4cc25-107">Get a texture-buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cc25-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4cc25-108">Syntax</span></span>


```C++
HRESULT GetTextureBuffer(
   ID3D11ShaderResourceView **ppTextureBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="4cc25-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4cc25-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cc25-110">*ppTextureBuffer*</span><span class="sxs-lookup"><span data-stu-id="4cc25-110">*ppTextureBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="4cc25-111">Tipo: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="4cc25-111">Type: **[**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span></span>

<span data-ttu-id="4cc25-112">Dirección de un puntero a una interfaz de vista de recursos del sombreador para tener acceso a un búfer de textura.</span><span class="sxs-lookup"><span data-stu-id="4cc25-112">The address of a pointer to a shader-resource-view interface for accessing a texture buffer.</span></span> <span data-ttu-id="4cc25-113">Vea [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="4cc25-113">See [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cc25-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4cc25-114">Return value</span></span>

<span data-ttu-id="4cc25-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4cc25-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4cc25-116">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="4cc25-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4cc25-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4cc25-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4cc25-118">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="4cc25-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="4cc25-119">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="4cc25-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="4cc25-120">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="4cc25-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4cc25-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4cc25-121">Requirements</span></span>



| <span data-ttu-id="4cc25-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cc25-122">Requirement</span></span> | <span data-ttu-id="4cc25-123">Value</span><span class="sxs-lookup"><span data-stu-id="4cc25-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cc25-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4cc25-124">Header</span></span><br/>  | <dl> <span data-ttu-id="4cc25-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cc25-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="4cc25-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4cc25-126">Library</span></span><br/> | <dl> <span data-ttu-id="4cc25-127"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="4cc25-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cc25-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="4cc25-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cc25-129">ID3DX11EffectConstantBuffer</span><span class="sxs-lookup"><span data-stu-id="4cc25-129">ID3DX11EffectConstantBuffer</span></span>](id3dx11effectconstantbuffer.md)
</dt> </dl>

 

 





