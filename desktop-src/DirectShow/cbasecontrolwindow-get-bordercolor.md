---
description: El \_ método get BorderColor recupera el color del borde actual.
ms.assetid: 4b4cae1d-bef7-4f8d-8011-c220fcfb73eb
title: Método CBaseControlWindow.get_BorderColor (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_BorderColor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d889f211b204c2c0180ae757a0240c8588552e83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670541"
---
# <a name="cbasecontrolwindowget_bordercolor-method"></a>CBaseControlWindow. Get \_ BorderColor (método)

El `get_BorderColor` método recupera el color actual del borde.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_BorderColor(
   long *Color
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Color* 
</dt> <dd>

Puntero al color del borde actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="remarks"></a>Observaciones

Una aplicación puede establecer un rectángulo de destino en el que se debe mostrar el vídeo. Este rectángulo es relativo al área cliente de la ventana. Si esto se hace (el valor predeterminado es pintar siempre toda la ventana), hay un borde que rodea el vídeo. Esta propiedad afecta al color utilizado por el borde. Aunque el parámetro se especifica como un tipo **Long** , en realidad es un valor de **COLORREF** .

Esta función miembro está pensada para que la llamen los objetos externos a través de la interfaz [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) y, por tanto, bloquea la sección crítica para sincronizar con el filtro asociado. Llame a la función miembro [**CBaseControlWindow:: GetBorderColour**](cbasecontrolwindow-getbordercolour.md) para recuperar esta propiedad si no llama a desde un objeto externo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




