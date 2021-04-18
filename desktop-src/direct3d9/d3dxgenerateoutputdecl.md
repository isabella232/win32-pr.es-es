---
description: Genera una declaración de vértices de salida a partir de la declaración de entrada. La declaración de salida está pensada para que la usen las funciones de teselación de malla.
ms.assetid: 528b0da3-fc31-4872-98f2-31e03c1cae5e
title: Función D3DXGenerateOutputDecl (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGenerateOutputDecl
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ce3fed752e74df3afa812c228a174503e20c6adf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718200"
---
# <a name="d3dxgenerateoutputdecl-function"></a><span data-ttu-id="4fc5e-104">D3DXGenerateOutputDecl función)</span><span class="sxs-lookup"><span data-stu-id="4fc5e-104">D3DXGenerateOutputDecl function</span></span>

<span data-ttu-id="4fc5e-105">Genera una declaración de vértices de salida a partir de la declaración de entrada.</span><span class="sxs-lookup"><span data-stu-id="4fc5e-105">Generates an output vertex declaration from the input declaration.</span></span> <span data-ttu-id="4fc5e-106">La declaración de salida está pensada para que la usen las funciones de teselación de malla.</span><span class="sxs-lookup"><span data-stu-id="4fc5e-106">The output declaration is intended for use by the mesh tessellation functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fc5e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4fc5e-107">Syntax</span></span>


```C++
HRESULT D3DXGenerateOutputDecl(
  _Out_       D3DVERTEXELEMENT9 *pOutput,
  _In_  const D3DVERTEXELEMENT9 *pInput
);
```



## <a name="parameters"></a><span data-ttu-id="4fc5e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4fc5e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fc5e-109">*pOutput* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4fc5e-109">*pOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4fc5e-110">Tipo: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span><span class="sxs-lookup"><span data-stu-id="4fc5e-110">Type: **[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="4fc5e-111">Puntero a la declaración de vértices de salida.</span><span class="sxs-lookup"><span data-stu-id="4fc5e-111">Pointer to the output vertex declaration.</span></span> <span data-ttu-id="4fc5e-112">Vea [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="4fc5e-112">See [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

</dd> <dt>

<span data-ttu-id="4fc5e-113">*pInput* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4fc5e-113">*pInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fc5e-114">Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="4fc5e-114">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="4fc5e-115">Puntero a la declaración de vértices de entrada.</span><span class="sxs-lookup"><span data-stu-id="4fc5e-115">Pointer to the input vertex declaration.</span></span> <span data-ttu-id="4fc5e-116">Vea [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="4fc5e-116">See [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fc5e-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4fc5e-117">Return value</span></span>

<span data-ttu-id="4fc5e-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4fc5e-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4fc5e-119">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4fc5e-119">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4fc5e-120">Si se produce un error en la función, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="4fc5e-120">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fc5e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4fc5e-121">Requirements</span></span>



| <span data-ttu-id="4fc5e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="4fc5e-122">Requirement</span></span> | <span data-ttu-id="4fc5e-123">Value</span><span class="sxs-lookup"><span data-stu-id="4fc5e-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4fc5e-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4fc5e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="4fc5e-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fc5e-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="4fc5e-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4fc5e-126">Library</span></span><br/> | <dl> <span data-ttu-id="4fc5e-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4fc5e-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4fc5e-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="4fc5e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fc5e-129">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="4fc5e-129">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 




