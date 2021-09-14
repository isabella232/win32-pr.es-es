---
title: IAgentNotifySink RequestComplete
description: IAgentNotifySink RequestComplete
ms.assetid: 995bc961-f175-4429-94a4-91962161298b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0265a7111369dec687fd74b9c66c27275a40e164
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361203"
---
# <a name="iagentnotifysinkrequestcomplete"></a>IAgentNotifySink::RequestComplete

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT RequestComplete(
   long dwRequestID,  // request ID
   long hrStatus      // status code
);                          
```

Notifica a una aplicación cliente cuando se completa una solicitud.

-   No de devuelve ningún valor.

<dl> <dt>

<span id="dwRequestID"></span><span id="dwrequestid"></span><span id="DWREQUESTID"></span>*dwRequestID*
</dt> <dd>

Identificador de la solicitud que se inició.

</dd> <dt>

<span id="hrStatus"></span><span id="hrstatus"></span><span id="HRSTATUS"></span>*hrStatus*
</dt> <dd>

Código de estado. Este parámetro devuelve el código de estado de la solicitud.

</dd> </dl>

Este evento le permite realizar un seguimiento de cuándo finaliza un método en cola con su identificador de solicitud.

## <a name="see-also"></a>Consulte también

[**IAgentNotifySink::RequestStart**](iagentnotifysink--requeststart.md), [**IAgent::Load**](iagent--load.md), [**IAgentCharacter::GestureAt**](iagentcharacter--gestureat.md), [**IAgentCharacter::Hide**](iagentcharacter--hide.md), [**IAgentCharacter::Interrupt**](iagentcharacter--interrupt.md), [**IAgentCharacter::MoveTo**](iagentcharacter--moveto.md), [**IAgentCharacter::P repare**](iagentcharacter--prepare.md), [**IAgentCharacter::P lay**](iagentcharacter--play.md), [**IAgentCharacter::Show**](iagentcharacter--show.md), [**IAgentCharacter::Speak**](iagentcharacter--speak.md), [**IAgentCharacter::Wait**](iagentcharacter--wait.md)


 

 




