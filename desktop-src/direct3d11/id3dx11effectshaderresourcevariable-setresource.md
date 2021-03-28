---
title: Método ID3DX11EffectShaderResourceVariable SetResource (D3dx11effect. h)
description: Establezca un recurso de sombreador.
ms.assetid: f85c33ff-dc00-4421-939c-74f9317faadc
keywords:
- Método SetResource Direct3D 11
- Método SetResource Direct3D 11, interfaz ID3DX11EffectShaderResourceVariable
- Interfaz ID3DX11EffectShaderResourceVariable Direct3D 11, método SetResource
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderResourceVariable.SetResource
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddec6c7daa2db552d6b5befee02bf57c6047dc5a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362819"
---
# <a name="id3dx11effectshaderresourcevariablesetresource-method"></a><span data-ttu-id="db3d8-106">ID3DX11EffectShaderResourceVariable:: SetResource (método)</span><span class="sxs-lookup"><span data-stu-id="db3d8-106">ID3DX11EffectShaderResourceVariable::SetResource method</span></span>

<span data-ttu-id="db3d8-107">Establezca un recurso de sombreador.</span><span class="sxs-lookup"><span data-stu-id="db3d8-107">Set a shader resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="db3d8-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="db3d8-108">Syntax</span></span>


```C++
HRESULT SetResource(
   ID3D11ShaderResourceView *pResource
);
```



## <a name="parameters"></a><span data-ttu-id="db3d8-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="db3d8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db3d8-110">*código fuente*</span><span class="sxs-lookup"><span data-stu-id="db3d8-110">*pResource*</span></span> 
</dt> <dd>

<span data-ttu-id="db3d8-111">Tipo: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\***</span><span class="sxs-lookup"><span data-stu-id="db3d8-111">Type: **[**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\***</span></span>

<span data-ttu-id="db3d8-112">Dirección de un puntero a una interfaz de vista de recursos del sombreador.</span><span class="sxs-lookup"><span data-stu-id="db3d8-112">The address of a pointer to a shader-resource-view interface.</span></span> <span data-ttu-id="db3d8-113">Vea [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="db3d8-113">See [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db3d8-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="db3d8-114">Return value</span></span>

<span data-ttu-id="db3d8-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="db3d8-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="db3d8-116">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="db3d8-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="db3d8-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="db3d8-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="db3d8-118">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="db3d8-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="db3d8-119">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="db3d8-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="db3d8-120">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="db3d8-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="db3d8-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db3d8-121">Requirements</span></span>



| <span data-ttu-id="db3d8-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="db3d8-122">Requirement</span></span> | <span data-ttu-id="db3d8-123">Value</span><span class="sxs-lookup"><span data-stu-id="db3d8-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db3d8-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="db3d8-124">Header</span></span><br/>  | <dl> <span data-ttu-id="db3d8-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="db3d8-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="db3d8-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="db3d8-126">Library</span></span><br/> | <dl> <span data-ttu-id="db3d8-127"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="db3d8-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db3d8-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="db3d8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db3d8-129">ID3DX11EffectShaderResourceVariable</span><span class="sxs-lookup"><span data-stu-id="db3d8-129">ID3DX11EffectShaderResourceVariable</span></span>](id3dx11effectshaderresourcevariable.md)
</dt> </dl>

 

 





