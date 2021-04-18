---
title: Método ID3DX11EffectPass GetDomainShaderDesc (D3dx11effect. h)
description: Obtiene una descripción del sombreador de dominio.
ms.assetid: 02109930-0922-46b8-9381-bb75abd0c4a0
keywords:
- Método GetDomainShaderDesc Direct3D 11
- Método GetDomainShaderDesc Direct3D 11, interfaz ID3DX11EffectPass
- Interfaz ID3DX11EffectPass Direct3D 11, método GetDomainShaderDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetDomainShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2157134d97332fc9c76267f5e0db49d2c40e96a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987108"
---
# <a name="id3dx11effectpassgetdomainshaderdesc-method"></a><span data-ttu-id="df09d-106">ID3DX11EffectPass:: GetDomainShaderDesc (método)</span><span class="sxs-lookup"><span data-stu-id="df09d-106">ID3DX11EffectPass::GetDomainShaderDesc method</span></span>

<span data-ttu-id="df09d-107">Obtiene una descripción del sombreador de dominio.</span><span class="sxs-lookup"><span data-stu-id="df09d-107">Get a domain-shader description.</span></span>

## <a name="syntax"></a><span data-ttu-id="df09d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="df09d-108">Syntax</span></span>


```C++
HRESULT GetDomainShaderDesc(
   D3DX11_PASS_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="df09d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="df09d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df09d-110">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="df09d-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="df09d-111">Tipo: **[ **D3DX11 \_ Pass \_ Shader \_ DESC**](d3dx11-pass-shader-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="df09d-111">Type: **[**D3DX11\_PASS\_SHADER\_DESC**](d3dx11-pass-shader-desc.md)\***</span></span>

<span data-ttu-id="df09d-112">Un puntero a una descripción del sombreador de dominio (vea [**D3DX11 \_ Pass \_ Shader \_ DESC**](d3dx11-pass-shader-desc.md)).</span><span class="sxs-lookup"><span data-stu-id="df09d-112">A pointer to a domain-shader description (see [**D3DX11\_PASS\_SHADER\_DESC**](d3dx11-pass-shader-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df09d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="df09d-113">Return value</span></span>

<span data-ttu-id="df09d-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="df09d-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="df09d-115">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="df09d-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="df09d-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="df09d-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="df09d-117">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="df09d-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="df09d-118">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="df09d-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="df09d-119">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="df09d-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="df09d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df09d-120">Requirements</span></span>



| <span data-ttu-id="df09d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="df09d-121">Requirement</span></span> | <span data-ttu-id="df09d-122">Value</span><span class="sxs-lookup"><span data-stu-id="df09d-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df09d-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="df09d-123">Header</span></span><br/>  | <dl> <span data-ttu-id="df09d-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="df09d-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="df09d-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="df09d-125">Library</span></span><br/> | <dl> <span data-ttu-id="df09d-126"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="df09d-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df09d-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="df09d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df09d-128">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="df09d-128">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

 





