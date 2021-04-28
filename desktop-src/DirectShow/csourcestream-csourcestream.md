---
description: 'Constructor CSourceStream.CSourceStream: método constructor.'
ms.assetid: 9078b2f5-b11e-4780-8143-6738e9df4f4b
title: Constructor CSourceStream.CSourceStream (Source.h)
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
ms.openlocfilehash: 75d94bb89ca109c2a7974c294153d46235f92f23
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085193"
---
# <a name="csourcestreamcsourcestream-constructor"></a>Constructor CSourceStream.CSourceStream

Método constructor.

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

Puntero a una cadena que contiene el nombre de depuración del pin.

</dd> <dt>

*Phr* 
</dt> <dd>

Puntero a una variable que recibe un **valor HRESULT** que indica el éxito o error del método. Inicialice el valor en S \_ OK antes de crear el objeto . El valor solo se cambia si se produce un error.

</dd> <dt>

*Pms* 
</dt> <dd>

Puntero al [**filtro CSource**](csource.md) que creó este pin.

</dd> <dt>

*pName* 
</dt> <dd>

Puntero a una cadena que contiene el nombre del pin.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La cadena especificada en el *parámetro pObjectName* solo se usa con fines de depuración. Para obtener más información, vea [**CBaseObject**](cbaseobject.md).

La cadena especificada en el *parámetro pName* es el nombre devuelto por el [**método IPin::QueryPinInfo.**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) La `CSourceStream` clase no usa este nombre para el identificador de pin devuelto por el método [**CSourceStream::QueryId.**](csourcestream-queryid.md) En su lugar, **QueryId** calcula un identificador de pin basado en el número de pin. (Los identificadores de pin admiten la persistencia del grafo. Para obtener más información, [**vea IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid)).

El constructor agrega automáticamente el pin al filtro propietario, llamando a [**CSource::AddPin**](csource-addpin.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source.h (incluir Streams.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CSourceStream (clase)**](csourcestream.md)
</dt> </dl>

 

 




