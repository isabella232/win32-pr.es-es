---
title: Registro de IAgent
description: Registro de IAgent
ms.assetid: 3592e8ba-979e-4914-8197-17e645806f97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9dd611219fa994f4fe61f7f3e08facf02c9fb73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903522"
---
# <a name="iagentregister"></a>IAgent:: Register

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT Register(
   IUnknown * punkNotifySink  // IUnknown address for client notification sink
   long * pdwSinkID           // address of the notification sink ID
);
```

Registra un receptor de notificaciones para la aplicación cliente.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*
</dt> <dd>

Dirección de [**IUnknown**](https://www.bing.com/search?q=**IUnknown**) para la interfaz del receptor de notificaciones.

</dd> <dt>

<span id="pdwSinkID"></span><span id="pdwsinkid"></span><span id="PDWSINKID"></span>*pdwSinkID*
</dt> <dd>

Dirección del identificador del receptor de notificaciones (se usa para anular el registro del receptor de notificaciones).

</dd> </dl>

Debe registrar el receptor de notificaciones (también conocido como receptor de notificaciones o receptores de eventos) para recibir eventos del servidor de agente de Microsoft.

## <a name="see-also"></a>Consulte también

[**IAgent:: unregister**](iagent--unregister.md)


 

 




