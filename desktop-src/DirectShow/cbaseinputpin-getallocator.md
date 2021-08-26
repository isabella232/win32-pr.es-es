---
description: 'Método CBaseInputPin.GetAllocator: el método GetAllocator recupera el asignador de memoria propuesto por este pin. Este método implementa el método IMemInputPin::GetAllocator.'
ms.assetid: 07bc77f8-a877-4403-b424-20bda715a818
title: Método CBaseInputPin.GetAllocator (Amfilter.h)
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
ms.openlocfilehash: 119f3ffaa5863584b55210306b38b011c758f9bab0febac47547bdfe469b5ac0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056345"
---
# <a name="cbaseinputpingetallocator-method"></a>CBaseInputPin.GetAllocator (método)

El `GetAllocator` método recupera el asignador de memoria propuesto por este pin. Este método implementa el [**método IMemInputPin::GetAllocator.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator)

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

Dirección de una variable que recibe un puntero a la interfaz [**IMemAllocator del**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) asignador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se realiza correctamente o un código de error de la función **CoCreateInstance.**

## <a name="remarks"></a>Comentarios

Este método crea un [**objeto CMemAllocator.**](cmemallocator.md) Invalide este método si el filtro usa un asignador de un pin de nivel inferior o un asignador personalizado.

Si el método se realiza correctamente, la **interfaz IMemAllocator** tiene un recuento de referencias pendiente. Asegúrese de liberarlo cuando haya terminado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseInputPin (clase)**](cbaseinputpin.md)
</dt> </dl>

 

 




