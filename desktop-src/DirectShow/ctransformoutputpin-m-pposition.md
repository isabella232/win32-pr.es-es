---
description: Objeto auxiliar para pasar comandos de búsqueda ascendentes.
ms.assetid: 2ca9bae7-a133-4e09-8aa7-1c4601ec5db0
title: 'Miembro CTransformOutputPin:: m_pPosition (Transfrm. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pPosition
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dc98e439d7f6a2d6c6392ffb665b04e502047eb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661004"
---
# <a name="ctransformoutputpinm_pposition-member"></a><span data-ttu-id="440e7-103">Miembro pPosition CTransformOutputPin:: m \_</span><span class="sxs-lookup"><span data-stu-id="440e7-103">CTransformOutputPin::m\_pPosition member</span></span>

<span data-ttu-id="440e7-104">Objeto auxiliar para pasar comandos de búsqueda ascendentes.</span><span class="sxs-lookup"><span data-stu-id="440e7-104">Helper object to pass seek commands upstream.</span></span>

## <a name="syntax"></a><span data-ttu-id="440e7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="440e7-105">Syntax</span></span>


```C++
IUnknown *m_pPosition;
```



## <a name="remarks"></a><span data-ttu-id="440e7-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="440e7-106">Remarks</span></span>

<span data-ttu-id="440e7-107">Cuando el PIN se consulta por primera vez para la interfaz [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) o [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) , crea y agrega un objeto auxiliar [**CPosPassThru**](cpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="440e7-107">When the pin is first queried for the [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) or [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface, it creates and aggregates a [**CPosPassThru**](cpospassthru.md) helper object.</span></span>

## <a name="requirements"></a><span data-ttu-id="440e7-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="440e7-108">Requirements</span></span>



| <span data-ttu-id="440e7-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="440e7-109">Requirement</span></span> | <span data-ttu-id="440e7-110">Value</span><span class="sxs-lookup"><span data-stu-id="440e7-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="440e7-111">Encabezado</span><span class="sxs-lookup"><span data-stu-id="440e7-111">Header</span></span><br/>  | <dl> <span data-ttu-id="440e7-112"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="440e7-112"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="440e7-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="440e7-113">Library</span></span><br/> | <dl> <span data-ttu-id="440e7-114"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="440e7-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




