---
description: Evalúa una expresión y produce una excepción de punto de interrupción si la expresión es FALSE. El texto de la expresión, el nombre del archivo de origen y el número de línea se registran mediante la macro DbgLog. Se omite en las compilaciones comerciales.
ms.assetid: fd116403-df23-490f-b3a8-b2a8bf2b4a5f
title: Macro HEXADECIMALSERT (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KASSERT
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: a1eb6738ea3e9d4535bf9f8291dc71349d67bb51d143b6bc73e83290f36657cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817062"
---
# <a name="kassert-macro"></a>Macro DE MACROS DEERT

Evalúa una expresión y produce una excepción de punto de interrupción si la expresión es **FALSE.** El texto de la expresión, el nombre del archivo de origen y el número de línea se registran mediante la [**macro DbgLog.**](dbglog.md) Se omite en las compilaciones comerciales.

## <a name="syntax"></a>Sintaxis


```C++
void KASSERT(
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

## <a name="remarks"></a>Comentarios

A diferencia [**de las**](assert.md) macros ASSERT y [**EXECUTE \_ ASSERT,**](execute-assert.md) esta macro no muestra un cuadro de mensaje que solicita al usuario. En las compilaciones de depuración, si la expresión es **FALSE**, la macro hace automáticamente una excepción de punto de interrupción.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wxdebug.h (incluir Secuencias.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Aserción y macros de punto de interrupción](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




