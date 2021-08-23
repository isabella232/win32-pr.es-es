---
description: El método PossiblyEatMessage permite que una clase derivada reenvía mensajes a otra ventana.
ms.assetid: d8775182-44ed-4df2-b4b8-1fdf289e2c1a
title: Método CBaseWindow.PossiblyEatMessage (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PossiblyEatMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 851f46d14f949a49c9422256f9b2bda1ba314e5789773121387e89c011f7a424
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016463"
---
# <a name="cbasewindowpossiblyeatmessage-method"></a>CBaseWindow.PossiblyEatMessage (método)

El `PossiblyEatMessage` método permite que una clase derivada reenvía mensajes a otra ventana.

## <a name="syntax"></a>Sintaxis


```C++
virtual BOOL PossiblyEatMessage(
   UINT   uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*uMsg* 
</dt> <dd>

Identificador del mensaje.

</dd> <dt>

*wParam* 
</dt> <dd>

Primer parámetro de mensaje.

</dd> <dt>

*lParam* 
</dt> <dd>

Segundo parámetro de mensaje.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se reenvía el mensaje o FALSE en **caso** contrario. La clase base devuelve **FALSE.**

## <a name="remarks"></a>Comentarios

Antes de [**que el método CBaseWindow::OnReceiveMessage**](cbasewindow-onreceivemessage.md) controle un mensaje, llama a `PossiblyEatMessage` . Si `PossiblyEatMessage` devuelve **TRUE**, **OnReceiveMessage** omite el mensaje. Una clase derivada puede invalidar `PossiblyEatMessage` para que reenvía algunos mensajes a una ventana de propietario. Por ejemplo, la [**clase CBaseControlWindow,**](cbasecontrolwindow.md) que deriva de **CBaseWindow,** reenvía los mensajes del teclado y del mouse.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseWindow (clase)**](cbasewindow.md)
</dt> </dl>

 

 




