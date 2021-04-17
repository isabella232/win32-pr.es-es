---
description: Establece un número de punto flotante.
ms.assetid: 920cbcf2-ccb9-4533-abbc-6bab8b159ebe
title: 'ID3DXConstantTable:: SetFloat (método) (D3DX9Shader. h)'
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
ms.openlocfilehash: 5048f08acc470e5244de80f4e5618c7416bc1bbf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698279"
---
# <a name="id3dxconstanttablesetfloat-method"></a><span data-ttu-id="0e9ba-103">ID3DXConstantTable:: SetFloat (método)</span><span class="sxs-lookup"><span data-stu-id="0e9ba-103">ID3DXConstantTable::SetFloat method</span></span>

<span data-ttu-id="0e9ba-104">Establece un número de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="0e9ba-104">Sets a floating-point number.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e9ba-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0e9ba-105">Syntax</span></span>


```C++
HRESULT SetFloat(
  [in] LPDIRECT3DDEVICE9 pDevice,
  [in] D3DXHANDLE        hConstant,
  [in] FLOAT             f
);
```



## <a name="parameters"></a><span data-ttu-id="0e9ba-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0e9ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e9ba-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0e9ba-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e9ba-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="0e9ba-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="0e9ba-109">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo asociado a la tabla de constantes.</span><span class="sxs-lookup"><span data-stu-id="0e9ba-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="0e9ba-110">*hConstant* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0e9ba-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e9ba-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="0e9ba-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="0e9ba-112">Identificador único de la constante.</span><span class="sxs-lookup"><span data-stu-id="0e9ba-112">Unique identifier to the constant.</span></span> <span data-ttu-id="0e9ba-113">Vea [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="0e9ba-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e9ba-114">*f* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="0e9ba-114">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e9ba-115">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0e9ba-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0e9ba-116">Número de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="0e9ba-116">Floating-point number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e9ba-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0e9ba-117">Return value</span></span>

<span data-ttu-id="0e9ba-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0e9ba-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0e9ba-119">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0e9ba-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0e9ba-120">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="0e9ba-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e9ba-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e9ba-121">Requirements</span></span>



| <span data-ttu-id="0e9ba-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e9ba-122">Requirement</span></span> | <span data-ttu-id="0e9ba-123">Value</span><span class="sxs-lookup"><span data-stu-id="0e9ba-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e9ba-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0e9ba-124">Header</span></span><br/>  | <dl> <span data-ttu-id="0e9ba-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e9ba-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="0e9ba-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0e9ba-126">Library</span></span><br/> | <dl> <span data-ttu-id="0e9ba-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e9ba-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0e9ba-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="0e9ba-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e9ba-129">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="0e9ba-129">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
