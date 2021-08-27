---
title: Atributos de tipo
description: Llamada a procedimiento remoto (RPC) y los atributos de tipo MIDL que se pueden aplicar a las declaraciones de tipo.
ms.assetid: cd7fd582-6162-4154-9dff-6c86c344b9ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5da8f3beb62f443b95a42283d4625200812436bce1bc667edc07d68f2542544
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011173"
---
# <a name="type-attributes"></a>Atributos de tipo

Los atributos de tipo son los atributos MIDL que se pueden aplicar a las declaraciones de tipo:

-   **\[**[**Manejar**](/windows/desktop/Midl/handle)**\]**
-   **\[**[**identificador de \_ contexto**](/windows/desktop/Midl/context-handle)**\]**
-   **\[**[**tipo \_ de conmutador**](/windows/desktop/Midl/switch-type)**\]**
-   [atributos de tipo de puntero](three-pointer-types.md)

El **\[ atributo switch \_ type \]** designa el tipo de un discriminador de unión. Este atributo solo se aplica a una unión nocapsulada.

Un identificador de contexto es un puntero con un atributo **\[ de identificador \_ de \]** contexto. El **\[ atributo de \_ identificador \]** de contexto permite escribir procedimientos que mantienen información de estado entre llamadas a procedimientos remotos. Un identificador de contexto con un valor distinto de NULL representa el contexto guardado y sirve para dos propósitos:

-   En el lado cliente, contiene la información necesaria para que la biblioteca en tiempo de ejecución rpc dirija la llamada al servidor.
-   En el lado servidor, actúa como identificador en el contexto activo.

El **\[** [**atributo**](/windows/desktop/Midl/handle) handle especifica que un tipo puede producirse como un identificador **\]** definido por el usuario (genérico). Esta característica permite el diseño de identificadores que son significativos para la aplicación. El usuario debe proporcionar rutinas de enlace y desenlace para convertir entre el tipo de identificador definido por el usuario y el tipo de identificador primitivo rpc, **\_ handle t**. Un identificador primitivo contiene información de destino significativa para las bibliotecas en tiempo de ejecución de RPC. Un identificador definido por el usuario solo se puede definir en una declaración de tipo, no en una declaración de función. Un parámetro con el **\[ atributo handle \]** tiene un propósito doble. Se usa para determinar el enlace de la llamada y se transmite al procedimiento llamado como un parámetro de datos normal.

 

 