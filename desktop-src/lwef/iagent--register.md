---
title: Registro de IAgent
description: Registro de IAgent
ms.assetid: 3592e8ba-979e-4914-8197-17e645806f97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00f3400e6f29e62b3d8c194186f52591a0f7bb039a858c3d450e8e8332df4313
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962675"
---
# <a name="iagentregister"></a>IAgent::Register

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT Register(
   IUnknown * punkNotifySink  // IUnknown address for client notification sink
   long * pdwSinkID           // address of the notification sink ID
);
```

Registra un receptor de notificaciones para la aplicación cliente.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*Iunknown*
</dt> <dd>

Dirección de [**IUnknown para**](https://www.bing.com/search?q=**IUnknown**) la interfaz del receptor de notificaciones.

</dd> <dt>

<span id="pdwSinkID"></span><span id="pdwsinkid"></span><span id="PDWSINKID"></span>*pdwSinkID*
</dt> <dd>

Dirección del identificador del receptor de notificación (se usa para anular el registro del receptor de notificaciones).

</dd> </dl>

Debe registrar el receptor de notificaciones (también conocido como receptor de notificaciones o receptor de eventos) para recibir eventos del servidor de Microsoft Agent.

## <a name="see-also"></a>Consulte también

[**IAgent::Unregister**](iagent--unregister.md)


 

 




