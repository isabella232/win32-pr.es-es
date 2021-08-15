---
description: El método \_ get MessageDrain recupera la purga del mensaje actual.
ms.assetid: d679e7f7-4628-479b-b722-843cdd91ffe6
title: CBaseControlWindow.get_MessageDrain método (Ctlutil.h)
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
ms.openlocfilehash: 9a1e63e96950093bb7cc5760032d0b1f622c5df93a6f31673c595f54e5ea8e70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017403"
---
# <a name="cbasecontrolwindowget_messagedrain-method"></a>CBaseControlWindow.get \_ MessageDrain (método)

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

Puntero a la ventana actual que recibe mensajes de ventana.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Comentarios

Los mensajes enviados al filtro del representador de vídeo se pueden publicar en otra ventana. La ventana registrada para recibir estos mensajes (mediante la función miembro **CBaseControlWindow::get \_ MessageDrain)** es la purga del mensaje actual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseControlWindow (clase)**](cbasecontrolwindow.md)
</dt> </dl>

 

 




