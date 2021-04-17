---
description: Método de constructor.
ms.assetid: a51d90c9-4046-42dc-b7cf-51b904c5f57a
title: Constructor CSourceSeeking. CSourceSeeking (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.CSourceSeeking
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 309e926ddf001cf9933b19334992f5210fc7f17b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661038"
---
# <a name="csourceseekingcsourceseeking-constructor"></a>Constructor CSourceSeeking. CSourceSeeking

Método de constructor.

## <a name="syntax"></a>Sintaxis


```C++
CSourceSeeking(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         CCritSec  *pLock
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* 
</dt> <dd>

Puntero a una cadena que contiene el nombre del objeto. Para obtener más información, vea [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*pUnk* 
</dt> <dd>

Puntero al propietario de este objeto. Si se agrega el objeto, pase un puntero a la interfaz **IUnknown** del objeto de agregación. De lo contrario, establezca este parámetro en **null**.

</dd> <dt>

*phr* 
</dt> <dd>

Puntero a un valor **HRESULT** . ignorado.

</dd> <dt>

*pLock* 
</dt> <dd>

Puntero a un objeto [**CCritSec**](ccritsec.md) . En la clase derivada, declare una variable de miembro **CCritSec** y use la dirección de esta para este parámetro. La `CSourceSeeking` clase utiliza esta sección crítica para sincronizar el acceso a las horas de inicio y de finalización, la duración y la velocidad de reproducción. Siempre que obtenga acceso a esas variables en la clase derivada, conserve este bloqueo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




