---
title: min (macro) (Minwindef. h)
description: La macro min compara dos valores y devuelve el menor. El tipo de datos puede ser cualquier tipo de datos numérico, con signo o sin signo. El tipo de datos de los argumentos y el valor devuelto es el mismo.
ms.assetid: c7d5094c-6f26-4799-95c8-804a8b48d39e
keywords:
- min macros multimedia de Windows
topic_type:
- apiref
api_name:
- min
api_location:
- minwindef.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b50680d5902ae2dc895f53f023c4b229b03c7e86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804094"
---
# <a name="min-macro"></a>min (macro)

La macro **min** compara dos valores y devuelve el menor. El tipo de datos puede ser cualquier tipo de datos numérico, con signo o sin signo. El tipo de datos de los argumentos y el valor devuelto es el mismo.

## <a name="syntax"></a>Sintaxis


```C++
 min(
    value1,
    value2
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*value1* 
</dt> <dd>

Especifica el primero de dos valores.

</dd> <dt>

*value2* 
</dt> <dd>

Especifica el segundo de dos valores.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el menor de los dos valores especificados.

## <a name="remarks"></a>Observaciones

La macro **min** se define de la siguiente manera:


```C++
#define min(a, b)  (((a) < (b)) ? (a) : (b)) 
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Minwindef. h</dt> </dl> |



 

 





