---
title: IAgentCommand SetConfidenceThreshold
description: IAgentCommand SetConfidenceThreshold
ms.assetid: f62d646a-895d-468c-9397-0495680109a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 244f181fb4d9e706271440797e1261fd381897e00a5a216d681e0f3984d24a6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976305"
---
# <a name="iagentcommandsetconfidencethreshold"></a>IAgentCommand::SetConfidenceThreshold

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetConfidenceThreshold(
   long lConfidence  // Confidence setting for Command
);
```

Establece el valor de la [**propiedad Confidence**](confidence-property.md) para un [**comando**](/windows/desktop/lwef/the-command-object).

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="lConfidence"></span><span id="lconfidence"></span><span id="LCONFIDENCE"></span>*lConfidence*
</dt> <dd>

Valor de la [**propiedad Confidence**](confidence-property.md) de un [**comando**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

Si el valor de confianza devuelto de la mejor coincidencia devuelta en el evento [**Command**](/windows/desktop/lwef/the-command-object) no supera el valor establecido para la [**propiedad ConfidenceThreshold,**](/windows/desktop/lwef/confidence-property) el texto proporcionado en [**SetConfidenceText**](iagentcommand--setconfidencetext.md) se muestra en la sugerencia de escucha.

## <a name="see-also"></a>Consulte también

[**IAgentCommand::GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md), [**IAgentCommand::SetConfidenceText**](iagentcommand--setconfidencetext.md), [**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md)


 

 