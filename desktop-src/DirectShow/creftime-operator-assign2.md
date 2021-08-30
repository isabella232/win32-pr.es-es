---
description: El operador = asigna una nueva hora de referencia. Este método usa el *parámetro ll.*
ms.assetid: 556c2e8a-4726-42ab-949d-9a028ebb1b95
title: 'Método CRefTime.operator= (Reftime.h): parámetro ll'
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
ms.openlocfilehash: 9c7ed872807af0ad6b8512f842aa9c91b6706f9e430fabf2d9c16f03f47dd67a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108065"
---
# <a name="creftimeoperator-method-reftimeh---ll-parameter"></a>Método CRefTime.operator= (Reftime.h): parámetro ll

El operador = asigna una nueva hora de referencia.

## <a name="syntax"></a>Sintaxis


```C++
CRefTime& operator=(
   const LONGLONG ll
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Ll* 
</dt> <dd>

Nuevo tiempo de referencia, en unidades de 100 nanosegundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve una referencia al objeto .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado  | Reftime.h (incluir Secuencias.h)                                                                                   |
| Biblioteca | Strmbase.lib (compilaciones comerciales); Strmbasd.lib (compilaciones de depuración) |



 

 




