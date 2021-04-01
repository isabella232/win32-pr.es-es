---
description: La lista siguiente contiene los miembros de la dirección CMSP.
ms.assetid: ef15adef-1f4d-4bfc-8362-97fe1d118204
title: Miembros de CMSPAddress
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83213646427e7379b3eb2b45a0670f7908877175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913818"
---
# <a name="cmspaddress-members"></a><span data-ttu-id="e3afa-103">Miembros de CMSPAddress</span><span class="sxs-lookup"><span data-stu-id="e3afa-103">CMSPAddress Members</span></span>



| <span data-ttu-id="e3afa-104">Tipos de miembro</span><span class="sxs-lookup"><span data-stu-id="e3afa-104">Member types</span></span>                    | <span data-ttu-id="e3afa-105">Nombre</span><span class="sxs-lookup"><span data-stu-id="e3afa-105">Name</span></span>                    | <span data-ttu-id="e3afa-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3afa-106">Description</span></span>                                                                                      |
|---------------------------------|-------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3afa-107">Iunknown</span><span class="sxs-lookup"><span data-stu-id="e3afa-107">Iunknown</span></span>                        | <span data-ttu-id="e3afa-108">\*m \_ pFTM</span><span class="sxs-lookup"><span data-stu-id="e3afa-108">\*m\_pFTM</span></span>               | <span data-ttu-id="e3afa-109">Puntero al serializador de subprocesamiento libre.</span><span class="sxs-lookup"><span data-stu-id="e3afa-109">Pointer to the free threaded marshaller.</span></span>                                                         |
| <span data-ttu-id="e3afa-110">HANDLE</span><span class="sxs-lookup"><span data-stu-id="e3afa-110">HANDLE</span></span>                          | <span data-ttu-id="e3afa-111">m \_ htEvent</span><span class="sxs-lookup"><span data-stu-id="e3afa-111">m\_htEvent</span></span>              | <span data-ttu-id="e3afa-112">Identificador del evento de Tapi3.dll, que se usa para notificar a TAPI que el MSP quiere enviar datos a él.</span><span class="sxs-lookup"><span data-stu-id="e3afa-112">Handle to Tapi3.dll's event, which is used to notify TAPI that the MSP wants to send data to it.</span></span> |
| <span data-ttu-id="e3afa-113">entrada de lista \_</span><span class="sxs-lookup"><span data-stu-id="e3afa-113">LIST\_ENTRY</span></span>                     | <span data-ttu-id="e3afa-114">EventList de m \_</span><span class="sxs-lookup"><span data-stu-id="e3afa-114">m\_EventList</span></span>            | <span data-ttu-id="e3afa-115">Lista de eventos.</span><span class="sxs-lookup"><span data-stu-id="e3afa-115">List of events.</span></span>                                                                                  |
| <span data-ttu-id="e3afa-116">CMSPCritSection</span><span class="sxs-lookup"><span data-stu-id="e3afa-116">CMSPCritSection</span></span>                 | <span data-ttu-id="e3afa-117">m \_ EventDataLock</span><span class="sxs-lookup"><span data-stu-id="e3afa-117">m\_EventDataLock</span></span>        | <span data-ttu-id="e3afa-118">El bloqueo que protege los datos relacionados con el control de eventos con TAPI.</span><span class="sxs-lookup"><span data-stu-id="e3afa-118">The lock that protects the data related to event handling with TAPI.</span></span>                             |
| <span data-ttu-id="e3afa-119">ITTerminalManager</span><span class="sxs-lookup"><span data-stu-id="e3afa-119">ITTerminalManager</span></span>               | <span data-ttu-id="e3afa-120">\*m \_ pITTerminalManager</span><span class="sxs-lookup"><span data-stu-id="e3afa-120">\*m\_pITTerminalManager</span></span> | <span data-ttu-id="e3afa-121">Puntero al objeto de administrador de Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="e3afa-121">The pointer to the Terminal Manager object.</span></span>                                                      |
| <span data-ttu-id="e3afa-122">CMSPArray <ITTerminal \*></span><span class="sxs-lookup"><span data-stu-id="e3afa-122">CMSPArray <ITTerminal \*></span></span> | <span data-ttu-id="e3afa-123">m \_ terminales</span><span class="sxs-lookup"><span data-stu-id="e3afa-123">m\_Terminals</span></span>            | <span data-ttu-id="e3afa-124">Lista de los terminales estáticos que se pueden usar en la dirección.</span><span class="sxs-lookup"><span data-stu-id="e3afa-124">The list of static terminals that can be used on the address.</span></span>                                    |
| <span data-ttu-id="e3afa-125">BOOL</span><span class="sxs-lookup"><span data-stu-id="e3afa-125">BOOL</span></span>                            | <span data-ttu-id="e3afa-126">m \_ fTerminalsUpToDate</span><span class="sxs-lookup"><span data-stu-id="e3afa-126">m\_fTerminalsUpToDate</span></span>   | <span data-ttu-id="e3afa-127">Esta marca es **true** si la lista de terminales está actualizada.</span><span class="sxs-lookup"><span data-stu-id="e3afa-127">This flag is **TRUE** if the terminal list is up to date.</span></span>                                        |
| <span data-ttu-id="e3afa-128">CMSPCritSection</span><span class="sxs-lookup"><span data-stu-id="e3afa-128">CMSPCritSection</span></span>                 | <span data-ttu-id="e3afa-129">m \_ TerminalDataLock</span><span class="sxs-lookup"><span data-stu-id="e3afa-129">m\_TerminalDataLock</span></span>     | <span data-ttu-id="e3afa-130">El bloqueo que protege los miembros de datos relacionados con terminal.</span><span class="sxs-lookup"><span data-stu-id="e3afa-130">The lock that protects the terminal-related data members.</span></span>                                        |



 

 

 



