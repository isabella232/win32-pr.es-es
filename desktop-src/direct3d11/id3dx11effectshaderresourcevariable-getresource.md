---
title: Método GetResource de ID3DX11EffectShaderResourceVariable (D3dx11effect. h)
description: Obtiene un recurso de sombreador.
ms.assetid: 7c56aba0-ce60-4b50-9c1a-802bf1d73c6b
keywords:
- Método GetResource Direct3D 11
- Método GetResource Direct3D 11, interfaz ID3DX11EffectShaderResourceVariable
- Interfaz ID3DX11EffectShaderResourceVariable Direct3D 11, método GetResource
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderResourceVariable.GetResource
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cea841ae63646958603396d5b65305c242961942
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280251"
---
# <a name="id3dx11effectshaderresourcevariablegetresource-method"></a><span data-ttu-id="79593-106">ID3DX11EffectShaderResourceVariable:: GetResource (método)</span><span class="sxs-lookup"><span data-stu-id="79593-106">ID3DX11EffectShaderResourceVariable::GetResource method</span></span>

<span data-ttu-id="79593-107">Obtiene un recurso de sombreador.</span><span class="sxs-lookup"><span data-stu-id="79593-107">Get a shader resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="79593-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="79593-108">Syntax</span></span>


```C++
HRESULT GetResource(
   ID3D11ShaderResourceView **ppResource
);
```



## <a name="parameters"></a><span data-ttu-id="79593-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="79593-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79593-110">*ppResource*</span><span class="sxs-lookup"><span data-stu-id="79593-110">*ppResource*</span></span> 
</dt> <dd>

<span data-ttu-id="79593-111">Tipo: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="79593-111">Type: **[**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span></span>

<span data-ttu-id="79593-112">Dirección de un puntero a una interfaz de vista de recursos del sombreador.</span><span class="sxs-lookup"><span data-stu-id="79593-112">The address of a pointer to a shader-resource-view interface.</span></span> <span data-ttu-id="79593-113">Vea [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="79593-113">See [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79593-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="79593-114">Return value</span></span>

<span data-ttu-id="79593-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="79593-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="79593-116">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="79593-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="79593-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="79593-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="79593-118">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="79593-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="79593-119">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="79593-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="79593-120">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="79593-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="79593-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79593-121">Requirements</span></span>



| <span data-ttu-id="79593-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="79593-122">Requirement</span></span> | <span data-ttu-id="79593-123">Value</span><span class="sxs-lookup"><span data-stu-id="79593-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79593-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="79593-124">Header</span></span><br/>  | <dl> <span data-ttu-id="79593-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="79593-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="79593-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="79593-126">Library</span></span><br/> | <dl> <span data-ttu-id="79593-127"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="79593-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79593-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="79593-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79593-129">ID3DX11EffectShaderResourceVariable</span><span class="sxs-lookup"><span data-stu-id="79593-129">ID3DX11EffectShaderResourceVariable</span></span>](id3dx11effectshaderresourcevariable.md)
</dt> </dl>

 

 





