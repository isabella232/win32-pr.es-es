---
description: El método AlignUp redondea un valor hasta un límite de alineación especificado. Nota Quitado en Windows 7. .
ms.assetid: fa2a6567-3eb1-4aa9-b966-2e88b15c67b1
title: Método CPullPin.AlignUp (Pullpin.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063330"
---
# <a name="cpullpinalignup-method"></a>Método CPullPin.AlignUp

El **método AlignUp** redondea un valor hasta un límite de alineación especificado.

> [!Note]  
> Se ha quitado Windows 7.

 

## <a name="syntax"></a>Sintaxis


```C++
LONGLONG AlignUp(
   LONGLONG ll,
   LONG     lAlign
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Ll* 
</dt> <dd>

Especifica el número que se debe alinear.

</dd> <dt>

*lAlign* 
</dt> <dd>

Especifica el límite de alineación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el resultado alineado.

## <a name="remarks"></a>Observaciones

> [!Caution]  
> Este método puede provocar un desbordamiento numérico *si ll* + (*lAlign* - 1) se desborda.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CPullPin (clase)**](cpullpin.md)
</dt> </dl>

 

 




