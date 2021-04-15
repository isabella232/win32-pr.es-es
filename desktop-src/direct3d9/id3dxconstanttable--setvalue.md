---
description: Establece el contenido del búfer en la tabla de constantes.
ms.assetid: 6058795c-fa32-42aa-9a36-af0b7f6eed1d
title: 'ID3DXConstantTable:: SetValue (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetValue
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e5e02c43e0d0ad84615650bc0b1c0d5fd5654e38
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707903"
---
# <a name="id3dxconstanttablesetvalue-method"></a><span data-ttu-id="6a87f-103">ID3DXConstantTable:: SetValue (método)</span><span class="sxs-lookup"><span data-stu-id="6a87f-103">ID3DXConstantTable::SetValue method</span></span>

<span data-ttu-id="6a87f-104">Establece el contenido del búfer en la tabla de constantes.</span><span class="sxs-lookup"><span data-stu-id="6a87f-104">Sets the contents of the buffer to the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a87f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6a87f-105">Syntax</span></span>


```C++
HRESULT SetValue(
  [in] LPDIRECT3DDEVICE9 pDevice,
  [in] D3DXHANDLE        hConstant,
  [in] LPCVOID           pData,
  [in] UINT              Bytes
);
```



## <a name="parameters"></a><span data-ttu-id="6a87f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6a87f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a87f-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6a87f-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a87f-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="6a87f-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="6a87f-109">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo asociado a la tabla de constantes.</span><span class="sxs-lookup"><span data-stu-id="6a87f-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="6a87f-110">*hConstant* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6a87f-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a87f-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="6a87f-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="6a87f-112">Identificador único de una constante.</span><span class="sxs-lookup"><span data-stu-id="6a87f-112">Unique identifier to a constant.</span></span> <span data-ttu-id="6a87f-113">Vea [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="6a87f-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="6a87f-114">*pdata* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6a87f-114">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a87f-115">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a87f-115">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a87f-116">Búfer que contiene los datos.</span><span class="sxs-lookup"><span data-stu-id="6a87f-116">Buffer containing data.</span></span>

</dd> <dt>

<span data-ttu-id="6a87f-117">*Bytes* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6a87f-117">*Bytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a87f-118">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a87f-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a87f-119">Tamaño del búfer, en bytes.</span><span class="sxs-lookup"><span data-stu-id="6a87f-119">Size of the buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a87f-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6a87f-120">Return value</span></span>

<span data-ttu-id="6a87f-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6a87f-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6a87f-122">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6a87f-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6a87f-123">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="6a87f-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a87f-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a87f-124">Requirements</span></span>



| <span data-ttu-id="6a87f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a87f-125">Requirement</span></span> | <span data-ttu-id="6a87f-126">Value</span><span class="sxs-lookup"><span data-stu-id="6a87f-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a87f-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6a87f-127">Header</span></span><br/>  | <dl> <span data-ttu-id="6a87f-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a87f-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="6a87f-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6a87f-129">Library</span></span><br/> | <dl> <span data-ttu-id="6a87f-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a87f-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="6a87f-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a87f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a87f-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="6a87f-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
