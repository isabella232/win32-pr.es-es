---
description: El método SetControlWindowPin establece el pin con el que se va a sincronizar.
ms.assetid: 6373c046-5448-4159-88b9-9b2babdb938b
title: Método CBaseControlWindow.SetControlWindowPin (Ctlutil.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361412"
---
# <a name="cbasecontrolwindowsetcontrolwindowpin-method"></a>Método CBaseControlWindow.SetControlWindowPin

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

Esta función miembro establece la variable miembro m \_ pPin igual al parámetro pPin. Como se describe en el constructor, solo se puede llamar a la interfaz cuando el filtro se ha conectado correctamente. El objeto se pasa a través de esta función miembro al pin con el que debe sincronizarse. En la mayoría de los casos, determinará si el pin está conectado siempre que tenga un método de interfaz llamado y devolverá VFW E NOT CONNECTED si se produce \_ \_ un \_ error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseControlWindow (clase)**](cbasecontrolwindow.md)
</dt> </dl>

 

 




