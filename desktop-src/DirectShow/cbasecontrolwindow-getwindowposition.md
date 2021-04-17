---
description: El método GetWindowPosition recupera las coordenadas actuales para la ventana.
ms.assetid: a2f46a87-b2cd-450f-8d2b-0f8695432fda
title: Método CBaseControlWindow. GetWindowPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetWindowPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: af2b1bdb8b2c839644e8c0629e3e272c123d3c21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660594"
---
# <a name="cbasecontrolwindowgetwindowposition-method"></a>CBaseControlWindow. GetWindowPosition, método

El `GetWindowPosition` método recupera las coordenadas actuales para la ventana.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetWindowPosition(
   long *pLeft,
   long *pTop,
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pLeft* 
</dt> <dd>

Puntero a la coordenada izquierda, en coordenadas de pantalla.

</dd> <dt>

*pTop* 
</dt> <dd>

Puntero en la coordenada superior, en coordenadas de la pantalla.

</dd> <dt>

*pWidth* 
</dt> <dd>

Puntero en el ancho de la ventana, en coordenadas de la pantalla.

</dd> <dt>

*pHeight* 
</dt> <dd>

Puntero al alto de la ventana, en coordenadas de la pantalla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




