---
description: Cola de ejemplo multimedia.
ms.assetid: 910f1c0c-2ce9-452f-a97b-aa424da9a93e
title: 'Miembro COutputQueue:: m_List (Outputq. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_List
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 32840ed0ed9f976cceb1e0dc6dc8debc3f774377
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680221"
---
# <a name="coutputqueuem_list-member"></a>Miembro de la lista COutputQueue:: m \_

Cola de ejemplo multimedia.

## <a name="syntax"></a>Sintaxis


```C++
CSampleList *m_List;
```



## <a name="remarks"></a>Observaciones

Esta variable miembro es un puntero a un objeto [**CGenericList**](cgenericlist.md) que contiene punteros [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) . El tipo **CSampleList** se define de la siguiente manera:

``` syntax
typedef CGenericList<IMediaSample> CSampleList;
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Outputq. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




