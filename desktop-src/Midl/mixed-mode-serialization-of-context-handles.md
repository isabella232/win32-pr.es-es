---
title: Serialización en modo mixto de identificadores de contexto
description: En Microsoft Windows XP, una sola interfaz puede dar cabida a identificadores de contexto serializados y no serializados, lo que se denomina serialización en modo mixto.
ms.assetid: b52c1d6f-cdc5-4597-a36e-bb957e4aab01
keywords:
- MIDL de referencia del lenguaje MIDL, serialización en modo mixto de identificadores de contexto
- control de contexto MIDL
- MIDL de serialización en modo mixto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aaa35f02a939a50e2484ace29630783ee219d6313d7538cba54b1f54cd83007
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787435"
---
# <a name="mixed-mode-serialization-of-context-handles"></a>Serialización en modo mixto de identificadores de contexto

A partir de Windows XP, una sola interfaz puede dar cabida a identificadores de contexto serializados y no serializados, lo que permite que un método de una interfaz acceda a un identificador de contexto exclusivamente (serializado), mientras que otros métodos acceden a ese identificador de contexto en modo compartido (no serializado). Para obtener más información sobre los identificadores de contexto, vea los atributos siguientes:

-   [**identificador de \_ contexto**](context-handle.md)
-   [**serialización \_ del \_ identificador de contexto**](context-handle-serialize.md)
-   [**noserialize \_ del \_ identificador de contexto**](context-handle-noserialize.md)

Las funcionalidades de acceso en modo compartido y serializado son comparables a los mecanismos de bloqueo de lectura y escritura. Los métodos que usan un identificador de contexto serializado son usuarios exclusivos (escritores), mientras que los métodos que usan un identificador de contexto no serializado son usuarios compartidos (lectores). Se deben serializar los métodos que destruyen o modifican el estado de un identificador de contexto. Los métodos que no modifican el estado de un identificador de contexto, como los métodos que simplemente leen de un identificador de contexto, pueden no serializarse. El uso de un identificador de contexto en modo mixto puede mejorar considerablemente la escalabilidad de un servidor, especialmente cuando varios subprocesos hacen llamadas simultáneas al mismo identificador de contexto.

RPC no aplica el "bloqueo de escritura" en los métodos mediante un identificador de contexto en modo compartido, lo que significa que las aplicaciones deben asegurarse de que los identificadores de contexto del modo compartido no se modifican. La modificación de un identificador de contexto usado en modo compartido puede provocar daños sutiles en el contenido del identificador de contexto, que son imposibles de depurar.

Cambiar la lógica de serialización de un identificador de contexto solo afecta al servidor. Además, cambiar la lógica de serialización de un identificador de contexto no afecta al formato de conexión y, por lo tanto, los cambios en la lógica de serialización en un servidor no afectan a la capacidad de los clientes existentes para interactuar con el servidor.

No se recomienda usar solo identificadores de contexto no serializados. Los servidores que usan identificadores no serializados deben cambiar al acceso serializado para el método que cierra el identificador de contexto.

Los identificadores de contexto que están fuera de - solo se usan normalmente en los métodos de creación \[ y no requieren ninguna \] serialización. Por lo tanto, cualquier atributo de serialización aplicado a los identificadores de contexto out -only, como la serialización de identificadores de contexto o el identificador de contexto \[ \] [**\_ \_ noserialize**](context-handle-noserialize.md) [**\_ \_**](context-handle-serialize.md) , se omite mediante RPC.

> [!Note]  
> Los métodos de creación se serializan implícitamente.

 

## <a name="examples"></a>Ejemplos

En los dos ejemplos siguientes se muestra cómo habilitar la serialización en modo mixto de identificadores de contexto.

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

[**identificador de \_ contexto**](context-handle.md)
</dt> <dt>

[**serialización \_ del \_ identificador de contexto**](context-handle-serialize.md)
</dt> <dt>

[**noserialize \_ del \_ identificador de contexto**](context-handle-noserialize.md)
</dt> </dl>

 

 




