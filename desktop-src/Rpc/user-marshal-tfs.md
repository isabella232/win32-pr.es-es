---
title: Serialización de usuario
description: 'Usuario: serialización en llamada a procedimiento remoto (RPC).'
ms.assetid: 5119e959-d8b8-4fca-8910-568bb9063a9d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c901fd8c75137b4657322a89692ff8a3afb5408
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903472"
---
# <a name="user-marshal"></a>Serialización de usuario

La serialización de usuario tiene una cadena de formato similar a transmitir \_ como:

``` syntax
FC_USER_MARSHAL
flags<1>
quadruple_index<2>
user_type_memory_size<2>
transmitted_type_buffer size<2>
offset_to_the_transmitted_type<2>
```

Las marcas<1> byte están formadas por el recorte superior de la marca y el recorte de alineación inferior.

Los 2 bits superiores del recorte de la marca se usan para describir si el tipo de conexión se define como un puntero único, un puntero de referencia o ningún puntero (no puede ser un PTR). Los siguientes manifiestos se han definido para establecer u obtener las marcas:

``` syntax
#define USER_MARSHAL_UNIQUE         0x80
#define USER_MARSHAL_REF            0x40
#define USER_MARSHAL_POINTER        0xc0  /* unique or ref */
#define USER_MARSHAL_IID            0x20  /* JIT compiler only */
```

El recorte de alineación de la palabra de marca mantiene la alineación del cable del tipo transmitido.

El \_ Índice quadruple<2> es un índice de la rutina de devolución de llamada cuádruple de las funciones de cálculo de referencias de usuario. Las posiciones de rutina son las siguientes: el ajuste de tamaño, serialización, desserialización y liberación de rutina.

El \_ \_ \_ tamaño de memoria de tipo de usuario<2> proporciona un tamaño para el tipo específico del usuario, incluidos los tipos desconocidos.

El tamaño del búfer de tipo transmitido \_ \_ \_<2> es cero cuando el tamaño es variable o el tamaño fijo real. Se trata de una optimización que permite a MIDL omitir las devoluciones de llamada al cambiar el tamaño del búfer y también cuando se libera.

## <a name="range"></a>Intervalo

La \[ comprobación de intervalo \] proporciona medios adicionales para la validación de argumentos en la capa de NDR. El \[ \] descriptor de intervalo tiene el siguiente formato:

``` syntax
FC_RANGE,   flags_type <1>
low value<4>
high value<4>
```

Las marcas toman el recorte superior y el tipo el recorte inferior del segundo byte. Los valores bajo y alto dependen del tipo de variable que se va a comprobar.

Las marcas están diseñadas como vehículo de expansión; el compilador ha establecido el recorte en cero.

 

 




