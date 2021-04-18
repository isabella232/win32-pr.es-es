---
description: Obtiene un valor BOOLEANO.
ms.assetid: 9d61efcd-f267-4c45-b685-d363588796f7
title: 'ID3DXBaseEffect:: GetBool (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetBool
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 0476c62733379a7e92aca55c3cdc2c31a3526de2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718519"
---
# <a name="id3dxbaseeffectgetbool-method"></a><span data-ttu-id="b585e-103">ID3DXBaseEffect:: GetBool (método)</span><span class="sxs-lookup"><span data-stu-id="b585e-103">ID3DXBaseEffect::GetBool method</span></span>

<span data-ttu-id="b585e-104">Obtiene un valor BOOLEANO.</span><span class="sxs-lookup"><span data-stu-id="b585e-104">Gets a BOOL value.</span></span>

## <a name="syntax"></a><span data-ttu-id="b585e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b585e-105">Syntax</span></span>


```C++
HRESULT GetBool(
  [in]  D3DXHANDLE hParameter,
  [out] BOOL       *pb
);
```



## <a name="parameters"></a><span data-ttu-id="b585e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b585e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b585e-107">*hParameter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b585e-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b585e-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="b585e-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="b585e-109">Identificador único.</span><span class="sxs-lookup"><span data-stu-id="b585e-109">Unique identifier.</span></span> <span data-ttu-id="b585e-110">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="b585e-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="b585e-111">*PB* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b585e-111">*pb* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b585e-112">Tipo: **[ **bool**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b585e-112">Type: **[**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b585e-113">Devuelve un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="b585e-113">Returns a Boolean value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b585e-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b585e-114">Return value</span></span>

<span data-ttu-id="b585e-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b585e-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b585e-116">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b585e-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b585e-117">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b585e-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="b585e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b585e-118">Requirements</span></span>



| <span data-ttu-id="b585e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b585e-119">Requirement</span></span> | <span data-ttu-id="b585e-120">Value</span><span class="sxs-lookup"><span data-stu-id="b585e-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b585e-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b585e-121">Header</span></span><br/>  | <dl> <span data-ttu-id="b585e-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="b585e-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="b585e-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b585e-123">Library</span></span><br/> | <dl> <span data-ttu-id="b585e-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b585e-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b585e-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="b585e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b585e-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="b585e-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="b585e-127">**SetBool**</span><span class="sxs-lookup"><span data-stu-id="b585e-127">**SetBool**</span></span>](id3dxbaseeffect--setbool.md)
</dt> </dl>

 

 
