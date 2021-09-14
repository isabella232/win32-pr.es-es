---
description: Evalúa una expresión en compilaciones de depuración y comercial. En las compilaciones de depuración, muestra un mensaje de diagnóstico si la expresión es FALSE.
ms.assetid: 259a3d30-0b20-4430-8b74-83ec619576ae
title: EXECUTE_ASSERT macro (Wxdebug.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255224"
---
# <a name="execute_assert-macro"></a>Execute \_ ASSERT macro

Evalúa una expresión en compilaciones de depuración y comercial. En las compilaciones de depuración, muestra un mensaje de diagnóstico si la expresión es **FALSE.**

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

Esta macro no devuelve un valor.

## <a name="remarks"></a>Observaciones

A diferencia de la macro [**ASSERT,**](assert.md) esta macro evalúa la expresión en las compilaciones comerciales. En las compilaciones de depuración, si la expresión es **FALSE,** la macro muestra un cuadro de mensaje con el texto de la expresión, el nombre del archivo de origen y el número de línea. El usuario puede omitir la aserción, escribir el depurador o salir de la aplicación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wxdebug.h (incluir Secuencias.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Aserción y macros de punto de interrupción](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




