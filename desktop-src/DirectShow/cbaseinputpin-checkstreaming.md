---
description: Determina si el pin puede aceptar muestras.
ms.assetid: bc66ab4c-99de-4031-bdac-b1430f736e20
title: Método CBaseInputPin.CheckStreaming (Amfilter.h)
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
ms.openlocfilehash: de22d8a6fc634ffbb16ac111de1ad20dc0638660c5091c835a44f256d9ed1d4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076625"
---
# <a name="cbaseinputpincheckstreaming-method"></a>Método CBaseInputPin.CheckStreaming

Determina si el pin puede aceptar muestras.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT CheckStreaming();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** enumerados en la tabla siguiente.



| Código devuelto                                                                                           | Descripción                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Correcto.<br/>                   |
| <dl> <dt>**S \_ FALSE**</dt> </dl>               | El pin se está vacíando actualmente.<br/> |
| <dl> <dt>**ERROR EN TIEMPO DE EJECUCIÓN DE VFW \_ E \_ \_**</dt> </dl> | Se produjo un error en tiempo de ejecución.<br/> |
| <dl> <dt>**VFW \_ E \_ ESTADO \_ INCORRECTO**</dt> </dl>   | El pin se detiene.<br/>        |



 

## <a name="remarks"></a>Comentarios

La clase derivada puede invalidar este método para realizar comprobaciones adicionales. En el método de invalidación, llame también a la implementación de la clase base.

El [**método CBaseInputPin::Receive**](cbaseinputpin-receive.md) llama a este método. Debe invalidar el [**método CBasePin::EndOfStream**](cbasepin-endofstream.md) para llamar también a este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseInputPin (clase)**](cbaseinputpin.md)
</dt> </dl>

 

 




