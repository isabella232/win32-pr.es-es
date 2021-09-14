---
description: 'Constructor CTransformOutputPin.CTransformOutputPin: método constructor.'
ms.assetid: 6213ce92-d98a-4fb6-b66c-e7cdea6dff0d
title: Constructor CTransformOutputPin.CTransformOutputPin (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CTransformOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a1f7cb9dd811c878eba258a6087e00a85d4c24a0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255375"
---
# <a name="ctransformoutputpinctransformoutputpin-constructor"></a>Constructor CTransformOutputPin.CTransformOutputPin

Método constructor.

## <a name="syntax"></a>Sintaxis


```C++
CTransformOutputPin(
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

El *parámetro pName* especifica el nombre del pin, que devuelve el [**método IPin::QueryPinInfo.**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) Sin embargo, la cadena no se usa para el identificador de pin. El identificador de pin de esta clase siempre es "Out". Para obtener más información, vea [**QueryId**](ctransformoutputpin-queryid.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




