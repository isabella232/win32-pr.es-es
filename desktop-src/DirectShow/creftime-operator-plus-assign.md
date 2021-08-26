---
description: El operador += agrega dos tiempos de referencia.
ms.assetid: 016d3dac-4d7c-490a-83aa-1d88a2080748
title: Método CRefTime.operator+= (Reftime.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator+=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2280eca51cef8c84cb51f806a0c95748070459bf0a48670ca6144b2d499fd337
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108055"
---
# <a name="creftimeoperator-method"></a>CRefTime.operator+= (método)

El operador += agrega dos tiempos de referencia.

## <a name="syntax"></a>Sintaxis


```C++
CRefTime& operator+=(
  [ref] const CRefTime &rt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*rt* \[ Ref\]
</dt> <dd>

Referencia a un **objeto CRefTime.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve una referencia al objeto .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Reftime.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




