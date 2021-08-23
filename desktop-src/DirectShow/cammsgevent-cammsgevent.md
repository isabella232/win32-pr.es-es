---
description: 'Constructor CAMMsgEvent.CAMMsgEvent: método constructor.'
ms.assetid: 7871a624-70c0-4f21-b62a-2c4c2eaa762b
title: Constructor CAMMsgEvent.CAMMsgEvent (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMMsgEvent.CAMMsgEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0fc2eeaab10134022388e6a57628d1c3c5a87fc0e0a443efab19f016a1e5c27b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955504"
---
# <a name="cammsgeventcammsgevent-constructor"></a>Constructor CAMMsgEvent.CAMMsgEvent

Método constructor.

## <a name="syntax"></a>Sintaxis


```C++
CAMMsgEvent(
   HRESULT *phr
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Phr* 
</dt> <dd>

Puntero a un **valor HRESULT.** Si se produce un error en el constructor, este parámetro recibe un código de error. Si esto ocurre, el objeto no está en un estado válido.

Para la compatibilidad con versiones anteriores de strmbase.lib, este parámetro tiene como valor predeterminado **NULL**. Sin embargo, se prefiere pasar un valor distinto de **NULL,** para que el autor de la llamada pueda comprobar el estado del objeto.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CLASE CAMMsgEvent**](cammsgevent.md)
</dt> </dl>

 

 




