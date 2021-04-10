---
description: Establece una matriz de números de punto flotante.
ms.assetid: 7a622dd5-47ed-4166-a6df-f484b03e0b5a
title: 'ID3DXConstantTable:: SetFloatArray (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetFloatArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d75d4171ab51859e4095acbe5d3e86d704b1f437
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280355"
---
# <a name="id3dxconstanttablesetfloatarray-method"></a><span data-ttu-id="55433-103">ID3DXConstantTable:: SetFloatArray (método)</span><span class="sxs-lookup"><span data-stu-id="55433-103">ID3DXConstantTable::SetFloatArray method</span></span>

<span data-ttu-id="55433-104">Establece una matriz de números de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="55433-104">Sets an array of floating-point numbers.</span></span>

## <a name="syntax"></a><span data-ttu-id="55433-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="55433-105">Syntax</span></span>


```C++
HRESULT SetFloatArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const FLOAT             *pf,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="55433-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="55433-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55433-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="55433-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55433-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="55433-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="55433-109">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo asociado a la tabla de constantes.</span><span class="sxs-lookup"><span data-stu-id="55433-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="55433-110">*hConstant* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="55433-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55433-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="55433-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="55433-112">Identificador único de la matriz de constantes.</span><span class="sxs-lookup"><span data-stu-id="55433-112">Unique identifier to the array of constants.</span></span> <span data-ttu-id="55433-113">Vea [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="55433-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="55433-114">*PF* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="55433-114">*pf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55433-115">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="55433-115">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="55433-116">Matriz de números de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="55433-116">Array of floating-point numbers.</span></span>

</dd> <dt>

<span data-ttu-id="55433-117">*Recuento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="55433-117">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55433-118">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="55433-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="55433-119">Número de valores de punto flotante de la matriz.</span><span class="sxs-lookup"><span data-stu-id="55433-119">Number of floating-point values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55433-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="55433-120">Return value</span></span>

<span data-ttu-id="55433-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="55433-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="55433-122">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="55433-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="55433-123">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="55433-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="55433-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55433-124">Requirements</span></span>



| <span data-ttu-id="55433-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="55433-125">Requirement</span></span> | <span data-ttu-id="55433-126">Value</span><span class="sxs-lookup"><span data-stu-id="55433-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="55433-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="55433-127">Header</span></span><br/>  | <dl> <span data-ttu-id="55433-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="55433-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="55433-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="55433-129">Library</span></span><br/> | <dl> <span data-ttu-id="55433-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="55433-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="55433-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="55433-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55433-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="55433-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
