---
title: Método ID3DX11EffectShaderVariable GetGeometryShader (D3dx11effect. h)
description: Obtiene un sombreador de geometría.
ms.assetid: 395d5c92-a941-4fbf-9bb9-b43634c1810b
keywords:
- Método GetGeometryShader Direct3D 11
- Método GetGeometryShader Direct3D 11, interfaz ID3DX11EffectShaderVariable
- Interfaz ID3DX11EffectShaderVariable Direct3D 11, método GetGeometryShader
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetGeometryShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe30478d84e0048ff7a56e5bd8faee8d50548417
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362746"
---
# <a name="id3dx11effectshadervariablegetgeometryshader-method"></a><span data-ttu-id="43e88-106">ID3DX11EffectShaderVariable:: GetGeometryShader (método)</span><span class="sxs-lookup"><span data-stu-id="43e88-106">ID3DX11EffectShaderVariable::GetGeometryShader method</span></span>

<span data-ttu-id="43e88-107">Obtiene un sombreador de geometría.</span><span class="sxs-lookup"><span data-stu-id="43e88-107">Get a geometry shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="43e88-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="43e88-108">Syntax</span></span>


```C++
HRESULT GetGeometryShader(
   UINT                 ShaderIndex,
   ID3D11GeometryShader **ppGS
);
```



## <a name="parameters"></a><span data-ttu-id="43e88-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="43e88-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43e88-110">*ShaderIndex*</span><span class="sxs-lookup"><span data-stu-id="43e88-110">*ShaderIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="43e88-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="43e88-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="43e88-112">Un índice basado en cero.</span><span class="sxs-lookup"><span data-stu-id="43e88-112">A zero-based index.</span></span>

</dd> <dt>

<span data-ttu-id="43e88-113">*ppGS*</span><span class="sxs-lookup"><span data-stu-id="43e88-113">*ppGS*</span></span> 
</dt> <dd>

<span data-ttu-id="43e88-114">Tipo: **[ **ID3D11GeometryShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader)\*\***</span><span class="sxs-lookup"><span data-stu-id="43e88-114">Type: **[**ID3D11GeometryShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader)\*\***</span></span>

<span data-ttu-id="43e88-115">Un puntero a un puntero [**ID3D11GeometryShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader) que se establecerá en el sombreador de geometría en la devolución.</span><span class="sxs-lookup"><span data-stu-id="43e88-115">A pointer to an [**ID3D11GeometryShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader) pointer that will be set to the geometry shader on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43e88-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="43e88-116">Return value</span></span>

<span data-ttu-id="43e88-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="43e88-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="43e88-118">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="43e88-118">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="43e88-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="43e88-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="43e88-120">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="43e88-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="43e88-121">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="43e88-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="43e88-122">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="43e88-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="43e88-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43e88-123">Requirements</span></span>



| <span data-ttu-id="43e88-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="43e88-124">Requirement</span></span> | <span data-ttu-id="43e88-125">Value</span><span class="sxs-lookup"><span data-stu-id="43e88-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43e88-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="43e88-126">Header</span></span><br/>  | <dl> <span data-ttu-id="43e88-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="43e88-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="43e88-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="43e88-128">Library</span></span><br/> | <dl> <span data-ttu-id="43e88-129"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="43e88-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43e88-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="43e88-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43e88-131">ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="43e88-131">ID3DX11EffectShaderVariable</span></span>](id3dx11effectshadervariable.md)
</dt> </dl>

 

