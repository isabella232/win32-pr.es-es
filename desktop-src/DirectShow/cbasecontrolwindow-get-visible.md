---
description: El \_ método get visible recupera la visibilidad de la ventana actual.
ms.assetid: 7e643569-1116-4562-be33-babd12a7e899
title: Método CBaseControlWindow.get_Visible (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Visible
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3bc38a0b35f46de223ed84174c3b10f5300cc94d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671566"
---
# <a name="cbasecontrolwindowget_visible-method"></a>CBaseControlWindow. get ( \_ método visible)

El `get_Visible` método recupera la visibilidad de la ventana actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Visible(
   long *pVisible
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pVisible* 
</dt> <dd>

Puntero a una marca booleana de Automation (0 es OFF, 1 es ON).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="remarks"></a>Observaciones

Esta función miembro devuelve 1 si la ventana tiene el \_ estilo visible de WS; en caso contrario, es 0.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




