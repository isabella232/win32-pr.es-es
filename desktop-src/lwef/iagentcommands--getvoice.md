---
title: IAgentCommands GetVoice
description: IAgentCommands GetVoice
ms.assetid: ef8983bc-c70c-48c7-9c5f-1dae61028d90
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b1915512c89611267df3788e5dcaa84fb0874a4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420714"
---
# <a name="iagentcommandsgetvoice"></a><span data-ttu-id="ce3f3-103">IAgentCommands::GetVoice</span><span class="sxs-lookup"><span data-stu-id="ce3f3-103">IAgentCommands::GetVoice</span></span>

<span data-ttu-id="ce3f3-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ce3f3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVoice(
   BSTR * pbszVoice  // address of Voice setting for Commands collection
);
```

<span data-ttu-id="ce3f3-105">Recupera el valor de la propiedad [**Voice**](voice-property.md) para una colección [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="ce3f3-105">Retrieves the value of the [**Voice**](voice-property.md) property for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="ce3f3-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="ce3f3-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="ce3f3-107"><span id="pbszVoice"></span><span id="pbszvoice"></span><span id="PBSZVOICE"></span>*pbszVoice*</span><span class="sxs-lookup"><span data-stu-id="ce3f3-107"><span id="pbszVoice"></span><span id="pbszvoice"></span><span id="PBSZVOICE"></span>*pbszVoice*</span></span>
</dt> <dd>

<span data-ttu-id="ce3f3-108">Dirección de un BSTR que recibe el valor de la configuración del texto de la [**voz**](voice-property.md) de una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="ce3f3-108">The address of a BSTR that receives the value of the [**Voice**](voice-property.md) text setting for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="ce3f3-109">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ce3f3-109">See Also</span></span>

<span data-ttu-id="ce3f3-110">[**IAgentCommands:: SetVoice**](iagentcommands--setvoice.md), [**IAgentCommands:: GetCaption**](iagentcommands--getcaption.md), [**IAgentCommands:: GetVisible**](iagentcommands--getvisible.md)</span><span class="sxs-lookup"><span data-stu-id="ce3f3-110">[**IAgentCommands::SetVoice**](iagentcommands--setvoice.md), [**IAgentCommands::GetCaption**](iagentcommands--getcaption.md), [**IAgentCommands::GetVisible**](iagentcommands--getvisible.md)</span></span>


 

 