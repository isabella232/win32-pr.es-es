---
description: 'Método ID3DXConstantTable::SetVectorArray: establece una matriz de vectores 4D.'
ms.assetid: bd453384-4f38-4017-a9a5-cac605919940
title: Método ID3DXConstantTable::SetVectorArray (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetVectorArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fe93ef7a75cda743399133445a5f6efd34dd5ad7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115013"
---
# <a name="id3dxconstanttablesetvectorarray-method"></a><span data-ttu-id="ea9d2-103">Método ID3DXConstantTable::SetVectorArray</span><span class="sxs-lookup"><span data-stu-id="ea9d2-103">ID3DXConstantTable::SetVectorArray method</span></span>

<span data-ttu-id="ea9d2-104">Establece una matriz de vectores 4D.</span><span class="sxs-lookup"><span data-stu-id="ea9d2-104">Sets an array of 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea9d2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ea9d2-105">Syntax</span></span>


```C++
HRESULT SetVectorArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXVECTOR4       *pVector,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="ea9d2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ea9d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea9d2-107">*pDevice* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="ea9d2-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea9d2-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="ea9d2-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="ea9d2-109">Puntero a una [**interfaz IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo asociado a la tabla constante.</span><span class="sxs-lookup"><span data-stu-id="ea9d2-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="ea9d2-110">*hConstant* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="ea9d2-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea9d2-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="ea9d2-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="ea9d2-112">Identificador único de la matriz de constantes vectoriales.</span><span class="sxs-lookup"><span data-stu-id="ea9d2-112">Unique identifier to the array of vector constants.</span></span> <span data-ttu-id="ea9d2-113">Vea [D3DXHANDLE.](dx9-graphics-reference-effects-constants.md)</span><span class="sxs-lookup"><span data-stu-id="ea9d2-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea9d2-114">*pVector* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="ea9d2-114">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea9d2-115">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="ea9d2-115">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="ea9d2-116">Matriz de vectores 4D.</span><span class="sxs-lookup"><span data-stu-id="ea9d2-116">Array of 4D vectors.</span></span>

</dd> <dt>

<span data-ttu-id="ea9d2-117">*Recuento* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="ea9d2-117">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea9d2-118">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ea9d2-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ea9d2-119">Número de vectores de la matriz.</span><span class="sxs-lookup"><span data-stu-id="ea9d2-119">Number of vectors in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea9d2-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ea9d2-120">Return value</span></span>

<span data-ttu-id="ea9d2-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ea9d2-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ea9d2-122">Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ea9d2-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ea9d2-123">Si se produce un error en el método , el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="ea9d2-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea9d2-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea9d2-124">Requirements</span></span>



| <span data-ttu-id="ea9d2-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea9d2-125">Requirement</span></span> | <span data-ttu-id="ea9d2-126">Value</span><span class="sxs-lookup"><span data-stu-id="ea9d2-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea9d2-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ea9d2-127">Header</span></span><br/>  | <dl> <span data-ttu-id="ea9d2-128"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="ea9d2-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="ea9d2-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ea9d2-129">Library</span></span><br/> | <dl> <span data-ttu-id="ea9d2-130"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea9d2-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ea9d2-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ea9d2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea9d2-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="ea9d2-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
