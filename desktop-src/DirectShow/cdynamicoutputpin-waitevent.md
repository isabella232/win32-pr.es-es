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
ms.openlocfilehash: b27f3c387c82eaeebc119f967deaca8e7314ccd7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062499"
---
# <a name="cdynamicoutputpinwaitevent-method"></a>Método CDynamicOutputPin.WaitEvent

El `WaitEvent` método espera hasta que se señala el evento especificado.

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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CDynamicOutputPin (clase)**](cdynamicoutputpin.md)
</dt> </dl>

 

 




