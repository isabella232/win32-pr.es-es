---
description: Método de constructor.
ms.assetid: 35c9ac07-8756-42b1-beeb-5f0e79466742
title: Constructor CAMEvent. CAMEvent (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.CAMEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a01d9d1f592675f58d19e81b800c966dddaca1c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660162"
---
# <a name="cameventcamevent-constructor"></a>Constructor CAMEvent. CAMEvent

Método de constructor.

## <a name="syntax"></a>Sintaxis


```C++
CAMEvent(
   BOOL    fManualReset,
   HRESULT *phr
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fManualReset* 
</dt> <dd>

Valor booleano que especifica si el objeto es un evento de restablecimiento manual o un evento de restablecimiento automático. Si es **true**, el objeto es un evento de restablecimiento manual. De lo contrario, es un evento de restablecimiento automático.

</dd> <dt>

*phr* 
</dt> <dd>

Puntero a un valor **HRESULT** . Si se produce un error en el constructor, este parámetro recibe un código de error. Si esto ocurre, el objeto no tiene un estado válido.

Para mantener la compatibilidad con versiones anteriores de strmbase. lib, este parámetro tiene como valor predeterminado **null**. Sin embargo, se prefiere pasar un valor distinto de **null** para que el autor de la llamada pueda comprobar el estado del objeto.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El evento comienza en un estado no señalado.

Con un evento de restablecimiento automático, el método [**CAMEvent:: wait**](camevent-wait.md) restablece el evento a no señalizado cuando el método devuelve. Con un evento de restablecimiento manual, el evento permanece señalado hasta que se llama al método [**CAMEvent:: RESET**](camevent-reset.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CAMEvent**](camevent.md)
</dt> </dl>

 

 




