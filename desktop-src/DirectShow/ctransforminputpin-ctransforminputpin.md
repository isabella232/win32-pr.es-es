---
description: 'Constructor CTransformInputPin.CTransformInputPin: método constructor.'
ms.assetid: 097dce19-b430-42d6-8914-68350c7eca40
title: Constructor CTransformInputPin.CTransformInputPin (Transfrm.h)
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
ms.openlocfilehash: 4e893b4e1c7d4f396644a468d3d71fa3046fb712
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255465"
---
# <a name="ctransforminputpinctransforminputpin-constructor"></a>Constructor CTransformInputPin.CTransformInputPin

Método constructor.

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

Puntero al filtro que creó este pin, que debe ser un [**objeto CTransformFilter.**](ctransformfilter.md)

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

El *parámetro pName* especifica el nombre del pin, que devuelve el [**método IPin::QueryPinInfo.**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) Sin embargo, la cadena no se usa para el identificador de pin. El identificador de pin de esta clase siempre es "In". Para obtener más información, vea [**QueryId**](ctransforminputpin-queryid.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




