---
description: Devuelve FALSE si el subproceso actual es el propietario de la sección crítica especificada.
ms.assetid: 1a2cb56c-2806-4bb2-b904-985af332b290
title: Función CritCheckOut (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CritCheckOut
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fb1289bd89771797be88220f49d8af6f468a11c54e9954c32786e3af72dc1956
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908095"
---
# <a name="critcheckout-function"></a>Función CritCheckOut

Devuelve **FALSE** si el subproceso actual es el propietario de la sección crítica especificada.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI CritCheckOut(
   CCritSec *pcCrit
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pcCrit* 
</dt> <dd>

Puntero a una sección crítica de [**CCritSec.**](ccritsec.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

En las compilaciones de depuración, **devuelve FALSE** si el subproceso actual es el propietario de esta sección crítica o TRUE en **caso** contrario. En las compilaciones comerciales, siempre devuelve **TRUE**.

## <a name="remarks"></a>Comentarios

Esta función es la inversa de la [**función CritCheckIn.**](critcheckin.md) Si **CritCheckIn devuelve** **TRUE,** **CritCheckOut** devuelve **FALSE** y viceversa.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de depuración de sección crítica](critical-section-debugging-functions.md)
</dt> </dl>

 

 




