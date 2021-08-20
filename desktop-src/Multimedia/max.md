---
title: max macro (Minwindef.h)
description: La macro max compara dos valores y devuelve el mayor. El tipo de datos puede ser cualquier tipo de datos numérico, con signo o sin signo. El tipo de datos de los argumentos y el valor devuelto es el mismo.
ms.assetid: 224d2ef7-6764-49c0-9782-51bfadbfb77f
keywords:
- max macro Windows Multimedia
topic_type:
- apiref
api_name:
- max
api_location:
- minwindef.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc592fcc588c14ee04c1f595c5b5bc95c860b2ab0b761906886010db478d5f1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138651"
---
# <a name="max-macro"></a>max (macro)

La **macro** max compara dos valores y devuelve el mayor. El tipo de datos puede ser cualquier tipo de datos numérico, con signo o sin signo. El tipo de datos de los argumentos y el valor devuelto es el mismo.

## <a name="syntax"></a>Sintaxis


```C++
 max(
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

El valor devuelto es el mayor de los dos valores especificados.

## <a name="remarks"></a>Comentarios

La **macro** max se define de la siguiente manera:


```C++
#define max(a, b)  (((a) > (b)) ? (a) : (b)) 
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Minwindef.h</dt> </dl> |



 

 





