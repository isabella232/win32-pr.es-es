---
description: 'El método FindPin obtiene el pin con el identificador especificado. Este método implementa el método IBaseFilter:: FindPin.'
ms.assetid: 56ee3e0d-9e3f-4d25-846b-50119b55a122
title: Método CTransformFilter. FindPin (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1631651932d5adbc49fb59d44291dccea55fd41f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660621"
---
# <a name="ctransformfilterfindpin-method"></a>CTransformFilter. FindPin, método

El método **FindPin** obtiene el pin con el identificador especificado. Este método implementa el método [**IBaseFilter:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) .

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

Cadena de caracteres anchos que contiene el identificador del PIN.

</dd> <dt>

*ppPin* 
</dt> <dd>

Recibe un puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN. Si se produce un error en el método, `*ppPin` se establece en **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                       | Descripción                                           |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>              | Correcto.<br/>                                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>     | Memoria insuficiente.<br/>                       |
| <dl> <dt>**\_puntero E**</dt> </dl>         | Argumento de puntero **nulo** .<br/>                 |
| <dl> <dt>**VFW \_ E \_ no \_ encontrado**</dt> </dl> | No se encontró un pin con este identificador.<br/> |



 

## <a name="remarks"></a>Observaciones

> [!IMPORTANT]
> La implementación de este método no llama a [**IPin:: queryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) para que coincida con el identificador del PIN. En su lugar, el método supone que el PIN de entrada se denomina "in" y el PIN de salida se denomina "out". Si usa un conjunto de identificadores de PIN diferente, Invalide este método.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




