---
description: Evalúa una expresión en las compilaciones de depuración y comerciales. En compilaciones de depuración, muestra un mensaje de diagnóstico si la expresión es falsa.
ms.assetid: 259a3d30-0b20-4430-8b74-83ec619576ae
title: Macro EXECUTE_ASSERT (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXECUTE_ASSERT
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 5db5e78d198cc9f66aa5de6fdb0160e325b82591
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105654001"
---
# <a name="execute_assert-macro"></a>EJECUTAR \_ macro Assert

Evalúa una expresión en las compilaciones de depuración y comerciales. En compilaciones de depuración, muestra un mensaje de diagnóstico si la expresión es **falsa**.

## <a name="syntax"></a>Sintaxis


```C++
void EXECUTE_ASSERT(
    cond
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Cond* 
</dt> <dd>

Expresión que se va a evaluar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta macro no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

A diferencia de la macro [**Assert**](assert.md) , esta macro evalúa la expresión en las compilaciones comerciales. En las compilaciones de depuración, si la expresión es **falsa**, la macro muestra un cuadro de mensaje con el texto de la expresión, el nombre del archivo de código fuente y el número de línea. El usuario puede omitir la aserción, entrar en el depurador o salir de la aplicación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wxdebug. h (incluir streams. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Macros Assert y Breakpoint](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




