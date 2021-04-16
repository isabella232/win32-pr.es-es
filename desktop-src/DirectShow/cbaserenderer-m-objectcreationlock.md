---
description: Bloqueo para proteger la creación de objetos dentro del filtro.
ms.assetid: ad1d2584-0d9e-42a8-83ea-0c1907ddcf33
title: 'Miembro CBaseRenderer:: m_ObjectCreationLock (Renbase. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_ObjectCreationLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e344b20b4924ac26ebe6253f5388136b350abefe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671523"
---
# <a name="cbaserendererm_objectcreationlock-member"></a><span data-ttu-id="67c2d-103">Miembro ObjectCreationLock CBaseRenderer:: m \_</span><span class="sxs-lookup"><span data-stu-id="67c2d-103">CBaseRenderer::m\_ObjectCreationLock member</span></span>

<span data-ttu-id="67c2d-104">Bloqueo para proteger la creación de objetos dentro del filtro.</span><span class="sxs-lookup"><span data-stu-id="67c2d-104">Lock to protect the creation of objects inside the filter.</span></span> <span data-ttu-id="67c2d-105">El filtro contiene este bloqueo cuando crea el PIN de entrada ([**CBaseRenderer:: m \_ pInputPin**](cbaserenderer-m-pinputpin.md)) o el objeto [**CRendererPosPassThru**](crendererpospassthru.md) ([**CBaseRenderer:: m \_ pPosition**](cbaserenderer-m-pposition.md)).</span><span class="sxs-lookup"><span data-stu-id="67c2d-105">The filter holds this lock when it creates the input pin ([**CBaseRenderer::m\_pInputPin**](cbaserenderer-m-pinputpin.md)) or the [**CRendererPosPassThru**](crendererpospassthru.md) object ([**CBaseRenderer::m\_pPosition**](cbaserenderer-m-pposition.md)).</span></span> <span data-ttu-id="67c2d-106">Este bloqueo impide que varios subprocesos intenten crear uno de estos objetos al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="67c2d-106">This lock prevents multiple threads from attempting to create one of these objects at the same time.</span></span>

## <a name="syntax"></a><span data-ttu-id="67c2d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="67c2d-107">Syntax</span></span>


```C++
CCritSec m_ObjectCreationLock;
```



## <a name="requirements"></a><span data-ttu-id="67c2d-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67c2d-108">Requirements</span></span>



| <span data-ttu-id="67c2d-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="67c2d-109">Requirement</span></span> | <span data-ttu-id="67c2d-110">Value</span><span class="sxs-lookup"><span data-stu-id="67c2d-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67c2d-111">Encabezado</span><span class="sxs-lookup"><span data-stu-id="67c2d-111">Header</span></span><br/>  | <dl> <span data-ttu-id="67c2d-112"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="67c2d-112"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="67c2d-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="67c2d-113">Library</span></span><br/> | <dl> <span data-ttu-id="67c2d-114"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="67c2d-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67c2d-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="67c2d-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67c2d-116">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="67c2d-116">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




