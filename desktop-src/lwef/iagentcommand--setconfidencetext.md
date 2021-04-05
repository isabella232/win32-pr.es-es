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
# <a name="iagentcommandsetconfidencetext"></a><span data-ttu-id="dc0a7-103">IAgentCommand::SetConfidenceText</span><span class="sxs-lookup"><span data-stu-id="dc0a7-103">IAgentCommand::SetConfidenceText</span></span>

<span data-ttu-id="dc0a7-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="dc0a7-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetConfidenceText(
   BSTR bszTipText  // ConfidenceText setting for Command 
);
```

<span data-ttu-id="dc0a7-105">Establece el valor del texto de la sugerencia de escucha para un [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="dc0a7-105">Sets the value of the Listening Tip text for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="dc0a7-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="dc0a7-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="dc0a7-107"><span id="bszTipText"></span><span id="bsztiptext"></span><span id="BSZTIPTEXT"></span>*bszTipText*</span><span class="sxs-lookup"><span data-stu-id="dc0a7-107"><span id="bszTipText"></span><span id="bsztiptext"></span><span id="BSZTIPTEXT"></span>*bszTipText*</span></span>
</dt> <dd>

<span data-ttu-id="dc0a7-108">BSTR que especifica el texto de la propiedad [**ConfidenceText**](confidencetext-property.md) de un [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="dc0a7-108">A BSTR that specifies the text for the [**ConfidenceText**](confidencetext-property.md) property of a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="dc0a7-109">Si el valor de confianza devuelto de la mejor coincidencia devuelta en el evento de [**comando**](/windows/desktop/lwef/the-command-object) no supera el valor establecido para la propiedad [**ConfidenceThreshold**](/windows/desktop/lwef/confidence-property) , se muestra el texto proporcionado en *BszTipText* en la sugerencia de escucha.</span><span class="sxs-lookup"><span data-stu-id="dc0a7-109">If the confidence value returned of the best match returned in the [**Command**](/windows/desktop/lwef/the-command-object) event does not exceed the value set for the [**ConfidenceThreshold**](/windows/desktop/lwef/confidence-property) property, the text supplied in *bszTipText* is displayed in the Listening Tip.</span></span>

## <a name="see-also"></a><span data-ttu-id="dc0a7-110">Consulte también</span><span class="sxs-lookup"><span data-stu-id="dc0a7-110">See Also</span></span>

<span data-ttu-id="dc0a7-111">[**IAgentCommand:: SetConfidenceThreshold**](iagentcommand--setconfidencethreshold.md), [**IAgentCommand:: GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md), [**IAgentCommand:: GetConfidenceText**](iagentcommand--getconfidencetext.md), [**IAgentUserInput:: GetItemConfidence**](iagentuserinput--getitemconfidence.md)</span><span class="sxs-lookup"><span data-stu-id="dc0a7-111">[**IAgentCommand::SetConfidenceThreshold**](iagentcommand--setconfidencethreshold.md), [**IAgentCommand::GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md), [**IAgentCommand::GetConfidenceText**](iagentcommand--getconfidencetext.md), [**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md)</span></span>


 

 