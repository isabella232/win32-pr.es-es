---
description: El método PaintWindow hace que se vuelva a dibujar la ventana.
ms.assetid: dce3d782-00e5-4176-9365-378d59d48ebc
title: Método CBaseWindow. PaintWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PaintWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3b0932422f85cb31d587485976dfacbaa51e2bf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661233"
---
# <a name="cbasewindowpaintwindow-method"></a>CBaseWindow. PaintWindow, método

El `PaintWindow` método hace que se vuelva a dibujar la ventana.

## <a name="syntax"></a>Sintaxis


```C++
void PaintWindow(
   BOOL bErase
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bErase* 
</dt> <dd>

Valor booleano que especifica si se borra el fondo. Si el valor es **true**, se borra el fondo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método genera un mensaje de dibujo de WM \_ invalidando el área de cliente completa de la ventana.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




