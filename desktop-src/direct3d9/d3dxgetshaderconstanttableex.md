---
description: 'Función D3DXGetShaderConstantTableEx: obtiene la tabla shader-constant incrustada dentro de un sombreador.'
ms.assetid: f7e846e4-9cb4-4634-95e3-4b2a752978a8
title: Función D3DXGetShaderConstantTableEx (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderConstantTableEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2cac525f6f6fc4f4e3b6e5900aa9b655e7c7f60d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114442"
---
# <a name="d3dxgetshaderconstanttableex-function"></a><span data-ttu-id="78926-103">Función D3DXGetShaderConstantTableEx</span><span class="sxs-lookup"><span data-stu-id="78926-103">D3DXGetShaderConstantTableEx function</span></span>

<span data-ttu-id="78926-104">Obtiene la tabla shader-constant incrustada dentro de un sombreador.</span><span class="sxs-lookup"><span data-stu-id="78926-104">Gets the shader-constant table embedded inside a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="78926-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="78926-105">Syntax</span></span>


```C++
HRESULT D3DXGetShaderConstantTableEx(
  _In_  const DWORD               *pFunction,
  _In_        DWORD               Flags,
  _Out_       LPD3DXCONSTANTTABLE * ppConstantTable
);
```



## <a name="parameters"></a><span data-ttu-id="78926-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="78926-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78926-107">*pFunction* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="78926-107">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78926-108">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="78926-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="78926-109">Puntero a la secuencia DWORD de la función.</span><span class="sxs-lookup"><span data-stu-id="78926-109">Pointer to the function DWORD stream.</span></span>

</dd> <dt>

<span data-ttu-id="78926-110">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="78926-110">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78926-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="78926-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="78926-112">Use la marca LARGEADDRESSAWARE de D3DXCONSTTABLE para acceder a hasta 4 GB de espacio de direcciones virtuales (en lugar del valor predeterminado \_ de 2 GB).</span><span class="sxs-lookup"><span data-stu-id="78926-112">Use the D3DXCONSTTABLE\_LARGEADDRESSAWARE flag to access up to 4 GB of virtual address space (instead of the default of 2 GB).</span></span> <span data-ttu-id="78926-113">Si no necesita el espacio de direcciones virtuales adicional, use [**D3DXGetShaderConstantTable**](d3dxgetshaderconstanttable.md).</span><span class="sxs-lookup"><span data-stu-id="78926-113">If you do not need the additional virtual address space, use [**D3DXGetShaderConstantTable**](d3dxgetshaderconstanttable.md).</span></span>

</dd> <dt>

 <span data-ttu-id="78926-114">*ppConstantTable* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="78926-114">*ppConstantTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="78926-115">Tipo: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span><span class="sxs-lookup"><span data-stu-id="78926-115">Type: **[**LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span></span>

<span data-ttu-id="78926-116">Devuelve la interfaz de tabla constante [**(vea ID3DXConstantTable)**](id3dxconstanttable.md)que administra la tabla constante.</span><span class="sxs-lookup"><span data-stu-id="78926-116">Returns the constant table interface (see [**ID3DXConstantTable**](id3dxconstanttable.md)) that manages the constant table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78926-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="78926-117">Return value</span></span>

<span data-ttu-id="78926-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="78926-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="78926-119">Si la función se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="78926-119">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="78926-120">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="78926-120">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="78926-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="78926-121">Remarks</span></span>

<span data-ttu-id="78926-122">[**D3DXCompileShader**](d3dxcompileshader.md) genera una tabla constante e incrustada en el cuerpo del sombreador.</span><span class="sxs-lookup"><span data-stu-id="78926-122">A constant table is generated by [**D3DXCompileShader**](d3dxcompileshader.md) and embedded in the shader body.</span></span>

## <a name="requirements"></a><span data-ttu-id="78926-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78926-123">Requirements</span></span>



| <span data-ttu-id="78926-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="78926-124">Requirement</span></span> | <span data-ttu-id="78926-125">Value</span><span class="sxs-lookup"><span data-stu-id="78926-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="78926-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="78926-126">Header</span></span><br/>  | <dl> <span data-ttu-id="78926-127"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="78926-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="78926-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="78926-128">Library</span></span><br/> | <dl> <span data-ttu-id="78926-129"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="78926-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="78926-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="78926-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78926-131">Funciones de sombreador</span><span class="sxs-lookup"><span data-stu-id="78926-131">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
