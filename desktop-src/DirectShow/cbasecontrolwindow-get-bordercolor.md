---
description: El método get \_ BorderColor recupera el color del borde actual.
ms.assetid: 4b4cae1d-bef7-4f8d-8011-c220fcfb73eb
title: CBaseControlWindow.get_BorderColor método (Ctlutil.h)
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
ms.openlocfilehash: a351e794765f3dddb5275d8a588ca54ade06bb789ed720bfb17997fc11e358f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660759"
---
# <a name="cbasecontrolwindowget_bordercolor-method"></a>CBaseControlWindow.get \_ BorderColor (método)

El `get_BorderColor` método recupera el color del borde actual.

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

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Observaciones

Una aplicación puede establecer un rectángulo de destino en el que se debe mostrar el vídeo. Este rectángulo es relativo al área de cliente de la ventana. Si esto se hace (el valor predeterminado es pintar siempre toda la ventana), hay un borde que rodea el vídeo. Esta propiedad afecta al color utilizado por el borde. Aunque el parámetro se especifica como **un tipo LONG,** en realidad es un **valor COLORREF.**

Esta función miembro está pensada para que la llamen objetos externos a través de la interfaz [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) y, por tanto, bloquea la sección crítica para sincronizarse con el filtro asociado. Llame a [**la función miembro CBaseControlWindow::GetBorderColour**](cbasecontrolwindow-getbordercolour.md) para recuperar esta propiedad si no llama a desde un objeto externo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlWindow (clase)**](cbasecontrolwindow.md)
</dt> </dl>

 

 




