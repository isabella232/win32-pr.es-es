---
title: Serialización de tipos
description: El compilador MIDL genera hasta tres funciones para cada tipo al que se aplica el atributo \ encode\ o \ decode\.
ms.assetid: 948f1dd7-c8b0-4fa0-88d8-9d122de52ba1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 681d898a077ff55bb03a76fbd7579e28a8bcdf18c792330b32b1eb832c6b9058
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011103"
---
# <a name="type-serialization"></a>Serialización de tipos

El compilador MIDL genera hasta tres funciones para cada tipo al que se aplica el atributo de codificación \[ [](/windows/desktop/Midl/encode) \] \[ [](/windows/desktop/Midl/decode) \] o descodificación. Por ejemplo, para un tipo definido por el usuario denominado *MyType*, el compilador genera código para las funciones MyType \_ Encode, MyType Decode y \_ MyType \_ AlignSize. Para estas funciones, el compilador escribe prototipos en Stub.h y código fuente en Stub \_ c.c. Por lo general, puede codificar un objeto *MyType* con MyType Encode y descodificar un objeto del \_ búfer mediante MyType \_ Decode. MyType AlignSize se usa si necesita conocer el tamaño del búfer de serialización \_ antes de asignarlo.

El compilador MIDL genera la siguiente función de codificación. Esta función serializa los datos del objeto al que apunta pObject y el búfer se obtiene según el método especificado en el identificador. Después de escribir los datos serializados en el búfer, puede controlar el búfer. Tenga en cuenta que el identificador hereda el estado de las llamadas anteriores y que los búferes deben estar alineados en 8.

Para un identificador implícito:

``` syntax
void MyType_Encode (MyType __RPC_FAR * pObject);
```

Para un identificador explícito:

``` syntax
void MyType_Encode (handle_t Handle, MyType __RPC_FAR * pObject);
```

La función siguiente deserializa los datos del almacenamiento de la aplicación en el objeto al que apunta pObject. Proporcione un búfer serializado según el método especificado en el identificador. Tenga en cuenta que el identificador puede heredar el estado de las llamadas anteriores y los búferes deben estar alineados en 8.

Para un identificador implícito:

``` syntax
void MyType_Decode (MyType __RPC_FAR * pObject);
```

Para un identificador explícito:

``` syntax
void MyType_Decode (handle_t Handle, MyType __RPC_FAR * pObject);
```

La función siguiente devuelve un tamaño, en bytes, que incluye la instancia de tipo más los bytes de relleno necesarios para alinear los datos. Esto permite serializar un conjunto de instancias de los mismos tipos o diferentes en un búfer, al tiempo que se garantiza que los datos de cada objeto se alinean correctamente. MyType AlignSize supone que la instancia a la que apunta pObject se serializará en un búfer a partir del \_ desplazamiento alineado en 8.

Para un identificador implícito:

``` syntax
size_t MyType_AlignSize (MyType __RPC_FAR * pObject);
```

Para un identificador explícito:

``` syntax
size_t MyType_AlignSize (handle_t Handle, MyType __RPC_FAR * pObject);
```

Tenga en cuenta que ambos procedimientos remotos con identificadores de enlace implícitos y tipos serializados con identificadores de serialización implícita usan la misma variable de identificador global. Por lo tanto, es aconsejable no mezclar la serialización de tipos y los procedimientos remotos en una interfaz con identificadores implícitos. Para obtener más información, [vea Identificadores implícitos frente a identificadores explícitos.](implicit-versus-explicit-handles.md)

 

 