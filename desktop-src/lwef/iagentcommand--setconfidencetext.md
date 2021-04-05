---
title: IAgentCommand SetConfidenceText
description: IAgentCommand SetConfidenceText
ms.assetid: e776a2ba-3592-4f26-a3e3-2c044eed7f0c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cff1ae34c03f8ff67da61bea1834c25d6844ab2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420552"
---
# <a name="iagentcommandsetconfidencetext"></a>IAgentCommand::SetConfidenceText

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetConfidenceText(
   BSTR bszTipText  // ConfidenceText setting for Command 
);
```

Establece el valor del texto de la sugerencia de escucha para un [**comando**](/windows/desktop/lwef/the-command-object).

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="bszTipText"></span><span id="bsztiptext"></span><span id="BSZTIPTEXT"></span>*bszTipText*
</dt> <dd>

BSTR que especifica el texto de la propiedad [**ConfidenceText**](confidencetext-property.md) de un [**comando**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

Si el valor de confianza devuelto de la mejor coincidencia devuelta en el evento de [**comando**](/windows/desktop/lwef/the-command-object) no supera el valor establecido para la propiedad [**ConfidenceThreshold**](/windows/desktop/lwef/confidence-property) , se muestra el texto proporcionado en *BszTipText* en la sugerencia de escucha.

## <a name="see-also"></a>Consulte también

[**IAgentCommand:: SetConfidenceThreshold**](iagentcommand--setconfidencethreshold.md), [**IAgentCommand:: GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md), [**IAgentCommand:: GetConfidenceText**](iagentcommand--getconfidencetext.md), [**IAgentUserInput:: GetItemConfidence**](iagentuserinput--getitemconfidence.md)


 

 