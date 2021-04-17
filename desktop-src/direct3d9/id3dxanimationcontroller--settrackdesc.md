---
description: Establece la descripción de la pista.
ms.assetid: bc3324b3-ca23-4035-958d-9763a70071f2
title: 'ID3DXAnimationController:: SetTrackDesc (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1aca9385f1e9bc9439b9fe4b3dc1acddda94e395
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718408"
---
# <a name="id3dxanimationcontrollersettrackdesc-method"></a><span data-ttu-id="36292-103">ID3DXAnimationController:: SetTrackDesc (método)</span><span class="sxs-lookup"><span data-stu-id="36292-103">ID3DXAnimationController::SetTrackDesc method</span></span>

<span data-ttu-id="36292-104">Establece la descripción de la pista.</span><span class="sxs-lookup"><span data-stu-id="36292-104">Sets the track description.</span></span>

## <a name="syntax"></a><span data-ttu-id="36292-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="36292-105">Syntax</span></span>


```C++
HRESULT SetTrackDesc(
  [in] UINT             Track,
  [in] LPD3DXTRACK_DESC pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="36292-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="36292-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36292-107">*Seguimiento* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="36292-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36292-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="36292-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="36292-109">Identificador de la pista que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="36292-109">Identifier of the track to modify.</span></span>

</dd> <dt>

<span data-ttu-id="36292-110">*pDesc* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="36292-110">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36292-111">Tipo: **[ **LPD3DXTRACK \_ DESC**](d3dxtrack-desc.md)**</span><span class="sxs-lookup"><span data-stu-id="36292-111">Type: **[**LPD3DXTRACK\_DESC**](d3dxtrack-desc.md)**</span></span>

<span data-ttu-id="36292-112">Descripción de la pista.</span><span class="sxs-lookup"><span data-stu-id="36292-112">Description of the track.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36292-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="36292-113">Return value</span></span>

<span data-ttu-id="36292-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="36292-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="36292-115">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="36292-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="36292-116">Si se produce un error en el método, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="36292-116">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="36292-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36292-117">Requirements</span></span>



| <span data-ttu-id="36292-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="36292-118">Requirement</span></span> | <span data-ttu-id="36292-119">Value</span><span class="sxs-lookup"><span data-stu-id="36292-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="36292-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="36292-120">Header</span></span><br/>  | <dl> <span data-ttu-id="36292-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="36292-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="36292-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="36292-122">Library</span></span><br/> | <dl> <span data-ttu-id="36292-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="36292-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="36292-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="36292-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36292-125">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="36292-125">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
