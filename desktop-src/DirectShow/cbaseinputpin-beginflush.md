---
description: 'El método CBaseInputPin inicia una operación de vaciado. Este método implementa el método IPin:: BeginFlush.'
ms.assetid: 3f149d4f-765b-44c1-87e5-6313f6a4d50d
title: Método CBaseInputPin. BeginFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 93c0f687daf65e91443f4f59896d641b9b0cfd43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660573"
---
# <a name="cbaseinputpinbeginflush-method"></a>CBaseInputPin. BeginFlush, método

El `CBaseInputPin` método inicia una operación de vaciado. Este método implementa el método [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT BeginFlush();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

Este método establece la marca [**CBaseInputPin:: m \_ BFlushing**](cbaseinputpin-m-bflushing.md) en **true**, lo que hace que el método [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) rechace cualquier ejemplo más.

La clase derivada debe invalidar este método y realizar los pasos siguientes:

1.  Llame al método [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) en las clavijas de entrada de nivel inferior. Si el PIN no ha entregado todavía ningún ejemplo de multimedia en el nivel inferior, puede omitir este paso. Si los pin de salida derivan de la clase [**CBaseOutputPin**](cbaseoutputpin.md) , puede llamar al método [**eliverbeginflush de CBaseOutputPin::D**](cbaseoutputpin-deliverbeginflush.md) .
2.  Llame al método de la clase base.
3.  Empezar a descartar los datos en cola.
4.  Devuelve de cualquier llamada bloqueada al método **Receive** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




