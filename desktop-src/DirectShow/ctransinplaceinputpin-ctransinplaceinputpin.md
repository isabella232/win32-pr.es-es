---
description: 'Constructor CTransInPlaceInputPin.CTransInPlaceInputPin: método constructor.'
ms.assetid: db0a3f78-ddb9-43b5-aab5-da2faaebb527
title: Constructor CTransInPlaceInputPin.CTransInPlaceInputPin (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.CTransInPlaceInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6f97c89142e43691c91b2a4c0d04721d9112ed49
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160178"
---
# <a name="ctransinplaceinputpinctransinplaceinputpin-constructor"></a>Constructor CTransInPlaceInputPin.CTransInPlaceInputPin

Método constructor.

## <a name="syntax"></a>Sintaxis


```C++
CTransInPlaceInputPin(
   TCHAR               *pObjectName,
   CTransInPlaceFilter *pFilter,
   HRESULT             *phr,
   LPCWSTR             pName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pObjectName* 
</dt> <dd>

Cadena que contiene el nombre de depuración del objeto. Para obtener más información, vea [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*pFilter* 
</dt> <dd>

Puntero al filtro que creó este pin, que debe ser [**un objeto CTransInPlaceFilter.**](ctransinplacefilter.md)

</dd> <dt>

*Phr* 
</dt> <dd>

Puntero a una variable que recibe un **valor HRESULT** que indica el éxito o error del método. Inicialice el valor en S \_ OK antes de crear el objeto . El valor solo se cambia si se produce un error.

</dd> <dt>

*pName* 
</dt> <dd>

Cadena de caracteres anchos que contiene el nombre del pin.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El *parámetro pName* especifica el nombre del pin, que devuelve el [**método IPin::QueryPinInfo.**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) Sin embargo, esta cadena no se usa para el identificador de pin. El identificador de pin de esta clase siempre es In. Para obtener más información, [**vea CTransformInputPin::QueryId**](ctransforminputpin-queryid.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transip.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CTransInPlaceInputPin (clase)**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




