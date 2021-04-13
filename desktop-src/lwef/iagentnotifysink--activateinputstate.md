---
title: IAgentNotifySink ActivateInputState
description: IAgentNotifySink ActivateInputState
ms.assetid: 2476e475-d80c-47e9-bb60-e0fca41becc9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5821f5943bb87f9c19a66125028604fa5d116a7e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269119"
---
# <a name="iagentnotifysinkactivateinputstate"></a>IAgentNotifySink::ActivateInputState

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT ActivateInputState(
   long dwCharID,   // character ID
   long bActivated  // input activation flag
);                          
```

Notifica a una aplicación cliente que ha cambiado el estado activo de entrada de un carácter.

-   No de devuelve ningún valor.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificador del carácter cuyo estado de activación de entrada ha cambiado.

</dd> <dt>

<span id="bActivated"></span><span id="bactivated"></span><span id="BACTIVATED"></span>*bActivated*
</dt> <dd>

Marca activa de entrada. Este valor booleano es **true** si el carácter al que hace referencia *dwCharID* se convirtió en una entrada activa; y **false** si el carácter perdió su estado activo de entrada.

</dd> </dl>

 

 




