---
title: Diferencias entre MIDL y MkTypLib
description: Diferencias entre MIDL y MkTypLib
ms.assetid: 86abd70b-7238-49a6-a996-2c8906a14449
keywords:
- MIDL y ODL MIDL, diferencias entre MIDL y MkTypLib
- MkTypLib (MIDL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a54b6103cc230e1c5e6700b0ddc93312c767f9b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076363"
---
# <a name="differences-between-midl-and-mktyplib"></a>Diferencias entre MIDL y MkTypLib

> [!Note]  
> La herramienta Mktyplib.exe está obsoleta. En su lugar, utilice el compilador de MIDL.

 

Existen algunas áreas clave en las que el compilador MIDL difiere de MkTypLib. La mayoría de estas diferencias surgen porque MIDL está orientado más hacia la sintaxis de C que a MkTypLib.

En general, querrá usar la sintaxis de MIDL en los archivos IDL. Sin embargo, si necesita compilar un archivo ODL existente o mantener la compatibilidad con MkTypLib, use la opción del compilador de MIDL [**/mktyplib203**](-mktyplib203.md) para forzar que MIDL se comporte como Mkktyplib.exe, versión 2,03. (Esta es la última versión de la herramienta MkTypLib). En concreto, la opción **/mktyplib203** resuelve estas diferencias:

-   Sintaxis de TypeDef para tipos de datos complejos

    En MkTypLib, las dos definiciones siguientes generan un registro TKIND \_ para "This \_ struct" en la biblioteca de tipos. La etiqueta "struct \_ Tag" es opcional y, si se utiliza, no se mostrará en la biblioteca de tipos.

    ``` syntax
    typedef struct struct_tag { ... } this_struct;
    typedef struct { ... } that_struct;
    ```

    Si falta una etiqueta opcional, MIDL la generará, con lo que se agregará una etiqueta a la definición proporcionada por el usuario. Dado que la primera definición tiene una etiqueta, MIDL generará un \_ registro TKIND para "This \_ struct" y un \_ alias TKIND para "This \_ struct" (que define "This \_ struct" como alias para "struct \_ Tag"). Dado que la etiqueta falta en la segunda definición, MIDL generará un \_ registro TKIND para un nombre alterado, interno a MIDL, que no es significativo para el usuario y un \_ alias TKIND para "ese \_ struct".

    Esto tiene implicaciones potenciales para los exploradores de biblioteca de tipos que simplemente muestran el nombre de un registro en su interfaz de usuario. Si espera que un \_ registro TKIND tenga un nombre real, los nombres irreconocibles podrían aparecer en la interfaz de usuario. Este comportamiento también se aplica a las definiciones de [**Unión**](union.md) y [**enumeración**](enum.md) , con el compilador MIDL que genera TKIND \_ uniones y TKIND \_ enumeraciones, respectivamente.

    MIDL también permite definiciones de [**struct**](struct.md), [**Union**](union.md)y [**enum**](enum.md) de estilo C. Por ejemplo, la siguiente definición es válida en MIDL:

    ``` syntax
    struct my_struct { ... };
    typedef struct my_struct your_struct;
    ```

-   tipos de datos booleanos

    En MkTypLib, el tipo base [**booleano**](boolean.md) y el tipo de datos MkTypLib bool equivalen a VT \_ bool, que se asigna a la variante \_ bool y que se define como un valor [**Short**](short.md). En MIDL, el tipo base **booleano** es equivalente a VT \_ UI1, que se define como un [**carácter sin signo**](unsigned.md)y el tipo de datos bool se define como un [**valor Long**](long.md). Esto conduce a dificultades si se mezcla la sintaxis IDL y la sintaxis ODL en el mismo archivo mientras se sigue intentando mantener la compatibilidad con MkTypLib. Dado que los tipos de datos tienen tamaños diferentes, el código de serialización no coincidirá con lo que se describe en la información de tipo. Si desea un VT \_ bool en la biblioteca de tipos, debe usar el tipo de \_ datos Variant bool.

-   Definiciones de GUID en archivos de encabezado

    En MkTypLib, los GUID se definen en el archivo de encabezado con una macro que se puede compilar condicionalmente para generar una predefinición de GUID o un GUID con instancias. MIDL normalmente coloca las predefiniciones de GUID en los archivos de encabezado generados y las instancias GUID solo en el archivo generado por el modificador [**/IID**](-iid.md)

Las siguientes diferencias de comportamiento no se pueden resolver mediante el modificador [**/mktyplib203**](-mktyplib203.md) :

-   Distinción entre mayúsculas y minúsculas

    MIDL distingue mayúsculas de minúsculas, la automatización OLE no lo es.

-   Ámbito de los símbolos en una declaración de enumeración

    En MkTypLib, el ámbito de los símbolos de una enumeración es local. En MIDL, el ámbito de los símbolos en una enumeración es global, como en C. Por ejemplo, el siguiente código se compilará en MkTypLib, pero generará un error de nombre duplicado en MIDL:

    ``` syntax
    typedef struct { ... } a;
    enum {a=1, b=2, c=3};
    ```

-   Ámbito de atributo público

    Si aplica el atributo [**público**](public.md) a un bloque de interfaz, MkTypLib trata cada typedef dentro de ese bloque de interfaz como público. MIDL requiere que aplique explícitamente el atributo **público** a las definiciones de usuario que desee que sean públicas.

-   Orden de búsqueda de importlib

    Si importa más de una biblioteca de tipos y estas bibliotecas contienen referencias duplicadas, MkTypLib la resuelve con la primera referencia que encuentre. MIDL usará la última referencia que encuentre. Por ejemplo, dada la siguiente sintaxis de ODL, la biblioteca C usará la definición de tipo MOO de la biblioteca A si se compila con MkTypLib y la definición de tipo MOO de la biblioteca B Si se compila con MIDL:

    ``` syntax
    [...]library A
    {
        typedef struct tagMOO
        {...}MOO
    }

    [...]library B
    {
        typedef struct tagMOO
        {...} MOO
    }

    [...]library C
    {
        importlib (A.TLB)
        importlib (B.TLB)
        typedef struct tagBAA
        {MOO y;}BAA
    }
    ```

    La solución adecuada para esto es calificar cada referencia con el nombre de la biblioteca de importación correcto, de la siguiente manera:

    ``` syntax
    typedef struct tagBAA
        {A.MOO y;}BAA
    ```

-   No se reconoce el tipo de datos VOID

    MIDL reconoce el tipo de datos [**void**](void.md) del lenguaje C y no reconoce el tipo de datos void de OLE Automation. Si tiene un archivo ODL que usa VOID, coloque esta definición en la parte superior del archivo:

    ``` syntax
#define VOID void
    ```

-   Notación exponencial

    MIDL requiere que los valores expresados en la notación exponencial estén incluidos entre comillas. Por ejemplo, "-2.5 E + 3"

-   Constantes y valores de LCID

    Normalmente, MIDL no tiene en cuenta el LCID al analizar archivos. Para forzar este comportamiento para un valor, o si necesita usar la notación específica de la configuración regional al definir una constante, incluya el valor o la constante entre comillas.

Para obtener más información, vea [**/mktyplib203**](-mktyplib203.md), [**/IID**](-iid.md)y [serialización de tipos de datos OLE](marshaling-ole-data-types.md).

 

 




