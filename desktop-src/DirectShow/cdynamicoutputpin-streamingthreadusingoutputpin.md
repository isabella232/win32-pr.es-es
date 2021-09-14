---
description: El método StreamingThreadUsingOutputPin determina si algún subproceso está realizando una operación de streaming en el pin.
ms.assetid: b6432a11-4e8b-4eb4-ad8e-aaff9398641b
title: Método CDynamicOutputPin.StreamingThreadUsingOutputPin (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.StreamingThreadUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 797dcb94e227861642de2a05e6edf24f675bb4e7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062505"
---
# <a name="cdynamicoutputpinstreamingthreadusingoutputpin-method"></a>Método CDynamicOutputPin.StreamingThreadUsingOutputPin

El método StreamingThreadUsingOutputPin determina si algún subproceso está realizando una operación de streaming en el pin.

## <a name="syntax"></a>Sintaxis


```C++
virtual bool StreamingThreadUsingOutputPin();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si un subproceso realiza una operación de streaming en el pin. De lo contrario, **devuelve FALSE**.

## <a name="remarks"></a>Observaciones

Si algún subproceso ha devuelto correctamente desde el método [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) y no ha realizado una llamada correspondiente al método [**CDynamicOutputPin::StopUsingOutputPin,**](cdynamicoutputpin-stopusingoutputpin.md) este método devuelve **TRUE**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CDynamicOutputPin (clase)**](cdynamicoutputpin.md)
</dt> </dl>

 

 




