---
title: Definiciones de tipo, declaraciones de construcción e importaciones
description: Las definiciones de tipo, las declaraciones de construcción y las importaciones pueden producirse fuera del cuerpo de la interfaz.
ms.assetid: 5d9011ab-bfc4-41f6-bd69-953660191652
keywords:
- interfaces MIDL , definiciones de tipo
- interfaces MIDL, declaraciones de construcción
- interfaces MIDL , imports
- definiciones de tipo MIDL
- declaraciones de construcción MIDL
- importaciones MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aca1f80bca0a5d03ea0e935b05f973a6370c4180c9ce5c0fe7dea5d8f5c9c7de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829226"
---
# <a name="type-definitions-construct-declarations-and-imports"></a>Definiciones de tipo, declaraciones de construcción e importaciones

Las definiciones de tipo, las declaraciones de construcción y las importaciones pueden producirse fuera del cuerpo de la interfaz. Todas las definiciones del archivo IDL principal aparecerán en el archivo de encabezado generado y todos los procedimientos de todas las interfaces del archivo IDL principal generarán rutinas de código auxiliar. Esto permite que las aplicaciones que admiten varias interfaces combinen archivos IDL en un único archivo IDL combinado.

Como resultado, requiere menos tiempo para compilar los archivos y también permite que MIDL reduzca los redundancias en los códigos auxiliares generados. Esto puede mejorar significativamente las [**interfaces**](object.md) de objeto a través de la capacidad de compartir código común para interfaces base e interfaces derivadas. Para las interfaces **que no** son de objeto, los nombres de procedimiento deben ser únicos en todas las interfaces. Para **las** interfaces de objeto, los nombres de procedimiento solo deben ser únicos dentro de una interfaz. Tenga en cuenta que no se permiten varias interfaces cuando se usa el [**modificador /osf.**](-osf.md)

## <a name="declarative-constructs"></a>Construcciones declarativas

La sintaxis de las construcciones declarativas en el archivo IDL es similar a la de C. MIDL admite todas las construcciones declarativas de Microsoft C/C++, excepto las siguientes:

-   Declaradores de estilo anteriores que permiten especificar un declarador sin un especificador de tipo, como:

    ``` syntax
    x (y) 
    short x (y)
    ```

-   Declaraciones con inicializadores (MIDL solo acepta declaraciones que se ajustan a la sintaxis [**const de**](const.md) MIDL).

La [**palabra clave import**](import.md) especifica los nombres de uno o varios archivos IDL que se importarán. La directiva import es similar a la directiva [**include**](include.md) de C, salvo que solo los tipos de datos se integran en el archivo IDL de importación.

## <a name="constant-declaration"></a>Declaración constante

La declaración constante especifica [**constantes booleanas,**](boolean.md)integer, character, wide-character, string y **\* void_.* Para obtener más información, vea [_ *const* *](const.md).

## <a name="general-declaration"></a>Declaración general

Una declaración general es similar a la instrucción [**typedef de**](typedef.md) C con la adición de atributos de tipo IDL. Excepto en [**el modo /osf,**](-osf.md) el compilador MIDL también permite una declaración implícita en forma de definición de variable.

## <a name="function-declaration"></a>Declaración de función

El declarador de función es un caso especial de la declaración general. Puede usar atributos IDL para especificar el comportamiento del tipo de valor devuelto de función y cada uno de los parámetros.

## <a name="examples"></a>Ejemplos

``` syntax
[ 
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(3.1), 
    pointer_default(unique) 
] 
interface IdlGrammarExample 
{ 
    import "windows.idl", "other.idl"; 
    const wchar_t * NAME = L"Example Program"; 
    typedef char * PCHAR; 
 
    HRESULT DictCheckSpelling( 
        [in, string] PCHAR   word,     // word to look up 
        [out]        short * isPresent // 0 if not present 
    ); 
}
```

 

 




