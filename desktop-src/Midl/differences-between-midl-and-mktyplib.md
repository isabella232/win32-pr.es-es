---
title: Diferencias entre MIDL y MkTypLib
description: Diferencias entre MIDL y MkTypLib
ms.assetid: 86abd70b-7238-49a6-a996-2c8906a14449
keywords:
- MIDL y ODL MIDL, diferencias entre MIDL y MkTypLib
- MkTypLib MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43ae20e00dab492a140f48c9de683abeac04676824bd6513ccf086889b4460e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118643629"
---
# <a name="differences-between-midl-and-mktyplib"></a>Diferencias entre MIDL y MkTypLib

> [!Note]  
> La Mktyplib.exe está obsoleta. En su lugar, use el compilador MIDL.

 

Hay algunas áreas clave en las que el compilador MIDL difiere de MkTypLib. La mayoría de estas diferencias surgen porque MIDL está más orientado a la sintaxis de C que a MkTypLib.

En general, querrá usar la sintaxis MIDL en los archivos IDL. Sin embargo, si necesita compilar un archivo ODL existente o mantener la compatibilidad con MkTypLib, use la opción del compilador MIDL [**/mktyplib203**](-mktyplib203.md) para obligar a MIDL a comportarse como Mkktyplib.exe, versión 2.03. (Esta es la última versión de la herramienta MkTypLib). En concreto, la **opción /mktyplib203** resuelve estas diferencias:

-   Sintaxis typedef para tipos de datos complejos

    En MkTypLib, las dos definiciones siguientes generan un registro TKIND \_ para "esta \_ estructura" en la biblioteca de tipos. La etiqueta "struct tag" es opcional y, si se \_ usa, no se mostrará en la biblioteca de tipos.

    ``` syntax
    typedef struct struct_tag { ... } this_struct;
    typedef struct { ... } that_struct;
    ```

    Si falta una etiqueta opcional, MIDL la generará, agregando eficazmente una etiqueta a la definición proporcionada por el usuario. Puesto que la primera definición tiene una etiqueta, MIDL generará un registro TKIND para "this struct" y un ALIAS de TKIND para \_ \_ \_ "this \_ struct" (definiendo "this struct" como un alias para \_ "struct \_ tag"). Dado que falta la etiqueta en la segunda definición, MIDL generará un registro de TKIND para un nombre perdido, interno a MIDL, que no es significativo para el usuario y un ALIAS de TKIND para \_ \_ "esa \_ estructura".

    Esto tiene posibles implicaciones para los exploradores de la biblioteca de tipos que simplemente muestran el nombre de un registro en su interfaz de usuario. Si espera que un registro de TKIND tenga un nombre real, podrían aparecer nombres \_ irreconocibles en la interfaz de usuario. Este comportamiento también se [](enum.md) aplica a [**las**](union.md) definiciones de unión y enumeración, y el compilador MIDL genera LOS UNION de TKIND y los ENUM \_ de \_ TKIND, respectivamente.

    MIDL también permite definiciones [](union.md)de [**enumeración,**](struct.md)unión y estructura [**de**](enum.md) estilo C. Por ejemplo, la siguiente definición es legal en MIDL:

    ``` syntax
    struct my_struct { ... };
    typedef struct my_struct your_struct;
    ```

-   tipos de datos booleanos

    En MkTypLib, el tipo [**base**](boolean.md) booleano y el tipo de datos MkTypLib BOOL equivalen a VT BOOL, que se asigna \_ a VARIANT BOOL y que se define como un \_ [**corto**](short.md). En MIDL, el tipo **base** booleano es equivalente a VT UI1, que se define como un carácter sin signo y el tipo de datos BOOL se define como \_ [**un largo**](long.md). [](unsigned.md) Esto conduce a dificultades si mezcla la sintaxis de IDL y la sintaxis de ODL en el mismo archivo mientras sigue intentando mantener la compatibilidad con MkTypLib. Dado que los tipos de datos tienen tamaños diferentes, el código de serialización no coincidirá con lo que se describe en la información de tipos. Si desea un VT \_ BOOL en la biblioteca de tipos, debe usar el tipo de datos VARIANT \_ BOOL.

-   Definiciones de GUID en archivos de encabezado

    En MkTypLib, los GUID se definen en el archivo de encabezado con una macro que se puede compilar condicionalmente para generar una definición previa de GUID o un GUID con instancias. MIDL normalmente coloca las predefiniciones guid en sus archivos de encabezado generados y las instancias GUID solo en el archivo generado por el [**modificador /iid.**](-iid.md)

Las siguientes diferencias de comportamiento no se pueden resolver mediante el modificador [**/mktyplib203:**](-mktyplib203.md)

-   Distinción entre mayúsculas y minúsculas

    MIDL distingue mayúsculas de minúsculas y OLE Automation no.

-   Ámbito de símbolos en una declaración de enumeración

    En MkTypLib, el ámbito de los símbolos de una enumeración es local. En MIDL, el ámbito de los símbolos de una enumeración es global, como en C. Por ejemplo, el código siguiente se compilará en MkTypLib, pero generará un error de nombre duplicado en MIDL:

    ``` syntax
    typedef struct { ... } a;
    enum {a=1, b=2, c=3};
    ```

-   Ámbito del atributo público

    Si aplica el atributo [**public a**](public.md) un bloque de interfaz, MkTypLib trata cada typedef dentro de ese bloque de interfaz como público. MIDL requiere que aplique explícitamente el atributo **public** a las definiciones de tipo que desea que sea pública.

-   Orden de búsqueda de la biblioteca de importación

    Si importa más de una biblioteca de tipos y estas bibliotecas contienen referencias duplicadas, MkTypLib lo resuelve mediante la primera referencia que encuentra. MIDL usará la última referencia que encuentre. Por ejemplo, dada la siguiente sintaxis de ODL, la biblioteca C usará la definición de tipo MOO de la biblioteca A si compila con MkTypLib y la definición de tipo DE LA BIBLIOTECA B si compila con MIDL:

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

    La solución alternativa adecuada para esto es calificar cada una de estas referencias con el nombre correcto de la biblioteca de importación, de la siguiente manera:

    ``` syntax
    typedef struct tagBAA
        {A.MOO y;}BAA
    ```

-   Tipo de datos VOID no reconocido

    MIDL reconoce el tipo de datos [**void**](void.md) del lenguaje C y no reconoce el tipo de datos VOID de OLE Automation. Si tiene un archivo ODL que usa VOID, coloque esta definición en la parte superior del archivo:

    ``` syntax
#define VOID void
    ```

-   Notación exponencial

    MIDL requiere que los valores expresados en notación exponencial se contengan entre comillas. Por ejemplo, "-2.5E+3"

-   Constantes y valores LCID

    Normalmente, MIDL no tiene en cuenta el LCID al analizar archivos. Para forzar este comportamiento para un valor, o si necesita usar la notación específica de la configuración regional al definir una constante, incluya el valor o la constante entre comillas.

Para obtener más información, [**vea /mktyplib203**](-mktyplib203.md), [**/iid**](-iid.md)y [Serializar tipos de datos OLE](marshaling-ole-data-types.md).

 

 




