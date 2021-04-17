---
description: Establece una matriz de nontransposed.
ms.assetid: 30369e34-6e9d-4480-a142-e38f46fd38b0
title: 'ID3DXConstantTable:: SetMatrix (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0ae227663a61087fae309d1954b8f0dc438f6df2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698278"
---
# <a name="id3dxconstanttablesetmatrix-method"></a><span data-ttu-id="0d9d3-103">ID3DXConstantTable:: SetMatrix (método)</span><span class="sxs-lookup"><span data-stu-id="0d9d3-103">ID3DXConstantTable::SetMatrix method</span></span>

<span data-ttu-id="0d9d3-104">Establece una matriz de nontransposed.</span><span class="sxs-lookup"><span data-stu-id="0d9d3-104">Sets a nontransposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d9d3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0d9d3-105">Syntax</span></span>


```C++
HRESULT SetMatrix(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="0d9d3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0d9d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d9d3-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0d9d3-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d9d3-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="0d9d3-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="0d9d3-109">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo asociado a la tabla de constantes.</span><span class="sxs-lookup"><span data-stu-id="0d9d3-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="0d9d3-110">*hConstant* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0d9d3-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d9d3-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="0d9d3-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="0d9d3-112">Identificador único de la matriz de constantes.</span><span class="sxs-lookup"><span data-stu-id="0d9d3-112">Unique identifier to the matrix of constants.</span></span> <span data-ttu-id="0d9d3-113">Vea [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="0d9d3-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d9d3-114">*pMatrix* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0d9d3-114">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d9d3-115">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="0d9d3-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0d9d3-116">Puntero a una matriz nontransposed.</span><span class="sxs-lookup"><span data-stu-id="0d9d3-116">Pointer to a nontransposed matrix.</span></span> <span data-ttu-id="0d9d3-117">Vea [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="0d9d3-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d9d3-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0d9d3-118">Return value</span></span>

<span data-ttu-id="0d9d3-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0d9d3-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0d9d3-120">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0d9d3-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0d9d3-121">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="0d9d3-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d9d3-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d9d3-122">Requirements</span></span>



| <span data-ttu-id="0d9d3-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d9d3-123">Requirement</span></span> | <span data-ttu-id="0d9d3-124">Value</span><span class="sxs-lookup"><span data-stu-id="0d9d3-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d9d3-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0d9d3-125">Header</span></span><br/>  | <dl> <span data-ttu-id="0d9d3-126"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d9d3-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="0d9d3-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0d9d3-127">Library</span></span><br/> | <dl> <span data-ttu-id="0d9d3-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0d9d3-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0d9d3-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="0d9d3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d9d3-130">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="0d9d3-130">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
