---
title: Trabajar con definiciones en archivos IDL
description: En esta página se describe por qué los símbolos definidos con \ define desaparecen del compilador MIDL y archivos H generados y lo que se puede hacer al respecto. Esta explicación se aplica a todos los archivos procesados por MIDL, como los archivos \. idl, \. ACF, \. h.
ms.assetid: 148dabda-96cc-4f7c-abc7-4bf78ac166ea
keywords:
- MIDL del compilador MIDL, tratar con define
- define MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4af77979824c2e76352d6f28bef72161249845d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075678"
---
# <a name="dealing-with-defines-in-idl-files"></a>Trabajar con \# definiciones en archivos IDL

En esta página se describe por qué los símbolos definidos con una **\# definición** desaparecen del compilador MIDL archivos H generados y lo que se puede hacer al respecto. Esta explicación se aplica a todos los archivos procesados por MIDL, como \* archivos. idl, \* . ACF y \* . h.

La desaparición de símbolos de **\# definición** es el resultado de que MIDL delegue el preprocesamiento de los archivos de entrada a un preprocesador. De forma predeterminada, el preprocesador es un preprocesador de C/C++ del entorno de compilación. Después del preprocesamiento, el flujo de entrada MIDL recibe solo las \# directivas de preprocesador de línea. En concreto, el preprocesador revierte todas las definiciones de macro en los archivos de entrada y, por consiguiente, MIDL no puede detectar su presencia. Por consiguiente, cuando MIDL Replica definiciones de tipo de un archivo de entrada en el archivo H generado, las definiciones \# no se replican. Por lo tanto, no use \# define directamente en archivos IDL si se van a utilizar más adelante desde el archivo H generado.

Se recomiendan las cuatro soluciones alternativas siguientes:

-   Use la especificación de declaración [**const**](const.md) .
-   Use archivos de encabezado independientes que se importen o incluyan en el archivo IDL y que se incluyan más adelante en el código fuente de C.
-   Use constantes de enumeración en el archivo IDL.
-   Use [**CPP \_ Quote**](cpp-quote.md) para reproducir la **\# definición** en el archivo de encabezado generado.

Puede reproducir constantes de manifiesto mediante la **Sintaxis de declaración de constantes de IDL**. Tenga en cuenta que [**const**](const.md) en la declaración de constante IDL es diferente de la semántica de C/C++ **const** y simplemente presenta una constante con nombre para una compilación de IDL. Por ejemplo:

``` syntax
const short ARRSIZE = 10
```

Este ejemplo especifica que **ARRSIZE** es una constante con un valor de 10. Las constantes con nombre se pueden usar en declaradores de matriz IDL y en otros lugares donde un programador de C usaría un manifiesto definido. Además, esta sintaxis da como resultado la generación de la siguiente línea en el archivo de encabezado:

``` syntax
#define ARRSIZE 10
```

Otra manera de controlar las **\#** instrucciones de definición consiste en empaquetarlas en un archivo de encabezado independiente, ya sea en un archivo dedicado a **\#** definir instrucciones o en un archivo que contenga solo definiciones de tipo. Un archivo que contenga solo directivas de preprocesador puede incluirse de forma segura en el archivo IDL y en los archivos de código fuente de C. Aunque las directivas no estarán disponibles en el archivo de encabezado generado por el compilador MIDL, el programa de origen C puede incluir el archivo de encabezado independiente. De forma similar, un archivo de encabezado con **\#** instrucciones de definición y definiciones de tipos regulares se puede importar desde el archivo IDL. Este enfoque encapsula las **\#** instrucciones de definición y typedef mediante su uso en un archivo H de modo que los **\#** símbolos de definición no se usan directamente en el archivo IDL de importación. La importación de un archivo de encabezado o IDL a otro archivo IDL impide que las instrucciones typedef se repliquen en el archivo H generado por MIDL (que, a diferencia de las **\#** instrucciones include). Este enfoque permite hacer referencia al archivo de encabezado original de forma segura desde el código C a lo largo del archivo H generado sin tener un problema con las definiciones duplicadas.

El uso de constantes de enumeración en el archivo IDL también es eficaz. Estas constantes se pueden usar en expresiones constantes en IDL, por ejemplo, en declaradores de matriz. Las constantes de enumeración no se quitan durante las primeras fases de la compilación de MIDL por parte del preprocesador del compilador de C, por lo que las constantes de enumeración están disponibles en el archivo de encabezado generado por el compilador de MIDL. Considere la instrucción siguiente:

``` syntax
typedef enum midlworkaround { MAXSTRINGCOUNT = 300 };
```

Esta instrucción no se quitará durante la compilación de MIDL del preprocesador de C y la definición de tipo se replicará en el archivo H generado. La constante MAXSTRINGCOUNT está disponible para los programas de origen de C que incluyen el archivo de encabezado generado por el compilador MIDL.

Por último, se puede usar la Directiva de [**\_ comillas de CPP**](cpp-quote.md) de MIDL para escribir una cadena arbitraria directamente en el archivo H generado. Por ejemplo, para obtener la constante de manifiesto utilizada anteriormente en esta página con la **\_ comilla CPP**, se puede usar la siguiente instrucción:

``` syntax
cpp_quote ("#define ARRSIZE 10")
```

Esta instrucción da como resultado la generación de la siguiente línea en el archivo de encabezado:

``` syntax
#define ARRSIZE 10
```

 

 




