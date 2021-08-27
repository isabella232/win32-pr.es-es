---
title: Modificador /error
description: El modificador /error determina los tipos de comprobación de errores que realizarán los códigos auxiliares generados en tiempo de ejecución.
ms.assetid: abd3616a-2d2c-4a7d-bf3a-c84a43387894
keywords:
- /error switch MIDL
topic_type:
- apiref
api_name:
- /error
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7af27de3d83171c8f1f89d0b860bf0b38ddfb6639a12bf40f90a58f06a273cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105635"
---
# <a name="error-switch"></a>Modificador /error

El **modificador /error** determina los tipos de comprobación de errores que realizarán los códigos auxiliares generados en tiempo de ejecución.

> [!Note]  
> Esta característica está obsoleta y ya no se admite. Se recomienda el uso [**del modificador /robust.**](-robust.md)

 

``` syntax
midl /error { allocation | stub_data | ref | bounds_check | none | all }
```

## <a name="switch-options"></a>Cambiar opciones

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="allocation"></span><span id="ALLOCATION"></span>

<span id="allocation"></span><span id="ALLOCATION"></span>allocation**


</dt> <dd>

Comprueba si [**la asignación \_ de usuario \_ medio**](midl-user-allocate-1.md) devuelve **un valor NULL,** lo que indica un error de memoria fuera de memoria.

</dd> <dt>

<span id="stub_data"></span><span id="STUB_DATA"></span>

<span id="stub_data"></span><span id="STUB_DATA"></span>datos \_ de código auxiliar**


</dt> <dd>

Genera un código auxiliar que detecta las excepciones de desmarque en el lado servidor y las propaga de nuevo al cliente.

</dd> <dt>

<span id="ref"></span><span id="REF"></span>

<span id="ref"></span><span id="REF"></span>ref**


</dt> <dd>

Genera código que ejecuta una comprobación en tiempo de ejecución para asegurarse de que no se pasan punteros de referencia **NULL** a los códigos auxiliares de cliente y genera una excepción RPC X NULL REF POINTER si encuentra \_ \_ \_ \_ alguna.

</dd> <dt>

<span id="bounds_check"></span><span id="BOUNDS_CHECK"></span>

<span id="bounds_check"></span><span id="BOUNDS_CHECK"></span>bounds \_ check**


</dt> <dd>

Comprueba el tamaño de las matrices conformes y variables con respecto a la especificación de longitud de transmisión.

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span id="none"></span><span id="NONE"></span>none**


</dt> <dd>

No realiza ninguna comprobación de errores.

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span id="all"></span><span id="ALL"></span>all**


</dt> <dd>

Realiza todas las comprobación de errores. A partir de la versión 5.0 de MIDL, se trata de un modificador del compilador predeterminado.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

El **modificador /error** selecciona el número de comprobaciones de error que realizarán los archivos de código auxiliar generados. A partir de la versión 5.0 de MIDL, el valor predeterminado es **/error all**.

Los errores de enumeración que se comprueban (de forma predeterminada en todas  las versiones de MIDL) son errores  de truncamiento causados al convertir entre tipos de enumeración largos (enteros de 32 bits) y tipos de enumeración cortos (la representación de datos de red de [**la**](enum.md)enumeración ) y el número de identificadores de una enumeración superior a 32 767.

La comprobación de errores de acceso a memoria (también de forma predeterminada en todas las versiones de MIDL) es para los punteros que superan el final del búfer en el código de serialización y para las matrices compatibles cuyo tamaño es menor que cero. Use la **marca de comprobación /error bounds \_** para comprobar si hay otros límites de matriz no válidos.

Al especificar la **asignación /error**, los códigos auxiliares incluyen código que genera una excepción cuando la asignación de usuario medio devuelve 0. [**\_ \_**](midl-user-allocate-1.md)

La **opción /error stub \_ data** impide que los datos de cliente se bloquean en el servidor durante la desmarque, lo que proporciona un método más sólido para controlar la operación de desmarque.

A partir de Windows 2000, el motor de serialización MARSHAL en tiempo de ejecución subyacente realiza la mayoría de estas comprobaciones. Esto significa que si usa uno de los modos totalmente interpretados ([**/Oi**](-oi.md), **/Oif)** de generación de código auxiliar, la elección de diferentes opciones de comprobación de errores no tendrá un efecto marcado en el rendimiento.

## <a name="examples"></a>Ejemplos

**midl /error allocation filename.idl**

**midl /error none filename.idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/robust**](-robust.md)
</dt> </dl>

 

 




