---
description: Valor booleano que indica si el filtro está quitando actualmente fotogramas. Si este valor es TRUE, el filtro sigue colocando fotogramas hasta que alcanza el siguiente fotograma clave o hasta que recibe 30 fotogramas Delta en una fila sin un fotograma clave.
ms.assetid: 1af22879-bf9b-4835-b3b5-06fb52b3140f
title: 'Miembro CVideoTransformFilter:: m_bSkipping (Vtrans. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bSkipping
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7beb4073052149e246a55ffbb1ff057e836704c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660928"
---
# <a name="cvideotransformfilterm_bskipping-member"></a><span data-ttu-id="d1d85-104">Miembro bSkipping CVideoTransformFilter:: m \_</span><span class="sxs-lookup"><span data-stu-id="d1d85-104">CVideoTransformFilter::m\_bSkipping member</span></span>

<span data-ttu-id="d1d85-105">Valor booleano que indica si el filtro está quitando actualmente fotogramas.</span><span class="sxs-lookup"><span data-stu-id="d1d85-105">Boolean value that indicates whether the filter is currently dropping frames.</span></span> <span data-ttu-id="d1d85-106">Si este valor es **true**, el filtro sigue colocando fotogramas hasta que alcanza el siguiente fotograma clave o hasta que recibe 30 fotogramas Delta en una fila sin un fotograma clave.</span><span class="sxs-lookup"><span data-stu-id="d1d85-106">If this value is **TRUE**, the filter continues to drop frames until it reaches the next key frame, or until it receives 30 delta frames in a row without a key frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1d85-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d1d85-107">Syntax</span></span>


```C++
BOOL m_bSkipping;
```



## <a name="requirements"></a><span data-ttu-id="d1d85-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1d85-108">Requirements</span></span>



| <span data-ttu-id="d1d85-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1d85-109">Requirement</span></span> | <span data-ttu-id="d1d85-110">Value</span><span class="sxs-lookup"><span data-stu-id="d1d85-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1d85-111">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d1d85-111">Header</span></span><br/>  | <dl> <span data-ttu-id="d1d85-112"><dt>Vtrans. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d1d85-112"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="d1d85-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d1d85-113">Library</span></span><br/> | <dl> <span data-ttu-id="d1d85-114"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="d1d85-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1d85-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1d85-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1d85-116">**Clase CVideoTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="d1d85-116">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




