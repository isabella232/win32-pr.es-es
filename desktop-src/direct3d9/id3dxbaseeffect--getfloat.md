---
description: Obtiene un valor de punto flotante.
ms.assetid: 239dd29c-092a-4b9f-ba24-eb6181e91461
title: 'ID3DXBaseEffect:: GetFloat (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFloat
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 51edaa1872223727abdc396766552720cd34d726
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698414"
---
# <a name="id3dxbaseeffectgetfloat-method"></a><span data-ttu-id="df6a0-103">ID3DXBaseEffect:: GetFloat (método)</span><span class="sxs-lookup"><span data-stu-id="df6a0-103">ID3DXBaseEffect::GetFloat method</span></span>

<span data-ttu-id="df6a0-104">Obtiene un valor de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="df6a0-104">Gets a floating point value.</span></span>

## <a name="syntax"></a><span data-ttu-id="df6a0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="df6a0-105">Syntax</span></span>


```C++
HRESULT GetFloat(
  [in]  D3DXHANDLE hParameter,
  [out] FLOAT      *pf
);
```



## <a name="parameters"></a><span data-ttu-id="df6a0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="df6a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df6a0-107">*hParameter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="df6a0-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df6a0-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="df6a0-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="df6a0-109">Identificador único.</span><span class="sxs-lookup"><span data-stu-id="df6a0-109">Unique identifier.</span></span> <span data-ttu-id="df6a0-110">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="df6a0-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="df6a0-111">*PF* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="df6a0-111">*pf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df6a0-112">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="df6a0-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="df6a0-113">Devuelve un valor de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="df6a0-113">Returns a floating point value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df6a0-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="df6a0-114">Return value</span></span>

<span data-ttu-id="df6a0-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="df6a0-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="df6a0-116">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="df6a0-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="df6a0-117">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="df6a0-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="df6a0-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df6a0-118">Requirements</span></span>



| <span data-ttu-id="df6a0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="df6a0-119">Requirement</span></span> | <span data-ttu-id="df6a0-120">Value</span><span class="sxs-lookup"><span data-stu-id="df6a0-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="df6a0-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="df6a0-121">Header</span></span><br/>  | <dl> <span data-ttu-id="df6a0-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="df6a0-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="df6a0-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="df6a0-123">Library</span></span><br/> | <dl> <span data-ttu-id="df6a0-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="df6a0-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="df6a0-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="df6a0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df6a0-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="df6a0-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="df6a0-127">**SetFloat**</span><span class="sxs-lookup"><span data-stu-id="df6a0-127">**SetFloat**</span></span>](id3dxbaseeffect--setfloat.md)
</dt> </dl>

 

 
