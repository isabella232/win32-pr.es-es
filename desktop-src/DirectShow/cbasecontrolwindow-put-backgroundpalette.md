---
description: El \_ método put BackgroundPalette establece una marca para obtener la paleta en segundo plano.
ms.assetid: db420e75-e300-41fa-bae4-fb267cc99c7c
title: Método CBaseControlWindow.put_BackgroundPalette (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_BackgroundPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 04aeb445be91426e7995ecd01c9326cda586a447
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660629"
---
# <a name="cbasecontrolwindowput_backgroundpalette-method"></a>CBaseControlWindow. put \_ BackgroundPalette (método)

El `put_BackgroundPalette` método establece una marca para obtener la paleta en segundo plano.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_BackgroundPalette(
   long BackgroundPalette
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*BackgroundPalette* 
</dt> <dd>

Marca booleana de Automation (0 está desactivado, 1 en).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="remarks"></a>Observaciones

Para reproducir un vídeo dentro de otra aplicación o documento, es posible que la aplicación desee usar su propia paleta. Puede solicitar que el vídeo use la paleta de primer plano actual en lugar de la suya propia como paleta de fondo; para ello, establezca esta marca en 1. Si se establece en 0, la ventana instalará y obtendrá su propia paleta preferida. Pedir a la ventana que use una paleta diferente producirá penalizaciones de rendimiento graves.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




