---
description: Evalúa una expresión y produce una excepción de punto de interrupción Si la expresión es falsa. El texto de la expresión, el nombre del archivo de código fuente y el número de línea se registran con la macro DbgLog. Se omite en las compilaciones comerciales.
ms.assetid: fd116403-df23-490f-b3a8-b2a8bf2b4a5f
title: Macro KASSERT (Wxdebug. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681185"
---
# <a name="kassert-macro"></a>KASSERT (macro)

Evalúa una expresión y produce una excepción de punto de interrupción Si la expresión es **falsa**. El texto de la expresión, el nombre del archivo de código fuente y el número de línea se registran con la macro [**DbgLog**](dbglog.md) . Se omite en las compilaciones comerciales.

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

Esta macro no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

A diferencia de las macros [**Assert**](assert.md) y [**Execute \_ Assert**](execute-assert.md) , esta macro no muestra un cuadro de mensaje que pide al usuario. En las compilaciones de depuración, si la expresión es **falsa**, la macro provoca automáticamente que se produzca una excepción de punto de interrupción.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wxdebug. h (incluir streams. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Macros Assert y Breakpoint](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




