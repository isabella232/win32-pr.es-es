---
description: Método de constructor.
ms.assetid: 097dce19-b430-42d6-8914-68350c7eca40
title: Constructor CTransformInputPin. CTransformInputPin (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CTransformInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39b99e3e2cf1437c1b35f68d9863a692746bd98d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660684"
---
# <a name="ctransforminputpinctransforminputpin-constructor"></a>Constructor CTransformInputPin. CTransformInputPin

Método de constructor.

## <a name="syntax"></a>Sintaxis


```C++
CTransformInputPin(
   TCHAR            *pObjectName,
   CTransformFilter *pTransformFilter,
   HRESULT          *phr,
   LPCWSTR          pName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pObjectName* 
</dt> <dd>

Cadena que contiene el nombre de depuración del objeto. Para obtener más información, vea [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*pTransformFilter* 
</dt> <dd>

Puntero al filtro que creó este pin, que debe ser un objeto [**CTransformFilter**](ctransformfilter.md) .

</dd> <dt>

*phr* 
</dt> <dd>

Puntero a una variable que recibe un valor **HRESULT** que indica si el método se ha ejecutado correctamente o no. Inicialice el valor a S \_ OK antes de crear el objeto. Solo se cambia el valor si se produce un error.

</dd> <dt>

*pName* 
</dt> <dd>

Cadena de caracteres anchos que contiene el nombre del PIN.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El parámetro *pName* especifica el nombre del PIN, devuelto por el método [**IPin:: QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) . Sin embargo, la cadena no se utiliza para el identificador del PIN. El identificador del PIN para esta clase siempre es "in". Para obtener más información, vea [**queryId**](ctransforminputpin-queryid.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




