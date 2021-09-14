---
description: 'Constructor CMediaEvent.CMediaEvent: método constructor.'
ms.assetid: 7f7a0a9f-e531-4e22-8601-b84ab088e9e7
title: Constructor CMediaEvent.CMediaEvent (Ctlutil.h)
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
ms.openlocfilehash: 36cd82b086241012542701001c4de1fe16ac2d8e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062474"
---
# <a name="cmediaeventcmediaevent-constructor"></a>Constructor CMediaEvent.CMediaEvent

Método constructor.

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

Puntero al nombre del objeto con fines de depuración.

</dd> <dt>

*Punk* 
</dt> <dd>

Puntero al propietario de este objeto.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Asigne el *parámetro pName* en la memoria estática. Este nombre aparece en el terminal de depuración tras la creación y eliminación del objeto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CMediaEvent (clase)**](cmediaevent.md)
</dt> </dl>

 

 




