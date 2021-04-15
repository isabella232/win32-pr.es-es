---
title: IAgentUserInput
description: IAgentUserInput
ms.assetid: 59ce7337-6031-4449-8b29-fd0c6737c3e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b37d195d6b5d1294c071a1b73d1da95548cb7a0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420634"
---
# <a name="iagentuserinput"></a><span data-ttu-id="ecbc6-103">IAgentUserInput</span><span class="sxs-lookup"><span data-stu-id="ecbc6-103">IAgentUserInput</span></span>

<span data-ttu-id="ecbc6-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ecbc6-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="ecbc6-105">Cuando el servidor notifica al cliente de entrada-activo con [**IAgentNotifySink:: Command**](iagentnotifysink--command.md), devuelve información a través del objeto [**IAgentUserInput**](/windows/desktop/lwef/iagentuserinput) .</span><span class="sxs-lookup"><span data-stu-id="ecbc6-105">When the server notifies the input-active client with [**IAgentNotifySink::Command**](iagentnotifysink--command.md), it returns information through the [**IAgentUserInput**](/windows/desktop/lwef/iagentuserinput) object.</span></span> <span data-ttu-id="ecbc6-106">**IAgentUserInput** define una interfaz que permite a las aplicaciones consultar estos valores.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-106">**IAgentUserInput** defines an interface that allows applications to query these values.</span></span>

<span data-ttu-id="ecbc6-107">**Métodos en orden de Vtable**</span><span class="sxs-lookup"><span data-stu-id="ecbc6-107">**Methods in Vtable Order**</span></span>



| <span data-ttu-id="ecbc6-108">Métodos IAgentUserInput</span><span class="sxs-lookup"><span data-stu-id="ecbc6-108">IAgentUserInput Methods</span></span>                                         | <span data-ttu-id="ecbc6-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ecbc6-109">Description</span></span>                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ecbc6-110">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="ecbc6-110">**GetCount**</span></span>](iagentuserinput--getcount.md)                   | <span data-ttu-id="ecbc6-111">Devuelve el número de alternativas de comando devueltas en un evento de [**comando**](command-event.md) .</span><span class="sxs-lookup"><span data-stu-id="ecbc6-111">Returns the number of command alternatives returned in a [**Command**](command-event.md) event.</span></span>                                         |
| [<span data-ttu-id="ecbc6-112">**GetItemID**</span><span class="sxs-lookup"><span data-stu-id="ecbc6-112">**GetItemID**</span></span>](iagentuserinput--getitemid.md)                 | <span data-ttu-id="ecbc6-113">Devuelve el identificador de una alternativa de [**comando**](command-event.md) específica.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-113">Returns the ID for a specific [**Command**](command-event.md) alternative.</span></span>                                                              |
| [<span data-ttu-id="ecbc6-114">**GetItemConfidence**</span><span class="sxs-lookup"><span data-stu-id="ecbc6-114">**GetItemConfidence**</span></span>](iagentuserinput--getitemconfidence.md) | <span data-ttu-id="ecbc6-115">Devuelve el valor de la propiedad [**Confidence**](confidence-property.md) para una alternativa de [**comando**](command-event.md) concreta.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-115">Returns the value of the [**Confidence**](confidence-property.md) property for a specific [**Command**](command-event.md) alternative.</span></span> |
| [<span data-ttu-id="ecbc6-116">**GetItemText**</span><span class="sxs-lookup"><span data-stu-id="ecbc6-116">**GetItemText**</span></span>](iagentuserinput--getitemtext.md)             | <span data-ttu-id="ecbc6-117">Devuelve el valor del texto de la [**voz**](voice-property.md) de una alternativa de [**comando**](command-event.md) específica.</span><span class="sxs-lookup"><span data-stu-id="ecbc6-117">Returns the value of [**Voice**](voice-property.md) text for a specific [**Command**](command-event.md) alternative.</span></span>                   |
| [<span data-ttu-id="ecbc6-118">**GetAllItemData**</span><span class="sxs-lookup"><span data-stu-id="ecbc6-118">**GetAllItemData**</span></span>](iagentuserinput--getallitemdata.md)       | <span data-ttu-id="ecbc6-119">Devuelve los datos para todas las alternativas de [**comando**](command-event.md) .</span><span class="sxs-lookup"><span data-stu-id="ecbc6-119">Returns the data for all [**Command**](command-event.md) alternatives.</span></span>                                                                  |



 

 

 