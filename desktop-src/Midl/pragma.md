---
title: pragma (atributo)
description: La directiva \ pragma midl echo indica a MIDL que emita la cadena especificada, sin los caracteres de \_ comillas, en el archivo de encabezado generado.
ms.assetid: b8a175d2-ea07-4103-ab45-0de7e477d27a
keywords:
- atributo pragma MIDL
topic_type:
- apiref
api_name:
- pragma
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72f5e1c00c089bc8915adc2d9f3363305c677a96
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159417"
---
# <a name="pragma-attribute"></a>pragma (atributo)

La \# **directiva de \_ eco pragma midl** indica a MIDL que emita la cadena especificada, sin los caracteres de comillas, en el archivo de encabezado generado.

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

Especifica una secuencia de tokens que se insertan en el archivo de encabezado generado como parte de una directiva **\# pragma** sin que el compilador MIDL lo procese.

</dd> <dt>

*n* 
</dt> <dd>

Especifica el tamaño del paquete actual. Los valores válidos son 1, 2, 4, 8 y 16.

</dd> <dt>

*id* 
</dt> <dd>

Especifica el identificador de usuario.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El preprocesador del compilador de C procesa las directivas de preprocesamiento del lenguaje C que aparecen en el archivo IDL. Las **\# directivas define** del archivo IDL están disponibles durante la compilación midl, aunque no para el compilador de C.

Por ejemplo, cuando el preprocesador encuentra la directiva "define WINDOWS 4", el preprocesador reemplaza todas las apariciones de "WINDOWS" en el archivo \# IDL por "4". El símbolo "WINDOWS" no está disponible en tiempo de compilación de C.

Para permitir que las definiciones de macro del preprocesador de C pasen a través del compilador MIDL al compilador de C, use la directiva **\# pragma midl \_ echo** o [**cpp \_ quote.**](cpp-quote.md) Estas directivas indica al compilador MIDL que genere un archivo de encabezado que contenga la cadena de parámetro con las comillas quitadas. Las **\# directivas pragma midl \_ echo** y **cpp \_ quote** son equivalentes.

El compilador de MIDL usa la directiva **\# pragma pack** para controlar el empaquetado de estructuras. Invalida el modificador de línea de comandos [**/Zp.**](-zp.md) La opción pack (*n*) establece el tamaño del paquete actual en un valor específico: 1, 2, 4, 8 o 16. Las opciones pack (push) y pack (pop) tienen las siguientes características:

-   El compilador mantiene una pila de empaquetado. Los elementos de la pila de empaquetado incluyen un tamaño de paquete y un identificador *opcional.* La pila solo está limitada por la memoria disponible con el tamaño del paquete actual en la parte superior de la pila.
-   Pack (push) da como resultado el tamaño actual del paquete que se inserta en la pila de empaquetado. La pila está limitada por la memoria disponible.
-   Pack (push,*n*) es igual que pack (push) seguido de pack (*n*).
-   Pack (push, *id)* también inserta *el identificador en* la pila de empaquetado junto con el tamaño del paquete.
-   Pack (push, *id*, *n*) es igual que pack (push, *id)* seguido de pack (*n*).
-   El empaquetado (pop) da como resultado el desmontamiento de la pila de empaquetado. Los elementos emergentes desequilibrados provocan advertencias y establecen el tamaño del paquete actual en el valor de la línea de comandos.
-   Si se especifica pack (pop, *id*, *n*), se omite *n.*

El compilador MIDL coloca las cadenas especificadas en las directivas [**\\ cpp \_ quote**](cpp-quote.md) y **pragma** en el archivo de encabezado en la secuencia en la que se especifican en el archivo IDL y en relación con otros componentes de interfaz del archivo IDL. Las cadenas normalmente deben aparecer en la sección interface-body del archivo IDL después de todas las [**operaciones de**](import.md) importación.

El compilador MIDL no intenta procesar directivas **\# pragma** que no comienzan con el prefijo "midl". \_ Otras **\# directivas pragma** del archivo IDL se pasan al archivo de encabezado generado sin cambios.

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

[**cpp \_ quote**](cpp-quote.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Importación**](import.md)
</dt> <dt>

[**/Zp**](-zp.md)
</dt> </dl>

 

 




