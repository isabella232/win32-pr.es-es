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
ms.openlocfilehash: 41a763a4b9151f22615aa0af3dae57af8281751209a016dc3135f3572e9d8ef3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768295"
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



 

## <a name="remarks"></a>Comentarios

El [**método CAMThread::InitialThreadProc**](camthread-initialthreadproc.md) llama a este método auxiliar, que llama a la función CoInitializeEx. Usa la marca COINIT DISABLE OLE1DDE para deshabilitar datos dinámicos Exchange \_ \_ (DDE). Para más información, consulte el SDK de plataforma.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CLASE CAMThread**](camthread.md)
</dt> </dl>

 

 




