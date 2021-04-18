---
description: Produce una excepción de punto de interrupción y registra la cadena especificada mediante la macro DbgLog. Se omite en las compilaciones comerciales.
ms.assetid: 475810db-692b-4727-9ef1-ece74e9618d0
title: Macro KDbgBreak (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KDbgBreak
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 9631dc8d956652137810b25ae5923cc1c6927bee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690019"
---
# <a name="kdbgbreak-macro"></a>KDbgBreak (macro)

Produce una excepción de punto de interrupción y registra la cadena especificada mediante la macro [**DbgLog**](dbglog.md) . Se omite en las compilaciones comerciales.

## <a name="syntax"></a>Sintaxis


```C++
void KDbgBreak(
    strLiteral
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*strLiteral* 
</dt> <dd>

Cadena de texto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta macro no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

A diferencia de la macro [**DbgBreak**](dbgbreak.md) , esta macro no muestra un cuadro de mensaje que pide al usuario. En las compilaciones de depuración, provoca automáticamente que se produzca una excepción de punto de interrupción.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wxdebug. h (incluir streams. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Macros Assert y Breakpoint](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




