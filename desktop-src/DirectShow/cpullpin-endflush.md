---
description: El método EndFlush informa al filtro propietario de que finalice una operación de vaciado. La clase derivada debe implementar este método.
ms.assetid: 5b178b09-019c-4b5b-9794-5176b5402e1c
title: Método CPullPin. EndFlush (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9e58cb9a903f0841de2442216fab0e360007206b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671387"
---
# <a name="cpullpinendflush-method"></a>CPullPin. EndFlush, método

El `EndFlush` método informa al filtro propietario de que finalice una operación de vaciado. La clase derivada debe implementar este método.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT EndFlush() = 0;
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="remarks"></a>Observaciones

El método [**CPullPin:: Seek**](cpullpin-seek.md) llama a este método. Implemente este método para llamar al método [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) en cada pin de entrada de nivel inferior que reciba datos de este objeto. Si los anclajes de salida del filtro se derivan de **CBaseOutputPin**, llame al método **eliverendflush de CBaseOutputPin::D** .

Este diseño permite que el filtro busque el flujo simplemente mediante una llamada a **Seek** en el objeto **CPullPin** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CPullPin**](cpullpin.md)
</dt> </dl>

 

 




