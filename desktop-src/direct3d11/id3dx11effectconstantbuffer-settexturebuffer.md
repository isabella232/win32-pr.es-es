---
title: Método ID3DX11EffectConstantBuffer SetTextureBuffer (D3dx11effect. h)
description: Establezca un búfer de textura.
ms.assetid: b8c327e4-52ff-498e-81e9-187e58bbe5d2
keywords:
- Método SetTextureBuffer Direct3D 11
- Método SetTextureBuffer Direct3D 11, interfaz ID3DX11EffectConstantBuffer
- Interfaz ID3DX11EffectConstantBuffer Direct3D 11, método SetTextureBuffer
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer.SetTextureBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 736ec4c5f0125dfc37925d67875cf97c5441117c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986833"
---
# <a name="id3dx11effectconstantbuffersettexturebuffer-method"></a><span data-ttu-id="2e689-106">ID3DX11EffectConstantBuffer:: SetTextureBuffer (método)</span><span class="sxs-lookup"><span data-stu-id="2e689-106">ID3DX11EffectConstantBuffer::SetTextureBuffer method</span></span>

<span data-ttu-id="2e689-107">Establezca un búfer de textura.</span><span class="sxs-lookup"><span data-stu-id="2e689-107">Set a texture-buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e689-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2e689-108">Syntax</span></span>


```C++
HRESULT SetTextureBuffer(
   ID3D11ShaderResourceView *pTextureBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="2e689-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2e689-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e689-110">*pTextureBuffer*</span><span class="sxs-lookup"><span data-stu-id="2e689-110">*pTextureBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="2e689-111">Tipo: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\***</span><span class="sxs-lookup"><span data-stu-id="2e689-111">Type: **[**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\***</span></span>

<span data-ttu-id="2e689-112">Puntero a una interfaz de vista de recursos del sombreador para tener acceso a un búfer de textura.</span><span class="sxs-lookup"><span data-stu-id="2e689-112">A pointer to a shader-resource-view interface for accessing a texture buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e689-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2e689-113">Return value</span></span>

<span data-ttu-id="2e689-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2e689-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2e689-115">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="2e689-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2e689-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e689-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2e689-117">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="2e689-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="2e689-118">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="2e689-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="2e689-119">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="2e689-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2e689-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e689-120">Requirements</span></span>



| <span data-ttu-id="2e689-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e689-121">Requirement</span></span> | <span data-ttu-id="2e689-122">Value</span><span class="sxs-lookup"><span data-stu-id="2e689-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e689-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2e689-123">Header</span></span><br/>  | <dl> <span data-ttu-id="2e689-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e689-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="2e689-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2e689-125">Library</span></span><br/> | <dl> <span data-ttu-id="2e689-126"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="2e689-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e689-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e689-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e689-128">ID3DX11EffectConstantBuffer</span><span class="sxs-lookup"><span data-stu-id="2e689-128">ID3DX11EffectConstantBuffer</span></span>](id3dx11effectconstantbuffer.md)
</dt> </dl>

 

 





