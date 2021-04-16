---
description: Número máximo actual de fotogramas Delta que se van a quitar.
ms.assetid: d14c594e-55ab-42c2-bdb0-6829f71d02dd
title: 'Miembro CVideoTransformFilter:: m_nWaitForKey (Vtrans. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_nWaitForKey
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a168a26816825c33c0e047d93cc8b14ebd0f3536
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678944"
---
# <a name="cvideotransformfilterm_nwaitforkey-member"></a><span data-ttu-id="cf6b7-103">Miembro nWaitForKey CVideoTransformFilter:: m \_</span><span class="sxs-lookup"><span data-stu-id="cf6b7-103">CVideoTransformFilter::m\_nWaitForKey member</span></span>

<span data-ttu-id="cf6b7-104">Número máximo actual de fotogramas Delta que se van a quitar.</span><span class="sxs-lookup"><span data-stu-id="cf6b7-104">The current maximum number of delta frames to drop.</span></span> <span data-ttu-id="cf6b7-105">Aunque esta variable es mayor que cero, el filtro quitará los fotogramas hasta que llegue a un fotograma clave.</span><span class="sxs-lookup"><span data-stu-id="cf6b7-105">While this variable is greater than zero, the filter will drop frames until it reaches a key frame.</span></span> <span data-ttu-id="cf6b7-106">Para cada fotograma que se quita, el filtro reduce esta variable en uno, lo que impide que el filtro Quite un número excesivo de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="cf6b7-106">For each frame that is dropped, the filter decrements this variable by one, which prevents the filter from dropping an excessive number of frames.</span></span> <span data-ttu-id="cf6b7-107">Después de 30 fotogramas Delta en una fila sin fotogramas clave, el filtro comenzará a entregar fotogramas de nuevo.</span><span class="sxs-lookup"><span data-stu-id="cf6b7-107">After 30 delta frames in a row with no key frames, the filter will start delivering frames again.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf6b7-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cf6b7-108">Syntax</span></span>


```C++
int m_nWaitForKey;
```



## <a name="requirements"></a><span data-ttu-id="cf6b7-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf6b7-109">Requirements</span></span>



| <span data-ttu-id="cf6b7-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf6b7-110">Requirement</span></span> | <span data-ttu-id="cf6b7-111">Value</span><span class="sxs-lookup"><span data-stu-id="cf6b7-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf6b7-112">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cf6b7-112">Header</span></span><br/>  | <dl> <span data-ttu-id="cf6b7-113"><dt>Vtrans. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cf6b7-113"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="cf6b7-114">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cf6b7-114">Library</span></span><br/> | <dl> <span data-ttu-id="cf6b7-115"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="cf6b7-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf6b7-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="cf6b7-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf6b7-117">**Clase CVideoTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="cf6b7-117">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




