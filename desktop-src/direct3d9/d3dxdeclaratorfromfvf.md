---
description: Devuelve un declarador de un código de formato de vértice flexible (FVF).
ms.assetid: 0272239c-0873-4a5c-b046-541f4ba603f4
title: Función D3DXDeclaratorFromFVF (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDeclaratorFromFVF
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: de5360c7f9bd28d4c97184f985f06e48ca0002d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707888"
---
# <a name="d3dxdeclaratorfromfvf-function"></a><span data-ttu-id="e5073-103">D3DXDeclaratorFromFVF función)</span><span class="sxs-lookup"><span data-stu-id="e5073-103">D3DXDeclaratorFromFVF function</span></span>

<span data-ttu-id="e5073-104">Devuelve un declarador de un código de formato de vértice flexible (FVF).</span><span class="sxs-lookup"><span data-stu-id="e5073-104">Returns a declarator from a flexible vertex format (FVF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5073-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e5073-105">Syntax</span></span>


```C++
HRESULT D3DXDeclaratorFromFVF(
  _In_    DWORD             FVF,
  _Inout_ D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a><span data-ttu-id="e5073-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e5073-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5073-107">*FVF* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e5073-107">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5073-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e5073-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e5073-109">Combinación de [D3DFVF](d3dfvf.md) que describe el FVF desde el que se va a generar la matriz declaradora devuelta.</span><span class="sxs-lookup"><span data-stu-id="e5073-109">Combination of [D3DFVF](d3dfvf.md) that describes the FVF from which to generate the returned declarator array.</span></span>

</dd> <dt>

<span data-ttu-id="e5073-110">*Declaración* \[ de in, out\]</span><span class="sxs-lookup"><span data-stu-id="e5073-110">*Declaration* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5073-111">Tipo: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span><span class="sxs-lookup"><span data-stu-id="e5073-111">Type: **[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span></span>

<span data-ttu-id="e5073-112">Matriz de elementos [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) que describe el formato de vértice de los vértices de malla.</span><span class="sxs-lookup"><span data-stu-id="e5073-112">An array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements describing the vertex format of the mesh vertices.</span></span> <span data-ttu-id="e5073-113">El límite superior de esta matriz de declarador es el [**tamaño máximo de \_ FVF \_ decl \_**](./max-fvf-decl-size.md).</span><span class="sxs-lookup"><span data-stu-id="e5073-113">The upper limit of this declarator array is [**MAX\_FVF\_DECL\_SIZE**](./max-fvf-decl-size.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5073-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e5073-114">Return value</span></span>

<span data-ttu-id="e5073-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e5073-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e5073-116">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e5073-116">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e5073-117">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DXERR \_ INVALIDMESH.</span><span class="sxs-lookup"><span data-stu-id="e5073-117">If the function fails, the return value can be one of the following: D3DXERR\_INVALIDMESH.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5073-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5073-118">Requirements</span></span>



| <span data-ttu-id="e5073-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5073-119">Requirement</span></span> | <span data-ttu-id="e5073-120">Value</span><span class="sxs-lookup"><span data-stu-id="e5073-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5073-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e5073-121">Header</span></span><br/>  | <dl> <span data-ttu-id="e5073-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5073-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e5073-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e5073-123">Library</span></span><br/> | <dl> <span data-ttu-id="e5073-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5073-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e5073-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="e5073-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5073-126">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="e5073-126">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="e5073-127">**D3DXFVFFromDeclarator**</span><span class="sxs-lookup"><span data-stu-id="e5073-127">**D3DXFVFFromDeclarator**</span></span>](d3dxfvffromdeclarator.md)
</dt> </dl>

 

 
