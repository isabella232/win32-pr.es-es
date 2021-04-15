---
description: Establece una matriz transpuesta.
ms.assetid: 1c4d64ce-64bd-47d4-9912-879f4834c0e8
title: 'ID3DXConstantTable:: SetMatrixTranspose (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrixTranspose
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: aa84f9e483be0c6c2ddae37c52ef6df2c43fda90
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707904"
---
# <a name="id3dxconstanttablesetmatrixtranspose-method"></a><span data-ttu-id="17c2f-103">ID3DXConstantTable:: SetMatrixTranspose (método)</span><span class="sxs-lookup"><span data-stu-id="17c2f-103">ID3DXConstantTable::SetMatrixTranspose method</span></span>

<span data-ttu-id="17c2f-104">Establece una matriz transpuesta.</span><span class="sxs-lookup"><span data-stu-id="17c2f-104">Sets a transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="17c2f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="17c2f-105">Syntax</span></span>


```C++
HRESULT SetMatrixTranspose(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="17c2f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="17c2f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17c2f-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="17c2f-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17c2f-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="17c2f-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="17c2f-109">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo asociado a la tabla de constantes.</span><span class="sxs-lookup"><span data-stu-id="17c2f-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="17c2f-110">*hConstant* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="17c2f-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17c2f-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="17c2f-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="17c2f-112">Identificador único de la matriz de constantes.</span><span class="sxs-lookup"><span data-stu-id="17c2f-112">Unique identifier to the matrix of constants.</span></span> <span data-ttu-id="17c2f-113">Vea [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="17c2f-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="17c2f-114">*pMatrix* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="17c2f-114">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17c2f-115">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="17c2f-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="17c2f-116">Puntero a una matriz transpuesta.</span><span class="sxs-lookup"><span data-stu-id="17c2f-116">Pointer to a transposed matrix.</span></span> <span data-ttu-id="17c2f-117">Vea [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="17c2f-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17c2f-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="17c2f-118">Return value</span></span>

<span data-ttu-id="17c2f-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="17c2f-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="17c2f-120">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="17c2f-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="17c2f-121">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="17c2f-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="17c2f-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17c2f-122">Requirements</span></span>



| <span data-ttu-id="17c2f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="17c2f-123">Requirement</span></span> | <span data-ttu-id="17c2f-124">Value</span><span class="sxs-lookup"><span data-stu-id="17c2f-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="17c2f-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="17c2f-125">Header</span></span><br/>  | <dl> <span data-ttu-id="17c2f-126"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="17c2f-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="17c2f-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="17c2f-127">Library</span></span><br/> | <dl> <span data-ttu-id="17c2f-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="17c2f-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="17c2f-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="17c2f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17c2f-130">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="17c2f-130">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
