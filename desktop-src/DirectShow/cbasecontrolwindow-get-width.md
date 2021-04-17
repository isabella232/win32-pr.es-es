---
description: El \_ método get width recupera el ancho de la ventana actual.
ms.assetid: 8c5fbb0b-da80-4cfe-9c52-8ed4d9e52888
title: Método CBaseControlWindow.get_Width (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Width
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 56e863b8add52e1b98714e13466a48e3d0d52bba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661204"
---
# <a name="cbasecontrolwindowget_width-method"></a>CBaseControlWindow. Get \_ width (método)

El `get_Width` método recupera el ancho de la ventana actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Width(
   long *pWidth
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pWidth* 
</dt> <dd>

Puntero en el ancho de la ventana, en píxeles.

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

 

 




