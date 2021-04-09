---
title: Serialización de tipo
description: El compilador MIDL genera hasta tres funciones para cada tipo al que se aplica el atributo \ encode \ o \ decode \.
ms.assetid: 948f1dd7-c8b0-4fa0-88d8-9d122de52ba1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4674617bc98c92dbc684a29d1a3c91ac6a7429e1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149425"
---
# <a name="type-serialization"></a>Serialización de tipo

El compilador MIDL genera hasta tres funciones para cada tipo al que \[ [](/windows/desktop/Midl/encode) \] se aplica el atributo de codificación o \[ [descodificación](/windows/desktop/Midl/decode) \] . Por ejemplo, para un tipo definido por el usuario denominado mi *tipo*, el compilador genera código para las \_ funciones de codificación, \_ descodificación y tipo \_ AlignSize. Para estas funciones, el compilador escribe prototipos en stub. h y el código fuente en stub \_ c.c. Por lo general, puede codificar un objeto de *tipo* de usuario con \_ la codificación de tipo y descodificar un objeto del búfer mediante la \_ descodificación de tipo. \_Se utiliza AlignSize si necesita conocer el tamaño del búfer de serialización antes de asignarlo.

El compilador MIDL genera la siguiente función de codificación. Esta función serializa los datos para el objeto al que apunta pObject y el búfer se obtiene según el método especificado en el identificador. Después de escribir los datos serializados en el búfer, se controla el búfer. Tenga en cuenta que el identificador hereda el estado de las llamadas anteriores y los búferes se deben alinear en 8.

Para un identificador implícito:

``` syntax
void MyType_Encode (MyType __RPC_FAR * pObject);
```

Para un identificador explícito:

``` syntax
void MyType_Encode (handle_t Handle, MyType __RPC_FAR * pObject);
```

La función siguiente deserializa los datos del almacenamiento de la aplicación en el objeto al que apunta pObject. Proporcione un búfer calculado según el método especificado en el identificador. Tenga en cuenta que el identificador puede heredar el estado de las llamadas anteriores y los búferes se deben alinear en 8.

Para un identificador implícito:

``` syntax
void MyType_Decode (MyType __RPC_FAR * pObject);
```

Para un identificador explícito:

``` syntax
void MyType_Decode (handle_t Handle, MyType __RPC_FAR * pObject);
```

La función siguiente devuelve un tamaño, en bytes, que incluye la instancia de tipo más los bytes de relleno necesarios para alinear los datos. Esto permite serializar un conjunto de instancias del mismo tipo o de tipos diferentes en un búfer, a la vez que se garantiza que los datos de cada objeto están alineados correctamente. \_AlignSize da por supuesto que la instancia a la que apunta pObject se serializará en un búfer que comienza en el desplazamiento alineado en 8.

Para un identificador implícito:

``` syntax
size_t MyType_AlignSize (MyType __RPC_FAR * pObject);
```

Para un identificador explícito:

``` syntax
size_t MyType_AlignSize (handle_t Handle, MyType __RPC_FAR * pObject);
```

Tenga en cuenta que los procedimientos remotos con identificadores de enlace implícitos y tipos serializados con identificadores de serialización implícitos usan la misma variable de identificador global. Por lo tanto, es aconsejable no mezclar la serialización de tipos y los procedimientos remotos en una interfaz con identificadores implícitos. Para obtener más información, vea [identificadores implícitos e explícitos](implicit-versus-explicit-handles.md).

 

 