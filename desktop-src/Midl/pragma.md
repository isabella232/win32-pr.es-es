---
title: pragma (atributo)
description: La Directiva \ pragma MIDL \_ echo indica a MIDL que emita la cadena especificada, sin los caracteres de Comillas, en el archivo de encabezado generado.
ms.assetid: b8a175d2-ea07-4103-ab45-0de7e477d27a
keywords:
- pragma (atributo) MIDL
topic_type:
- apiref
api_name:
- pragma
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72f5e1c00c089bc8915adc2d9f3363305c677a96
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103994637"
---
# <a name="pragma-attribute"></a>pragma (atributo)

La \# directiva **pragma MIDL \_ echo** indica a MIDL que emita la cadena especificada, sin los caracteres de Comillas, en el archivo de encabezado generado.

``` syntax
#pragma midl_echo("string")
#pragma token-sequence
#pragma pack (n)
#pragma pack ( [push] [, id] [, n} )
#pragma pack ( [pop] [, id] [, n} )
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*string* 
</dt> <dd>

Especifica una cadena que se inserta en el archivo de encabezado generado. Las comillas se quitan durante el proceso de inserción.

</dd> <dt>

*secuencia de tokens* 
</dt> <dd>

Especifica una secuencia de tokens que se insertan en el archivo de encabezado generado como parte de una directiva **\# pragma** sin ser procesados por el compilador de MIDL.

</dd> <dt>

*n* 
</dt> <dd>

Especifica el tamaño actual del paquete. Los valores válidos son 1, 2, 4, 8 y 16.

</dd> <dt>

*id* 
</dt> <dd>

Especifica el identificador de usuario.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El preprocesador del compilador de C procesa las directivas de preprocesamiento de lenguaje c que aparecen en el archivo IDL. Las directivas de **\# definición** en el archivo IDL están disponibles durante la compilación de MIDL, aunque no en el compilador de C.

Por ejemplo, cuando el preprocesador encuentra la Directiva " \# definir Windows 4", el preprocesador reemplaza todas las apariciones de "Windows" en el archivo IDL por "4". El símbolo "WINDOWS" no está disponible en tiempo de compilación de C.

Para permitir que las definiciones de macro del preprocesador de C pasen a través del compilador de MIDL al compilador de C, use la directiva **\# pragma MIDL \_ echo** o [**CPP \_ Quote**](cpp-quote.md) . Estas directivas indican al compilador de MIDL que genere un archivo de encabezado que contenga la cadena de parámetro con las comillas quitadas. Las directivas **\# pragma MIDL \_ echo** y **CPP \_ Quote** son equivalentes.

El compilador MIDL utiliza la directiva **\# pragma Pack** para controlar el empaquetado de estructuras. Invalida el modificador de la línea de comandos [**/ZP**](-zp.md) . La opción Pack (*n*) establece el tamaño actual del paquete en un valor específico: 1, 2, 4, 8 o 16. Las opciones de Pack (de extracción) y de paquete (pop) tienen las siguientes características:

-   El compilador mantiene una pila de empaquetado. Los elementos de la pila de empaquetado incluyen un tamaño de paquete y un *identificador* opcional. La pila solo está limitada por la memoria disponible con el tamaño de paquete actual en la parte superior de la pila.
-   Pack (push) hace que el tamaño actual del paquete se inserte en la pila de empaquetado. La pila está limitada por la memoria disponible.
-   Pack (Inserte,*n*) es el mismo que Pack (Inserte) seguido del Pack (*n*).
-   Pack (Inserte, *ID*) también inserciones el *identificador* en la pila de empaquetado junto con el tamaño del paquete.
-   Pack (inserciones, *ID.*, *n*) es el mismo que el Pack (Inserte, *ID*) seguido de Pack (*n*).
-   Pack (pop) da como resultado la extracción de la pila de empaquetado. Los pop desequilibrados causan advertencias y establecen el tamaño actual del paquete en el valor de la línea de comandos.
-   Si se especifica Pack (pop, *ID*, *n*), se omite *n* .

El compilador MIDL coloca las cadenas especificadas en las directivas [**\\ CPP \_ Quote**](cpp-quote.md) y **pragma** en el archivo de encabezado en la secuencia en la que se especifican en el archivo IDL y con respecto a otros componentes de la interfaz en el archivo IDL. Las cadenas deben aparecer normalmente en la sección del cuerpo de la interfaz del archivo IDL después de todas las operaciones de [**importación**](import.md) .

El compilador MIDL no intenta procesar directivas **\# pragma** que no empiecen por el prefijo "MIDL" \_ . Otras directivas **\# pragma** del archivo IDL se pasan al archivo de encabezado generado sin cambios.

## <a name="examples"></a>Ejemplos

``` syntax
/* IDL file */ 
#pragma midl_echo("#define UNICODE") 
cpp_quote("#define __DELAYED_PREPROCESSING__ 1") 
#pragma hdrstop 
#pragma check_pointer(on) 
 
/* generated header file */ 
#define UNICODE 
#define __DELAYED_PREPROCESSING__ 1 
#pragma hdrstop 
#pragma check_pointer(on)
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**comilla CPP \_**](cpp-quote.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**importar**](import.md)
</dt> <dt>

[**/ZP**](-zp.md)
</dt> </dl>

 

 




