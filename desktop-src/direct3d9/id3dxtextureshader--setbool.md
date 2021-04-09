---
description: Establece un valor BOOLEANO.
ms.assetid: 0d3c1f3a-f497-4e92-81e9-8647006910e1
title: 'ID3DXTextureShader:: SetBool (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetBool
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 49fbc2d2841957e75a8bc3adaf40ce0fdf5e2a1f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821359"
---
# <a name="id3dxtextureshadersetbool-method"></a><span data-ttu-id="a235f-103">ID3DXTextureShader:: SetBool (método)</span><span class="sxs-lookup"><span data-stu-id="a235f-103">ID3DXTextureShader::SetBool method</span></span>

<span data-ttu-id="a235f-104">Establece un valor BOOLEANO.</span><span class="sxs-lookup"><span data-stu-id="a235f-104">Sets a BOOL value.</span></span>

## <a name="syntax"></a><span data-ttu-id="a235f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a235f-105">Syntax</span></span>


```C++
HRESULT SetBool(
  [in] D3DXHANDLE hConstant,
  [in] BOOL       b
);
```



## <a name="parameters"></a><span data-ttu-id="a235f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a235f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a235f-107">*hConstant* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a235f-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a235f-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="a235f-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="a235f-109">Identificador único de la constante.</span><span class="sxs-lookup"><span data-stu-id="a235f-109">Unique identifier to the constant.</span></span> <span data-ttu-id="a235f-110">Vea [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="a235f-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="a235f-111">*b* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="a235f-111">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a235f-112">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a235f-112">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a235f-113">Valor BOOLEANO.</span><span class="sxs-lookup"><span data-stu-id="a235f-113">BOOL value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a235f-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a235f-114">Return value</span></span>

<span data-ttu-id="a235f-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a235f-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a235f-116">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a235f-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a235f-117">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="a235f-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="a235f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a235f-118">Requirements</span></span>



| <span data-ttu-id="a235f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a235f-119">Requirement</span></span> | <span data-ttu-id="a235f-120">Value</span><span class="sxs-lookup"><span data-stu-id="a235f-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a235f-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a235f-121">Header</span></span><br/>  | <dl> <span data-ttu-id="a235f-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="a235f-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="a235f-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a235f-123">Library</span></span><br/> | <dl> <span data-ttu-id="a235f-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a235f-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a235f-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="a235f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a235f-126">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="a235f-126">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
