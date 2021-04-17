---
description: Método de constructor.
ms.assetid: 3f758c45-21ec-4728-ba7d-41da7b2fa02f
title: Constructor CMsgThread. CMsgThread (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.CMsgThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e77d3a84e349ab370b6319cd973f6ba86d632366
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680348"
---
# <a name="cmsgthreadcmsgthread-constructor"></a>Constructor CMsgThread. CMsgThread

Método de constructor.

## <a name="syntax"></a>Sintaxis


```C++
CMsgThread();
```



## <a name="parameters"></a>Parámetros

Este constructor no tiene parámetros.

## <a name="remarks"></a>Observaciones

La construcción de un objeto de subproceso de mensaje no crea automáticamente el subproceso. Debe llamar a la función miembro [**CMsgThread:: CreateThread**](cmsgthread-createthread.md) para crear el subproceso.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Msgthrd. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMsgThread**](cmsgthread.md)
</dt> </dl>

 

 




