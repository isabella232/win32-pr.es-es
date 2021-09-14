---
description: Este operador asigna una nueva hora de referencia.
ms.assetid: ae6a33ab-f4e0-4f1c-80a0-8a25ee1e9dc5
title: Método COARefTime.operator= (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3f5a051cea555975fd8606c3693d4b7d63cb9ce4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061257"
---
# <a name="coareftimeoperator-method-ctlutilh"></a>Método COARefTime.operator= (Ctlutil.h)

Este operador asigna una nueva hora de referencia.

## <a name="syntax"></a>Sintaxis


```C++
COARefTime& operator=(
  [ref] const double &rd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*rd* \[ Ref\]
</dt> <dd>

Referencia a un **valor double** que especifica el nuevo tiempo de referencia en segundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve una referencia al objeto .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**COARefTime (clase)**](coareftime.md)
</dt> </dl>

 

 




