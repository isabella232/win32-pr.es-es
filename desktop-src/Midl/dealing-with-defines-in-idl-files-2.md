---
title: Trabajar con define en archivos IDL
description: En esta página se describe por qué los símbolos definidos con \ define desaparecen de los archivos H generados por el compilador MIDL y qué se puede hacer al respecto. Esta explicación se aplica a los archivos procesados por MIDL, como \ .idl, \ .acf, \ archivos .h.
ms.assetid: 148dabda-96cc-4f7c-abc7-4bf78ac166ea
keywords:
- MIDL del compilador MIDL, que trata con define
- define MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22c8a63423943d72326b16d53272f63d6efbe7d614661990560b00989be04cf1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979714"
---
# <a name="dealing-with-defines-in-idl-files"></a>Trabajar con \# define en archivos IDL

En esta página se describe **\#** por qué los símbolos definidos con una definición desaparecen de los archivos H generados por el compilador MIDL y qué se puede hacer al respecto. Esta explicación se aplica a los archivos procesados por MIDL, como \* archivos .idl, \* .acf y \* .h.

La tensión **\# de definir** símbolos es el resultado de que MIDL delega el preprocesamiento de los archivos de entrada en un preprocesador. De forma predeterminada, el preprocesador es un preprocesador de C/C++ del entorno de compilación. Después del preprocesamiento, el flujo de entrada que recibe MIDL solo tiene \# directivas de preprocesador de línea. En concreto, el preprocesador desinsluye todas las definiciones de macro en los archivos de entrada y, por lo tanto, MIDL no puede detectar su presencia. Por lo tanto, cuando MIDL replica definiciones de tipo de un archivo de entrada en el archivo H generado, las \# definiciones no se replican. Por lo tanto, no use define directamente en los archivos IDL si se van a \# usar más adelante desde el archivo H generado.

Se recomiendan las cuatro soluciones alternativas siguientes:

-   Use la [**especificación de declaración const.**](const.md)
-   Use archivos de encabezado independientes que se importen o incluyan en el archivo IDL y que se incluyan posteriormente en el código fuente de C.
-   Use constantes de enumeración en el archivo IDL.
-   Use [**la comilla cpp \_**](cpp-quote.md) para reproducir la **\# definición** en el archivo de encabezado generado.

Puede reproducir constantes de manifiesto mediante la **sintaxis de declaración constante de IDL**. Tenga en cuenta que [**el const**](const.md) de la declaración constante de IDL es diferente de la semántica **const** de C/C++ y simplemente introduce una constante con nombre para una compilación de IDL. Por ejemplo:

``` syntax
const short ARRSIZE = 10
```

En este ejemplo se especifica **que ARRSIZE** es una constante con un valor de 10. Las constantes con nombre se pueden usar en declaradores de matriz IDL y en otros lugares donde un programador de C usaría un manifiesto define. Además, esta sintaxis da como resultado que se genere la siguiente línea en el archivo de encabezado:

``` syntax
#define ARRSIZE 10
```

Otra manera de controlar las instrucciones define es empaquetarlos en un archivo de encabezado independiente, ya sea en un archivo dedicado a definir instrucciones o en un archivo que contenga solo definiciones **\#** **\#** de tipo. El archivo IDL y los archivos de origen C pueden incluir de forma segura un archivo que contenga solo directivas de preprocesador. Aunque las directivas no estarán disponibles en el archivo de encabezado generado por el compilador MIDL, el programa de origen de C puede incluir el archivo de encabezado independiente. De forma similar, se puede importar un archivo de encabezado con instrucciones define y definiciones de tipo **\#** normal desde el archivo IDL. Este enfoque encapsula las instrucciones define y typedef usándolos en un archivo H para que los símbolos definidos no se usen directamente en el archivo **\#** **\#** IDL de importación. La importación de un archivo de encabezado o IDL a otro archivo IDL impide que las instrucciones typedef se repliquen en el archivo H generado por MIDL (que es a diferencia de las instrucciones **\#** include). Este enfoque permite hacer referencia de forma segura al archivo de encabezado original desde el código C a lo largo del archivo H generado sin tener ningún problema con definiciones duplicadas.

El uso de constantes de enumeración en el archivo IDL también es efectivo. Estas constantes se pueden usar en expresiones constantes en IDL, por ejemplo, en declaradores de matriz. El preprocesador del compilador de C no quita las constantes de enumeración durante las primeras fases de la compilación MIDL, por lo que las constantes de enumeración están disponibles en el archivo de encabezado generado por el compilador midl. Considere la instrucción siguiente:

``` syntax
typedef enum midlworkaround { MAXSTRINGCOUNT = 300 };
```

El preprocesador de C no quitará esta instrucción durante la compilación MIDL y la definición de tipo se replicará en el archivo H generado. La constante MAXSTRINGCOUNT está disponible para los programas de código fuente de C que incluyen el archivo de encabezado generado por el compilador MIDL.

Por último, la [**directiva de \_ comillas cpp**](cpp-quote.md) de MIDL se puede usar para escribir una cadena arbitraria directamente en el archivo H generado. Por ejemplo, para obtener la constante de manifiesto usada anteriormente en esta página con la cita **cpp \_**, se puede usar la siguiente instrucción:

``` syntax
cpp_quote ("#define ARRSIZE 10")
```

Esta instrucción genera la siguiente línea en el archivo de encabezado:

``` syntax
#define ARRSIZE 10
```

 

 




