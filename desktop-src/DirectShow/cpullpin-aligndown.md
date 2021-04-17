---
description: El método AlignDown trunca un valor en un límite de alineación especificado.
ms.assetid: f0efdedb-67ec-49d6-92a8-54485aa04e15
title: Método CPullPin. AlignDown (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.AlignDown
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1383517f4931fa153fd141878475cc8775a61045
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680278"
---
# <a name="cpullpinaligndown-method"></a>CPullPin. AlignDown, método

El `AlignDown` método trunca un valor en un límite de alineación especificado.

## <a name="syntax"></a>Sintaxis


```C++
LONGLONG AlignDown(
   LONGLONG ll,
   LONG     lAlign
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ll* 
</dt> <dd>

Especifica el número que se va a alinear.

</dd> <dt>

*lAlign* 
</dt> <dd>

Especifica el límite de alineación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el resultado alineado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CPullPin**](cpullpin.md)
</dt> </dl>

 

 




