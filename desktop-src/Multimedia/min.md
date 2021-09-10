---
title: min macro (Minwindef.h)
description: La macro min compara dos valores y devuelve el más pequeño. El tipo de datos puede ser cualquier tipo de datos numérico, con signo o sin signo. El tipo de datos de los argumentos y el valor devuelto es el mismo.
ms.assetid: c7d5094c-6f26-4799-95c8-804a8b48d39e
keywords:
- min macro Windows Multimedia
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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370147"
---
# <a name="min-macro"></a>min (macro)

La **macro** min compara dos valores y devuelve el más pequeño. El tipo de datos puede ser cualquier tipo de datos numérico, con signo o sin signo. El tipo de datos de los argumentos y el valor devuelto es el mismo.

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

La **macro** min se define de la siguiente manera:


```C++
#define min(a, b)  (((a) < (b)) ? (a) : (b)) 
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Minwindef.h</dt> </dl> |



 

 





