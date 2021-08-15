---
title: IAgentCharacterEx GetActive
description: IAgentCharacterEx GetActive
ms.assetid: b14ae69a-a50e-4488-b5a7-33702e6555eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 533f9cb05143d4948fbcae1f8d9ed74a7216c5a2520b28f4c299321bcbac4272
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478038"
---
# <a name="iagentcharacterexgetactive"></a>IAgentCharacterEx::GetActive

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetActive(
   short * psState  // address of active state setting
);
```

Recupera si la aplicación cliente es el cliente activo del carácter y si el carácter es superior.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="psState"></span><span id="psstate"></span><span id="PSSTATE"></span>*psState*
</dt> <dd>

Dirección de una variable que recibe uno de los siguientes valores para la configuración de estado:



| Valor                                                              | Descripción                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------|
| **const unsigned short** **ACTIVATE \_ NOTACTIVE = 0;**<br/>   | El cliente no es el cliente activo del carácter.                |
| **const unsigned short** **ACTIVATE ACTIVE = \_ 1;**<br/>      | El cliente es el cliente activo del carácter.                    |
| **const unsigned short** **ACTIVATE \_ INPUTACTIVE = 2;**<br/> | El cliente está activo en la entrada (cliente activo del carácter superior). |



 

</dd> </dl>

Esta configuración le permite saber si es el cliente activo del carácter o si el carácter es el carácter activo de entrada. Cuando varias aplicaciones cliente comparten el mismo carácter, el cliente activo del carácter recibe la entrada del mouse (por ejemplo, eventos de clic o arrastre del control de Microsoft Agent). De forma similar, cuando se muestran varios caracteres, el cliente activo del carácter superior (también conocido como cliente activo de entrada) recibe eventos [**IAgentNotifySink::Command.**](iagentnotifysink--command.md)

Use el [**método Activate**](iagentcharacter--activate.md) para establecer si la aplicación es el cliente activo del carácter o para convertir la aplicación en el cliente activo de entrada (que también hace que el carácter sea el más alto).

## <a name="see-also"></a>Consulte también

[**IAgentCharacter::Activate**](iagentcharacter--activate.md), [ **IAgentNotifySinkEx::ActiveClientChange**](iagentnotifysinkex--activeclientchange.md)


 

 





