---
description: Establece una matriz de enteros.
ms.assetid: 15add9df-966d-45aa-b29c-d4bed2a125f4
title: 'ID3DXConstantTable:: SetIntArray (método) (D3DX9Shader. h)'
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
ms.openlocfilehash: 9f89de7d784ce355570d369606bfa67ddd6f5acf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718251"
---
# <a name="id3dxconstanttablesetintarray-method"></a><span data-ttu-id="5aef6-103">ID3DXConstantTable:: SetIntArray (método)</span><span class="sxs-lookup"><span data-stu-id="5aef6-103">ID3DXConstantTable::SetIntArray method</span></span>

<span data-ttu-id="5aef6-104">Establece una matriz de enteros.</span><span class="sxs-lookup"><span data-stu-id="5aef6-104">Sets an array of integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="5aef6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5aef6-105">Syntax</span></span>


```C++
HRESULT SetIntArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const INT               *pn,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="5aef6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5aef6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5aef6-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5aef6-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5aef6-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="5aef6-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="5aef6-109">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo asociado a la tabla de constantes.</span><span class="sxs-lookup"><span data-stu-id="5aef6-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="5aef6-110">*hConstant* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5aef6-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5aef6-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="5aef6-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="5aef6-112">Identificador único de la matriz de constantes.</span><span class="sxs-lookup"><span data-stu-id="5aef6-112">Unique identifier to the array of constants.</span></span> <span data-ttu-id="5aef6-113">Vea [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="5aef6-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="5aef6-114">*PN* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5aef6-114">*pn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5aef6-115">Tipo: **const [**int**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="5aef6-115">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5aef6-116">Matriz de enteros.</span><span class="sxs-lookup"><span data-stu-id="5aef6-116">Array of integers.</span></span>

</dd> <dt>

<span data-ttu-id="5aef6-117">*Recuento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5aef6-117">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5aef6-118">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5aef6-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5aef6-119">Número de enteros de la matriz.</span><span class="sxs-lookup"><span data-stu-id="5aef6-119">Number of integers in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5aef6-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5aef6-120">Return value</span></span>

<span data-ttu-id="5aef6-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5aef6-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5aef6-122">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5aef6-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5aef6-123">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="5aef6-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="5aef6-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5aef6-124">Requirements</span></span>



| <span data-ttu-id="5aef6-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="5aef6-125">Requirement</span></span> | <span data-ttu-id="5aef6-126">Value</span><span class="sxs-lookup"><span data-stu-id="5aef6-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5aef6-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5aef6-127">Header</span></span><br/>  | <dl> <span data-ttu-id="5aef6-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="5aef6-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="5aef6-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5aef6-129">Library</span></span><br/> | <dl> <span data-ttu-id="5aef6-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5aef6-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="5aef6-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="5aef6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5aef6-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="5aef6-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
