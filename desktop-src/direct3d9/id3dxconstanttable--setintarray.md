---
description: 'Método ID3DXConstantTable::SetIntArray: establece una matriz de enteros.'
ms.assetid: 15add9df-966d-45aa-b29c-d4bed2a125f4
title: Método ID3DXConstantTable::SetIntArray (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetIntArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5f674bc730398c386856314a7e7305f33f3e7fa1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115113"
---
# <a name="id3dxconstanttablesetintarray-method"></a><span data-ttu-id="95c7d-103">Método ID3DXConstantTable::SetIntArray</span><span class="sxs-lookup"><span data-stu-id="95c7d-103">ID3DXConstantTable::SetIntArray method</span></span>

<span data-ttu-id="95c7d-104">Establece una matriz de enteros.</span><span class="sxs-lookup"><span data-stu-id="95c7d-104">Sets an array of integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="95c7d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="95c7d-105">Syntax</span></span>


```C++
HRESULT SetIntArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const INT               *pn,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="95c7d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="95c7d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95c7d-107">*pDevice* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="95c7d-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95c7d-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="95c7d-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="95c7d-109">Puntero a una [**interfaz IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo asociado a la tabla constante.</span><span class="sxs-lookup"><span data-stu-id="95c7d-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="95c7d-110">*hConstant* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="95c7d-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95c7d-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="95c7d-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="95c7d-112">Identificador único de la matriz de constantes.</span><span class="sxs-lookup"><span data-stu-id="95c7d-112">Unique identifier to the array of constants.</span></span> <span data-ttu-id="95c7d-113">Vea [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="95c7d-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="95c7d-114">*pn* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="95c7d-114">*pn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95c7d-115">Tipo: **const [**INT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="95c7d-115">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="95c7d-116">Matriz de enteros.</span><span class="sxs-lookup"><span data-stu-id="95c7d-116">Array of integers.</span></span>

</dd> <dt>

<span data-ttu-id="95c7d-117">*Recuento* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="95c7d-117">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95c7d-118">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="95c7d-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="95c7d-119">Número de enteros de la matriz.</span><span class="sxs-lookup"><span data-stu-id="95c7d-119">Number of integers in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95c7d-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="95c7d-120">Return value</span></span>

<span data-ttu-id="95c7d-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="95c7d-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="95c7d-122">Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="95c7d-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="95c7d-123">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="95c7d-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="95c7d-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95c7d-124">Requirements</span></span>



| <span data-ttu-id="95c7d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="95c7d-125">Requirement</span></span> | <span data-ttu-id="95c7d-126">Value</span><span class="sxs-lookup"><span data-stu-id="95c7d-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="95c7d-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="95c7d-127">Header</span></span><br/>  | <dl> <span data-ttu-id="95c7d-128"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="95c7d-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="95c7d-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="95c7d-129">Library</span></span><br/> | <dl> <span data-ttu-id="95c7d-130"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="95c7d-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="95c7d-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="95c7d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95c7d-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="95c7d-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
