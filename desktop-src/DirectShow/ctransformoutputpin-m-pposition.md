---
description: 'CTransformOutputPin::m_pPosition miembro: objeto auxiliar para pasar comandos seek ascendentes.'
ms.assetid: 2ca9bae7-a133-4e09-8aa7-1c4601ec5db0
title: CTransformOutputPin::m_pPosition miembro (Transfrm.h)
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
ms.openlocfilehash: b9c5a1b5d5ced7a9f3985ceebdd2bdcb8e491d2e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084863"
---
# <a name="ctransformoutputpinm_pposition-member"></a><span data-ttu-id="a73ac-103">Miembro CTransformOutputPin::m \_ pPosition</span><span class="sxs-lookup"><span data-stu-id="a73ac-103">CTransformOutputPin::m\_pPosition member</span></span>

<span data-ttu-id="a73ac-104">Objeto auxiliar para pasar comandos seek ascendentes.</span><span class="sxs-lookup"><span data-stu-id="a73ac-104">Helper object to pass seek commands upstream.</span></span>

## <a name="syntax"></a><span data-ttu-id="a73ac-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a73ac-105">Syntax</span></span>


```C++
IUnknown *m_pPosition;
```



## <a name="remarks"></a><span data-ttu-id="a73ac-106">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a73ac-106">Remarks</span></span>

<span data-ttu-id="a73ac-107">Cuando el pin se consulta por primera vez para la interfaz [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) o [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) crea y agrega un objeto auxiliar [**CPosPassThru.**](cpospassthru.md)</span><span class="sxs-lookup"><span data-stu-id="a73ac-107">When the pin is first queried for the [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) or [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface, it creates and aggregates a [**CPosPassThru**](cpospassthru.md) helper object.</span></span>

## <a name="requirements"></a><span data-ttu-id="a73ac-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a73ac-108">Requirements</span></span>



| <span data-ttu-id="a73ac-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="a73ac-109">Requirement</span></span> | <span data-ttu-id="a73ac-110">Value</span><span class="sxs-lookup"><span data-stu-id="a73ac-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a73ac-111">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a73ac-111">Header</span></span><br/>  | <dl> <span data-ttu-id="a73ac-112"><dt>Transfrm.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="a73ac-112"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a73ac-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a73ac-113">Library</span></span><br/> | <dl> <span data-ttu-id="a73ac-114"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a73ac-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




