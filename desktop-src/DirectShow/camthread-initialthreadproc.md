---
description: El método InitialThreadProc llama al procedimiento del subproceso principal.
ms.assetid: 1546c214-7ea9-4484-974b-dbd4b2b3e296
title: CAMThread.Inimétodo tialThreadProc (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.InitialThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d12e8d41ac0c6e1fd2af06c21accbb5c62e4eb25f2fc3f6c36988101a9b64d89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540305"
---
# <a name="camthreadinitialthreadproc-method"></a>CAMThread.Inimétodo tialThreadProc

El `InitialThreadProc` método llama al procedimiento del subproceso principal.

## <a name="syntax"></a>Sintaxis


```C++
DWORD InitialThreadProc(
   LPVOID pv
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pv* 
</dt> <dd>

`this` Puntero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el **DWORD** devuelto por [**CAMThread::ThreadProc**](camthread-threadproc.md). La clase derivada define este valor.

## <a name="remarks"></a>Comentarios

El [**método CAMThread::Create**](camthread-create.md) usa este método para el procedimiento de subproceso cuando crea el subproceso. Usa el puntero `this` como argumento del subproceso.

Este método llama al [**método CAMThread::CoInitializeHelper**](camthread-coinitializehelper.md) y, después, a ThreadProc.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CLASE CAMThread**](camthread.md)
</dt> </dl>

 

 




