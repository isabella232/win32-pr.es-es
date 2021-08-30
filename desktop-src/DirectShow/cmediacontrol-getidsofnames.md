---
description: Mapas una función miembro única y un conjunto opcional de parámetros en un conjunto correspondiente de identificadores de distribución de enteros (DISPID), que se pueden usar en llamadas posteriores a la función miembro CMediaControl::Invoke.
ms.assetid: 9ce1b1aa-ea03-4a65-bff7-e46771cd0772
title: Método CMediaControl.GetIDsOfNames (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d328a4311746f6fdab9cf7eaa3376c7ba49c2b13b9db1d3aaac19142d2d583d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055184"
---
# <a name="cmediacontrolgetidsofnames-method"></a>Método CMediaControl.GetIDsOfNames

Mapas una función miembro única y un conjunto opcional de parámetros en un conjunto correspondiente de identificadores de distribución de enteros (DISPID), que se pueden usar en llamadas posteriores a la función miembro [**CMediaControl::Invoke.**](cmediacontrol-invoke.md)

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

Dirección de un puntero a una matriz de nombres pasada que se va a asignar.

</dd> <dt>

*cNames* 
</dt> <dd>

Número de nombres que se van a asignar.

</dd> <dt>

*lcid* 
</dt> <dd>

Contexto de configuración regional en el que se interpretarán los nombres.

</dd> <dt>

*rgdispid* 
</dt> <dd>

Puntero a una matriz asignada por el autor de la llamada, cuyo elemento contiene un identificador correspondiente a uno de los nombres pasados en la *matriz rgszNames.* El primer elemento representa el nombre del miembro; los elementos subsiguientes representan cada uno de los parámetros del miembro.

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMediaControl (clase)**](cmediacontrol.md)
</dt> </dl>

 

 




