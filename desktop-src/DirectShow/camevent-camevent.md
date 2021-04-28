---
description: 'Constructor DEEVENT.CAMEvent: método constructor.'
ms.assetid: 35c9ac07-8756-42b1-beeb-5f0e79466742
title: Constructor CAMEvent.CAMEvent (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.CAMEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cdd37ba72d9467c16d46b2aec3ec40c206466eaf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096542"
---
# <a name="cameventcamevent-constructor"></a>Constructor DE EVENTOS.CAMEvent

Método constructor.

## <a name="syntax"></a>Sintaxis


```C++
CAMEvent(
   BOOL    fManualReset,
   HRESULT *phr
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fManualReset* 
</dt> <dd>

Valor booleano que especifica si el objeto es un evento de restablecimiento manual o un evento de restablecimiento automático. Si **es TRUE,** el objeto es un evento de restablecimiento manual. De lo contrario, es un evento de restablecimiento automático.

</dd> <dt>

*Phr* 
</dt> <dd>

Puntero a un **valor HRESULT.** Si se produce un error en el constructor, este parámetro recibe un código de error. Si esto ocurre, el objeto no está en un estado válido.

Para la compatibilidad con versiones anteriores de strmbase.lib, el valor predeterminado de este parámetro es **NULL.** Sin embargo, se prefiere pasar un valor distinto de **NULL,** para que el autor de la llamada pueda comprobar el estado del objeto.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El evento comienza en un estado sin signo.

Con un evento de restablecimiento automático, el método [**CAMEvent::Wait**](camevent-wait.md) restablece el evento a no firma cuando el método vuelve. Con un evento de restablecimiento manual, el evento permanece señalado hasta que se llama al [**método CAMEvent::Reset.**](camevent-reset.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Streams.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CLASE CAMEvent**](camevent.md)
</dt> </dl>

 

 




