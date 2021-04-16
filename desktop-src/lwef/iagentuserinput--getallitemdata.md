---
title: IAgentUserInput GetAllItemData
description: IAgentUserInput GetAllItemData
ms.assetid: d1857b28-c745-4ed2-b49e-774f247e7348
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ced6a618d4fbbc093bf54c19fc393b7e195f2069
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486534"
---
# <a name="iagentuserinputgetallitemdata"></a><span data-ttu-id="4d780-103">IAgentUserInput::GetAllItemData</span><span class="sxs-lookup"><span data-stu-id="4d780-103">IAgentUserInput::GetAllItemData</span></span>

<span data-ttu-id="4d780-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4d780-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetAllItemData(
   VARIANT * pdwItemIndices,  // address of variable for alternative IDs
   VARIANT * plConfidences,   // address of variable for confidence scores
   VARIANT * pbszText         // address of variable for voice text
);
```

<span data-ttu-id="4d780-105">Recupera los datos para todas las alternativas de [**comando**](command-event.md) que se pasan a una devolución de llamada de [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="4d780-105">Retrieves the data for all [**Command**](command-event.md) alternatives passed to an [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

-   <span data-ttu-id="4d780-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="4d780-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="4d780-107"><span id="pdwItemIndices"></span><span id="pdwitemindices"></span><span id="PDWITEMINDICES"></span>*pdwItemIndices*</span><span class="sxs-lookup"><span data-stu-id="4d780-107"><span id="pdwItemIndices"></span><span id="pdwitemindices"></span><span id="PDWITEMINDICES"></span>*pdwItemIndices*</span></span>
</dt> <dd>

<span data-ttu-id="4d780-108">Dirección de una variable que recibe los identificadores de [**comandos**](command-event.md) pasados a la devolución de llamada [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="4d780-108">Address of a variable that receives the IDs of [**Commands**](command-event.md) passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

</dd> <dt>

<span data-ttu-id="4d780-109"><span id="plConfidences"></span><span id="plconfidences"></span><span id="PLCONFIDENCES"></span>*plConfidences*</span><span class="sxs-lookup"><span data-stu-id="4d780-109"><span id="plConfidences"></span><span id="plconfidences"></span><span id="PLCONFIDENCES"></span>*plConfidences*</span></span>
</dt> <dd>

<span data-ttu-id="4d780-110">Dirección de una variable que recibe las puntuaciones de confianza para las alternativas de [**comando**](command-event.md) que se pasan a la devolución de llamada [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="4d780-110">Address of a variable that receives the confidence scores for [**Command**](command-event.md) alternatives passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

</dd> <dt>

<span data-ttu-id="4d780-111"><span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*pbszText*</span><span class="sxs-lookup"><span data-stu-id="4d780-111"><span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*pbszText*</span></span>
</dt> <dd>

<span data-ttu-id="4d780-112">Dirección de una variable que recibe el texto de la voz para las alternativas de [**comando**](command-event.md) que se pasan a la devolución de llamada [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="4d780-112">Address of a variable that receives the voice text for [**Command**](command-event.md) alternatives passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

</dd> </dl>

<span data-ttu-id="4d780-113">Si la entrada de voz desencadena [**IAgentNotifySink:: Command**](iagentnotifysink--command.md), el servidor devuelve la mejor coincidencia, la segunda coincidencia mejor y la tercera coincidencia, si la proporciona el motor de voz.</span><span class="sxs-lookup"><span data-stu-id="4d780-113">If speech input triggers [**IAgentNotifySink::Command**](iagentnotifysink--command.md), the server returns the best match, the second-best match, and the third-best match, if these are provided by the speech engine.</span></span> <span data-ttu-id="4d780-114">Proporciona las puntuaciones de confianza relativas, en el intervalo de-100 a 100 y el texto real "escuchado" por el motor de voz.</span><span class="sxs-lookup"><span data-stu-id="4d780-114">It provides the relative confidence scores, in the range of -100 to 100, and actual text "heard" by the speech engine.</span></span> <span data-ttu-id="4d780-115">Si la mejor coincidencia era un comando proporcionado por el servidor, el servidor envía un identificador nulo, pero todavía envía una puntuación de confianza y el texto de la [**voz**](voice-property.md) .</span><span class="sxs-lookup"><span data-stu-id="4d780-115">If the best match was a server-supplied command, the server sends a NULL ID, but still sends a confidence score and the [**Voice**](voice-property.md) text.</span></span>

<span data-ttu-id="4d780-116">Si la entrada de voz no era el origen del evento; por ejemplo, si el usuario seleccionó el comando en el menú emergente del carácter, el servidor de agente de Microsoft devuelve el identificador del [**comando**](command-event.md) seleccionado, con una puntuación de confianza de 100 y el texto de voz como null.</span><span class="sxs-lookup"><span data-stu-id="4d780-116">If speech input was not the source for the event; for example, if the user selected the command from the character's pop-up menu, the Microsoft Agent server returns the ID of the [**Command**](command-event.md) selected, with a confidence score of 100 and voice text as NULL.</span></span> <span data-ttu-id="4d780-117">Las demás alternativas devuelven como NULL con puntuaciones de confianza de cero (0) y texto de voz como NULL.</span><span class="sxs-lookup"><span data-stu-id="4d780-117">The other alternatives return as NULL with confidence scores of zero (0) and voice text as NULL.</span></span>

> [!Note]  
> <span data-ttu-id="4d780-118">No todos los motores de reconocimiento de voz pueden devolver todos los valores de todos los parámetros de este evento.</span><span class="sxs-lookup"><span data-stu-id="4d780-118">Not all speech recognition engines may return all the values for all the parameters of this event.</span></span> <span data-ttu-id="4d780-119">Consulte con el proveedor del motor para determinar si el motor es compatible con la interfaz de Microsoft Speech API para devolver alternativas y puntuaciones de confianza.</span><span class="sxs-lookup"><span data-stu-id="4d780-119">Check with your engine vendor to determine whether the engine supports the Microsoft Speech API interface for returning alternatives and confidence scores.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="4d780-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4d780-120">See Also</span></span>

<span data-ttu-id="4d780-121">[**IAgentUserInput:: GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput:: GetItemText**](iagentuserinput--getitemtext.md), [**IAgentUserInput:: GetItemID**](iagentuserinput--getitemid.md)</span><span class="sxs-lookup"><span data-stu-id="4d780-121">[**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput::GetItemText**](iagentuserinput--getitemtext.md), [**IAgentUserInput::GetItemID**](iagentuserinput--getitemid.md)</span></span>


 

 




