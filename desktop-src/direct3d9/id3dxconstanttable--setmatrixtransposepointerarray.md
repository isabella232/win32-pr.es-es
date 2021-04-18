---
description: Establece una matriz de punteros a matrices transpuestas.
ms.assetid: f2db10cb-a146-412d-8de8-f093253470fd
title: 'ID3DXConstantTable:: SetMatrixTransposePointerArray (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrixTransposePointerArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6c78c051ff2d2ab52c9a741fa117a89f66ff450d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718247"
---
# <a name="id3dxconstanttablesetmatrixtransposepointerarray-method"></a><span data-ttu-id="d2c5b-103">ID3DXConstantTable:: SetMatrixTransposePointerArray (método)</span><span class="sxs-lookup"><span data-stu-id="d2c5b-103">ID3DXConstantTable::SetMatrixTransposePointerArray method</span></span>

<span data-ttu-id="d2c5b-104">Establece una matriz de punteros a matrices transpuestas.</span><span class="sxs-lookup"><span data-stu-id="d2c5b-104">Sets an array of pointers to transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2c5b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d2c5b-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposePointerArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        **ppMatrix,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="d2c5b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d2c5b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2c5b-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d2c5b-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2c5b-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="d2c5b-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="d2c5b-109">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo asociado a la tabla de constantes.</span><span class="sxs-lookup"><span data-stu-id="d2c5b-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="d2c5b-110">*hConstant* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d2c5b-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2c5b-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="d2c5b-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="d2c5b-112">Identificador único de la matriz de constantes de matriz.</span><span class="sxs-lookup"><span data-stu-id="d2c5b-112">Unique identifier to the array of matrix constants.</span></span> <span data-ttu-id="d2c5b-113">Vea [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="d2c5b-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="d2c5b-114">*ppMatrix* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d2c5b-114">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2c5b-115">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="d2c5b-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="d2c5b-116">Matriz de punteros a matrices transpuestas.</span><span class="sxs-lookup"><span data-stu-id="d2c5b-116">Array of pointers to transposed matrices.</span></span> <span data-ttu-id="d2c5b-117">Vea [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="d2c5b-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="d2c5b-118">*Recuento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d2c5b-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2c5b-119">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d2c5b-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d2c5b-120">Número de matrices de la matriz.</span><span class="sxs-lookup"><span data-stu-id="d2c5b-120">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2c5b-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d2c5b-121">Return value</span></span>

<span data-ttu-id="d2c5b-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d2c5b-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d2c5b-123">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d2c5b-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d2c5b-124">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d2c5b-124">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2c5b-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d2c5b-125">Remarks</span></span>

<span data-ttu-id="d2c5b-126">Una matriz transpuesta contiene datos principales de columna; es decir, cada vector está contenido en una columna.</span><span class="sxs-lookup"><span data-stu-id="d2c5b-126">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2c5b-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2c5b-127">Requirements</span></span>



| <span data-ttu-id="d2c5b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2c5b-128">Requirement</span></span> | <span data-ttu-id="d2c5b-129">Value</span><span class="sxs-lookup"><span data-stu-id="d2c5b-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2c5b-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d2c5b-130">Header</span></span><br/>  | <dl> <span data-ttu-id="d2c5b-131"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2c5b-131"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="d2c5b-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d2c5b-132">Library</span></span><br/> | <dl> <span data-ttu-id="d2c5b-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2c5b-133"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d2c5b-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="d2c5b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2c5b-135">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="d2c5b-135">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
