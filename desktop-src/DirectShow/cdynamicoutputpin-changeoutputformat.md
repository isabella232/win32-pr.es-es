---
description: El método ChangeOutputFormat cambia dinámicamente el tipo de medio para la conexión y proporciona información de segmento nuevo.
ms.assetid: d1204ca0-a489-48a0-8fe5-3ade04f51c93
title: Método CDynamicOutputPin.ChangeOutputFormat (Amfilter.h)
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
ms.openlocfilehash: 534d588bc1633770c35b0e0edbc2079ed8f7ab5035d3a8d2ff181042d26fdb3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074279"
---
# <a name="cdynamicoutputpinchangeoutputformat-method"></a>Método CDynamicOutputPin.ChangeOutputFormat

El `ChangeOutputFormat` método cambia dinámicamente el tipo de medio para la conexión y proporciona información de segmento nuevo. El cambio puede producirse mientras se ejecuta el gráfico de filtros. Una vez que se llama a este método, no se pueden entregar ejemplos con el tipo de medio anterior. El autor de la llamada debe asegurarse de que no hay ninguna muestra antigua pendiente.

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

*Pmt* 
</dt> <dd>

Puntero a una [**estructura \_ AM MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) que especifica el tipo de medio.

</dd> <dt>

*tSegmentStart* 
</dt> <dd>

Hora de inicio del segmento.

</dd> <dt>

*tSegmentStop* 
</dt> <dd>

Hora de detenerse del segmento.

</dd> <dt>

*dSegmentRate* 
</dt> <dd>

Velocidad de segmento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                                           | Descripción                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Correcto.<br/>                                                                                                                      |
| <dl> <dt>**E \_ FAIL**</dt> </dl>                | Error. Posiblemente, el filtro propietario no llamó [**a CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md).<br/> |
| <dl> <dt>**VFW \_ E \_ NO \_ CONECTADO**</dt> </dl> | El pin no está conectado.<br/>                                                                                                     |



 

## <a name="remarks"></a>Comentarios

Este método cambia el tipo de formato mientras se ejecuta el filtro. Si la marca de nivel inferior acepta el nuevo formato, no es necesaria ninguna reconexión. De lo contrario, el método intenta volver a conectar el pin. Si el método cambia correctamente el formato, proporciona la nueva información de segmento. Este método llama al [**método CDynamicOutputPin::ChangeMediaType**](cdynamicoutputpin-changemediatype.md) para realizar el cambio de formato.

Debe llamar al método [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) antes de llamar a este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CDynamicOutputPin (clase)**](cdynamicoutputpin.md)
</dt> </dl>

 

 




