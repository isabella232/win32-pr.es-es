---
description: Método de constructor.
ms.assetid: f696e433-b051-4de0-80e5-f9cd31fd0f23
title: Constructor CEnumPins. CEnumPins (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.CEnumPins
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 536782de6992acfc1613d5866f13af658fba6e71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671155"
---
# <a name="cenumpinscenumpins-constructor"></a>Constructor CEnumPins. CEnumPins

Método de constructor.

## <a name="syntax"></a>Sintaxis


```C++
CEnumPins(
   CBaseFilter *pFilter,
   CEnumPins   *pEnumPins
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFilter* 
</dt> <dd>

Puntero al filtro en el que se enumeran los pin.

</dd> <dt>

*pEnumPins* 
</dt> <dd>

Puntero a la interfaz [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) de un enumerador que se va a clonar o **null**.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si *pEnumPins* es **null**, este método inicializa el enumerador al principio de la secuencia de enumeración. De lo contrario, duplica el estado interno del enumerador especificado por *pEnumPins*.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CEnumPins**](cenumpins.md)
</dt> </dl>

 

 




