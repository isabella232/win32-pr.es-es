---
description: Identificador del subproceso.
ms.assetid: 93d1182a-58f0-4570-8568-fe0fded762cb
title: Miembro M_HTHREAD (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hThread
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e83dd225da0c3673f9c7f423e0bf56da7431b097
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160248"
---
# <a name="camthreadm_hthread-member"></a>Miembro CAMThread::m \_ hThread

Identificador del subproceso.

## <a name="syntax"></a>Sintaxis


```C++
HANDLE m_hThread;
```



## <a name="remarks"></a>Observaciones

Esta variable se inicializa como **NULL.** El [**método CAMThread::Create**](camthread-create.md) establece esta variable en el identificador del subproceso. Para determinar si el subproceso existe, llame al [**método CAMThread::ThreadExists.**](camthread-threadexists.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CLASE CAMThread**](camthread.md)
</dt> </dl>

 

 




