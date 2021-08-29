---
description: Indica si el bloque \_ \_ try de un controlador de terminación finalizó con normalidad. Solo se puede llamar a la función desde el bloque \_ \_ finally de un controlador de terminación.
ms.assetid: 0ddaef1f-03f0-45fc-9c5e-8d6a26a73245
title: Macro AbnormalTermination
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AbnormalTermination
api_type:
- NA
api_location: ''
ms.openlocfilehash: 137d6667c993d4a107be057e46c4ee469a513ec95d358b6d3cc50654a5bba520
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957134"
---
# <a name="abnormaltermination-macro"></a>Macro AbnormalTermination

Indica si el bloque **\_ \_ try** de un controlador de terminación finalizó con normalidad. Solo se puede llamar a la función desde el bloque **\_ \_ finally** de un controlador de terminación.

> [!Note]  
> El compilador de optimización de Microsoft C/C++ interpreta esta función como una palabra clave y su uso fuera de la sintaxis adecuada de control de excepciones genera un error del compilador.

 

## <a name="syntax"></a>Sintaxis


```C++
BOOL AbnormalTermination(void);
```



## <a name="parameters"></a>Parámetros

Esta macro no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si el **\_ \_ bloque try** finalizó de forma anómala, el valor devuelto es distinto de cero.

Si el **\_ \_ bloque try** finalizó con normalidad, el valor devuelto es cero.

## <a name="remarks"></a>Comentarios

El **\_ \_ bloque try** finaliza normalmente solo si la ejecución sale del bloque secuencialmente después de ejecutar la última instrucción del bloque. Las instrucciones (como **return**, **goto**, **continue** o **break)** que hacen que la ejecución deje el resultado del bloque **\_ \_ try** en una terminación anómala del bloque. Este es el caso incluso si esta instrucción es la última instrucción del **\_ \_ bloque try.**

La terminación anómala de **\_ \_ un bloque try** hace que el sistema busque hacia atrás en todos los marcos de pila para determinar si se debe llamar a los controladores de terminación. Esto puede dar lugar **a** la ejecución de cientos de instrucciones, por lo que es importante evitar la terminación anómala de un bloque **\_ \_ try** debido a una instrucción return , **goto**, **continue** **o break.** Tenga en cuenta que estas instrucciones no generan una excepción, aunque la terminación sea anómala.

Para evitar la terminación anómala, la ejecución debe continuar hasta el final del bloque. También puede ejecutar la **\_ \_ instrucción leave.** La **\_ \_ instrucción leave** permite la terminación inmediata del bloque **\_ \_ try** sin provocar una terminación anómala y su penalización de rendimiento. Compruebe la documentación del compilador para determinar si se admite la instrucción **\_ \_ leave.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones estructuradas de control de excepciones](structured-exception-handling-functions.md)
</dt> <dt>

[Información general sobre el control estructurado de excepciones](structured-exception-handling.md)
</dt> </dl>

 

 




