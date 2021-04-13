---
title: /error (modificador)
description: El modificador/error determina los tipos de comprobación de errores que realizará el código auxiliar generado en tiempo de ejecución.
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
ms.openlocfilehash: f84a56c1ae3d57ab1931ec175aa8dc9010ea6b8a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419652"
---
# <a name="error-switch"></a>/error (modificador)

El modificador **/error** determina los tipos de comprobación de errores que realizará el código auxiliar generado en tiempo de ejecución.

> [!Note]  
> Esta característica está obsoleta y ya no se admite. Se recomienda el uso del modificador [**/Robust**](-robust.md) .

 

``` syntax
midl /error { allocation | stub_data | ref | bounds_check | none | all }
```

## <a name="switch-options"></a>Opciones de conmutador

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="allocation"></span><span id="ALLOCATION"></span>

<span id="allocation"></span><span id="ALLOCATION"></span>asignación * * * *


</dt> <dd>

Comprueba si el usuario de la [**\_ \_ asignación de MIDL**](midl-user-allocate-1.md) devuelve un valor **null** , lo que indica un error de memoria insuficiente.

</dd> <dt>

<span id="stub_data"></span><span id="STUB_DATA"></span>

<span id="stub_data"></span><span id="STUB_DATA"></span>datos de código auxiliar * * * * \_


</dt> <dd>

Genera un código auxiliar que detecta las excepciones de cálculo de referencias en el lado del servidor y los propaga de nuevo al cliente.

</dd> <dt>

<span id="ref"></span><span id="REF"></span>

<span id="ref"></span><span id="REF"></span>Ref * * * *


</dt> <dd>

Genera código que ejecuta una comprobación en tiempo de ejecución para garantizar que no se pasen punteros de referencia **nulos** al código auxiliar del cliente y genere una excepción de puntero de referencia null de RPC \_ X \_ \_ \_ si encuentra alguna.

</dd> <dt>

<span id="bounds_check"></span><span id="BOUNDS_CHECK"></span>

<span id="bounds_check"></span><span id="BOUNDS_CHECK"></span>comprobación de límites * * * * \_


</dt> <dd>

Comprueba el tamaño de las matrices variables y variables conformes con la especificación de longitud de transmisión.

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span id="none"></span><span id="NONE"></span>ninguno * * * *


</dt> <dd>

No realiza ninguna comprobación de errores.

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span id="all"></span><span id="ALL"></span>todo * * * *


</dt> <dd>

Realiza todas las comprobaciones de errores. A partir de la versión 5,0 de MIDL, se trata de un modificador de compilador predeterminado.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

El modificador **/error** selecciona el número de comprobaciones de errores que realizarán los archivos stub generados. A partir de la versión 5,0 de MIDL, el valor predeterminado es **/error All**.

Los errores de enumeración que se comprueban (de forma predeterminada en todas las versiones de MIDL) son errores de truncamiento producidos al convertir entre tipos de **enumeración largos** (enteros de 32 bits) y tipos de **enumeración cortos** (la representación de datos de red de [**enum**](enum.md)) y el número de identificadores en una enumeración que supera 32.767.

La comprobación de errores de acceso a memoria (también de forma predeterminada en todas las versiones de MIDL) es para punteros que superan el final del búfer en el cálculo de referencias de código y para matrices compatibles cuyo tamaño es menor que cero. Use la marca de **\_ comprobación** de los límites de/error para buscar otros límites de matriz no válidos.

Cuando se especifica **/error Allocation**, los códigos auxiliares incluyen código que genera una excepción cuando el usuario de la [**\_ \_ asignación de MIDL**](midl-user-allocate-1.md) devuelve 0.

La opción **/error stub \_ Data** evita que los datos del cliente bloqueen el servidor durante la desserialización, lo que proporciona eficazmente un método más eficaz para controlar la operación de desserialización.

En vigor con Windows 2000, el motor de serialización de NDR en tiempo de ejecución subyacente realiza la mayoría de estas comprobaciones. Esto significa que, si usa uno de los modos que se interpretan totalmente ([**/OI**](-oi.md), **/OIF**) de la generación de código auxiliar, la elección de distintas opciones de comprobación de errores no tendrá ningún efecto marcado en el rendimiento.

## <a name="examples"></a>Ejemplos

**MIDL/error enasignación FILENAME. idl**

**MIDL/error None nombreDeArchivo. idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Robust**](-robust.md)
</dt> </dl>

 

 




