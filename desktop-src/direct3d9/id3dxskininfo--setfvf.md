---
description: Establece el tipo de formato de vértice flexible (FVF).
ms.assetid: e581dcd4-7e17-4c36-aac9-c2942924cf51
title: 'ID3DXSkinInfo:: SetFVF (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 010385597442ba1546c20122f6551fca0cfcf81c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707719"
---
# <a name="id3dxskininfosetfvf-method"></a><span data-ttu-id="5297a-103">ID3DXSkinInfo:: SetFVF (método)</span><span class="sxs-lookup"><span data-stu-id="5297a-103">ID3DXSkinInfo::SetFVF method</span></span>

<span data-ttu-id="5297a-104">Establece el tipo de formato de vértice flexible (FVF).</span><span class="sxs-lookup"><span data-stu-id="5297a-104">Sets the flexible vertex format (FVF) type.</span></span>

## <a name="syntax"></a><span data-ttu-id="5297a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5297a-105">Syntax</span></span>


```C++
HRESULT SetFVF(
  [in] DWORD FVF
);
```



## <a name="parameters"></a><span data-ttu-id="5297a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5297a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5297a-107">*FVF* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5297a-107">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5297a-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5297a-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5297a-109">Formato de vértice flexible.</span><span class="sxs-lookup"><span data-stu-id="5297a-109">Flexible vertex format.</span></span> <span data-ttu-id="5297a-110">Vea [D3DFVF](d3dfvf.md).</span><span class="sxs-lookup"><span data-stu-id="5297a-110">See [D3DFVF](d3dfvf.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5297a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5297a-111">Return value</span></span>

<span data-ttu-id="5297a-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5297a-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5297a-113">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5297a-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5297a-114">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="5297a-114">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="5297a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5297a-115">Requirements</span></span>



| <span data-ttu-id="5297a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5297a-116">Requirement</span></span> | <span data-ttu-id="5297a-117">Value</span><span class="sxs-lookup"><span data-stu-id="5297a-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5297a-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5297a-118">Header</span></span><br/>  | <dl> <span data-ttu-id="5297a-119"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="5297a-119"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="5297a-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5297a-120">Library</span></span><br/> | <dl> <span data-ttu-id="5297a-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5297a-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5297a-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="5297a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5297a-123">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="5297a-123">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 
