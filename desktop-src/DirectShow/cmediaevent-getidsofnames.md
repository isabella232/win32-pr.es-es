---
description: Mapas una función miembro única y un conjunto opcional de parámetros en un conjunto correspondiente de identificadores de distribución de enteros, que se pueden usar en llamadas posteriores a la función miembro CMediaEvent::Invoke.
ms.assetid: 04e607e6-0b68-4371-aacf-01af308a56a3
title: Método CMediaEvent.GetIDsOfNames (Ctlutil.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062473"
---
# <a name="cmediaeventgetidsofnames-method"></a>Método CMediaEvent.GetIDsOfNames

Mapas una función miembro única y un conjunto opcional de parámetros en un conjunto correspondiente de identificadores de distribución de enteros, que se pueden usar en las llamadas posteriores a la función miembro [**CMediaEvent::Invoke.**](cmediaevent-invoke.md)

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

Identificador de referencia. Reservado para uso futuro. Debe ser **NULL.**

</dd> <dt>

*rgszNames* 
</dt> <dd>

Dirección de un puntero a una matriz de nombres que se va a asignar.

</dd> <dt>

*cNames* 
</dt> <dd>

Número de nombres que se van a asignar.

</dd> <dt>

*lcid* 
</dt> <dd>

Contexto de configuración regional en el que se interpretan los nombres.

</dd> <dt>

*rgdispid* 
</dt> <dd>

Puntero a una matriz asignada por el autor de la llamada, cuyo elemento contiene un identificador correspondiente a uno de los nombres pasados en la *matriz rgszNames.* El primer elemento representa el nombre del miembro; los elementos posteriores representan cada uno de los parámetros del miembro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores siguientes.



| Código devuelto                                                                                            | Descripción                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**DISP \_ E \_ UNKNOWN \_ CLSID**</dt> </dl> | No se ha reconocido el CLSID.<br/>                                                                                                             |
| <dl> <dt>**DISP \_ E \_ UNKNOWNNAME**</dt> </dl>    | No se conocían uno o varios de los nombres. Los DISPID devueltos contienen DISPID \_ UNKNOWN para cada entrada que corresponde a un nombre desconocido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Memoria insuficiente<br/>                                                                                                                            |
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Correcto.<br/>                                                                                                                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CMediaEvent (clase)**](cmediaevent.md)
</dt> </dl>

 

 




