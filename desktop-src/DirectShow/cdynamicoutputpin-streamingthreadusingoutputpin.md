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
ms.openlocfilehash: 4687db225a616adef6d1c756ae9295e2c273c0315f37d119c7bacd0c226233e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119539725"
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

Devuelve **TRUE** si un subproceso realiza una operación de streaming en el pin. De lo contrario, **devuelve FALSE.**

## <a name="remarks"></a>Comentarios

Si algún subproceso ha devuelto correctamente desde el método [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) y no ha realizado una llamada correspondiente al método [**CDynamicOutputPin::StopUsingOutputPin,**](cdynamicoutputpin-stopusingoutputpin.md) este método devuelve **TRUE**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CDynamicOutputPin (clase)**](cdynamicoutputpin.md)
</dt> </dl>

 

 




