---
title: IAgentCharacterEx GetActive
description: IAgentCharacterEx GetActive
ms.assetid: b14ae69a-a50e-4488-b5a7-33702e6555eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1dab89ee9ba89c5982e34844917334d97169b9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903730"
---
# <a name="iagentcharacterexgetactive"></a>IAgentCharacterEx::GetActive

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetActive(
   short * psState  // address of active state setting
);
```

Recupera si la aplicación cliente es el cliente activo del carácter y si el carácter es superior.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="psState"></span><span id="psstate"></span><span id="PSSTATE"></span>*psState*
</dt> <dd>

Dirección de una variable que recibe uno de los siguientes valores para la configuración de estado:



| Value                                                              | Descripción                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------|
| **const unsigned short** **Activate \_ = 0;**<br/>   | El cliente no es el cliente activo del carácter.                |
| **const unsigned short** **Activate \_ Active = 1;**<br/>      | El cliente es el cliente activo del carácter.                    |
| **const unsigned short** **Active \_ INPUTACTIVE = 2;**<br/> | El cliente es de entrada-activo (cliente activo del carácter superior). |



 

</dd> </dl>

Esta configuración le permite saber si es el cliente activo del carácter o si el carácter es el carácter activo de entrada. Cuando varias aplicaciones cliente comparten el mismo carácter, el cliente activo del carácter recibe la entrada del mouse (por ejemplo, eventos de clic o arrastre de control del agente de Microsoft). Del mismo modo, cuando se muestran varios caracteres, el cliente activo del carácter superior (también conocido como cliente de entrada-activo) recibe los eventos [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .

Use el método [**Activate**](iagentcharacter--activate.md) para establecer si la aplicación es el cliente activo del carácter o para convertir la aplicación en el cliente activo de entrada (que también hace que el carácter sea más alto).

## <a name="see-also"></a>Consulte también

[**IAgentCharacter:: Activate**](iagentcharacter--activate.md), [ **IAgentNotifySinkEx:: ActiveClientChange**](iagentnotifysinkex--activeclientchange.md)


 

 





