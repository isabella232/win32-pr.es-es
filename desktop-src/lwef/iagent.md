---
title: IAgent
description: IAgent
ms.assetid: 35b12006-a938-450c-969a-7b73a3768a4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12900a4288b9917d695dd25d4b81362b67c93587
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357108"
---
# <a name="iagent"></a><span data-ttu-id="02bcd-103">IAgent</span><span class="sxs-lookup"><span data-stu-id="02bcd-103">IAgent</span></span>

<span data-ttu-id="02bcd-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="02bcd-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="02bcd-105">**IAgent** define una interfaz que permite a las aplicaciones cargar caracteres, recibir eventos y comprobar el estado actual del servidor de agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="02bcd-105">**IAgent** defines an interface that allows applications to load characters, receive events, and check the current state of the Microsoft Agent Server.</span></span> <span data-ttu-id="02bcd-106">Estas funciones también están disponibles en [**IAgentEx**](iagentex.md).</span><span class="sxs-lookup"><span data-stu-id="02bcd-106">These functions are also available from [**IAgentEx**](iagentex.md).</span></span>

<span data-ttu-id="02bcd-107">El método GetSuspended incluido en versiones anteriores está obsoleto y devuelve **false** para mantener la compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="02bcd-107">The GetSuspended method included in previous versions is obsolete and returns **False** for backward compatibility.</span></span>

<span data-ttu-id="02bcd-108">**Métodos en orden de Vtable**</span><span class="sxs-lookup"><span data-stu-id="02bcd-108">**Methods in Vtable Order**</span></span>



| <span data-ttu-id="02bcd-109">Métodos IAgent</span><span class="sxs-lookup"><span data-stu-id="02bcd-109">IAgent Methods</span></span>                               | <span data-ttu-id="02bcd-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="02bcd-110">Description</span></span>                                                   |
|----------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="02bcd-111">**Cargar**</span><span class="sxs-lookup"><span data-stu-id="02bcd-111">**Load**</span></span>](load-method.md)                  | <span data-ttu-id="02bcd-112">Carga el archivo de datos de un carácter.</span><span class="sxs-lookup"><span data-stu-id="02bcd-112">Loads a character's data file.</span></span>                                |
| [<span data-ttu-id="02bcd-113">**Cárguelo**</span><span class="sxs-lookup"><span data-stu-id="02bcd-113">**Unload**</span></span>](unload-method.md)              | <span data-ttu-id="02bcd-114">Descarga el archivo de datos de un carácter.</span><span class="sxs-lookup"><span data-stu-id="02bcd-114">Unloads a character's data file.</span></span>                              |
| [<span data-ttu-id="02bcd-115">**Register**</span><span class="sxs-lookup"><span data-stu-id="02bcd-115">**Register**</span></span>](iagent--register.md)         | <span data-ttu-id="02bcd-116">Registra un receptor de notificaciones para el cliente.</span><span class="sxs-lookup"><span data-stu-id="02bcd-116">Registers a notification sink for the client.</span></span>                 |
| [<span data-ttu-id="02bcd-117">**Unegister**</span><span class="sxs-lookup"><span data-stu-id="02bcd-117">**Unegister**</span></span>](iagent--unregister.md)      | <span data-ttu-id="02bcd-118">Anula el registro del receptor de notificaciones de un cliente.</span><span class="sxs-lookup"><span data-stu-id="02bcd-118">Unregisters a client's notification sink.</span></span>                     |
| [<span data-ttu-id="02bcd-119">**GetCharacter**</span><span class="sxs-lookup"><span data-stu-id="02bcd-119">**GetCharacter**</span></span>](iagent--getcharacter.md) | <span data-ttu-id="02bcd-120">Devuelve la interfaz IAgentCharacter para un carácter cargado.</span><span class="sxs-lookup"><span data-stu-id="02bcd-120">Returns the IAgentCharacter interface for a loaded character.</span></span> |



 

 

 




