---
description: 'Constructor CDynamicOutputPin.CDynamicOutputPin: método constructor.'
ms.assetid: 996adc69-8727-431e-a7f5-8fbcc0e305ae
title: Constructor CDynamicOutputPin.CDynamicOutputPin (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.CDynamicOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4fe6dad14399b5b124b0146ea8b7ca101c8fa817
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099313"
---
# <a name="cdynamicoutputpincdynamicoutputpin-constructor"></a>Constructor CDynamicOutputPin.CDynamicOutputPin

Método constructor.

## <a name="syntax"></a>Sintaxis


```C++
CDynamicOutputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pObjectName* 
</dt> <dd>

Puntero a una cadena que contiene el nombre del objeto. Para obtener más información, vea [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*pFilter* 
</dt> <dd>

Puntero al filtro que creó este pin.

</dd> <dt>

*Plock* 
</dt> <dd>

Puntero a un [**bloqueo CCritSec,**](ccritsec.md) que se usa para serializar los cambios de estado. Use la misma sección crítica que el bloqueo de filtro, [ **CBaseFilter::m \_ pLock.**](cbasefilter-m-plock.md)

</dd> <dt>

*Phr* 
</dt> <dd>

Puntero a una variable que recibe un **valor HRESULT** que indica el éxito o error del método. Inicialice el valor en S \_ OK antes de crear el objeto . El valor solo se cambia si se produce un error.

</dd> <dt>

*pName* 
</dt> <dd>

Puntero a una cadena de caracteres anchos que contiene el identificador de pin. Para obtener más información, [**vea IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Streams.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CDynamicOutputPin (clase)**](cdynamicoutputpin.md)
</dt> </dl>

 

 




