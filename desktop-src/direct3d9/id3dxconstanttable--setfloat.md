---
description: 'Método ID3DXConstantTable::SetFloat: establece un número de punto flotante.'
ms.assetid: 920cbcf2-ccb9-4533-abbc-6bab8b159ebe
title: Método ID3DXConstantTable::SetFloat (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetFloat
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6589d56e0b9dcf8debe14a7c81f86a4972a73405
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115223"
---
# <a name="id3dxconstanttablesetfloat-method"></a><span data-ttu-id="1f71d-103">Método ID3DXConstantTable::SetFloat</span><span class="sxs-lookup"><span data-stu-id="1f71d-103">ID3DXConstantTable::SetFloat method</span></span>

<span data-ttu-id="1f71d-104">Establece un número de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="1f71d-104">Sets a floating-point number.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f71d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1f71d-105">Syntax</span></span>


```C++
HRESULT SetFloat(
  [in] LPDIRECT3DDEVICE9 pDevice,
  [in] D3DXHANDLE        hConstant,
  [in] FLOAT             f
);
```



## <a name="parameters"></a><span data-ttu-id="1f71d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1f71d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f71d-107">*pDevice* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="1f71d-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f71d-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="1f71d-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="1f71d-109">Puntero a una [**interfaz IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo asociado a la tabla constante.</span><span class="sxs-lookup"><span data-stu-id="1f71d-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="1f71d-110">*hConstant* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="1f71d-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f71d-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="1f71d-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="1f71d-112">Identificador único de la constante.</span><span class="sxs-lookup"><span data-stu-id="1f71d-112">Unique identifier to the constant.</span></span> <span data-ttu-id="1f71d-113">Vea [D3DXHANDLE.](dx9-graphics-reference-effects-constants.md)</span><span class="sxs-lookup"><span data-stu-id="1f71d-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f71d-114">*f* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1f71d-114">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f71d-115">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1f71d-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1f71d-116">Número de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="1f71d-116">Floating-point number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f71d-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1f71d-117">Return value</span></span>

<span data-ttu-id="1f71d-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1f71d-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1f71d-119">Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1f71d-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1f71d-120">Si se produce un error en el método , el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="1f71d-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f71d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f71d-121">Requirements</span></span>



| <span data-ttu-id="1f71d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f71d-122">Requirement</span></span> | <span data-ttu-id="1f71d-123">Value</span><span class="sxs-lookup"><span data-stu-id="1f71d-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f71d-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1f71d-124">Header</span></span><br/>  | <dl> <span data-ttu-id="1f71d-125"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="1f71d-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="1f71d-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1f71d-126">Library</span></span><br/> | <dl> <span data-ttu-id="1f71d-127"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="1f71d-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="1f71d-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1f71d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f71d-129">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="1f71d-129">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
