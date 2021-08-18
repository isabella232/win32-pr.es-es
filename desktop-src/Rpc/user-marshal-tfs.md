---
title: Serialización de usuario
description: Serialización de usuario en llamada a procedimiento remoto (RPC).
ms.assetid: 5119e959-d8b8-4fca-8910-568bb9063a9d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6dcc9574b49a46b6e867fc4bca314944589ccf68b9d6e3fb8695a099eb255c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010853"
---
# <a name="user-marshal"></a>Serialización de usuario

El cálculo de referencias de usuario tiene una cadena de formato similar a transmitir \_ como:

``` syntax
FC_USER_MARSHAL
flags<1>
quadruple_index<2>
user_type_memory_size<2>
transmitted_type_buffer size<2>
offset_to_the_transmitted_type<2>
```

Las marcas<1> byte consta de la marca superior nibble y el nibble de alineación inferior.

Los 2 bits superiores de la marca nibble se usan para describir si el tipo de conexión se define como un puntero único, un puntero de referencia o ningún puntero (no puede ser un ptr). Se han definido los manifiestos siguientes para establecer o obtener las marcas:

``` syntax
#define USER_MARSHAL_UNIQUE         0x80
#define USER_MARSHAL_REF            0x40
#define USER_MARSHAL_POINTER        0xc0  /* unique or ref */
#define USER_MARSHAL_IID            0x20  /* JIT compiler only */
```

El nibble de alineación de la palabra de marca mantiene la alineación de la conexión del tipo transmitido.

El índice de<2> es un índice de la rutina de devolución de llamada \_ de las funciones de serialización de usuario. Las posiciones rutinarias son las siguientes: tamaño, serialización, desmarque y rutina de liberación.

El tamaño de memoria de tipo<2> proporciona un tamaño para el tipo específico del \_ \_ \_ usuario, incluidos los tipos desconocidos.

El tamaño de búfer de tipo transmitido<2> es cero cuando el tamaño varía \_ o el tamaño fijo \_ \_ real. Se trata de una optimización que permite a MIDL omitir las devoluciones de llamada al cambiar el tamaño del búfer y también al liberar.

## <a name="range"></a>Intervalo

La \[ comprobación \] de intervalos proporciona medios adicionales para la validación de argumentos en la capa RANGE. El \[ \] descriptor de intervalo tiene el formato siguiente:

``` syntax
FC_RANGE,   flags_type <1>
low value<4>
high value<4>
```

Las marcas toman el nibble superior y el tipo de la minúscula del segundo byte. Los valores bajo y alto dependen del tipo de la variable que se va a comprobar.

Las marcas están pensadas como un vehículo de expansión. el compilador ha estado estableciendo el valor de nibble en cero.

 

 




