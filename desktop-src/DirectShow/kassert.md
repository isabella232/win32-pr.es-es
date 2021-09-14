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
ms.openlocfilehash: f797e60a6175a86f2c1c9d675e9607a48a58c14a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061045"
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

## <a name="remarks"></a>Observaciones

A diferencia [**de las**](assert.md) macros ASSERT y [**EXECUTE \_ ASSERT,**](execute-assert.md) esta macro no muestra un cuadro de mensaje que solicita al usuario. En las compilaciones de depuración, si la expresión es **FALSE**, la macro hace automáticamente una excepción de punto de interrupción.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wxdebug.h (incluir Secuencias.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Aserción y macros de punto de interrupción](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




