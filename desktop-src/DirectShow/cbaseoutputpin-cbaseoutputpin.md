---
description: Método de constructor.
ms.assetid: 1105c951-a51d-49ab-a69d-f3d482d61233
title: Constructor CBaseOutputPin. CBaseOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.CBaseOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0461c5056ee48caa19f21d1fcb8fcf1636157d9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671512"
---
# <a name="cbaseoutputpincbaseoutputpin-constructor"></a>Constructor CBaseOutputPin. CBaseOutputPin

Método de constructor.

## <a name="syntax"></a>Sintaxis


```C++
CBaseOutputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pObjectName* 
</dt> <dd>

Cadena que contiene el nombre de depuración del objeto. Para obtener más información, vea [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*pFilter* 
</dt> <dd>

Puntero al filtro que creó este pin.

</dd> <dt>

*pLock* 
</dt> <dd>

Puntero a un bloqueo de [**CCritSec**](ccritsec.md) , que se usa para serializar los cambios de estado. Puede ser la misma sección crítica que el bloqueo de filtro, [**CBaseFilter:: m \_ Plock**](cbasefilter-m-plock.md).

</dd> <dt>

*phr* 
</dt> <dd>

Puntero a una variable que recibe un valor **HRESULT** que indica si el método se ha ejecutado correctamente o no.

</dd> <dt>

*pName* 
</dt> <dd>

Cadena de caracteres anchos que contiene el nombre del PIN (también se usa como identificador del PIN).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Todos los parámetros se pasan directamente al constructor [**CBasePin**](cbasepin.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




