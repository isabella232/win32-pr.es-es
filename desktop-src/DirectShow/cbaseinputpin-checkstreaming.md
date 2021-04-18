---
description: Determina si el pin puede aceptar ejemplos.
ms.assetid: bc66ab4c-99de-4031-bdac-b1430f736e20
title: Método CBaseInputPin. CheckStreaming (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.CheckStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba07d28ac93f7dc511390a851d3c737a833ef3f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660145"
---
# <a name="cbaseinputpincheckstreaming-method"></a>CBaseInputPin. CheckStreaming, método

Determina si el pin puede aceptar ejemplos.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT CheckStreaming();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                           | Descripción                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                  | Correcto.<br/>                   |
| <dl> <dt>**S \_ false**</dt> </dl>               | El PIN se está vaciando actualmente.<br/> |
| <dl> <dt>**\_error de \_ tiempo de ejecución de VFW E \_**</dt> </dl> | Se produjo un error en tiempo de ejecución.<br/> |
| <dl> <dt>**Estado de VFW \_ E \_ incorrecto \_**</dt> </dl>   | El PIN está detenido.<br/>        |



 

## <a name="remarks"></a>Observaciones

La clase derivada puede invalidar este método para realizar comprobaciones adicionales. En el método de reemplazo, llame también a la implementación de la clase base.

El método [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) llama a este método. Debe reemplazar el método [**CBasePin:: EndOfStream**](cbasepin-endofstream.md) para llamar también a este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




