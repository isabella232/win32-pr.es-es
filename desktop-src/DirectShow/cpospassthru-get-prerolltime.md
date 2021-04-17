---
description: 'El \_ método get PrerollTime recupera la cantidad de datos que se pondrán en cola antes de la posición de inicio. Este método implementa el método IMediaPosition:: get \_ PrerollTime.'
ms.assetid: 37c12798-eb0d-4859-8b2e-52d6ae147863
title: Método CPosPassThru.get_PrerollTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_PrerollTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 55cb2cc37a18c9ea00b4eb7115590f472b8d467e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660551"
---
# <a name="cpospassthruget_prerolltime-method"></a>CPosPassThru. Get \_ PrerollTime (método)

El `get_PrerollTime` método recupera la cantidad de datos que se pondrán en cola antes de la posición de inicio. Este método implementa el método [**IMediaPosition:: get \_ PrerollTime**](/windows/desktop/api/Control/nf-control-imediaposition-get_prerolltime) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_PrerollTime(
   REFTIME *pllTime
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pllTime* 
</dt> <dd>

Puntero a una variable que recibe el tiempo de prelanzamiento, en segundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el valor **HRESULT** del PIN conectado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




