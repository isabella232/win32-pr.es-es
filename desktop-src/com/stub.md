---
title: Agrupa
description: El código auxiliar, al igual que el proxy, se compone de una o varias partes de la interfaz y un administrador.
ms.assetid: ed7d5546-2d19-4055-b078-62b39d0317b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 109936ae16827dce7779b080902dbca74a8dfc51
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/03/2021
ms.locfileid: "105697898"
---
# <a name="stub"></a>Agrupa

El código auxiliar, al igual que el proxy, se compone de una o varias partes de la interfaz y un administrador. Cada código auxiliar de interfaz proporciona código para deshacer las referencias de los parámetros y el código que llama a una de las interfaces admitidas del objeto. Cada código auxiliar también proporciona una interfaz para la comunicación interna. El administrador de código auxiliar realiza un seguimiento de los códigos auxiliares de interfaz disponibles.

Sin embargo, hay las siguientes diferencias entre el código auxiliar y el proxy:

-   La diferencia más importante es que el código auxiliar representa el cliente en el espacio de direcciones del objeto.
-   El código auxiliar no se implementa como un objeto agregado porque no hay ningún requisito de que el cliente se pueda ver como una sola unidad; cada parte del código auxiliar es un componente independiente.
-   Los códigos auxiliares de la interfaz son privados en lugar de públicos.
-   El código auxiliar de la interfaz implementa [**IRpcStubBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcstubbuffer), no [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer).
-   En lugar de empaquetar los parámetros que se van a serializar, el código auxiliar los desempaquetará después de que se hayan calculado y, a continuación, empaquetará la respuesta.

## <a name="structure-of-the-stub"></a>Estructura del código auxiliar

En el diagrama siguiente se muestra la estructura del código auxiliar. Cada código auxiliar de interfaz está conectado a una interfaz en el objeto. El canal envía los mensajes entrantes al código auxiliar de la interfaz correspondiente. Todos los componentes se comunican con el canal a través de [**IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer), la interfaz que proporciona acceso a la biblioteca en tiempo de ejecución de RPC.

![Captura de pantalla que muestra la estructura del código auxiliar.](images/98714a22-733e-432f-bb90-408bbeecc23f.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canal](channel.md)
</dt> <dt>

[Comunicación entre objetos](inter-object-communication.md)
</dt> <dt>

[Detalles de serialización](marshaling-details.md)
</dt> <dt>

[Microsoft RPC](microsoft-rpc.md)
</dt> <dt>

[Proxy](proxy.md)
</dt> </dl>

 

 