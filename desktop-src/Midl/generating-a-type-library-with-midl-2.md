---
title: Generar una biblioteca de tipos con MIDL
description: El elemento de nivel superior de la sintaxis ODL es la instrucción Library (bloque de biblioteca).
ms.assetid: e21a9e6e-4e10-4280-af8f-24534cb2ab90
keywords:
- Lenguaje de definición de interfaz de Microsoft MIDL, tareas, generar una biblioteca de tipos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85f6e8f7ea6f65bc503c08872c9199ff3d5fd828
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105651374"
---
# <a name="generating-a-type-library-with-midl"></a>Generar una biblioteca de tipos con MIDL

El elemento de nivel superior de la sintaxis ODL es la instrucción Library (bloque de biblioteca). Todas las demás instrucciones ODL, con la excepción de los atributos que se aplican a la instrucción Library, deben definirse dentro del bloque de biblioteca. Cuando el compilador MIDL ve un bloque de biblioteca, genera una biblioteca de tipos prácticamente de la misma manera que en MkTypLib. Con algunas excepciones, descritas en [diferencias entre MIDL y MkTypLib](differences-between-midl-and-mktyplib.md), las instrucciones dentro del bloque de biblioteca deben seguir la misma sintaxis que en el lenguaje ODL y MkTypLib.

> [!Note]  
> La herramienta Mktyplib.exe está obsoleta. En su lugar, utilice el compilador de MIDL.

 

Puede aplicar atributos ODL a los elementos que se definen dentro o fuera del bloque de biblioteca. Estos atributos no tienen ningún efecto fuera del bloque de biblioteca a menos que se haga referencia al elemento al que se aplican desde dentro del bloque de biblioteca. Las instrucciones dentro del bloque de biblioteca pueden hacer referencia a un elemento externo mediante su uso como un tipo base, heredando de él o haciendo referencia a él en una línea, como se muestra a continuación:

``` syntax
<some IDL definitions including definitions for interface IFace and struct bar>
[<some attributes>]
library a
{
    interface IFace;
    struct this_struct;
...
};
```

Si se hace referencia a un elemento definido fuera del bloque de biblioteca dentro del bloque de biblioteca, su definición se colocará en la biblioteca de tipos generada. El compilador MIDL trata las instrucciones fuera de un bloque de biblioteca como un archivo IDL típico y analiza esas instrucciones tal y como se ha hecho siempre. Normalmente, esto significa generar códigos auxiliares de lenguaje C para una aplicación RPC.

Para obtener más información sobre la sintaxis general de un archivo ODL, vea [Sintaxis del archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax).

 

 