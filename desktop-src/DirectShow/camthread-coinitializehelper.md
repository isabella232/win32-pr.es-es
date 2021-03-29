---
description: El método CoInitializeHelper llama a la función CoInitializeEx al inicio del subproceso.
ms.assetid: 1a981e1e-c059-4e51-81d8-33bcb39ee580
title: Método CAMThread. CoInitializeHelper (Wxutil. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660437"
---
# <a name="camthreadcoinitializehelper-method"></a>CAMThread. CoInitializeHelper, método

El `CoInitializeHelper` método llama a la función CoInitializeEx al inicio del subproceso.

## <a name="syntax"></a>Sintaxis


```C++
static HRESULT CoInitializeHelper();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Los valores posibles son los siguientes.



| Código devuelto                                                                             | Descripción                                              |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | La función CoInitializeEx no está disponible.<br/> |
| <dl> <dt>**S \_ correcto**</dt> </dl>    | Correcto.<br/>                                      |
| <dl> <dt>**E \_ FAIL**</dt> </dl>  | Error.<br/>                                      |



 

## <a name="remarks"></a>Observaciones

El método [**CAMThread:: InitialThreadProc**](camthread-initialthreadproc.md) llama a este método auxiliar, que llama a la función CoInitializeEx. Usa la marca coinit \_ Disable \_ OLE1DDE para deshabilitar intercambio dinámico de datos (DDE). Para obtener más información, vea el SDK de la plataforma.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CAMThread**](camthread.md)
</dt> </dl>

 

 




