---
description: El método WaitEvent espera hasta que se señala el evento especificado.
ms.assetid: 64880f46-7b8f-4823-9d50-052e30ecf04b
title: Método CDynamicOutputPin.WaitEvent (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.WaitEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3797c9127d3e931cd64fa35e822eac3151acc7fa1a8c4c0c9e93d6a36c0dfe99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871935"
---
# <a name="cdynamicoutputpinwaitevent-method"></a>Método CDynamicOutputPin.WaitEvent

El `WaitEvent` método espera hasta que se señale el evento especificado.

## <a name="syntax"></a>Sintaxis


```C++
static HRESULT WaitEvent(
   HANDLE hEvent
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hEvent* 
</dt> <dd>

Identificador para un evento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                                  | Descripción                  |
|----------------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Correcto.<br/>          |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl> | error inesperado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CDynamicOutputPin (clase)**](cdynamicoutputpin.md)
</dt> </dl>

 

 




