---
description: Crea un objeto de sombreador de textura a partir del sombreador compilado.
ms.assetid: 3e8017f7-fe6b-4f4e-a80e-b16b16c0b348
title: Función D3DXCreateTextureShader (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c32715f1b939d30acb53b1cbe07e081d43d21823
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362580"
---
# <a name="d3dxcreatetextureshader-function"></a><span data-ttu-id="397ce-103">D3DXCreateTextureShader función)</span><span class="sxs-lookup"><span data-stu-id="397ce-103">D3DXCreateTextureShader function</span></span>

<span data-ttu-id="397ce-104">Crea un objeto de sombreador de textura a partir del sombreador compilado.</span><span class="sxs-lookup"><span data-stu-id="397ce-104">Creates a texture shader object from the compiled shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="397ce-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="397ce-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureShader(
  _In_  const DWORD               *pFunction,
  _Out_       LPD3DXTEXTURESHADER *ppTextureShader
);
```



## <a name="parameters"></a><span data-ttu-id="397ce-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="397ce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="397ce-107">*pFunction* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="397ce-107">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="397ce-108">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="397ce-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="397ce-109">Puntero a la secuencia DWORD de la función.</span><span class="sxs-lookup"><span data-stu-id="397ce-109">Pointer to the function DWORD stream.</span></span>

</dd> <dt>

<span data-ttu-id="397ce-110">*ppTextureShader* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="397ce-110">*ppTextureShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="397ce-111">Tipo: **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)\***</span><span class="sxs-lookup"><span data-stu-id="397ce-111">Type: **[**LPD3DXTEXTURESHADER**](id3dxtextureshader.md)\***</span></span>

<span data-ttu-id="397ce-112">Devuelve un objeto [**ID3DXTextureShader**](id3dxtextureshader.md) que se puede usar para rellenar de un procedimiento el contenido de una textura mediante las funciones [**D3DXFillTextureTX**](d3dxfilltexturetx.md) .</span><span class="sxs-lookup"><span data-stu-id="397ce-112">Returns an [**ID3DXTextureShader**](id3dxtextureshader.md) object which can be used to procedurally fill the contents of a texture using the [**D3DXFillTextureTX**](d3dxfilltexturetx.md) functions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="397ce-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="397ce-113">Return value</span></span>

<span data-ttu-id="397ce-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="397ce-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="397ce-115">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="397ce-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="397ce-116">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="397ce-116">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="397ce-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="397ce-117">Requirements</span></span>



| <span data-ttu-id="397ce-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="397ce-118">Requirement</span></span> | <span data-ttu-id="397ce-119">Value</span><span class="sxs-lookup"><span data-stu-id="397ce-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="397ce-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="397ce-120">Header</span></span><br/>  | <dl> <span data-ttu-id="397ce-121"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="397ce-121"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="397ce-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="397ce-122">Library</span></span><br/> | <dl> <span data-ttu-id="397ce-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="397ce-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="397ce-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="397ce-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="397ce-125">Funciones del sombreador</span><span class="sxs-lookup"><span data-stu-id="397ce-125">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
