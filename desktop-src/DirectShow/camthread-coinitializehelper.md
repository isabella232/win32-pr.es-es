---
description: El método CoInitializeHelper llama a la función CoInitializeEx al principio del subproceso.
ms.assetid: 1a981e1e-c059-4e51-81d8-33bcb39ee580
title: Método CAMThread.CoInitializeHelper (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CoInitializeHelper
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6c3eb7fbcb9e4abada43098339a29d208ded0d4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160257"
---
# <a name="camthreadcoinitializehelper-method"></a>Método CAMThread.CoInitializeHelper

El `CoInitializeHelper` método llama a la función CoInitializeEx al principio del subproceso.

## <a name="syntax"></a>Sintaxis


```C++
static HRESULT CoInitializeHelper();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** A continuación se den los valores posibles.



| Código devuelto                                                                             | Descripción                                              |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | La función CoInitializeEx no está disponible.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Correcto.<br/>                                      |
| <dl> <dt>**E \_ FAIL**</dt> </dl>  | Error.<br/>                                      |



 

## <a name="remarks"></a>Observaciones

El [**método CAMThread::InitialThreadProc**](camthread-initialthreadproc.md) llama a este método auxiliar, que llama a la función CoInitializeEx. Usa la marca COINIT \_ DISABLE \_ OLE1DDE para deshabilitar datos dinámicos Exchange (DDE). Para obtener más información, consulte el SDK de plataforma.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CLASE CAMThread**](camthread.md)
</dt> </dl>

 

 




