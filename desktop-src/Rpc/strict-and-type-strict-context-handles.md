---
title: Identificadores de contexto strict y type strict
description: Use el atributo strict \_ context handle para todos los \_ identificadores de contexto.
ms.assetid: 2483aa76-0814-4f63-9c38-0aa050d73772
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a45b4e7914034e315f2275e1d928293332012fc4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473502"
---
# <a name="strict-and-type-strict-context-handles"></a>Identificadores de contexto strict y type strict

Use el atributo [**strict \_ context \_ handle**](/windows/desktop/Midl/strict-context-handle) para todos los identificadores de contexto. De forma predeterminada, un identificador de contexto no está asociado a una interfaz, lo que significa que se puede crear un identificador de contexto en una interfaz y, a continuación, pasar a otra. Se trata de un ataque sencillo y muchos servidores RPC no pueden evitarlo.

Si dos interfaces coexisten en el mismo proceso, un atacante puede abrir un identificador de contexto en una interfaz y pasarlo a otra, lo que puede superar los datos inesperados. Muchos desarrolladores creen que su software es la única interfaz de un proceso, pero a menudo no es así, porque el sistema y muchos componentes de terceros usan RPC internamente, y esas interfaces pueden crear identificadores de contexto. Cuando se [**usa \_ el \_**](/windows/desktop/Midl/strict-context-handle) atributo de identificador de contexto estricto, el tiempo de ejecución rpc garantiza que un contexto creado en una interfaz solo se puede pasar como argumento a los métodos de esa interfaz.

En situaciones en las que se desarrolla una aplicación para Windows Vista, el uso del identificador de contexto estricto de tipo está disponible y recomendado. [**\_ \_ \_**](/windows/desktop/Midl/type-strict-context-handle) Los identificadores de contexto no están asociados a un tipo específico de forma predeterminada. Cuando se usan varios tipos de identificadores de contexto en el mismo proceso, es posible que un cliente malintencionado pase un identificador de contexto en lugar de otro para generar resultados no deseados. El uso del identificador de contexto estricto de **\_ \_ \_ tipo** permite a las aplicaciones aplicar la coherencia del tipo de identificador de contexto y evitar cualquier uso de tipos de identificador de contexto no coincidentes.

 

 