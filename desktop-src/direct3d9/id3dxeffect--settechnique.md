---
description: Establece la técnica activa.
ms.assetid: 18f19773-a9f8-47f9-9334-acc95e0f0eb7
title: 'ID3DXEffect:: SetTechnique (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.SetTechnique
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e93fbff9eb74e8885675b7ccf4ea69cc53d5da53
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003776"
---
# <a name="id3dxeffectsettechnique-method"></a><span data-ttu-id="f023e-103">ID3DXEffect:: SetTechnique (método)</span><span class="sxs-lookup"><span data-stu-id="f023e-103">ID3DXEffect::SetTechnique method</span></span>

<span data-ttu-id="f023e-104">Establece la técnica activa.</span><span class="sxs-lookup"><span data-stu-id="f023e-104">Sets the active technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="f023e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f023e-105">Syntax</span></span>


```C++
HRESULT SetTechnique(
  [in] D3DXHANDLE hTechnique
);
```



## <a name="parameters"></a><span data-ttu-id="f023e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f023e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f023e-107">*hTechnique* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f023e-107">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f023e-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="f023e-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="f023e-109">Identificador único de la técnica.</span><span class="sxs-lookup"><span data-stu-id="f023e-109">Unique handle to the technique.</span></span> <span data-ttu-id="f023e-110">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="f023e-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f023e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f023e-111">Return value</span></span>

<span data-ttu-id="f023e-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f023e-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f023e-113">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f023e-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f023e-114">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="f023e-114">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="f023e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f023e-115">Requirements</span></span>



| <span data-ttu-id="f023e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f023e-116">Requirement</span></span> | <span data-ttu-id="f023e-117">Value</span><span class="sxs-lookup"><span data-stu-id="f023e-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f023e-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f023e-118">Header</span></span><br/>  | <dl> <span data-ttu-id="f023e-119"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f023e-119"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="f023e-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f023e-120">Library</span></span><br/> | <dl> <span data-ttu-id="f023e-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f023e-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f023e-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="f023e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f023e-123">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="f023e-123">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 




