---
description: 'El método InitialThreadProc llama al método COutputQueue:: ThreadProc cuando se crea el subproceso.'
ms.assetid: 6093f0c3-ec58-418d-bb8c-618163c43ac7
title: COutputQueue.Inimétodo tialThreadProc (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.InitialThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfc7b8660d838b6ad31dd298c509b6282ab61810
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680886"
---
# <a name="coutputqueueinitialthreadproc-method"></a>COutputQueue.Inimétodo tialThreadProc

El `InitialThreadProc` método llama al método [**COutputQueue:: ThreadProc**](coutputqueue-threadproc.md) cuando se crea el subproceso.

## <a name="syntax"></a>Sintaxis


```C++
static DWORD WINAPI InitialThreadProc(
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

Devuelve el valor devuelto por el método [**COutputQueue:: ThreadProc**](coutputqueue-threadproc.md) .

## <a name="remarks"></a>Observaciones

Este método es el procedimiento de subproceso para el subproceso de trabajo del objeto. El puntero del objeto `this` es el parámetro Thread. El método desreferencia este para llamar a **ThreadProc**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Outputq. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




