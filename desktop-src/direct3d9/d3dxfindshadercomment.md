---
description: Busca un comentario determinado en un sombreador. El comentario se identifica mediante un código de cuatro caracteres (FOURCC) en el primer valor DWORD del comentario.
ms.assetid: 86ab8330-fd48-4d14-835c-92399c6c8a38
title: Función D3DXFindShaderComment (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFindShaderComment
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 394c72bcf7076075318cd664cf56bbb464d7e3cf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707885"
---
# <a name="d3dxfindshadercomment-function"></a><span data-ttu-id="39e06-104">D3DXFindShaderComment función)</span><span class="sxs-lookup"><span data-stu-id="39e06-104">D3DXFindShaderComment function</span></span>

<span data-ttu-id="39e06-105">Busca un comentario determinado en un sombreador.</span><span class="sxs-lookup"><span data-stu-id="39e06-105">Searches through a shader for a particular comment.</span></span> <span data-ttu-id="39e06-106">El comentario se identifica mediante un código de cuatro caracteres (FOURCC) en el primer valor DWORD del comentario.</span><span class="sxs-lookup"><span data-stu-id="39e06-106">The comment is identified by a four-character code (FOURCC) in the first DWORD of the comment.</span></span>

## <a name="syntax"></a><span data-ttu-id="39e06-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="39e06-107">Syntax</span></span>


```C++
HRESULT D3DXFindShaderComment(
  _In_  const DWORD   *pFunction,
  _In_        DWORD   FourCC,
  _In_        LPCVOID *ppData,
  _Out_       UINT    *pSizeInBytes
);
```



## <a name="parameters"></a><span data-ttu-id="39e06-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="39e06-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39e06-109">*pFunction* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="39e06-109">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39e06-110">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="39e06-110">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="39e06-111">Puntero a la secuencia DWORD de la función de sombreador.</span><span class="sxs-lookup"><span data-stu-id="39e06-111">Pointer to the shader function DWORD stream.</span></span>

</dd> <dt>

<span data-ttu-id="39e06-112">*FourCC* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="39e06-112">*FourCC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39e06-113">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="39e06-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="39e06-114">Código FOURCC que identifica el bloque de comentario.</span><span class="sxs-lookup"><span data-stu-id="39e06-114">FOURCC code that identifies the comment block.</span></span> <span data-ttu-id="39e06-115">Vea [formatos FourCC](d3dformat.md).</span><span class="sxs-lookup"><span data-stu-id="39e06-115">See [FourCC Formats](d3dformat.md).</span></span>

</dd> <dt>

<span data-ttu-id="39e06-116">*ppData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="39e06-116">*ppData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39e06-117">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="39e06-117">Type: **[**LPCVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="39e06-118">Devuelve un puntero a los datos de comentario (sin incluir el token de comentario y el código FOURCC).</span><span class="sxs-lookup"><span data-stu-id="39e06-118">Returns a pointer to the comment data (not including the comment token and FOURCC code).</span></span> <span data-ttu-id="39e06-119">Este valor puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="39e06-119">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="39e06-120">*pSizeInBytes* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="39e06-120">*pSizeInBytes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39e06-121">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="39e06-121">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="39e06-122">Devuelve el tamaño de los datos de comentario en bytes.</span><span class="sxs-lookup"><span data-stu-id="39e06-122">Returns the size of the comment data in bytes.</span></span> <span data-ttu-id="39e06-123">Este valor puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="39e06-123">This value can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39e06-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="39e06-124">Return value</span></span>

<span data-ttu-id="39e06-125">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="39e06-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="39e06-126">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="39e06-126">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="39e06-127">Si no se encuentra el comentario y no se ha producido ningún otro error, \_ se devuelve S false.</span><span class="sxs-lookup"><span data-stu-id="39e06-127">If the comment is not found, and no other error has occurred, S\_FALSE is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="39e06-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39e06-128">Requirements</span></span>



| <span data-ttu-id="39e06-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="39e06-129">Requirement</span></span> | <span data-ttu-id="39e06-130">Value</span><span class="sxs-lookup"><span data-stu-id="39e06-130">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="39e06-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="39e06-131">Header</span></span><br/>  | <dl> <span data-ttu-id="39e06-132"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="39e06-132"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="39e06-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="39e06-133">Library</span></span><br/> | <dl> <span data-ttu-id="39e06-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="39e06-134"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="39e06-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="39e06-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39e06-136">Funciones del sombreador</span><span class="sxs-lookup"><span data-stu-id="39e06-136">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
