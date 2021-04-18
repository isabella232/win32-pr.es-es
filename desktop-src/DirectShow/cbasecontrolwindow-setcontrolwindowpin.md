---
description: El método SetControlWindowPin establece el pin con el que se va a sincronizar.
ms.assetid: 6373c046-5448-4159-88b9-9b2babdb938b
title: Método CBaseControlWindow. SetControlWindowPin (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.SetControlWindowPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c1aa3d4960799c2286e17709258ea90b76332bc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661337"
---
# <a name="cbasecontrolwindowsetcontrolwindowpin-method"></a>CBaseControlWindow. SetControlWindowPin, método

El `SetControlWindowPin` método establece el pin con el que se va a sincronizar.

## <a name="syntax"></a>Sintaxis


```C++
void SetControlWindowPin(
   CBasePin *pPin
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pPin* 
</dt> <dd>

Puntero al pin con el que se sincroniza la interfaz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Esta función miembro establece la \_ variable miembro m pPin igual que el parámetro pPin. Tal y como se describe en el constructor, solo se puede llamar a la interfaz cuando el filtro se ha conectado correctamente. El objeto se pasa a través de esta función miembro al pin con el que se debe sincronizar; en la mayoría de los casos, determinará si el PIN está conectado siempre que tenga un método de interfaz llamado y devolverá VFW \_ E \_ no \_ conectado si se produce un error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




