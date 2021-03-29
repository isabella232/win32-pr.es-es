---
title: Serialización en modo mixto de identificadores de contexto
description: En Microsoft Windows XP, una sola interfaz puede alojar identificadores de contexto serializados y no serializados, lo que se denomina serialización en modo mixto.
ms.assetid: b52c1d6f-cdc5-4597-a36e-bb957e4aab01
keywords:
- Referencia del lenguaje MIDL (MIDL), serialización en modo mixto de identificadores de contexto
- identificadores de contexto MIDL
- MIDL de serialización en modo mixto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0922b53bfc7ba2e30ad8df0764e3cf9a36f0f723
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903440"
---
# <a name="mixed-mode-serialization-of-context-handles"></a>Serialización en modo mixto de identificadores de contexto

A partir de Windows XP, una sola interfaz puede alojar identificadores de contexto serializados y no serializados, lo que permite que un método de una interfaz tenga acceso a un identificador de contexto exclusivamente (serializado), mientras que otros métodos tienen acceso a ese identificador de contexto en modo compartido (no serializado). Para obtener más información sobre los identificadores de contexto, vea los siguientes atributos:

-   [**identificador de contexto \_**](context-handle.md)
-   [**\_serializar identificador de contexto \_**](context-handle-serialize.md)
-   [**identificador de contexto de \_ \_ noserialización**](context-handle-noserialize.md)

Las capacidades de acceso de modo de uso compartido y en serie son comparables a los mecanismos de bloqueo de lectura y escritura. los métodos que usan un identificador de contexto serializado son usuarios exclusivos (escritores), mientras que los métodos que usan un identificador de contexto no serializado son usuarios compartidos (lectores). Se deben serializar los métodos que destruyen o modifican el estado de un identificador de contexto. Los métodos que no modifican el estado de un identificador de contexto, como los métodos que simplemente leen un identificador de contexto, pueden ser no serializados. El uso de un identificador de contexto en modo mixto puede mejorar considerablemente la escalabilidad de un servidor, especialmente cuando varios subprocesos realizan llamadas simultáneas al mismo identificador de contexto.

RPC no exige "bloqueo de escritura" en los métodos que usan un identificador de contexto en modo compartido, lo que significa que las aplicaciones deben asegurarse de que los identificadores de contexto del modo compartido no se modifiquen. La modificación de un identificador de contexto que se usa en modo compartido puede dar lugar a daños sutiles en el contenido de los identificadores de contexto, que son imposibles de depurar.

El cambio de la lógica de serialización de un identificador de contexto solo afecta al servidor. Además, el cambio de la lógica de serialización de un identificador de contexto no afecta al formato de conexión y, por lo tanto, los cambios en la lógica de serialización en un servidor no afectan a la capacidad de los clientes existentes para interactuar con el servidor.

No se recomienda usar solo identificadores de contexto no serializados. Los servidores que usan identificadores no serializados deben cambiar al acceso serializado para el método que cierra el identificador de contexto.

\[ \] Los métodos de creación suelen usar identificadores de contexto que no son de solo uso y no requieren ninguna serialización. Por lo tanto, el atributo de serialización que se aplica a los \[ \] identificadores de contexto de solo salida, como [**\_ \_ serializar identificador**](context-handle-serialize.md) de contexto o [**identificador de contexto \_ \_ noserialización**](context-handle-noserialize.md), lo omite RPC.

> [!Note]  
> Los métodos de creación se serializan implícitamente.

 

## <a name="examples"></a>Ejemplos

Los dos ejemplos siguientes muestran cómo habilitar la serialización en modo mixto de identificadores de contexto.

En el primer ejemplo se muestra cómo hacerlo en el archivo IDL:

``` syntax
typedef [context_handle] void *TestContextHandleExclusive;
typedef [context_handle] TestContextHandleExclusive TestContextHandleShared;

void
UseShared(...
          [in] TestContextHandleShared *Ctx,
          ...);

void
UseExclusive(...
             [in, out] TestContextHandleExclusive *Ctx,
             ...);
```

En el segundo ejemplo se muestra cómo habilitar la serialización en modo mixto de identificadores de contexto en el archivo ACF:

``` syntax
typedef [context_handle_serialize] TestContextHandleExclusive;

typedef [context_handle_noserialize] TestContextHandleShared;
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**identificador de contexto \_**](context-handle.md)
</dt> <dt>

[**\_serializar identificador de contexto \_**](context-handle-serialize.md)
</dt> <dt>

[**identificador de contexto de \_ \_ noserialización**](context-handle-noserialize.md)
</dt> </dl>

 

 




