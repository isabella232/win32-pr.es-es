---
description: Establece un valor booleano.
ms.assetid: 652e5b68-88f3-4b05-959b-38bb530c546a
title: 'ID3DXConstantTable:: SetBool (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetBool
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 49fb38407aeaaf042d8d606c90e075a1891b9557
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821122"
---
# <a name="id3dxconstanttablesetbool-method"></a><span data-ttu-id="e8ebd-103">ID3DXConstantTable:: SetBool (método)</span><span class="sxs-lookup"><span data-stu-id="e8ebd-103">ID3DXConstantTable::SetBool method</span></span>

<span data-ttu-id="e8ebd-104">Establece un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="e8ebd-104">Sets a Boolean value.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8ebd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e8ebd-105">Syntax</span></span>


```C++
HRESULT SetBool(
  [in] LPDIRECT3DDEVICE9 pDevice,
  [in] D3DXHANDLE        hConstant,
  [in] BOOL              b
);
```



## <a name="parameters"></a><span data-ttu-id="e8ebd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e8ebd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8ebd-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e8ebd-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8ebd-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="e8ebd-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="e8ebd-109">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo asociado a la tabla de constantes.</span><span class="sxs-lookup"><span data-stu-id="e8ebd-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="e8ebd-110">*hConstant* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e8ebd-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8ebd-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="e8ebd-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="e8ebd-112">Identificador único de la constante.</span><span class="sxs-lookup"><span data-stu-id="e8ebd-112">Unique identifier to the constant.</span></span> <span data-ttu-id="e8ebd-113">Vea [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="e8ebd-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="e8ebd-114">*b* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="e8ebd-114">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8ebd-115">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e8ebd-115">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e8ebd-116">Valor booleano.</span><span class="sxs-lookup"><span data-stu-id="e8ebd-116">Boolean value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8ebd-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e8ebd-117">Return value</span></span>

<span data-ttu-id="e8ebd-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e8ebd-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e8ebd-119">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e8ebd-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e8ebd-120">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="e8ebd-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8ebd-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8ebd-121">Requirements</span></span>



| <span data-ttu-id="e8ebd-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8ebd-122">Requirement</span></span> | <span data-ttu-id="e8ebd-123">Value</span><span class="sxs-lookup"><span data-stu-id="e8ebd-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8ebd-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e8ebd-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e8ebd-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8ebd-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="e8ebd-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e8ebd-126">Library</span></span><br/> | <dl> <span data-ttu-id="e8ebd-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e8ebd-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e8ebd-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="e8ebd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8ebd-129">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="e8ebd-129">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
