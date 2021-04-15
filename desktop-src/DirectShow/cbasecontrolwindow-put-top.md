---
description: El \_ método put Top establece la coordenada superior de la ventana.
ms.assetid: cd39807f-363d-4b5b-8279-9dfb992dca10
title: Método CBaseControlWindow.put_Top (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Top
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fdbce19c3caf4129b1f224a740b27209b855a1f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661346"
---
# <a name="cbasecontrolwindowput_top-method"></a>CBaseControlWindow. put \_ Top (método)

El `put_Top` método establece la coordenada superior de la ventana.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_Top(
   long Top
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Top* (Principales) 
</dt> <dd>

Nueva coordenada superior, en píxeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="remarks"></a>Observaciones

La ventana tiene una posición en el escritorio. Se expresa en píxeles por cuatro coordenadas (izquierda, superior, derecha e inferior). Las interfaces automatizadas por OLE suelen expresar esta posición a la izquierda, la parte superior, el ancho y el alto. Esta es la Convención usada en DirectShow. Todas las coordenadas se expresan en píxeles y, al cambiar cualquier coordenada, la ventana se actualizará inmediatamente.

Al establecer las coordenadas izquierda o superior, la ventana se mueve a la izquierda o hacia arriba, respectivamente; estas coordenadas no tienen ningún efecto en el ancho y el alto de la ventana. Del mismo modo, establecer el ancho y el alto no afecta a las coordenadas izquierda y superior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




