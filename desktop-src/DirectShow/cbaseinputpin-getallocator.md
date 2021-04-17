---
description: 'El método GetAllocator recupera el asignador de memoria propuesto por este pin. Este método implementa el método IMemInputPin:: GetAllocator.'
ms.assetid: 07bc77f8-a877-4403-b424-20bda715a818
title: Método CBaseInputPin. GetAllocator (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.GetAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 098738fc63ba1834b1eefb4b2518e3309db35c43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660344"
---
# <a name="cbaseinputpingetallocator-method"></a>CBaseInputPin. GetAllocator, método

El `GetAllocator` método recupera el asignador de memoria propuesto por este pin. Este método implementa el método [**IMemInputPin:: GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetAllocator(
   IMemAllocator **ppAllocator
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppAllocator* 
</dt> <dd>

Dirección de una variable que recibe un puntero a la interfaz [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) del asignador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve \_ si es correcto, o un código de error de la función **CoCreateInstance** .

## <a name="remarks"></a>Observaciones

Este método crea un objeto [**CMemAllocator**](cmemallocator.md) . Invalide este método si el filtro usa un asignador de un PIN de nivel inferior o un asignador personalizado.

Si el método se ejecuta correctamente, la interfaz **IMemAllocator** tiene un recuento de referencias pendiente. Asegúrese de liberarlo cuando haya terminado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




