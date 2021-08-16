---
description: Evalúa una expresión y muestra un mensaje de diagnóstico si la expresión es FALSE. Se omite en las compilaciones comerciales.
ms.assetid: 8c3815bb-3164-4066-a947-974e791af5cd
title: Macro ASSERT (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ASSERT
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 1c64ae2256ae132fccdca6e483fae3f79d28b0cda66d7701acbe95abb1222d14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117824434"
---
# <a name="assert-macro"></a>ASSERT (macro)

Evalúa una expresión y muestra un mensaje de diagnóstico si la expresión es **FALSE.** Se omite en las compilaciones comerciales.

## <a name="syntax"></a>Sintaxis


```C++
void ASSERT(
   BOOL cond
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

En las compilaciones de depuración, si la expresión es **FALSE**, esta macro muestra un cuadro de mensaje con el texto de la expresión, el nombre del archivo de origen y el número de línea. El usuario puede omitir la aserción, escribir el depurador o salir de la aplicación.

## <a name="examples"></a>Ejemplos


```
ASSERT(rtStartTime <= rtEndTime);
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wxdebug.h (incluir Secuencias.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Aserción y macros de punto de interrupción](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




