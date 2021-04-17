---
description: Método de constructor.
ms.assetid: 7f7a0a9f-e531-4e22-8601-b84ab088e9e7
title: Constructor CMediaEvent. CMediaEvent (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.CMediaEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 77b87fa589728592874b0dea96f7b6efca501471
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670836"
---
# <a name="cmediaeventcmediaevent-constructor"></a>Constructor CMediaEvent. CMediaEvent

Método de constructor.

## <a name="syntax"></a>Sintaxis


```C++
CMediaEvent(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* 
</dt> <dd>

Puntero al nombre del objeto para la depuración.

</dd> <dt>

*pUnk* 
</dt> <dd>

Puntero al propietario de este objeto.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Asigne el parámetro *pName* en la memoria estática. Este nombre aparece en el terminal de depuración al crear y eliminar el objeto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMediaEvent**](cmediaevent.md)
</dt> </dl>

 

 




