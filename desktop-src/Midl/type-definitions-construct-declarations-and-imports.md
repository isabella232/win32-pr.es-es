---
title: Definiciones de tipos, declaraciones de construcción e importaciones
description: Las definiciones de tipo, las declaraciones de construcción y las importaciones se pueden producir fuera del cuerpo de la interfaz.
ms.assetid: 5d9011ab-bfc4-41f6-bd69-953660191652
keywords:
- interfaces MIDL, definiciones de tipo
- interfaces MIDL, declaraciones de construcción
- interfaces MIDL, importaciones
- definiciones de tipos MIDL
- declaraciones de construcción MIDL
- importa MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 645781f033566ba43dc6e355935ed112d0e8f5f6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665615"
---
# <a name="type-definitions-construct-declarations-and-imports"></a>Definiciones de tipos, declaraciones de construcción e importaciones

Las definiciones de tipo, las declaraciones de construcción y las importaciones se pueden producir fuera del cuerpo de la interfaz. Todas las definiciones del archivo IDL principal aparecerán en el archivo de encabezado generado y todos los procedimientos de todas las interfaces en el archivo IDL principal generarán rutinas de código auxiliar. Esto permite a las aplicaciones que admiten varias interfaces combinar archivos IDL en un único archivo IDL combinado.

Como resultado, requiere menos tiempo para compilar los archivos y también permite que MIDL reduzca las redundancias en el código auxiliar generado. Esto puede mejorar significativamente las interfaces de [**objeto**](object.md) a través de la capacidad de compartir código común para las interfaces base y las interfaces derivadas. En el caso de las interfaces que no son de **objeto** , los nombres de procedimiento deben ser únicos en todas las interfaces. En el caso de las interfaces de **objeto** , los nombres de procedimiento deben ser únicos solo dentro de una interfaz. Tenga en cuenta que no se permiten varias interfaces cuando se usa el modificador [**/OSF**](-osf.md)

## <a name="declarative-constructs"></a>Construcciones declarativas

La sintaxis de las construcciones declarativas en el archivo IDL es similar a la de C. MIDL es compatible con todas las construcciones declarativas de C/C++ de Microsoft, excepto las siguientes:

-   Declaradores de estilo más antiguos que permiten especificar un declarador sin un especificador de tipo, como:

    ``` syntax
    x (y) 
    short x (y)
    ```

-   Declaraciones con inicializadores (MIDL solo acepta declaraciones que se ajusten a la sintaxis de MIDL [**const**](const.md) ).

La palabra clave [**Import**](import.md) especifica los nombres de uno o varios archivos IDL que se van a importar. La Directiva de importación es similar a la directiva [**include**](include.md) de C, salvo que solo los tipos de datos se asimilan al archivo IDL de importación.

## <a name="constant-declaration"></a>Declaración de constantes

La declaración de constante especifica constantes de [**tipo booleano**](boolean.md), entero, carácter, caracteres anchos, cadenas y **void \*** . Para obtener más información, vea [**const**](const.md).

## <a name="general-declaration"></a>Declaración general

Una declaración general es similar a la instrucción [**typedef**](typedef.md) de C con la adición de atributos de tipo IDL. Excepto en el modo [**/OSF**](-osf.md) , el compilador MIDL también permite una declaración implícita en forma de definición de variable.

## <a name="function-declaration"></a>Declaración de función

El declarador de función es un caso especial de la declaración general. Puede usar atributos IDL para especificar el comportamiento del tipo de valor devuelto de la función y de cada uno de los parámetros.

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

 

 




