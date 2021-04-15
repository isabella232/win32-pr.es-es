---
description: Obtiene el identificador de una función.
ms.assetid: 97c82c28-4402-4605-8247-44d6f38bfa20
title: 'ID3DXBaseEffect:: GetFunction ((método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFunction
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: de0567b605f4a892c1f8274a346a74acfbbc0442
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708090"
---
# <a name="id3dxbaseeffectgetfunction-method"></a><span data-ttu-id="e51b9-103">ID3DXBaseEffect:: GetFunction ((método)</span><span class="sxs-lookup"><span data-stu-id="e51b9-103">ID3DXBaseEffect::GetFunction method</span></span>

<span data-ttu-id="e51b9-104">Obtiene el identificador de una función.</span><span class="sxs-lookup"><span data-stu-id="e51b9-104">Gets the handle of a function.</span></span>

## <a name="syntax"></a><span data-ttu-id="e51b9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e51b9-105">Syntax</span></span>


```C++
D3DXHANDLE GetFunction(
  [in] UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="e51b9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e51b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e51b9-107">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="e51b9-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e51b9-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e51b9-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e51b9-109">Índice de función.</span><span class="sxs-lookup"><span data-stu-id="e51b9-109">Function index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e51b9-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e51b9-110">Return value</span></span>

<span data-ttu-id="e51b9-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="e51b9-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="e51b9-112">Devuelve el identificador de la función especificada, o **null** si el índice no era válido.</span><span class="sxs-lookup"><span data-stu-id="e51b9-112">Returns the handle of the specified function, or **NULL** if the index was invalid.</span></span> <span data-ttu-id="e51b9-113">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="e51b9-113">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e51b9-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e51b9-114">Requirements</span></span>



| <span data-ttu-id="e51b9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e51b9-115">Requirement</span></span> | <span data-ttu-id="e51b9-116">Value</span><span class="sxs-lookup"><span data-stu-id="e51b9-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e51b9-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e51b9-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e51b9-118"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e51b9-118"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="e51b9-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e51b9-119">Library</span></span><br/> | <dl> <span data-ttu-id="e51b9-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e51b9-120"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e51b9-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="e51b9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e51b9-122">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="e51b9-122">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
