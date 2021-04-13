---
title: IAgentCommands SetCaption
description: IAgentCommands SetCaption
ms.assetid: 042f7366-0071-40a5-a47c-81c02cdbe3a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8c472bfbfd82235e21c28e24e7e0ce03223ff8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420574"
---
# <a name="iagentcommandssetcaption"></a><span data-ttu-id="ec519-103">IAgentCommands::SetCaption</span><span class="sxs-lookup"><span data-stu-id="ec519-103">IAgentCommands::SetCaption</span></span>

<span data-ttu-id="ec519-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ec519-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetCaption(
   BSTR bszCaption  // Caption setting for Commands collection
);
```

<span data-ttu-id="ec519-105">Establece el texto de [**título**](caption-property.md) que se muestra para una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="ec519-105">Sets the [**Caption**](caption-property.md) text displayed for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="ec519-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="ec519-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="ec519-107"><span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*</span><span class="sxs-lookup"><span data-stu-id="ec519-107"><span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*</span></span>
</dt> <dd>

<span data-ttu-id="ec519-108">BSTR que especifica el valor de la propiedad [**Caption**](caption-property.md) de una colección [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="ec519-108">A BSTR that specifies the value for the [**Caption**](caption-property.md) property for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> </dl>

<span data-ttu-id="ec519-109">Al establecer la propiedad [**Caption**](caption-property.md) de una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) , se define cómo aparecerá en el menú emergente del carácter cuando su propiedad [**visible**](visible-property.md) esté establecida en **true** y la aplicación no sea el cliente de entrada-activo.</span><span class="sxs-lookup"><span data-stu-id="ec519-109">Setting the [**Caption**](caption-property.md) property for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection defines how it will appear on the character's pop-up menu when its [**Visible**](visible-property.md) property is set to **True** and your application is not the input-active client.</span></span> <span data-ttu-id="ec519-110">Para especificar una tecla de acceso (tecla de acceso no alineada) para el **título**, incluya un carácter de y comercial (&) antes de ese carácter.</span><span class="sxs-lookup"><span data-stu-id="ec519-110">To specify an access key (unlined mnemonic) for your **Caption**, include an ampersand (&) character before that character.</span></span>

<span data-ttu-id="ec519-111">Si define comandos para una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) que tiene su conjunto de [**leyendas**](caption-property.md) , normalmente también se define un **título** para la colección de **comandos** .</span><span class="sxs-lookup"><span data-stu-id="ec519-111">If you define commands for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection that has its [**Caption**](caption-property.md) set, you typically also define a **Caption** for its **Commands** collection.</span></span>

## <a name="see-also"></a><span data-ttu-id="ec519-112">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ec519-112">See Also</span></span>

<span data-ttu-id="ec519-113">[**IAgentCommands:: GetCaption**](iagentcommands--getcaption.md), [**IAgentCommands:: setVisible**](iagentcommands--setvisible.md), [**IAgentCommands:: SetVoice**](iagentcommands--setvoice.md)</span><span class="sxs-lookup"><span data-stu-id="ec519-113">[**IAgentCommands::GetCaption**](iagentcommands--getcaption.md), [**IAgentCommands::SetVisible**](iagentcommands--setvisible.md), [**IAgentCommands::SetVoice**](iagentcommands--setvoice.md)</span></span>


 

 