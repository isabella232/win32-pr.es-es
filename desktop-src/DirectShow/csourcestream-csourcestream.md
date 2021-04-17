---
description: Método de constructor.
ms.assetid: 9078b2f5-b11e-4780-8143-6738e9df4f4b
title: Constructor CSourceStream. CSourceStream (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.CSourceStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a8671e939364d1c0cd22796b1518313002b5eb33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660445"
---
# <a name="csourcestreamcsourcestream-constructor"></a>Constructor CSourceStream. CSourceStream

Método de constructor.

## <a name="syntax"></a>Sintaxis


```C++
CSourceStream(
   TCHAR   *pObjectName,
   HRESULT *phr,
   CSource *pms,
   LPCWSTR pName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pObjectName* 
</dt> <dd>

Puntero a una cadena que contiene el nombre de depuración del código PIN.

</dd> <dt>

*phr* 
</dt> <dd>

Puntero a una variable que recibe un valor **HRESULT** que indica si el método se ha ejecutado correctamente o no. Inicialice el valor a S \_ OK antes de crear el objeto. Solo se cambia el valor si se produce un error.

</dd> <dt>

*jefes* 
</dt> <dd>

Puntero al filtro [**CSource**](csource.md) que creó este pin.

</dd> <dt>

*pName* 
</dt> <dd>

Puntero a una cadena que contiene el nombre del PIN.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La cadena especificada en el parámetro *pObjectName* solo se usa para la depuración. Para obtener más información, vea [**CBaseObject**](cbaseobject.md).

La cadena especificada en el parámetro *pName* es el nombre devuelto por el método [**IPin:: QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) . La `CSourceStream` clase no usa este nombre para el identificador de PIN devuelto por el método [**CSourceStream:: queryId**](csourcestream-queryid.md) . En su lugar, **queryId** calcula un identificador de PIN basado en el número de PIN. (Los identificadores de PIN admiten la persistencia de gráficos. Para obtener más información, vea [**IPin:: queryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid)).

El constructor agrega automáticamente el PIN al filtro propietario llamando a [**CSource:: AddPin**](csource-addpin.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




