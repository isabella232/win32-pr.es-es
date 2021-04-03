---
title: Atributos de tipo
description: La llamada a procedimiento remoto (RPC) y los atributos de tipo MIDL que se pueden aplicar a las declaraciones de tipos.
ms.assetid: cd7fd582-6162-4154-9dff-6c86c344b9ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 378fbc91f17e77baff7e259bd3551a47fde653cc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904618"
---
# <a name="type-attributes"></a>Atributos de tipo

Los atributos de tipo son los atributos MIDL que se pueden aplicar a las declaraciones de tipos:

-   **\[**[**asa**](/windows/desktop/Midl/handle)**\]**
-   **\[**[**identificador de contexto \_**](/windows/desktop/Midl/context-handle)**\]**
-   **\[**[**tipo de conmutador \_**](/windows/desktop/Midl/switch-type)**\]**
-   [atributos de tipo de puntero](three-pointer-types.md)

El atributo de **\[ \_ tipo \] de conmutador** designa el tipo de un discriminador de Unión. Este atributo solo se aplica a una Unión no encapsulada.

Un identificador de contexto es un puntero con un atributo de **\[ \_ identificador \] de contexto** . El atributo de **\[ \_ identificador \] de contexto** permite escribir procedimientos que mantienen información de estado entre llamadas a procedimientos remotos. Un identificador de contexto con un valor distinto de NULL representa el contexto guardado y sirve para dos propósitos:

-   En el lado del cliente, contiene la información necesaria para que la biblioteca en tiempo de ejecución de RPC dirija la llamada al servidor.
-   En el lado del servidor, actúa como un identificador en el contexto activo.

El **\[** [](/windows/desktop/Midl/handle) **\]** atributo Handle especifica que un tipo puede aparecer como un identificador definido por el usuario (Genérico). Esta característica permite el diseño de identificadores que son significativos para la aplicación. El usuario debe proporcionar rutinas de enlace y desenlace para realizar la conversión entre el tipo de identificador definido por el usuario y el tipo de identificador primitivo de RPC, **Handle \_ t**. Un identificador primitivo contiene información de destino significativa para las bibliotecas en tiempo de ejecución de RPC. Un identificador definido por el usuario solo se puede definir en una declaración de tipos, no en una declaración de función. Un parámetro con el atributo **\[ Handle \]** tiene un doble propósito. Se utiliza para determinar el enlace de la llamada y se transmite al procedimiento llamado como un parámetro de datos normal.

 

 