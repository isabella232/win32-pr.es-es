---
description: El método ChangeMediaType cambia dinámicamente el tipo de medio para la conexión.
ms.assetid: 38efdfdc-f636-4cad-b8d3-8c63a277644e
title: Método CDynamicOutputPin.ChangeMediaType (Amfilter.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061745"
---
# <a name="cdynamicoutputpinchangemediatype-method"></a>Método CDynamicOutputPin.ChangeMediaType

El `ChangeMediaType` método cambia dinámicamente el tipo de medio para la conexión. El cambio puede producirse mientras se ejecuta el gráfico de filtros. Una vez que se llama a este método, no se pueden entregar ejemplos con el tipo de medio antiguo. El autor de la llamada debe asegurarse de que no haya muestras antiguas pendientes.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ChangeMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pmt* 
</dt> <dd>

Puntero a una [**estructura \_ AM MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) que especifica el tipo de medio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                                           | Descripción                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Correcto.<br/>                                                                                                                      |
| <dl> <dt>**E \_ FAIL**</dt> </dl>                | Error. Posiblemente, el filtro propietario no llamó a [**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md).<br/> |
| <dl> <dt>**VFW \_ E \_ NO \_ CONECTADO**</dt> </dl> | El pin no está conectado.<br/>                                                                                                     |



 

## <a name="remarks"></a>Observaciones

Llame al [**método CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) antes de llamar a este método.

Este método comprueba primero si el pin de entrada de bajada puede aceptar el nuevo formato sin volver a conectarse. Consulta el pin de entrada para la [**interfaz IPinConnection.**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) Si el pin de entrada admite **IPinConnection,** el método llama al método [**IPinConnection::D ynamicQueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-dynamicqueryaccept) con el tipo de medio propuesto. Si el pin de entrada acepta el nuevo tipo de medio, el método llama al método [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) y vuelve a negociar los requisitos del asignador.

Por otro lado, si el pin de bajada no admite **IPinConnection** o si rechaza el nuevo tipo de medio, el método llama al método [**CDynamicOutputPin::D ynamicReconnect**](cdynamicoutputpin-dynamicreconnect.md) para realizar una reconexión dinámica.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CDynamicOutputPin (clase)**](cdynamicoutputpin.md)
</dt> </dl>

 

 




