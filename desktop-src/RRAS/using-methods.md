---
title: Usar métodos
description: Cuando un cliente se registra con el administrador de tablas de enrutamiento, puede exportar un conjunto de métodos. Otros clientes usan estos métodos para obtener información específica del cliente. Los métodos permiten la comunicación privada entre los clientes del administrador de tablas de enrutamiento.
ms.assetid: 6d984a02-d005-43ad-81c4-968ae9c1a105
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33bd895fbb3f8f54224522786b5794c5c6c57a9e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171302"
---
# <a name="using-methods"></a>Usar métodos

Cuando un cliente se registra con el administrador de tablas de enrutamiento, puede exportar un conjunto de métodos. Otros clientes usan estos métodos para obtener información específica del cliente. Los métodos permiten la comunicación privada entre los clientes del administrador de tablas de enrutamiento.

Un cliente puede obtener la lista de métodos exportados por otro cliente. El cliente llama a [**la función RtmGetEntityMethods**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentitymethods) y proporciona el identificador del cliente de destino.

Cada método exportado por un cliente se identifica de forma única mediante su identificador de método. Cada cliente puede exportar hasta 32 métodos. Cada método corresponde a un conjunto de bits en el **miembro MethodType** de la estructura [**\_ RTM ENTITY \_ EXPORT \_ METHOD.**](/windows/win32/api/rtmv2/nc-rtmv2-_entity_method) Para invocar varios métodos, el cliente debe realizar un OR lógico de los identificadores de esos métodos. La sintaxis y semántica de las estructuras de entrada y salida de cada protocolo deben especificarse cuando se implementa el protocolo.

> [!Note]  
> Microsoft reserva los valores de identificador de método que corresponden a un conjunto de bits en la mitad inferior del **miembro MethodType** (los 16 bits inferiores).

 

Para invocar el método de un segundo cliente, un cliente llama a la [**función RtmInvokeMethod.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) El administrador de tablas de enrutamiento invoca todas las solicitudes para invocar los métodos de un cliente. El administrador de tablas de enrutamiento realiza dos funciones cuando se entrelaza entre clientes:

-   Impedir que el segundo cliente invoje un método para un cliente que está anulando el registro.
-   Se mantiene una solicitud de "invocación" cuando se bloquean los métodos y se permite que la solicitud continúe cuando se desbloquean los métodos.

Si un cliente debe impedir que otros clientes ejecuten sus métodos, el cliente puede llamar a [**RtmBlockMethods**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmblockmethods). El administrador de tablas de enrutamiento no permitirá que se procese una llamada a [**RtmInvokeMethod**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) hasta que el cliente vuelva a desbloquear sus métodos.

Normalmente, los clientes bloquean los métodos al realizar cambios en los datos privados que se intercambian entre clientes. Los métodos de bloqueo son una acción opcional. Un cliente también puede usar bloqueos internos para evitar que otros clientes invojen métodos.

Para obtener código de ejemplo que muestra cómo usar estas funciones, vea [Obtener y llamar a los métodos exportados para un cliente](obtain-and-call-the-exported-methods-for-a-client.md).

 

 




