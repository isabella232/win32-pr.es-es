---
title: Trabajar con define en archivos IDL
description: En esta página se describe por qué los símbolos definidos con \ define desaparecen de los archivos H generados por el compilador MIDL y qué se puede hacer al respecto. Esta explicación se aplica a los archivos procesados por MIDL, como \ .idl, \ .acf, \ archivos .h.
ms.assetid: 148dabda-96cc-4f7c-abc7-4bf78ac166ea
keywords:
- MIDL del compilador MIDL, que trabaja con define
- define MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4af77979824c2e76352d6f28bef72161249845d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159633"
---
# <a name="dealing-with-defines-in-idl-files"></a>Trabajar con \# define en archivos IDL

En esta página se describe **\#** por qué los símbolos definidos con una definición desaparecen de los archivos H generados por el compilador MIDL y qué se puede hacer al respecto. Esta explicación se aplica a los archivos procesados por MIDL, como \* archivos .idl, \* .acf o \* .h.

La **\# deserción de** los símbolos de definición es el resultado de que MIDL delegue el preprocesamiento de los archivos de entrada a un preprocesador. De forma predeterminada, el preprocesador es un preprocesador de C/C++ del entorno de compilación. Después del preprocesamiento, el flujo de entrada que recibe MIDL solo tiene \# directivas de preprocesador de línea. En concreto, el preprocesador desinsluye todas las definiciones de macro en los archivos de entrada y, por lo tanto, MIDL no puede detectar su presencia. Por lo tanto, cuando MIDL replica definiciones de tipo de un archivo de entrada en el archivo H generado, las \# definiciones no se replican. Por lo tanto, no use define directamente en los archivos IDL si se van a usar \# más adelante desde el archivo H generado.

Se recomiendan las cuatro soluciones alternativas siguientes:

-   Use la [**especificación de declaración const.**](const.md)
-   Use archivos de encabezado independientes que se importan o se incluyen en el archivo IDL y que se incluyen más adelante en el código fuente de C.
-   Use constantes de enumeración en el archivo IDL.
-   Use [**la comilla cpp \_**](cpp-quote.md) para reproducir **\# define** en el archivo de encabezado generado.

Puede reproducir constantes de manifiesto mediante la **sintaxis de declaración constante de IDL**. Tenga en cuenta que [**el const**](const.md) de la declaración constante de IDL es diferente de la semántica **const** de C/C++ y simplemente introduce una constante con nombre para una compilación de IDL. Por ejemplo:

``` syntax
const short ARRSIZE = 10
```

En este ejemplo se especifica **que ARRSIZE** es una constante con un valor de 10. Las constantes con nombre se pueden usar en declaradores de matriz IDL y en otros lugares donde un programador de C usaría un manifiesto. Además, esta sintaxis genera la siguiente línea en el archivo de encabezado:

``` syntax
#define ARRSIZE 10
```

Otra manera de controlar las instrucciones define es empaquetarlos en un archivo de encabezado independiente, ya sea en un archivo dedicado a definir instrucciones o en un archivo que contenga solo definiciones **\#** **\#** de tipo. Un archivo que contiene solo directivas de preprocesador puede incluirse de forma segura tanto por el archivo IDL como por los archivos de código fuente de C. Aunque las directivas no estarán disponibles en el archivo de encabezado generado por el compilador MIDL, el programa de origen de C puede incluir el archivo de encabezado independiente. De forma similar, se puede importar un archivo de encabezado con instrucciones define y definiciones de tipo **\#** normal desde el archivo IDL. Este enfoque encapsula las instrucciones define y typedef usándolos en un archivo H de forma que los símbolos de definición no se usen directamente en el **\#** **\#** archivo IDL de importación. La importación de un archivo de encabezado o IDL a otro archivo IDL impide que las instrucciones typedef se repliquen en el archivo H generado por MIDL (que es a diferencia de las instrucciones **\#** include). Este enfoque permite hacer referencia de forma segura al archivo de encabezado original desde el código C a lo largo del archivo H generado sin tener ningún problema con definiciones duplicadas.

El uso de constantes de enumeración en el archivo IDL también es efectivo. Estas constantes se pueden usar en expresiones constantes en IDL, por ejemplo, en declaradores de matriz. Las constantes de enumeración no se quitan durante las primeras fases de la compilación MIDL mediante el preprocesador del compilador de C, por lo que las constantes de enumeración están disponibles en el archivo de encabezado generado por el compilador MIDL. Considere la instrucción siguiente:

``` syntax
typedef enum midlworkaround { MAXSTRINGCOUNT = 300 };
```

El preprocesador de C no quitará esta instrucción durante la compilación midL y la definición de tipo se replicará en el archivo H generado. La constante MAXSTRINGCOUNT está disponible para los programas de código fuente de C que incluyen el archivo de encabezado generado por el compilador MIDL.

Por último, la [**directiva de \_ comillas cpp**](cpp-quote.md) de MIDL se puede usar para escribir una cadena arbitraria directamente en el archivo H generado. Por ejemplo, para obtener la constante de manifiesto usada anteriormente en esta página con la comilla **cpp \_**, se puede usar la siguiente instrucción:

``` syntax
cpp_quote ("#define ARRSIZE 10")
```

Esta instrucción genera la siguiente línea en el archivo de encabezado:

``` syntax
#define ARRSIZE 10
```

 

 




