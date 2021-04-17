---
description: El método DynamicReconnect realiza una reconexión dinámica con un nuevo tipo de medio. La reconexión puede producirse mientras se ejecuta el gráfico de filtros.
ms.assetid: 1fe9f1cc-1f5d-407e-8c80-fea6cd1cb16f
title: Método CDynamicOutputPin. DynamicReconnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.DynamicReconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dd595748380a35f74e591283ed3d03273c683e97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660127"
---
# <a name="cdynamicoutputpindynamicreconnect-method"></a>CDynamicOutputPin. DynamicReconnect, método

El `DynamicReconnect` método realiza una reconexión dinámica con un nuevo tipo de medio. La reconexión puede producirse mientras se ejecuta el gráfico de filtros.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DynamicReconnect(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*p.p.* 
</dt> <dd>

Puntero a una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que especifica el tipo de medio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                            | Descripción                                                                                                                                         |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>   | Correcto.<br/>                                                                                                                                 |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Error. Es posible que el filtro propietario no llamara al método [**CDynamicOutputPin:: SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) .<br/> |



 

## <a name="remarks"></a>Observaciones

Se debe llamar a este método desde el mismo subproceso que entrega datos al pin. Una vez que se llama a este método, no se pueden entregar los ejemplos con el tipo de medio anterior. El llamador debe asegurarse de que no haya ejemplos antiguos pendientes.

Llame a [**CDynamicOutputPin:: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) antes de llamar a este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




