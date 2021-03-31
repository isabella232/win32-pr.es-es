---
description: Establezca el intervalo de una matriz que se va a pasar al dispositivo.
ms.assetid: 43f1c258-770c-4756-9033-e5667b379fe6
title: 'ID3DXBaseEffect:: SetArrayRange (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetArrayRange
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 59b981c1f2aff18d4bdb57f5726136945203f5fe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157132"
---
# <a name="id3dxbaseeffectsetarrayrange-method"></a><span data-ttu-id="9f82f-103">ID3DXBaseEffect:: SetArrayRange (método)</span><span class="sxs-lookup"><span data-stu-id="9f82f-103">ID3DXBaseEffect::SetArrayRange method</span></span>

<span data-ttu-id="9f82f-104">Establezca el intervalo de una matriz que se va a pasar al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9f82f-104">Set the range of an array to pass to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f82f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9f82f-105">Syntax</span></span>


```C++
HRESULT SetArrayRange(
  [in] D3DXHANDLE hParameter,
  [in] UINT       Start,
  [in] UINT       Stop
);
```



## <a name="parameters"></a><span data-ttu-id="9f82f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9f82f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f82f-107">*hParameter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9f82f-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f82f-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="9f82f-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="9f82f-109">Identificador único.</span><span class="sxs-lookup"><span data-stu-id="9f82f-109">Unique identifier.</span></span> <span data-ttu-id="9f82f-110">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="9f82f-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f82f-111">*Iniciar* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9f82f-111">*Start* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f82f-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9f82f-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9f82f-113">Índice de inicio.</span><span class="sxs-lookup"><span data-stu-id="9f82f-113">Start index.</span></span>

</dd> <dt>

<span data-ttu-id="9f82f-114">*Detener* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9f82f-114">*Stop* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f82f-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9f82f-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9f82f-116">Detener índice.</span><span class="sxs-lookup"><span data-stu-id="9f82f-116">Stop index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f82f-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9f82f-117">Return value</span></span>

<span data-ttu-id="9f82f-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9f82f-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9f82f-119">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9f82f-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9f82f-120">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="9f82f-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f82f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f82f-121">Requirements</span></span>



| <span data-ttu-id="9f82f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f82f-122">Requirement</span></span> | <span data-ttu-id="9f82f-123">Value</span><span class="sxs-lookup"><span data-stu-id="9f82f-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f82f-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9f82f-124">Header</span></span><br/>  | <dl> <span data-ttu-id="9f82f-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f82f-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="9f82f-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9f82f-126">Library</span></span><br/> | <dl> <span data-ttu-id="9f82f-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9f82f-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="9f82f-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="9f82f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f82f-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="9f82f-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
