---
description: 'El método FindPin recupera el pin con el identificador especificado. Este método implementa el método IBaseFilter:: FindPin.'
ms.assetid: ad593dbf-ca56-4409-ac6e-1b88908c8cee
title: CSource. FindPin (método) (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9fac8df1e53e4a129b42d1284a19392bc7b58aa2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670399"
---
# <a name="csourcefindpin-method"></a>CSource. FindPin, método

El `FindPin` método recupera el pin con el identificador especificado. Este método implementa el método [**IBaseFilter:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Id* 
</dt> <dd>

Puntero a una cadena terminada en null que identifica el PIN.

</dd> <dt>

*ppPin* 
</dt> <dd>

Recibe un puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN. Si se produce un error en el método, \* *ppPin* se establece en **null** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                       | Descripción                                           |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>              | Correcto.<br/>                                   |
| <dl> <dt>**\_puntero E**</dt> </dl>         | Argumento de puntero **nulo** .<br/>                 |
| <dl> <dt>**VFW \_ E \_ no \_ encontrado**</dt> </dl> | No se encontró un pin con este identificador.<br/> |



 

## <a name="remarks"></a>Observaciones

El primer PIN siempre se denomina "1"; el segundo PIN se denomina "2"; etc. Para obtener más información, vea [**CSourceStream:: queryId**](csourcestream-queryid.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CSource**](csource.md)
</dt> </dl>

 

 




