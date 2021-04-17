---
description: 'Asigna una sola función miembro y un conjunto opcional de parámetros a un conjunto correspondiente de identificadores de envío enteros, que se puede usar en las llamadas subsiguientes a la función miembro CMediaEvent:: Invoke.'
ms.assetid: 04e607e6-0b68-4371-aacf-01af308a56a3
title: Método CMediaEvent. GetIDsOfNames (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 191fa85264e4e7e22aa67f409db20cebd68f4319
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681015"
---
# <a name="cmediaeventgetidsofnames-method"></a>CMediaEvent. GetIDsOfNames (método)

Asigna una sola función miembro y un conjunto opcional de parámetros a un conjunto correspondiente de identificadores de envío enteros, que se puede usar en las llamadas subsiguientes a la función miembro [**CMediaEvent:: Invoke**](cmediaevent-invoke.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetIDsOfNames(
   REFIID  riid,
   OLECHAR **rgszNames,
   UINT    cNames,
   LCID    lcid,
   DISPID  *rgdispid
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*riid* 
</dt> <dd>

Identificador de referencia. Reservado para uso futuro. Debe ser **null**.

</dd> <dt>

*rgszNames* 
</dt> <dd>

Dirección de un puntero a una matriz de nombres pasada que se va a asignar.

</dd> <dt>

*CNAME* 
</dt> <dd>

Número de nombres que se van a asignar.

</dd> <dt>

*lcid* 
</dt> <dd>

Contexto de configuración regional en el que se van a interpretar los nombres.

</dd> <dt>

*rgdispid* 
</dt> <dd>

Puntero a una matriz asignada por el llamador, donde cada elemento contiene un identificador que corresponde a uno de los nombres pasados en la matriz *rgszNames* . El primer elemento representa el nombre del miembro; los elementos siguientes representan cada uno de los parámetros del miembro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores siguientes.



| Código devuelto                                                                                            | Descripción                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**DISP \_ . \_ \_ CLSID desconocido**</dt> </dl> | No se reconoció el CLSID.<br/>                                                                                                             |
| <dl> <dt>**DISP \_ E \_ UNKNOWNNAME**</dt> </dl>    | No se conocían uno o varios de los nombres. Los DISPID devueltos contienen un DISPID \_ desconocido para cada entrada que corresponde a un nombre desconocido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Memoria insuficiente<br/>                                                                                                                            |
| <dl> <dt>**S \_ correcto**</dt> </dl>                   | Correcto.<br/>                                                                                                                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMediaEvent**](cmediaevent.md)
</dt> </dl>

 

 




