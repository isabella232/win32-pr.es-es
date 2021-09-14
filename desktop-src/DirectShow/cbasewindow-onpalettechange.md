---
description: El método OnPaletteChange controla los mensajes de cambio de paleta.
ms.assetid: 2abae4f1-fbd0-4a32-8772-012fa96b6d6c
title: Método CBaseWindow.OnPaletteChange (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnPaletteChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9abcb2d9f5cdc875f70f5c1db1fd2f625ce911f0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973919"
---
# <a name="cbasewindowonpalettechange-method"></a>Método CBaseWindow.OnPaletteChange

El `OnPaletteChange` método controla los mensajes de cambio de paleta.

## <a name="syntax"></a>Sintaxis


```C++
virtual LRESULT OnPaletteChange(
   HWND hwnd,
   UINT Message
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Hwnd* 
</dt> <dd>

Identificador de la ventana.

</dd> <dt>

*Mensaje* 
</dt> <dd>

Identificador del mensaje.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se procesó el mensaje o 1 si no se procesó el mensaje.

## <a name="remarks"></a>Observaciones

Este método controla los mensajes \_ WM PALETTECHANGED y WM \_ QUERYNEWPALETTE. Llama al [**método CBaseWindow::D oRealisePalette**](cbasewindow-dorealisepalette.md) para realizar la nueva paleta.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseWindow (clase)**](cbasewindow.md)
</dt> </dl>

 

 




