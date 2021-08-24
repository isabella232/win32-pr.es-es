---
title: IAgentCharacter HasOtherClients
description: IAgentCharacter HasOtherClients
ms.assetid: ee74fa9b-2842-43ac-8493-bc69b480581e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6469c289d846cb34e14c6afabbed72647e6e786fbda273baaf70532d4ad6578c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665755"
---
# <a name="iagentcharacterhasotherclients"></a>IAgentCharacter::HasOtherClients

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT HasOtherClients(
   long * plNumOtherClients  // address of variable for number of clients 
);                           // for character 
```

Recupera si un carácter tiene otros clientes.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="plNumOtherClients"></span><span id="plnumotherclients"></span><span id="PLNUMOTHERCLIENTS"></span>*plNumOtherClients*
</dt> <dd>

Dirección de una variable que recibe el número de otros clientes conectados para el carácter (número total de clientes menos el cliente).

</dd> </dl>

 

 




