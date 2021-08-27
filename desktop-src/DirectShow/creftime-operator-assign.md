---
description: El operador = asigna una nueva hora de referencia.
ms.assetid: 0b11e2ea-23dc-4c75-88c6-94215a4b14b6
title: Método CRefTime.operator= (Reftime.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f4fe9a8f6f40dd1d0a7b0e38339c3ab21c44a989648e6c032b17a0ed3ac3b4f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108075"
---
# <a name="creftimeoperator-method-reftimeh"></a>Método CRefTime.operator= (Reftime.h)

El operador = asigna una nueva hora de referencia.

## <a name="syntax"></a>Sintaxis


```C++
CRefTime& operator=(
  [ref] const CRefTime &rt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*rt* \[ Ref\]
</dt> <dd>

Referencia a un **objeto CRefTime** que especifica la nueva hora de referencia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve una referencia al objeto .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Reftime.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




