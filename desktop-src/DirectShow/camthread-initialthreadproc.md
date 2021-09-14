---
description: El método InitialThreadProc llama al procedimiento del subproceso principal.
ms.assetid: 1546c214-7ea9-4484-974b-dbd4b2b3e296
title: Método CAMThread.InitialThreadProc (Wxutil.h)
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
ms.openlocfilehash: cd7fd0aa12d0659776db7e39fb223095762fc209
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160250"
---
# <a name="camthreadinitialthreadproc-method"></a>Método CAMThread.InitialThreadProc

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

## <a name="remarks"></a>Observaciones

El [**método CAMThread::Create**](camthread-create.md) usa este método para el procedimiento de subproceso cuando crea el subproceso. Usa el puntero `this` como argumento del subproceso.

Este método llama al [**método CAMThread::CoInitializeHelper**](camthread-coinitializehelper.md) y, después, a ThreadProc.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CLASE CAMThread**](camthread.md)
</dt> </dl>

 

 




