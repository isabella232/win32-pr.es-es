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
ms.openlocfilehash: 5b5e0d9a5a16a963b67643823e5e3b547a1076fc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061722"
---
# <a name="creftimeoperator-method"></a>Método CRefTime.operator+=

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



 

 




