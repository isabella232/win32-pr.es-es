---
title: Identificadores de contexto STRICT y Type STRICT
description: Use el \_ \_ atributo de identificador de contexto STRICT para todos los identificadores de contexto.
ms.assetid: 2483aa76-0814-4f63-9c38-0aa050d73772
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a45b4e7914034e315f2275e1d928293332012fc4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488010"
---
# <a name="strict-and-type-strict-context-handles"></a>Identificadores de contexto STRICT y Type STRICT

Use el atributo de [**\_ \_ identificador de contexto STRICT**](/windows/desktop/Midl/strict-context-handle) para todos los identificadores de contexto. De forma predeterminada, un identificador de contexto no está asociado a una interfaz, lo que significa que se puede crear un identificador de contexto en una interfaz y, a continuación, pasarse a otro. Este es un ataque sencillo y muchos servidores RPC no pueden evitarlo.

Si dos interfaces coexisten en el mismo proceso, un atacante puede abrir un identificador de contexto en una interfaz y pasarlo a otro, lo que puede hacer frente a los datos inesperados. Muchos desarrolladores consideran que el software es la única interfaz de un proceso, pero con frecuencia no es el caso, ya que tanto el sistema como muchos componentes de terceros usan RPC internamente, y esas interfaces pueden crear identificadores de contexto. Cuando se usa el atributo de [**\_ \_ identificador de contexto STRICT**](/windows/desktop/Midl/strict-context-handle) , el tiempo de ejecución de RPC garantiza que un contexto creado en una interfaz se puede pasar como argumento solo a los métodos de esa interfaz.

En situaciones en las que se desarrolla una aplicación para Windows Vista, el uso del [**\_ \_ \_ identificador de contexto STRICT**](/windows/desktop/Midl/type-strict-context-handle) está disponible y se recomienda. Los identificadores de contexto no se asocian a un tipo específico de forma predeterminada. Cuando se usan varios tipos de identificadores de contexto en el mismo proceso, es posible que un cliente malintencionado pase un identificador de contexto en lugar de otro para producir resultados no deseados. El uso del **\_ identificador de \_ contexto \_ STRICT de tipo** permite a las aplicaciones aplicar la coherencia del tipo de identificador de contexto y evitar el uso del tipo de identificador de contexto no coincidente.

 

 