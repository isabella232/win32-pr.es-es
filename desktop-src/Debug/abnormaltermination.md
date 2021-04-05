---
description: Indica si el \_ \_ bloque try de un controlador de terminación terminó normalmente. Solo se puede llamar a la función desde dentro del \_ \_ bloque Finally de un controlador de finalización.
ms.assetid: 0ddaef1f-03f0-45fc-9c5e-8d6a26a73245
title: AbnormalTermination (macro)
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
ms.openlocfilehash: 7c4869f36d8ba70c8dcd8ca526949d489f455e8c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000748"
---
# <a name="abnormaltermination-macro"></a>AbnormalTermination (macro)

Indica si el bloque **\_ \_ try** de un controlador de terminación terminó normalmente. Solo se puede llamar a la función desde dentro del bloque **\_ \_ Finally** de un controlador de finalización.

> [!Note]  
> El compilador de optimización de C/C++ de Microsoft interpreta esta función como una palabra clave y su uso fuera de la sintaxis de control de excepciones adecuada genera un error del compilador.

 

## <a name="syntax"></a>Sintaxis


```C++
BOOL AbnormalTermination(void);
```



## <a name="parameters"></a>Parámetros

Esta macro no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si el bloque **\_ \_ try** terminó de forma anómala, el valor devuelto es distinto de cero.

Si el bloque **\_ \_ try** terminó normalmente, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

El bloque **\_ \_ try** finaliza normalmente solo si la ejecución deja el bloque secuencialmente después de ejecutar la última instrucción del bloque. Las instrucciones (como **Return**, **goto**, **continue** o **break**) que provocan que la ejecución deje el bloque **\_ \_ try** dan como resultado una terminación anómala del bloque. Este es el caso incluso si dicha instrucción es la última instrucción del bloque **\_ \_ try** .

La terminación anómala de un bloque **\_ \_ try** hace que el sistema busque hacia atrás en todos los marcos de pila para determinar si se debe llamar a algún controlador de finalización. Esto puede dar lugar a la ejecución de cientos de instrucciones, por lo que es importante evitar la terminación anómala de un bloque **\_ \_ try** debido a una instrucción **Return**, **goto**, **continue** o **break** . Tenga en cuenta que estas instrucciones no generan una excepción, aunque la terminación sea anómala.

Para evitar la terminación anómala, la ejecución debería continuar hasta el final del bloque. También puede ejecutar la instrucción **\_ \_ leave** . La instrucción **\_ \_ leave** permite la terminación inmediata del bloque **\_ \_ try** sin causar una terminación anómala y su penalización en el rendimiento. Consulte la documentación del compilador para determinar si se admite la instrucción **\_ \_ leave** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de control de excepciones estructurado](structured-exception-handling-functions.md)
</dt> <dt>

[Información general sobre el control estructurado de excepciones](structured-exception-handling.md)
</dt> </dl>

 

 




