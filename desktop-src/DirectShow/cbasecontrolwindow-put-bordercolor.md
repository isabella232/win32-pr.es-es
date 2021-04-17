---
description: El \_ método debordercolor de put cambia el color del borde.
ms.assetid: bb19d338-7fd1-448c-be94-1c71d4a9a330
title: Método CBaseControlWindow.put_BorderColor (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_BorderColor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54db6de704f2ee0fde1a5087e83df4b362a57959
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660628"
---
# <a name="cbasecontrolwindowput_bordercolor-method"></a>Método BorderColor CBaseControlWindow. put \_

El `put_BorderColor` método cambia el color del borde.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_BorderColor(
   long Color
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Color* 
</dt> <dd>

Nuevo color del borde.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="remarks"></a>Observaciones

Una aplicación puede establecer un rectángulo de destino en el que se debe mostrar el vídeo. Este rectángulo es relativo al área cliente de la ventana. Si esto se hace (el valor predeterminado es pintar siempre toda la ventana), hay un borde que rodea el vídeo. Esta propiedad afecta al color utilizado por el borde. Aunque el parámetro se especifica como un tipo **Long** , en realidad es un valor de **COLORREF** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




