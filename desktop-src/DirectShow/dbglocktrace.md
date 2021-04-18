---
description: Habilita o deshabilita el registro de depuración de una sección crítica determinada.
ms.assetid: 6e6e3de4-8bea-4e28-b04e-54a52226b59a
title: Función DbgLockTrace (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgLockTrace
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8daf3c33b43bda95bb1d54145e9e5aebc6f89c2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660501"
---
# <a name="dbglocktrace-function"></a>DbgLockTrace función)

Habilita o deshabilita el registro de depuración de una sección crítica determinada.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI DbgLockTrace(
   CCritSec *pcCrit,
   BOOL     fTrace
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pcCrit* 
</dt> <dd>

Puntero a una sección crítica de [**CCritSec**](ccritsec.md) .

</dd> <dt>

*fTrace* 
</dt> <dd>

Valor que especifica si el registro está habilitado. Use **true** para habilitar el registro o **false** para deshabilitarlo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Utilice esta función para realizar un seguimiento de una sección crítica específica. De forma predeterminada, el registro de depuración de secciones críticas está deshabilitado debido al gran número de secciones críticas.

Para realizar un seguimiento de una sección crítica, realice los pasos siguientes:

1.  Defina depurar o \_ depurar antes de incluir los encabezados de DirectShow.
2.  Habilite el registro de depuración para las secciones críticas llamando a [**DbgSetModuleLevel**](dbgsetmodulelevel.md) con la marca de bloqueo del registro \_ .
3.  Llame a **DbgLockTrace** en la sección crítica en la que desea realizar un seguimiento.

En las compilaciones comerciales, la función **DbgLockTrace** no tiene ningún efecto.

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra cómo realizar un seguimiento de una sección crítica.


```
DbgInitialise(g_hInst);
DbgSetModuleLevel(LOG_LOCKING, 3);

{
    CCritSec MyLock;
    DbgLockTrace(&MyLock, TRUE);
    
    CAutoLock cObjectLock(&MyLock);

    // Protected section of code.    
    DbgOutString("This code is inside a critical section.\n");

} // Lock goes out of scope here.

DbgTerminate();
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de depuración de sección crítica](critical-section-debugging-functions.md)
</dt> </dl>

 

 




