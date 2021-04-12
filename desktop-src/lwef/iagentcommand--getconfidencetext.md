---
title: IAgentCommand GetConfidenceText
description: IAgentCommand GetConfidenceText
ms.assetid: d98339eb-0986-497c-b43c-4e4a952328e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 987dca39016a20d185fbd4b8fd2b554c8bec02f4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358815"
---
# <a name="iagentcommandgetconfidencetext"></a>IAgentCommand::GetConfidenceText

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetConfidenceText(
   BSTR * pbszTipText  // address of ConfidenceText setting for Command 
);
```

Recupera el texto de sugerencia de escucha previamente establecido para un [**comando**](/windows/desktop/lwef/the-command-object).

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="pbszTipText"></span><span id="pbsztiptext"></span><span id="PBSZTIPTEXT"></span>*pbszTipText*
</dt> <dd>

Dirección de un BSTR que recibe el valor del texto de la sugerencia de escucha para un [**comando**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

## <a name="see-also"></a>Consulte también

[**IAgentCommand:: SetConfidenceThreshold**](iagentcommand--setconfidencethreshold.md), [**IAgentCommand:: GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md), [**IAgentCommand:: SetConfidenceText**](iagentcommand--setconfidencetext.md), [**IAgentUserInput:: GetItemConfidence**](iagentuserinput--getitemconfidence.md)


 

 