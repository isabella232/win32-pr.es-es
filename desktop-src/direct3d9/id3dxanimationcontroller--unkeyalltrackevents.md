---
description: Quita todos los eventos de una pista de animación especificada.
ms.assetid: 25c4d04a-0d75-4113-ad90-db84aa937098
title: 'ID3DXAnimationController:: UnkeyAllTrackEvents (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.UnkeyAllTrackEvents
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5904e9e09c8a821cdc532f9046217ae64bbf3de5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718530"
---
# <a name="id3dxanimationcontrollerunkeyalltrackevents-method"></a><span data-ttu-id="ca20b-103">ID3DXAnimationController:: UnkeyAllTrackEvents (método)</span><span class="sxs-lookup"><span data-stu-id="ca20b-103">ID3DXAnimationController::UnkeyAllTrackEvents method</span></span>

<span data-ttu-id="ca20b-104">Quita todos los eventos de una pista de animación especificada.</span><span class="sxs-lookup"><span data-stu-id="ca20b-104">Removes all events from a specified animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca20b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ca20b-105">Syntax</span></span>


```C++
HRESULT UnkeyAllTrackEvents(
  [in] UINT Track
);
```



## <a name="parameters"></a><span data-ttu-id="ca20b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ca20b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca20b-107">*Seguimiento* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ca20b-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca20b-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ca20b-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ca20b-109">Identificador de la pista en la que se deben quitar todos los eventos.</span><span class="sxs-lookup"><span data-stu-id="ca20b-109">Identifier of the track on which all events should be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca20b-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ca20b-110">Return value</span></span>

<span data-ttu-id="ca20b-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ca20b-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ca20b-112">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ca20b-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ca20b-113">Si se produce un error en el método, se devolverá el valor siguiente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="ca20b-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca20b-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ca20b-114">Remarks</span></span>

<span data-ttu-id="ca20b-115">Este método evita la ejecución de todos los eventos programados previamente en la pista y descarta todos los datos asociados a esos eventos.</span><span class="sxs-lookup"><span data-stu-id="ca20b-115">This method prevents the execution of all events previously scheduled on the track, and discards all data associated with those events.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca20b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca20b-116">Requirements</span></span>



| <span data-ttu-id="ca20b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca20b-117">Requirement</span></span> | <span data-ttu-id="ca20b-118">Value</span><span class="sxs-lookup"><span data-stu-id="ca20b-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca20b-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ca20b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="ca20b-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca20b-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="ca20b-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ca20b-121">Library</span></span><br/> | <dl> <span data-ttu-id="ca20b-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ca20b-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ca20b-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="ca20b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca20b-124">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="ca20b-124">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
