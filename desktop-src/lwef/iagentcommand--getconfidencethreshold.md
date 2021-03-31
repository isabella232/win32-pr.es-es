---
title: IAgentCommand GetConfidenceThreshold
description: IAgentCommand GetConfidenceThreshold
ms.assetid: dfbaba7c-ed45-464e-82ab-39e33c023e89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af6557ad4e6831734106ee2c2e8021f923ef8806
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790611"
---
# <a name="iagentcommandgetconfidencethreshold"></a>IAgentCommand::GetConfidenceThreshold

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetConfidenceThreshold(
long * plConfidenceThreshold  // address of ConfidenceThreshold 
);                            // setting for Command
```

Recupera el valor de la propiedad [**ConfidenceThreshold**](/windows/desktop/lwef/confidence-property) de un [**comando**](/windows/desktop/lwef/the-command-object).

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="plConfidenceThreshold"></span><span id="plconfidencethreshold"></span><span id="PLCONFIDENCETHRESHOLD"></span>*plConfidenceThreshold*
</dt> <dd>

Dirección de una variable que recibe el valor de la propiedad [**ConfidenceThreshold**](/windows/desktop/lwef/confidence-property) de un comando.

</dd> </dl>

## <a name="see-also"></a>Consulte también

[**IAgentCommand:: SetConfidenceThreshold**](iagentcommand--setconfidencethreshold.md), [**IAgentCommand:: SetConfidenceText**](iagentcommand--setconfidencetext.md), [**IAgentUserInput:: GetItemConfidence**](iagentuserinput--getitemconfidence.md)


 

 