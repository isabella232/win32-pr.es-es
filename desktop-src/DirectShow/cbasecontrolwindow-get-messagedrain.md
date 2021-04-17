---
description: El \_ método get MessageDrain recupera la purga del mensaje actual.
ms.assetid: d679e7f7-4628-479b-b722-843cdd91ffe6
title: Método CBaseControlWindow.get_MessageDrain (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_MessageDrain
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aaf51c3f4297f238e51bbe8677303730c04b89d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660346"
---
# <a name="cbasecontrolwindowget_messagedrain-method"></a>CBaseControlWindow. Get \_ MessageDrain (método)

El `get_MessageDrain` método recupera la purga del mensaje actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_MessageDrain(
   OAHWND *Drain
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Purga* 
</dt> <dd>

Puntero a la ventana actual que recibe los mensajes de ventana.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="remarks"></a>Observaciones

Los mensajes enviados al filtro de representador de vídeo se pueden publicar en otra ventana. La ventana registrada para recibir estos mensajes (mediante la función miembro **CBaseControlWindow:: get \_ MessageDrain** ) es la purga del mensaje actual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




