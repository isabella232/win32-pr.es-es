---
title: Comando IAgentNotifySink
description: Comando IAgentNotifySink
ms.assetid: d54fb2e8-27d6-47a4-8a1e-5419a94ea26d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9690d2914db9d284cd4ba4b826905d3169b83f2c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995191"
---
# <a name="iagentnotifysinkcommand"></a><span data-ttu-id="d5c0b-103">IAgentNotifySink:: Command</span><span class="sxs-lookup"><span data-stu-id="d5c0b-103">IAgentNotifySink::Command</span></span>

<span data-ttu-id="d5c0b-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d5c0b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Command(
   long dwCommandID,         // Command ID of the best match
   IUnknown * punkUserInput  // address of IAgentUserInput object 
);                          
```

<span data-ttu-id="d5c0b-105">Notifica a una aplicación cliente que el usuario ha seleccionado un [**comando**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="d5c0b-105">Notifies a client application that a [**Command**](/windows/desktop/lwef/the-command-object) was selected by the user.</span></span>

-   <span data-ttu-id="d5c0b-106">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="d5c0b-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="d5c0b-107"><span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*</span><span class="sxs-lookup"><span data-stu-id="d5c0b-107"><span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*</span></span>
</dt> <dd>

<span data-ttu-id="d5c0b-108">Identificador de la alternativa del comando mejor coincidencia.</span><span class="sxs-lookup"><span data-stu-id="d5c0b-108">Identifier of the best match command alternative.</span></span>

</dd> <dt>

<span data-ttu-id="d5c0b-109"><span id="punkUserInput"></span><span id="punkuserinput"></span><span id="PUNKUSERINPUT"></span>*punkUserInput*</span><span class="sxs-lookup"><span data-stu-id="d5c0b-109"><span id="punkUserInput"></span><span id="punkuserinput"></span><span id="PUNKUSERINPUT"></span>*punkUserInput*</span></span>
</dt> <dd>

<span data-ttu-id="d5c0b-110">Dirección de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) para el objeto [**IAgentUserInput**](iagentuserinput.md) .</span><span class="sxs-lookup"><span data-stu-id="d5c0b-110">Address of the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface for the [**IAgentUserInput**](iagentuserinput.md) object.</span></span>

</dd> </dl>

<span data-ttu-id="d5c0b-111">Use [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para recuperar la interfaz [**IAgentUserInput**](iagentuserinput.md) .</span><span class="sxs-lookup"><span data-stu-id="d5c0b-111">Use [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to retrieve the [**IAgentUserInput**](iagentuserinput.md) interface.</span></span>

<span data-ttu-id="d5c0b-112">El servidor notifica al cliente de entrada-activo cuando el usuario elige un comando por voz o seleccionando un comando en el menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="d5c0b-112">The server notifies the input-active client when the user chooses a command by voice or by selecting a command from the character's pop-up menu.</span></span> <span data-ttu-id="d5c0b-113">El evento se produce incluso cuando el usuario selecciona uno de los comandos del servidor.</span><span class="sxs-lookup"><span data-stu-id="d5c0b-113">The event occurs even when the user selects one of the server's commands.</span></span> <span data-ttu-id="d5c0b-114">En este caso, el servidor devuelve un identificador de comando nulo, la puntuación de confianza y el texto de la voz que devuelve el motor de voz para esa entrada.</span><span class="sxs-lookup"><span data-stu-id="d5c0b-114">In this case the server returns a null command ID, the confidence score, and the voice text returned by the speech engine for that entry.</span></span>

## <a name="see-also"></a><span data-ttu-id="d5c0b-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d5c0b-115">See Also</span></span>

[<span data-ttu-id="d5c0b-116">**IAgentUserInput**</span><span class="sxs-lookup"><span data-stu-id="d5c0b-116">**IAgentUserInput**</span></span>](iagentuserinput.md)


 

 