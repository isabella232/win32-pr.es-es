---
title: Método ID3DX11EffectPass GetGeometryShaderDesc (D3dx11effect. h)
description: Obtiene una descripción del sombreador de geometría.
ms.assetid: 03298ec3-6b85-40bf-8920-a82c7606d326
keywords:
- Método GetGeometryShaderDesc Direct3D 11
- Método GetGeometryShaderDesc Direct3D 11, interfaz ID3DX11EffectPass
- Interfaz ID3DX11EffectPass Direct3D 11, método GetGeometryShaderDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetGeometryShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94c3b84ed9e8c245611c1442987b68a94e7b10ad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998467"
---
# <a name="id3dx11effectpassgetgeometryshaderdesc-method"></a><span data-ttu-id="bf2fc-106">ID3DX11EffectPass:: GetGeometryShaderDesc (método)</span><span class="sxs-lookup"><span data-stu-id="bf2fc-106">ID3DX11EffectPass::GetGeometryShaderDesc method</span></span>

<span data-ttu-id="bf2fc-107">Obtiene una descripción del sombreador de geometría.</span><span class="sxs-lookup"><span data-stu-id="bf2fc-107">Get a geometry-shader description.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf2fc-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bf2fc-108">Syntax</span></span>


```C++
HRESULT GetGeometryShaderDesc(
   D3DX11_PASS_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="bf2fc-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bf2fc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf2fc-110">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="bf2fc-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="bf2fc-111">Tipo: **[ **D3DX11 \_ Pass \_ Shader \_ DESC**](d3dx11-pass-shader-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="bf2fc-111">Type: **[**D3DX11\_PASS\_SHADER\_DESC**](d3dx11-pass-shader-desc.md)\***</span></span>

<span data-ttu-id="bf2fc-112">Un puntero a una descripción del sombreador de geometría (vea [**D3DX11 \_ Pass \_ Shader \_ DESC**](d3dx11-pass-shader-desc.md)).</span><span class="sxs-lookup"><span data-stu-id="bf2fc-112">A pointer to a geometry-shader description (see [**D3DX11\_PASS\_SHADER\_DESC**](d3dx11-pass-shader-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf2fc-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bf2fc-113">Return value</span></span>

<span data-ttu-id="bf2fc-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bf2fc-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bf2fc-115">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="bf2fc-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bf2fc-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bf2fc-116">Remarks</span></span>

<span data-ttu-id="bf2fc-117">Un paso de efecto puede contener asignaciones de estado de representación y asignaciones de objetos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="bf2fc-117">An effect pass can contain render state assignments and shader object assignments.</span></span>

> [!Note]  
> <span data-ttu-id="bf2fc-118">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="bf2fc-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="bf2fc-119">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="bf2fc-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="bf2fc-120">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="bf2fc-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bf2fc-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf2fc-121">Requirements</span></span>



| <span data-ttu-id="bf2fc-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf2fc-122">Requirement</span></span> | <span data-ttu-id="bf2fc-123">Value</span><span class="sxs-lookup"><span data-stu-id="bf2fc-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf2fc-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bf2fc-124">Header</span></span><br/>  | <dl> <span data-ttu-id="bf2fc-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf2fc-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="bf2fc-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bf2fc-126">Library</span></span><br/> | <dl> <span data-ttu-id="bf2fc-127"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="bf2fc-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf2fc-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="bf2fc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf2fc-129">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="bf2fc-129">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

 





