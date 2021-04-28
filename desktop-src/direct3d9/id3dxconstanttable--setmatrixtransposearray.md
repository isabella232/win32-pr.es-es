---
description: 'Método ID3DXConstantTable::SetMatrixTransposeArray: establece una matriz de matrices transpuestas.'
ms.assetid: a67afc21-f43d-4dc5-b145-f3d66dd86dbb
title: Método ID3DXConstantTable::SetMatrixTransposeArray (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrixTransposeArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0118c888adc52671a943b7b159bae80deca26a1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115053"
---
# <a name="id3dxconstanttablesetmatrixtransposearray-method"></a><span data-ttu-id="d6858-103">Método ID3DXConstantTable::SetMatrixTransposeArray</span><span class="sxs-lookup"><span data-stu-id="d6858-103">ID3DXConstantTable::SetMatrixTransposeArray method</span></span>

<span data-ttu-id="d6858-104">Establece una matriz de matrices transpuestas.</span><span class="sxs-lookup"><span data-stu-id="d6858-104">Sets an array of transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6858-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d6858-105">Syntax</span></span>


```C++
HRESULT SetMatrixTransposeArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        *pMatrix,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="d6858-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d6858-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6858-107">*pDevice* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d6858-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6858-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="d6858-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="d6858-109">Puntero a una [**interfaz IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo asociado a la tabla constante.</span><span class="sxs-lookup"><span data-stu-id="d6858-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="d6858-110">*hConstant* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d6858-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6858-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="d6858-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="d6858-112">Identificador único de la matriz de constantes de matriz.</span><span class="sxs-lookup"><span data-stu-id="d6858-112">Unique identifier to the array of matrix constants.</span></span> <span data-ttu-id="d6858-113">Vea [D3DXHANDLE.](dx9-graphics-reference-effects-constants.md)</span><span class="sxs-lookup"><span data-stu-id="d6858-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="d6858-114">*pMatrix* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d6858-114">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6858-115">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="d6858-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d6858-116">Matriz de matrices transpuestas.</span><span class="sxs-lookup"><span data-stu-id="d6858-116">Array of transposed matrices.</span></span> <span data-ttu-id="d6858-117">Vea [**D3DXMATRIX.**](d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="d6858-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="d6858-118">*Recuento* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d6858-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6858-119">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d6858-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d6858-120">Número de matrices de la matriz.</span><span class="sxs-lookup"><span data-stu-id="d6858-120">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6858-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d6858-121">Return value</span></span>

<span data-ttu-id="d6858-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d6858-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d6858-123">Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d6858-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d6858-124">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d6858-124">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6858-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6858-125">Requirements</span></span>



| <span data-ttu-id="d6858-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6858-126">Requirement</span></span> | <span data-ttu-id="d6858-127">Value</span><span class="sxs-lookup"><span data-stu-id="d6858-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6858-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d6858-128">Header</span></span><br/>  | <dl> <span data-ttu-id="d6858-129"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="d6858-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="d6858-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d6858-130">Library</span></span><br/> | <dl> <span data-ttu-id="d6858-131"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="d6858-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d6858-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d6858-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6858-133">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="d6858-133">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
