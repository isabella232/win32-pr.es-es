---
description: Método de constructor.
ms.assetid: 7871a624-70c0-4f21-b62a-2c4c2eaa762b
title: Constructor CAMMsgEvent. CAMMsgEvent (Wxutil. h)
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
ms.openlocfilehash: 0d207afae53a715728d8307656b0c2427ce9574c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671623"
---
# <a name="cammsgeventcammsgevent-constructor"></a>Constructor CAMMsgEvent. CAMMsgEvent

Método de constructor.

## <a name="syntax"></a>Sintaxis


```C++
CAMMsgEvent(
   HRESULT *phr
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*phr* 
</dt> <dd>

Puntero a un valor **HRESULT** . Si se produce un error en el constructor, este parámetro recibe un código de error. Si esto ocurre, el objeto no tiene un estado válido.

Para mantener la compatibilidad con versiones anteriores de strmbase. lib, este parámetro tiene como valor predeterminado **null**. Sin embargo, se prefiere pasar un valor distinto de **null** para que el autor de la llamada pueda comprobar el estado del objeto.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CAMMsgEvent**](cammsgevent.md)
</dt> </dl>

 

 




