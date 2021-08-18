---
description: 'Constructor CBasePin.CBasePin: método constructor.'
ms.assetid: e8cb5f1d-171f-4bf8-8ab6-6e547c4678d2
title: Constructor CBasePin.CBasePin (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CBasePin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cbeead09843aa8bf66471caeaabbdb42ee8d97d01cdaa9a54809f35c437b52d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916905"
---
# <a name="cbasepincbasepin-constructor"></a>Constructor CBasePin.CBasePin

Método constructor.

## <a name="syntax"></a>Sintaxis


```C++
CBasePin(
   TCHAR         *pObjectName,
   CBaseFilter   *pFilter,
   CCritSec      *pLock,
   HRESULT       *phr,
   LPCWSTR       pName,
   PIN_DIRECTION dir
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

Puntero al filtro que creó este pin.

</dd> <dt>

*Plock* 
</dt> <dd>

Puntero a un [**bloqueo CCritSec,**](ccritsec.md) que se usa para serializar los cambios de estado. Puede ser la misma sección crítica que el bloqueo de filtro, [**CBaseFilter::m \_ pLock**](cbasefilter-m-plock.md).

</dd> <dt>

*Phr* 
</dt> <dd>

Puntero a una variable que recibe un **valor HRESULT** que indica el éxito o error del método. Inicialice el valor en S \_ OK antes de crear el objeto . El valor solo se cambia si se produce un error.

</dd> <dt>

*pName* 
</dt> <dd>

Cadena de caracteres anchos que contiene el nombre del pin. Para obtener más información, [**vea CBasePin::QueryPinInfo**](cbasepin-querypininfo.md).

</dd> <dt>

*dir* 
</dt> <dd>

Miembro de la [**enumeración \_ PIN DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) que especifica la dirección del pin.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La sección crítica especificada por *pLock* serializa el estado del pin, incluido su estado de conexión, la elección del asignador, el tipo de medio y el estado de las operaciones de vaciado. No use esta sección crítica para serializar las operaciones de streaming. Para obtener más información, vea [Data Flow en filter Graph](data-flow-in-the-filter-graph.md).

Un filtro podría crear pasadores en su método de constructor, por lo que en este momento el *puntero pFilter* podría no hacer referencia a un objeto válido. Almacene el puntero, pero no desreferencialo dentro del constructor del pin.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBasePin (clase)**](cbasepin.md)
</dt> </dl>

 

 




