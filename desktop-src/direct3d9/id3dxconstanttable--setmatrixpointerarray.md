---
description: 'Método ID3DXConstantTable::SetMatrixPointerArray: establece una matriz de punteros en matrices no transaccionadas.'
ms.assetid: 1b985e03-b5cb-48e5-969f-115ca165acdc
title: Método ID3DXConstantTable::SetMatrixPointerArray (D3DX9Shader.h)
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
ms.openlocfilehash: bd9505f82674efc822d4921d7116c8eab17198c1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115073"
---
# <a name="id3dxconstanttablesetmatrixpointerarray-method"></a><span data-ttu-id="f9588-103">Método ID3DXConstantTable::SetMatrixPointerArray</span><span class="sxs-lookup"><span data-stu-id="f9588-103">ID3DXConstantTable::SetMatrixPointerArray method</span></span>

<span data-ttu-id="f9588-104">Establece una matriz de punteros a matrices no transaccionadas.</span><span class="sxs-lookup"><span data-stu-id="f9588-104">Sets an array of pointers to nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9588-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f9588-105">Syntax</span></span>


```C++
HRESULT SetMatrixPointerArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        **ppMatrix,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="f9588-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f9588-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9588-107">*pDevice* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="f9588-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9588-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="f9588-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="f9588-109">Puntero a una [**interfaz IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo asociado a la tabla constante.</span><span class="sxs-lookup"><span data-stu-id="f9588-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="f9588-110">*hConstant* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="f9588-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9588-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="f9588-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="f9588-112">Identificador único de una matriz de matrices constantes.</span><span class="sxs-lookup"><span data-stu-id="f9588-112">Unique identifier to an array of constant matrices.</span></span> <span data-ttu-id="f9588-113">Vea [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="f9588-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9588-114">*ppMatrix* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="f9588-114">*ppMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9588-115">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="f9588-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="f9588-116">Matriz de punteros a matrices no transpuestas.</span><span class="sxs-lookup"><span data-stu-id="f9588-116">Array of pointers to nontransposed matrices.</span></span> <span data-ttu-id="f9588-117">Vea [**D3DXMATRIX.**](d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="f9588-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9588-118">*Recuento* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="f9588-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9588-119">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f9588-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f9588-120">Número de matrices de la matriz.</span><span class="sxs-lookup"><span data-stu-id="f9588-120">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9588-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f9588-121">Return value</span></span>

<span data-ttu-id="f9588-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f9588-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f9588-123">Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f9588-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f9588-124">Si se produce un error en el método , el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="f9588-124">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9588-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f9588-125">Remarks</span></span>

<span data-ttu-id="f9588-126">Una matriz no transaccional contiene datos principales de fila; es decir, cada vector está contenido en una fila.</span><span class="sxs-lookup"><span data-stu-id="f9588-126">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9588-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9588-127">Requirements</span></span>



| <span data-ttu-id="f9588-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9588-128">Requirement</span></span> | <span data-ttu-id="f9588-129">Value</span><span class="sxs-lookup"><span data-stu-id="f9588-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9588-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f9588-130">Header</span></span><br/>  | <dl> <span data-ttu-id="f9588-131"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="f9588-131"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="f9588-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f9588-132">Library</span></span><br/> | <dl> <span data-ttu-id="f9588-133"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="f9588-133"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f9588-134">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f9588-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9588-135">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="f9588-135">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
