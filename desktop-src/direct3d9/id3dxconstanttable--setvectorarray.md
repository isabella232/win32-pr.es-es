---
description: Establece una matriz de vectores 4D.
ms.assetid: bd453384-4f38-4017-a9a5-cac605919940
title: 'ID3DXConstantTable:: SetVectorArray (método) (D3DX9Shader. h)'
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
ms.openlocfilehash: a6c68621a3f97251cdd88836792bf55980f28311
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707901"
---
# <a name="id3dxconstanttablesetvectorarray-method"></a><span data-ttu-id="69c8d-103">ID3DXConstantTable:: SetVectorArray (método)</span><span class="sxs-lookup"><span data-stu-id="69c8d-103">ID3DXConstantTable::SetVectorArray method</span></span>

<span data-ttu-id="69c8d-104">Establece una matriz de vectores 4D.</span><span class="sxs-lookup"><span data-stu-id="69c8d-104">Sets an array of 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="69c8d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="69c8d-105">Syntax</span></span>


```C++
HRESULT SetVectorArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXVECTOR4       *pVector,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="69c8d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="69c8d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69c8d-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="69c8d-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69c8d-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="69c8d-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="69c8d-109">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo asociado a la tabla de constantes.</span><span class="sxs-lookup"><span data-stu-id="69c8d-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="69c8d-110">*hConstant* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="69c8d-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69c8d-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="69c8d-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="69c8d-112">Identificador único de la matriz de constantes de vector.</span><span class="sxs-lookup"><span data-stu-id="69c8d-112">Unique identifier to the array of vector constants.</span></span> <span data-ttu-id="69c8d-113">Vea [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="69c8d-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="69c8d-114">*pVector* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="69c8d-114">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69c8d-115">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="69c8d-115">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="69c8d-116">Matriz de vectores 4D.</span><span class="sxs-lookup"><span data-stu-id="69c8d-116">Array of 4D vectors.</span></span>

</dd> <dt>

<span data-ttu-id="69c8d-117">*Recuento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="69c8d-117">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69c8d-118">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="69c8d-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="69c8d-119">Número de vectores de la matriz.</span><span class="sxs-lookup"><span data-stu-id="69c8d-119">Number of vectors in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69c8d-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="69c8d-120">Return value</span></span>

<span data-ttu-id="69c8d-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="69c8d-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="69c8d-122">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="69c8d-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="69c8d-123">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="69c8d-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="69c8d-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69c8d-124">Requirements</span></span>



| <span data-ttu-id="69c8d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="69c8d-125">Requirement</span></span> | <span data-ttu-id="69c8d-126">Value</span><span class="sxs-lookup"><span data-stu-id="69c8d-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="69c8d-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="69c8d-127">Header</span></span><br/>  | <dl> <span data-ttu-id="69c8d-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="69c8d-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="69c8d-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="69c8d-129">Library</span></span><br/> | <dl> <span data-ttu-id="69c8d-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="69c8d-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="69c8d-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="69c8d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69c8d-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="69c8d-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
