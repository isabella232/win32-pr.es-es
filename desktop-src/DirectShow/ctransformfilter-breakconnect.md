---
description: El método BreakConnect libera un pin de una conexión.
ms.assetid: cc384786-9cba-4f68-9c60-740205b35661
title: Método CTransformFilter.BreakConnect (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3c4e77e28548c1f181cb5f8a6c106572d243314c5afd9d9126024e9b84fbe02a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053815"
---
# <a name="ctransformfilterbreakconnect-method"></a>Método CTransformFilter.BreakConnect

El `BreakConnect` método libera un pin de una conexión.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT BreakConnect(
   PIN_DIRECTION dir
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dir* 
</dt> <dd>

Miembro del tipo [**enumerado \_ DIRECCIÓN**](/windows/win32/api/strmif/ne-strmif-pin_direction) del PIN, especificando qué conexión de pin se ha roto (entrada o salida).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

Los [**métodos CTransformInputPin::BreakConnect**](ctransforminputpin-breakconnect.md) y [**CTransformOutputPin::BreakConnect**](ctransformoutputpin-breakconnect.md) llaman a este método cuando se rompe una conexión de pin. Este método no hace nada en la clase base. Si invalida el [**método CheckConnect,**](ctransformfilter-checkconnect.md) invalide este método para liberar los recursos obtenidos en el **método CheckConnect,** incluidos los punteros de interfaz.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CTransformFilter (clase)**](ctransformfilter.md)
</dt> </dl>

 

 




