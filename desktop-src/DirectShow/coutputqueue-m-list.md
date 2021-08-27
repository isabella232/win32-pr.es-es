---
description: Cola de ejemplo multimedia.
ms.assetid: 910f1c0c-2ce9-452f-a97b-aa424da9a93e
title: COutputQueue::m_List miembro (Outputq.h)
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
ms.openlocfilehash: 3e261116961f23c845ec2e27c6f20748b2c50cd9c036d9bc7d42bfe24b9b4fb9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087075"
---
# <a name="coutputqueuem_list-member"></a>Miembro de lista COutputQueue::m \_

Cola de ejemplo multimedia.

## <a name="syntax"></a>Sintaxis


```C++
CSampleList *m_List;
```



## <a name="remarks"></a>Comentarios

Esta variable miembro es un puntero a [**un objeto CGenericList**](cgenericlist.md) que contiene [**punteros IMediaSample.**](/windows/desktop/api/Strmif/nn-strmif-imediasample) El **tipo CSampleList** se define de la siguiente manera:

``` syntax
typedef CGenericList<IMediaSample> CSampleList;
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Outputq.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**COutputQueue (clase)**](coutputqueue.md)
</dt> </dl>

 

 




