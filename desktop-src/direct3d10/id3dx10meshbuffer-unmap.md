---
description: Desasignar un búfer.
ms.assetid: 47f125cd-5c0a-4814-93c5-f2f11ce33ea6
title: 'ID3DX10MeshBuffer:: desasignar método (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10MeshBuffer.Unmap
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0c3b382e0cfd01a51d89ddacb51ad390446315a6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698454"
---
# <a name="id3dx10meshbufferunmap-method"></a><span data-ttu-id="d0e21-103">ID3DX10MeshBuffer:: unwith (método)</span><span class="sxs-lookup"><span data-stu-id="d0e21-103">ID3DX10MeshBuffer::Unmap method</span></span>

<span data-ttu-id="d0e21-104">Desasignar un búfer.</span><span class="sxs-lookup"><span data-stu-id="d0e21-104">Unmap a buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0e21-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d0e21-105">Syntax</span></span>


```C++
HRESULT Unmap();
```



## <a name="parameters"></a><span data-ttu-id="d0e21-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d0e21-106">Parameters</span></span>

<span data-ttu-id="d0e21-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="d0e21-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d0e21-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d0e21-108">Return value</span></span>

<span data-ttu-id="d0e21-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d0e21-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d0e21-110">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="d0e21-110">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d0e21-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d0e21-111">Remarks</span></span>



|                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0e21-112">Diferencias entre Direct3D 9 y Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="d0e21-112">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="d0e21-113">Desasignar () en Direct3D 10 es análogo al desbloqueo de recursos () en Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="d0e21-113">Unmap() in Direct3D 10 is analogous to resource Unlock() in Direct3D 9.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d0e21-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0e21-114">Requirements</span></span>



| <span data-ttu-id="d0e21-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0e21-115">Requirement</span></span> | <span data-ttu-id="d0e21-116">Value</span><span class="sxs-lookup"><span data-stu-id="d0e21-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d0e21-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d0e21-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d0e21-118"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0e21-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="d0e21-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d0e21-119">Library</span></span><br/> | <dl> <span data-ttu-id="d0e21-120"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d0e21-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0e21-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0e21-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0e21-122">ID3DX10MeshBuffer</span><span class="sxs-lookup"><span data-stu-id="d0e21-122">ID3DX10MeshBuffer</span></span>](id3dx10meshbuffer.md)
</dt> <dt>

[<span data-ttu-id="d0e21-123">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="d0e21-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




