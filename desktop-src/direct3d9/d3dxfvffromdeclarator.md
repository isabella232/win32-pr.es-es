---
description: Devuelve un código de formato de vértice flexible (FVF) de un declarador.
ms.assetid: 4f30087e-0042-44bc-a7a5-5386b18fcad7
title: Función D3DXFVFFromDeclarator (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFVFFromDeclarator
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fdaf6f80340a08562ed644ee44ac92c42874d149
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362567"
---
# <a name="d3dxfvffromdeclarator-function"></a><span data-ttu-id="8bb61-103">D3DXFVFFromDeclarator función)</span><span class="sxs-lookup"><span data-stu-id="8bb61-103">D3DXFVFFromDeclarator function</span></span>

<span data-ttu-id="8bb61-104">Devuelve un código de formato de vértice flexible (FVF) de un declarador.</span><span class="sxs-lookup"><span data-stu-id="8bb61-104">Returns a flexible vertex format (FVF) code from a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bb61-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8bb61-105">Syntax</span></span>


```C++
HRESULT D3DXFVFFromDeclarator(
  _In_  const LPD3DVERTEXELEMENT9 *pDeclaration,
  _Out_       DWORD               *pFVF
);
```



## <a name="parameters"></a><span data-ttu-id="8bb61-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8bb61-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bb61-107">*pDeclaration* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8bb61-107">*pDeclaration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bb61-108">Tipo: **const [**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="8bb61-108">Type: **const [**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="8bb61-109">Matriz de elementos [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , que describe el código FVF.</span><span class="sxs-lookup"><span data-stu-id="8bb61-109">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements, describing the FVF code.</span></span>

</dd> <dt>

<span data-ttu-id="8bb61-110">*pFVF* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8bb61-110">*pFVF* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8bb61-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8bb61-111">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8bb61-112">Puntero a un valor DWORD que representa la combinación devuelta de [D3DFVF](d3dfvf.md) que describe el formato de vértice devuelto por el declarador.</span><span class="sxs-lookup"><span data-stu-id="8bb61-112">Pointer to a DWORD value, representing the returned combination of [D3DFVF](d3dfvf.md) that describes the vertex format returned from the declarator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bb61-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8bb61-113">Return value</span></span>

<span data-ttu-id="8bb61-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8bb61-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8bb61-115">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8bb61-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8bb61-116">Si se produce un error en la función, el valor devuelto puede ser: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="8bb61-116">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="8bb61-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8bb61-117">Remarks</span></span>

<span data-ttu-id="8bb61-118">Se producirá un error en esta función para cualquier declarador que no se asigne directamente a un FVF.</span><span class="sxs-lookup"><span data-stu-id="8bb61-118">This function will fail for any declarator that does not map directly to an FVF.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bb61-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8bb61-119">Requirements</span></span>



| <span data-ttu-id="8bb61-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bb61-120">Requirement</span></span> | <span data-ttu-id="8bb61-121">Value</span><span class="sxs-lookup"><span data-stu-id="8bb61-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8bb61-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8bb61-122">Header</span></span><br/>  | <dl> <span data-ttu-id="8bb61-123"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="8bb61-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="8bb61-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8bb61-124">Library</span></span><br/> | <dl> <span data-ttu-id="8bb61-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8bb61-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8bb61-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="8bb61-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bb61-127">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="8bb61-127">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="8bb61-128">**D3DXDeclaratorFromFVF**</span><span class="sxs-lookup"><span data-stu-id="8bb61-128">**D3DXDeclaratorFromFVF**</span></span>](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
