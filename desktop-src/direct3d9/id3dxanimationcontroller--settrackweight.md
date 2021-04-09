---
description: Establece el peso de la pista. El peso se utiliza para determinar cómo combinar varias pistas.
ms.assetid: a00ceae4-47b4-4fb9-a028-97493e3dc071
title: 'ID3DXAnimationController:: SetTrackWeight (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackWeight
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc42d283231a0e49359531827cc785bd83aefc2b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821506"
---
# <a name="id3dxanimationcontrollersettrackweight-method"></a><span data-ttu-id="8e63c-104">ID3DXAnimationController:: SetTrackWeight (método)</span><span class="sxs-lookup"><span data-stu-id="8e63c-104">ID3DXAnimationController::SetTrackWeight method</span></span>

<span data-ttu-id="8e63c-105">Establece el peso de la pista.</span><span class="sxs-lookup"><span data-stu-id="8e63c-105">Sets the track weight.</span></span> <span data-ttu-id="8e63c-106">El peso se utiliza para determinar cómo combinar varias pistas.</span><span class="sxs-lookup"><span data-stu-id="8e63c-106">The weight is used to determine how to blend multiple tracks together.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e63c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8e63c-107">Syntax</span></span>


```C++
HRESULT SetTrackWeight(
  [in] UINT  Track,
  [in] FLOAT Weight
);
```



## <a name="parameters"></a><span data-ttu-id="8e63c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8e63c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e63c-109">*Seguimiento* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="8e63c-109">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e63c-110">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8e63c-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8e63c-111">Identificador de la pista en la que se va a establecer el peso.</span><span class="sxs-lookup"><span data-stu-id="8e63c-111">Identifier of the track to set the weight on.</span></span>

</dd> <dt>

<span data-ttu-id="8e63c-112">*Peso* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="8e63c-112">*Weight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e63c-113">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8e63c-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8e63c-114">Valor de peso.</span><span class="sxs-lookup"><span data-stu-id="8e63c-114">Weight value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e63c-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8e63c-115">Return value</span></span>

<span data-ttu-id="8e63c-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8e63c-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8e63c-117">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8e63c-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="8e63c-118">Si se produce un error en el método, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="8e63c-118">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e63c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e63c-119">Requirements</span></span>



| <span data-ttu-id="8e63c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e63c-120">Requirement</span></span> | <span data-ttu-id="8e63c-121">Value</span><span class="sxs-lookup"><span data-stu-id="8e63c-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e63c-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8e63c-122">Header</span></span><br/>  | <dl> <span data-ttu-id="8e63c-123"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e63c-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="8e63c-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8e63c-124">Library</span></span><br/> | <dl> <span data-ttu-id="8e63c-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8e63c-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8e63c-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="8e63c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e63c-127">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="8e63c-127">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
