---
description: Usa la función SetThreadPriority de Microsoft Win32 para establecer la prioridad del subproceso en un nuevo valor.
ms.assetid: 5b8ad024-e651-47e5-b32a-c44d56c086cd
title: Método CMsgThread. SetThreadPriority (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.SetThreadPriority
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0cfa3cd81907a251d2acf7129405e187286df3c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671726"
---
# <a name="cmsgthreadsetthreadpriority-method"></a>CMsgThread. SetThreadPriority, método

Usa la función **SetThreadPriority** de Microsoft Win32 para establecer la prioridad del subproceso en un nuevo valor.

## <a name="syntax"></a>Sintaxis


```C++
BOOL SetThreadPriority(
   int nPriority
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*nPriority* 
</dt> <dd>

Prioridad del subproceso.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores siguientes.



| Código devuelto                                                                              | Descripción                               |
|------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>TRUE * * * *</dt> </dl>  | La prioridad se estableció correctamente.<br/> |
| <dl> <dt>FALSE * * * *</dt> </dl> | No se estableció la prioridad.<br/>          |



 

## <a name="remarks"></a>Observaciones

El cliente y el subproceso de trabajo pueden llamar a esta función miembro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Msgthrd. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMsgThread**](cmsgthread.md)
</dt> </dl>

 

 




