---
description: Establece una matriz de punteros a matrices de nontransposed.
ms.assetid: 1b985e03-b5cb-48e5-969f-115ca165acdc
title: 'ID3DXConstantTable:: SetMatrixPointerArray (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrixPointerArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4b29d4298d8ca52d2826cc780fb90d769c3337f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707906"
---
# <a name="id3dxconstanttablesetmatrixpointerarray-method"></a><span data-ttu-id="cf5f8-103">ID3DXConstantTable:: SetMatrixPointerArray (método)</span><span class="sxs-lookup"><span data-stu-id="cf5f8-103">ID3DXConstantTable::SetMatrixPointerArray method</span></span>

<span data-ttu-id="cf5f8-104">Establece una matriz de punteros a matrices de nontransposed.</span><span class="sxs-lookup"><span data-stu-id="cf5f8-104">Sets an array of pointers to nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf5f8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cf5f8-105">Syntax</span></span>


```C++
HRESULT SetMatrixPointerArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        **ppMatrix,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="cf5f8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cf5f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf5f8-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cf5f8-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf5f8-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="cf5f8-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="cf5f8-109">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo asociado a la tabla de constantes.</span><span class="sxs-lookup"><span data-stu-id="cf5f8-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="cf5f8-110">*hConstant* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cf5f8-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf5f8-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="cf5f8-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="cf5f8-112">Identificador único de una matriz de matrices de constantes.</span><span class="sxs-lookup"><span data-stu-id="cf5f8-112">Unique identifier to an array of constant matrices.</span></span> <span data-ttu-id="cf5f8-113">Vea [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="cf5f8-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf5f8-114">*ppMatrix* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cf5f8-114">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf5f8-115">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="cf5f8-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="cf5f8-116">Matriz de punteros a matrices de nontransposed.</span><span class="sxs-lookup"><span data-stu-id="cf5f8-116">Array of pointers to nontransposed matrices.</span></span> <span data-ttu-id="cf5f8-117">Vea [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="cf5f8-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf5f8-118">*Recuento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cf5f8-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf5f8-119">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cf5f8-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cf5f8-120">Número de matrices de la matriz.</span><span class="sxs-lookup"><span data-stu-id="cf5f8-120">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf5f8-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cf5f8-121">Return value</span></span>

<span data-ttu-id="cf5f8-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cf5f8-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cf5f8-123">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cf5f8-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="cf5f8-124">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="cf5f8-124">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf5f8-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cf5f8-125">Remarks</span></span>

<span data-ttu-id="cf5f8-126">Una matriz nontransposed contiene datos principales de fila; es decir, cada vector está incluido en una fila.</span><span class="sxs-lookup"><span data-stu-id="cf5f8-126">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf5f8-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf5f8-127">Requirements</span></span>



| <span data-ttu-id="cf5f8-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf5f8-128">Requirement</span></span> | <span data-ttu-id="cf5f8-129">Value</span><span class="sxs-lookup"><span data-stu-id="cf5f8-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf5f8-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cf5f8-130">Header</span></span><br/>  | <dl> <span data-ttu-id="cf5f8-131"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf5f8-131"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="cf5f8-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cf5f8-132">Library</span></span><br/> | <dl> <span data-ttu-id="cf5f8-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cf5f8-133"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="cf5f8-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="cf5f8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf5f8-135">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="cf5f8-135">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
