---
description: El método ChangeOutputFormat cambia dinámicamente el tipo de medio para la conexión y proporciona información de nuevo segmento.
ms.assetid: d1204ca0-a489-48a0-8fe5-3ade04f51c93
title: Método CDynamicOutputPin. ChangeOutputFormat (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.ChangeOutputFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 57421b2fd9624d9798037151a5656343e386a497
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671756"
---
# <a name="cdynamicoutputpinchangeoutputformat-method"></a>CDynamicOutputPin. ChangeOutputFormat, método

El `ChangeOutputFormat` método cambia dinámicamente el tipo de medio para la conexión y proporciona información de nuevo segmento. El cambio puede producirse mientras se ejecuta el gráfico de filtros. Una vez que se llama a este método, no se pueden entregar los ejemplos con el tipo de medio anterior. El llamador debe asegurarse de que no haya ejemplos antiguos pendientes.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ChangeOutputFormat(
   const AM_MEDIA_TYPE  *pmt,
         REFERENCE_TIME tSegmentStart,
         REFERENCE_TIME tSegmentStop,
         double         dSegmentRate
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*p.p.* 
</dt> <dd>

Puntero a una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que especifica el tipo de medio.

</dd> <dt>

*tSegmentStart* 
</dt> <dd>

Hora de inicio del segmento.

</dd> <dt>

*tSegmentStop* 
</dt> <dd>

Hora de detención del segmento.

</dd> <dt>

*dSegmentRate* 
</dt> <dd>

Velocidad de segmento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                                           | Descripción                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                  | Correcto.<br/>                                                                                                                      |
| <dl> <dt>**E \_ FAIL**</dt> </dl>                | Error. Es posible que el filtro propietario no llamara a [**CDynamicOutputPin:: SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md).<br/> |
| <dl> <dt>**VFW \_ E \_ no \_ conectada**</dt> </dl> | El PIN no está conectado.<br/>                                                                                                     |



 

## <a name="remarks"></a>Observaciones

Este método cambia el tipo de formato mientras se está ejecutando el filtro. Si el PIN de bajada acepta el nuevo formato, no es necesario volver a conectar. De lo contrario, el método intenta volver a conectar el código PIN. Si el método cambia el formato correctamente, entrega la nueva información del segmento. Este método llama al método [**CDynamicOutputPin:: ChangeMediaType**](cdynamicoutputpin-changemediatype.md) para realizar el cambio de formato.

Debe llamar al método [**CDynamicOutputPin:: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) antes de llamar a este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




