---
description: El método AlignUp redondea un valor hasta un límite de alineación especificado. Nota quitada en Windows 7. .
ms.assetid: fa2a6567-3eb1-4aa9-b966-2e88b15c67b1
title: Método CPullPin. AlignUp (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.AlignUp
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4f33ae2b7434d90d909315edda4d49e07d8adab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680277"
---
# <a name="cpullpinalignup-method"></a>CPullPin. AlignUp, método

El método **AlignUp** redondea un valor hasta un límite de alineación especificado.

> [!Note]  
> Se quitó en Windows 7.

 

## <a name="syntax"></a>Sintaxis


```C++
LONGLONG AlignUp(
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

## <a name="remarks"></a>Observaciones

> [!Caution]  
> Este método puede producir un desbordamiento numérico si se desbordan *ll* + (*lAlign* -1).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CPullPin**](cpullpin.md)
</dt> </dl>

 

 




