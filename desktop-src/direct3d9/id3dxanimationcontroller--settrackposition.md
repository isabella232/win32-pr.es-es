---
description: Establece la pista en la hora de animación local especificada.
ms.assetid: 2ce87b06-1196-415f-958c-7bd407d6c69c
title: 'ID3DXAnimationController:: SetTrackPosition (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackPosition
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 95c408a43df3047a52d93da0cca3d9b17053d320
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718406"
---
# <a name="id3dxanimationcontrollersettrackposition-method"></a><span data-ttu-id="687c8-103">ID3DXAnimationController:: SetTrackPosition (método)</span><span class="sxs-lookup"><span data-stu-id="687c8-103">ID3DXAnimationController::SetTrackPosition method</span></span>

<span data-ttu-id="687c8-104">Establece la pista en la hora de animación local especificada.</span><span class="sxs-lookup"><span data-stu-id="687c8-104">Sets the track to the specified local animation time.</span></span>

## <a name="syntax"></a><span data-ttu-id="687c8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="687c8-105">Syntax</span></span>


```C++
HRESULT SetTrackPosition(
  [in] UINT   Track,
  [in] DOUBLE Position
);
```



## <a name="parameters"></a><span data-ttu-id="687c8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="687c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="687c8-107">*Seguimiento* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="687c8-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="687c8-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="687c8-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="687c8-109">Identificador de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="687c8-109">Track identifier.</span></span>

</dd> <dt>

<span data-ttu-id="687c8-110">*Posición* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="687c8-110">*Position* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="687c8-111">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="687c8-111">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="687c8-112">Valor de tiempo de animación local que se va a asignar a la pista.</span><span class="sxs-lookup"><span data-stu-id="687c8-112">Local animation time value to assign to the track.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="687c8-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="687c8-113">Return value</span></span>

<span data-ttu-id="687c8-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="687c8-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="687c8-115">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="687c8-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="687c8-116">Si se produce un error en el método, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="687c8-116">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="687c8-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="687c8-117">Requirements</span></span>



| <span data-ttu-id="687c8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="687c8-118">Requirement</span></span> | <span data-ttu-id="687c8-119">Value</span><span class="sxs-lookup"><span data-stu-id="687c8-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="687c8-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="687c8-120">Header</span></span><br/>  | <dl> <span data-ttu-id="687c8-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="687c8-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="687c8-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="687c8-122">Library</span></span><br/> | <dl> <span data-ttu-id="687c8-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="687c8-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="687c8-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="687c8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="687c8-125">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="687c8-125">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
