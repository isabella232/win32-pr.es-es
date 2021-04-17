---
description: Establece una matriz de valores booleanos.
ms.assetid: 323ad654-81e3-4986-a667-8333dd44a2d1
title: 'ID3DXConstantTable:: SetBoolArray (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetBoolArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d573a2c44b54809ec259a0ceb5abab02ef37df34
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698281"
---
# <a name="id3dxconstanttablesetboolarray-method"></a><span data-ttu-id="6bfce-103">ID3DXConstantTable:: SetBoolArray (método)</span><span class="sxs-lookup"><span data-stu-id="6bfce-103">ID3DXConstantTable::SetBoolArray method</span></span>

<span data-ttu-id="6bfce-104">Establece una matriz de valores booleanos.</span><span class="sxs-lookup"><span data-stu-id="6bfce-104">Sets an array of Boolean values.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bfce-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6bfce-105">Syntax</span></span>


```C++
HRESULT SetBoolArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const BOOL              *pB,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="6bfce-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6bfce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bfce-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6bfce-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bfce-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="6bfce-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="6bfce-109">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo asociado a la tabla de constantes.</span><span class="sxs-lookup"><span data-stu-id="6bfce-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="6bfce-110">*hConstant* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6bfce-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bfce-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="6bfce-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="6bfce-112">Identificador único de la matriz de constantes.</span><span class="sxs-lookup"><span data-stu-id="6bfce-112">Unique identifier to the array of constants.</span></span> <span data-ttu-id="6bfce-113">Vea [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="6bfce-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="6bfce-114">*PB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6bfce-114">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bfce-115">Tipo: **const [**bool**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="6bfce-115">Type: **const [**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6bfce-116">Matriz de valores booleanos.</span><span class="sxs-lookup"><span data-stu-id="6bfce-116">Array of Boolean values.</span></span>

</dd> <dt>

<span data-ttu-id="6bfce-117">*Recuento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6bfce-117">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bfce-118">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6bfce-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6bfce-119">Número de valores booleanos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="6bfce-119">Number of Boolean values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bfce-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6bfce-120">Return value</span></span>

<span data-ttu-id="6bfce-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6bfce-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6bfce-122">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6bfce-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6bfce-123">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="6bfce-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bfce-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6bfce-124">Requirements</span></span>



| <span data-ttu-id="6bfce-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bfce-125">Requirement</span></span> | <span data-ttu-id="6bfce-126">Value</span><span class="sxs-lookup"><span data-stu-id="6bfce-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bfce-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6bfce-127">Header</span></span><br/>  | <dl> <span data-ttu-id="6bfce-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="6bfce-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="6bfce-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6bfce-129">Library</span></span><br/> | <dl> <span data-ttu-id="6bfce-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6bfce-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="6bfce-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="6bfce-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bfce-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="6bfce-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
