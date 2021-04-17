---
description: Desensamblar un sombreador.
ms.assetid: 30159223-8f88-4929-8ef1-7a6acc13f485
title: Función D3DXDisassembleShader (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDisassembleShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6192b77c190ed73dc6e5038c9119152836eca375
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698256"
---
# <a name="d3dxdisassembleshader-function"></a><span data-ttu-id="ac099-103">D3DXDisassembleShader función)</span><span class="sxs-lookup"><span data-stu-id="ac099-103">D3DXDisassembleShader function</span></span>

<span data-ttu-id="ac099-104">Desensamblar un sombreador.</span><span class="sxs-lookup"><span data-stu-id="ac099-104">Disassemble a shader.</span></span>

> [!Note]  
> <span data-ttu-id="ac099-105">En lugar de usar esta función heredada, se recomienda usar la API de [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) .</span><span class="sxs-lookup"><span data-stu-id="ac099-105">Instead of using this legacy function, we recommend that you use the [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="ac099-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ac099-106">Syntax</span></span>


```C++
HRESULT D3DXDisassembleShader(
  _In_  const DWORD        *pShader,
  _In_        BOOL         EnableColorCode,
  _In_        LPCSTR       pComments,
  _Out_       LPD3DXBUFFER *ppDisassembly
);
```



## <a name="parameters"></a><span data-ttu-id="ac099-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ac099-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac099-108">*pShader* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ac099-108">*pShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac099-109">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="ac099-109">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ac099-110">Puntero a un búfer de memoria que contiene los datos del sombreador.</span><span class="sxs-lookup"><span data-stu-id="ac099-110">Pointer to a memory buffer that contains the shader data.</span></span>

</dd> <dt>

<span data-ttu-id="ac099-111">*EnableColorCode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ac099-111">*EnableColorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac099-112">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ac099-112">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ac099-113">Habilite el código de color para facilitar la lectura del desensamblado.</span><span class="sxs-lookup"><span data-stu-id="ac099-113">Enable color code to make it easier to read the disassembly.</span></span>

</dd> <dt>

<span data-ttu-id="ac099-114">*pComments* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ac099-114">*pComments* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac099-115">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ac099-115">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ac099-116">Cadena de comentario opcional terminada en NULL.</span><span class="sxs-lookup"><span data-stu-id="ac099-116">An optional NULL-terminated comment string.</span></span> <span data-ttu-id="ac099-117">Este valor puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="ac099-117">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ac099-118">*ppDisassembly* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ac099-118">*ppDisassembly* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac099-119">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="ac099-119">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="ac099-120">Devuelve un búfer que contiene el sombreador desensamblado.</span><span class="sxs-lookup"><span data-stu-id="ac099-120">Returns a buffer containing the disassembled shader.</span></span> <span data-ttu-id="ac099-121">Vea [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="ac099-121">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac099-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ac099-122">Return value</span></span>

<span data-ttu-id="ac099-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ac099-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ac099-124">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ac099-124">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ac099-125">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="ac099-125">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac099-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac099-126">Requirements</span></span>



| <span data-ttu-id="ac099-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac099-127">Requirement</span></span> | <span data-ttu-id="ac099-128">Value</span><span class="sxs-lookup"><span data-stu-id="ac099-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac099-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ac099-129">Header</span></span><br/>  | <dl> <span data-ttu-id="ac099-130"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac099-130"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="ac099-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ac099-131">Library</span></span><br/> | <dl> <span data-ttu-id="ac099-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac099-132"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ac099-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="ac099-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac099-134">Funciones del sombreador</span><span class="sxs-lookup"><span data-stu-id="ac099-134">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
