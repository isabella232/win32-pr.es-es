---
description: El método ChangeMediaType cambia dinámicamente el tipo de medio para la conexión.
ms.assetid: 38efdfdc-f636-4cad-b8d3-8c63a277644e
title: Método CDynamicOutputPin. ChangeMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.ChangeMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 89c15e3076a95f8fee3f2f2970fc59da5cf3bf4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661357"
---
# <a name="cdynamicoutputpinchangemediatype-method"></a>CDynamicOutputPin. ChangeMediaType, método

El `ChangeMediaType` método cambia dinámicamente el tipo de medio para la conexión. El cambio puede producirse mientras se ejecuta el gráfico de filtros. Una vez que se llama a este método, no se pueden entregar los ejemplos con el tipo de medio anterior. El llamador debe asegurarse de que no haya ejemplos antiguos pendientes.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ChangeMediaType(
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



| Código devuelto                                                                                           | Descripción                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                  | Correcto.<br/>                                                                                                                      |
| <dl> <dt>**E \_ FAIL**</dt> </dl>                | Error. Es posible que el filtro propietario no llamara a [**CDynamicOutputPin:: SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md).<br/> |
| <dl> <dt>**VFW \_ E \_ no \_ conectada**</dt> </dl> | El PIN no está conectado.<br/>                                                                                                     |



 

## <a name="remarks"></a>Observaciones

Llame al método [**CDynamicOutputPin:: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) antes de llamar a este método.

Este método comprueba primero si el PIN de entrada de nivel inferior puede aceptar el nuevo formato sin volver a conectarse. Consulta el PIN de entrada de la interfaz [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) . Si el PIN de entrada es compatible con **IPinConnection**, el método llama al método [**IPinConnection::D ynamicqueryaccept**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-dynamicqueryaccept) con el tipo de medio propuesto. Si el PIN de entrada acepta el nuevo tipo de archivo multimedia, el método llama al método [**IPin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) y vuelve a negociar los requisitos del asignador.

Por otro lado, si el PIN de bajada no admite **IPinConnection**, o si rechaza el nuevo tipo de medio, el método llama al método [**CDynamicOutputPin::D ynamicreconnect**](cdynamicoutputpin-dynamicreconnect.md) para realizar una reconexión dinámica.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




