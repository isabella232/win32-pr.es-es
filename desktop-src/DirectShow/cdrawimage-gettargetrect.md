---
description: El método GetTargetRect recupera el rectángulo de destino actual.
ms.assetid: b6542b06-af36-4666-b6fa-d9fa3c6c7044
title: Método CDrawImage. GetTargetRect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.GetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 547dd12117cec95ad1cb0159667a8dd72a95a6e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679451"
---
# <a name="cdrawimagegettargetrect-method"></a>CDrawImage. GetTargetRect, método

El `GetTargetRect` método recupera el rectángulo de destino actual.

## <a name="syntax"></a>Sintaxis


```C++
void GetTargetRect(
   RECT *pTargetRect
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTargetRect* 
</dt> <dd>

Puntero a una estructura **Rect** que recibe el rectángulo de destino.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CDrawImage**](cdrawimage.md)
</dt> </dl>

 

 




