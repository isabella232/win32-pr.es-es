---
description: Los objetos de datos contienen los datos reales o una referencia a los datos. Cada objeto de datos tiene una plantilla correspondiente que especifica el tipo de datos. En las secciones siguientes se describe el formulario y las partes de los objetos de datos.
ms.assetid: 61dbe241-2658-4dd0-af89-3db204b56fad
title: Datos (formato de archivo X, codificación de texto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0acd4222e2878b882b8777e3ba22e28f2d213fb5f3550686baf29b4ed6719e5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117730206"
---
# <a name="data-x-file-format-text-encoding"></a>Datos (formato de archivo X, codificación de texto)

Los objetos de datos contienen los datos reales o una referencia a los datos. Cada objeto de datos tiene una plantilla correspondiente que especifica el tipo de datos. En las secciones siguientes se describe el formulario y las partes de los objetos de datos.

## <a name="form-identifier-and-name"></a>Formulario, identificador y nombre

Los objetos de datos tienen el formato siguiente.


```
        <Identifier> [name] { [<UUID>]
    <member 1>;
...
    <member n>;
}
```



El identificador es obligatorio y debe coincidir con un tipo de datos definido previamente o primitivo. Sin embargo, el nombre es opcional.

## <a name="data-members"></a>Miembros de datos

Los miembros de datos pueden ser uno de los siguientes: objeto de datos, referencia de datos, lista de enteros, lista flotante o lista de cadenas.

Un objeto de datos es un objeto de datos anidado. Esto permite expresar la naturaleza jerárquica del formato de archivo. Los tipos de objetos de datos anidados permitidos en la jerarquía pueden estar restringidos.

Una referencia de datos es una referencia a un objeto de datos encontrado anteriormente, como se muestra en el ejemplo siguiente.


```
{
  name |
  UUID |
  name UUID
}
```



Una lista de enteros es una lista separada por punto y coma de enteros, como se muestra en el ejemplo siguiente.


```
1; 2; 3;
```



Una lista float es una lista separada por punto y coma de elementos float, como se muestra en el ejemplo siguiente.


```
1.0; 2.0; 3.0;
```



Una lista de cadenas es una lista separada por punto y coma de cadenas, como se muestra en el ejemplo siguiente.


```
"Moose"; "Goats"; "Sheep";
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Codificación de texto](text-encoding.md)
</dt> </dl>

 

 



