---
description: El \_ método get BackgroundPalette recupera la paleta realizada en la marca de fondo.
ms.assetid: cc649dbd-d049-4993-b187-4e297bef5152
title: Método CBaseControlWindow.get_BackgroundPalette (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_BackgroundPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dd06bcec9b3c435370ec3f12340c1c3aede3904c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660259"
---
# <a name="cbasecontrolwindowget_backgroundpalette-method"></a>CBaseControlWindow. Get \_ BackgroundPalette (método)

El `get_BackgroundPalette` método recupera la paleta realizada en la marca de fondo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_BackgroundPalette(
   long *pBackgroundPalette
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pBackgroundPalette* 
</dt> <dd>

Puntero a una marca booleana de Automation (0 es OFF, 1 es ON).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="remarks"></a>Observaciones

Esta función miembro implementa el método [**IVideoWindow:: get \_ BackgroundPalette**](/windows/desktop/api/Control/nf-control-ivideowindow-get_backgroundpalette) . Si se va a reproducir un vídeo dentro de otra aplicación o documento, es posible que la aplicación desee usar su propia paleta. Puede solicitar que el vídeo use la paleta de primer plano actual en lugar de la suya propia estableciendo esta marca en 1. Si se establece en 0, la ventana instalará y obtendrá su propia paleta preferida. Tenga en cuenta que pedir a la ventana que use una paleta diferente producirá penalizaciones de rendimiento graves.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




