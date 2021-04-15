---
description: Desensamblar un efecto.
ms.assetid: d95d6e97-2e79-4cd2-965e-483aa1a1ddbc
title: Función D3DXDisassembleEffect (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDisassembleEffect
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 945c30319d16264a2b7489d1dc0849a4678cbede
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707887"
---
# <a name="d3dxdisassembleeffect-function"></a><span data-ttu-id="b88da-103">D3DXDisassembleEffect función)</span><span class="sxs-lookup"><span data-stu-id="b88da-103">D3DXDisassembleEffect function</span></span>

<span data-ttu-id="b88da-104">Desensamblar un efecto.</span><span class="sxs-lookup"><span data-stu-id="b88da-104">Disassemble an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="b88da-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b88da-105">Syntax</span></span>


```C++
HRESULT D3DXDisassembleEffect(
  _In_  LPD3DXEFFECT pEffect,
  _In_  BOOL         EnableColorCode,
  _Out_ LPD3DXBUFFER *ppDisassembly
);
```



## <a name="parameters"></a><span data-ttu-id="b88da-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b88da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b88da-107">*pEffect* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b88da-107">*pEffect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b88da-108">Tipo: **[ **LPD3DXEFFECT**](id3dxeffect.md)**</span><span class="sxs-lookup"><span data-stu-id="b88da-108">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)**</span></span>

<span data-ttu-id="b88da-109">Puntero a una interfaz [**ID3DXEffect**](id3dxeffect.md) que contiene el efecto.</span><span class="sxs-lookup"><span data-stu-id="b88da-109">Pointer to an [**ID3DXEffect**](id3dxeffect.md) interface that contains the effect.</span></span>

</dd> <dt>

<span data-ttu-id="b88da-110">*EnableColorCode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b88da-110">*EnableColorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b88da-111">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b88da-111">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b88da-112">Habilite la codificación de colores para facilitar la lectura del desensamblado.</span><span class="sxs-lookup"><span data-stu-id="b88da-112">Enable color coding to make the disassembly easier to read.</span></span>

</dd> <dt>

<span data-ttu-id="b88da-113">*ppDisassembly* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b88da-113">*ppDisassembly* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b88da-114">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="b88da-114">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="b88da-115">Devuelve un búfer que contiene el sombreador desensamblado.</span><span class="sxs-lookup"><span data-stu-id="b88da-115">Returns a buffer containing the disassembled shader.</span></span> <span data-ttu-id="b88da-116">Vea [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="b88da-116">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b88da-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b88da-117">Return value</span></span>

<span data-ttu-id="b88da-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b88da-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b88da-119">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b88da-119">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b88da-120">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="b88da-120">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="b88da-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b88da-121">Requirements</span></span>



| <span data-ttu-id="b88da-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b88da-122">Requirement</span></span> | <span data-ttu-id="b88da-123">Value</span><span class="sxs-lookup"><span data-stu-id="b88da-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b88da-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b88da-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b88da-125"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b88da-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="b88da-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b88da-126">Library</span></span><br/> | <dl> <span data-ttu-id="b88da-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b88da-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b88da-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="b88da-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b88da-129">Funciones de efecto</span><span class="sxs-lookup"><span data-stu-id="b88da-129">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> </dl>

 

 
