---
description: Método de constructor.
ms.assetid: e8cb5f1d-171f-4bf8-8ab6-6e547c4678d2
title: Constructor CBasePin. CBasePin (Amfilter. h)
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
ms.openlocfilehash: dd4883d3d8e906e1da2f377344b735037c5e5cd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671636"
---
# <a name="cbasepincbasepin-constructor"></a>Constructor CBasePin. CBasePin

Método de constructor.

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

Cadena que contiene el nombre de depuración para el objeto. Para obtener más información, vea [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*pFilter* 
</dt> <dd>

Puntero al filtro que creó este pin.

</dd> <dt>

*pLock* 
</dt> <dd>

Puntero a un bloqueo de [**CCritSec**](ccritsec.md) , que se usa para serializar los cambios de estado. Puede ser la misma sección crítica que el bloqueo de filtro, [**CBaseFilter:: m \_ Plock**](cbasefilter-m-plock.md).

</dd> <dt>

*phr* 
</dt> <dd>

Puntero a una variable que recibe un valor **HRESULT** que indica si el método se ha ejecutado correctamente o no. Inicialice el valor a S \_ OK antes de crear el objeto. Solo se cambia el valor si se produce un error.

</dd> <dt>

*pName* 
</dt> <dd>

Cadena de caracteres anchos que contiene el nombre del PIN. Para obtener más información, vea [**CBasePin:: QueryPinInfo**](cbasepin-querypininfo.md).

</dd> <dt>

*dir* 
</dt> <dd>

Miembro de la enumeración de [**\_ dirección del PIN**](/windows/win32/api/strmif/ne-strmif-pin_direction) que especifica la dirección del PIN.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La sección crítica especificada por *Plock* serializa el estado del PIN, incluido el estado de la conexión, la elección del asignador, el tipo de medio y el estado de las operaciones de vaciado. No utilice esta sección crítica para serializar las operaciones de streaming. Para obtener más información, vea [flujo de datos en el gráfico de filtros](data-flow-in-the-filter-graph.md).

Un filtro podría crear PIN en su método de constructor, por lo que en este punto el puntero *pFilter* podría no hacer referencia a un objeto válido. Almacene el puntero, pero no desreferenciarlo mientras esté dentro del constructor del PIN.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBasePin**](cbasepin.md)
</dt> </dl>

 

 




