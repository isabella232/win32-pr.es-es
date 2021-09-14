---
description: 'Constructor CEnumPins.CEnumPins: método constructor.'
ms.assetid: f696e433-b051-4de0-80e5-f9cd31fd0f23
title: Constructor CEnumPins.CEnumPins (Amfilter.h)
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
ms.openlocfilehash: caa27dfe0190df15be1e41b7128c06249f1ae2b8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973879"
---
# <a name="cenumpinscenumpins-constructor"></a>Constructor CEnumPins.CEnumPins

Método constructor.

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

Puntero al filtro en el que se enumeran los pines.

</dd> <dt>

*pEnumPins* 
</dt> <dd>

Puntero a la [**interfaz IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) de un enumerador que se clona, o **NULL.**

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si *pEnumPins* es **NULL,** este método inicializa el enumerador al principio de la secuencia de enumeración. De lo contrario, duplica el estado interno del enumerador especificado por *pEnumPins*.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CEnumPins (clase)**](cenumpins.md)
</dt> </dl>

 

 




