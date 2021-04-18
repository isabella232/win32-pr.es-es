---
description: Método de constructor. El constructor bloquea el objeto de sección crítica especificado.
ms.assetid: 5a0d74f9-bb99-4922-9a92-2e7c1863421f
title: Constructor CAutoLock. CAutoLock (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoLock.CAutoLock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fed29011d4fe581ed146f64800351a3f1053d957
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670822"
---
# <a name="cautolockcautolock-constructor"></a>Constructor CAutoLock. CAutoLock

Método de constructor. El constructor bloquea el objeto de sección crítica especificado.

## <a name="syntax"></a>Sintaxis


```C++
CAutoLock(
   CCritSec *plock
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*plock* 
</dt> <dd>

Puntero a un objeto [**CCritSec**](ccritsec.md) , que contiene un objeto de sección crítica.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CAutoLock**](cautolock.md)
</dt> </dl>

 

 




