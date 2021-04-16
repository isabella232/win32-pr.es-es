---
description: El método InitialThreadProc llama al procedimiento de subproceso principal.
ms.assetid: 1546c214-7ea9-4484-974b-dbd4b2b3e296
title: CAMThread.Inimétodo tialThreadProc (Wxutil. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671290"
---
# <a name="camthreadinitialthreadproc-method"></a>CAMThread.Inimétodo tialThreadProc

El `InitialThreadProc` método llama al procedimiento de subproceso principal.

## <a name="syntax"></a>Sintaxis


```C++
DWORD InitialThreadProc(
   LPVOID pv
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FV* 
</dt> <dd>

`this` puntero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el **DWORD** devuelto por [**CAMThread:: ThreadProc**](camthread-threadproc.md). La clase derivada define este valor.

## <a name="remarks"></a>Observaciones

El método [**CAMThread:: Create**](camthread-create.md) usa este método para el procedimiento de subproceso al crear el subproceso. Utiliza el `this` puntero como argumento de subproceso.

Este método llama al método [**CAMThread:: CoInitializeHelper**](camthread-coinitializehelper.md) y después a ThreadProc.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CAMThread**](camthread.md)
</dt> </dl>

 

 




