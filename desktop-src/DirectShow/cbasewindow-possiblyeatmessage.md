---
description: El método PossiblyEatMessage permite a una clase derivada reenviar mensajes a otra ventana.
ms.assetid: d8775182-44ed-4df2-b4b8-1fdf289e2c1a
title: Método CBaseWindow. PossiblyEatMessage (Winutil. h)
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
ms.openlocfilehash: f218b62ac5464da27b8596992c34ce7ae5efde46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660314"
---
# <a name="cbasewindowpossiblyeatmessage-method"></a>CBaseWindow. PossiblyEatMessage, método

El `PossiblyEatMessage` método permite a una clase derivada reenviar mensajes a otra ventana.

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

Identificador de mensaje.

</dd> <dt>

*wParam* 
</dt> <dd>

Primer parámetro de mensaje.

</dd> <dt>

*lParam* 
</dt> <dd>

Segundo parámetro del mensaje.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si el mensaje se reenvió o **false** en caso contrario. La clase base devuelve **false**.

## <a name="remarks"></a>Observaciones

Antes de que el método [**CBaseWindow:: OnReceiveMessage**](cbasewindow-onreceivemessage.md) controle un mensaje, llama a `PossiblyEatMessage` . Si `PossiblyEatMessage` devuelve **true**, **OnReceiveMessage** omite el mensaje. Una clase derivada puede invalidar `PossiblyEatMessage` para que reenvíe algunos mensajes a una ventana propietaria. Por ejemplo, la clase [**CBaseControlWindow**](cbasecontrolwindow.md) , que se deriva de **CBaseWindow**, reenvía los mensajes de teclado y del mouse.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




