---
description: El método PaintWindow hace que se vuelva a dibujar la ventana.
ms.assetid: dce3d782-00e5-4176-9365-378d59d48ebc
title: Método CBaseWindow.PaintWindow (Winutil.h)
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
ms.openlocfilehash: 7cc998f270947890327fb3cbacce4a29183604047824b05b8a66538c163bdc08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635125"
---
# <a name="cbasewindowpaintwindow-method"></a>Método CBaseWindow.PaintWindow

El método hace que se vuelva a `PaintWindow` dibujar la ventana.

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

Valor booleano que especifica si se borra el fondo. Si el valor es **TRUE,** se borra el fondo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este método genera un mensaje WM PAINT invalidando el \_ área de cliente completa de la ventana.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseWindow (clase)**](cbasewindow.md)
</dt> </dl>

 

 




