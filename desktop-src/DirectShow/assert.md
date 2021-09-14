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
ms.openlocfilehash: 8617d1c86f655cc9b44ea6619931f73888ae2a67
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162242"
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

## <a name="remarks"></a>Observaciones

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

 

 




