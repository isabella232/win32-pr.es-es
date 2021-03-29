---
description: Permite realizar un seguimiento de las tarjetas en los lectores. Estas rutinas suelen usar la \_ estructura READERSTATE de la matriz en una matriz.
ms.assetid: b26b26bf-85ff-435f-a679-7529f19b1c1b
title: Funciones de seguimiento de tarjetas inteligentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde9bebfeea2718ce634d585c2740cb510500ce3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912074"
---
# <a name="smart-card-tracking-functions"></a><span data-ttu-id="0ef4e-104">Funciones de seguimiento de tarjetas inteligentes</span><span class="sxs-lookup"><span data-stu-id="0ef4e-104">Smart Card Tracking Functions</span></span>

<span data-ttu-id="0ef4e-105">Las siguientes funciones le permiten realizar un seguimiento de las tarjetas en los lectores.</span><span class="sxs-lookup"><span data-stu-id="0ef4e-105">The following functions let you track cards within readers.</span></span> <span data-ttu-id="0ef4e-106">Estas rutinas suelen usar la estructura [**\_ READERSTATE**](/windows/desktop/api/Winscard/ns-winscard-scard_readerstatea) de la matriz en una matriz.</span><span class="sxs-lookup"><span data-stu-id="0ef4e-106">These routines typically use the [**SCARD\_READERSTATE**](/windows/desktop/api/Winscard/ns-winscard-scard_readerstatea) structure within an array.</span></span>



| <span data-ttu-id="0ef4e-107">Tema</span><span class="sxs-lookup"><span data-stu-id="0ef4e-107">Topic</span></span>                                                | <span data-ttu-id="0ef4e-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="0ef4e-108">Description</span></span>                                                                                                                            |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0ef4e-109">**SCardLocateCards**</span><span class="sxs-lookup"><span data-stu-id="0ef4e-109">**SCardLocateCards**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardlocatecardsa)         | <span data-ttu-id="0ef4e-110">Busque una tarjeta cuya [*cadena ATR*](../secgloss/a-gly.md) coincida con un nombre de tarjeta proporcionado.</span><span class="sxs-lookup"><span data-stu-id="0ef4e-110">Search for a card whose [*ATR string*](../secgloss/a-gly.md) matches a supplied card name.</span></span> |
| [<span data-ttu-id="0ef4e-111">**SCardGetStatusChange**</span><span class="sxs-lookup"><span data-stu-id="0ef4e-111">**SCardGetStatusChange**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardgetstatuschangea) | <span data-ttu-id="0ef4e-112">Bloquear la ejecución hasta que cambie la disponibilidad actual de las tarjetas.</span><span class="sxs-lookup"><span data-stu-id="0ef4e-112">Block execution until the current availability of cards changes.</span></span>                                                                       |
| [<span data-ttu-id="0ef4e-113">**SCardCancel**</span><span class="sxs-lookup"><span data-stu-id="0ef4e-113">**SCardCancel**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardcancel)                   | <span data-ttu-id="0ef4e-114">Finalizar acciones pendientes.</span><span class="sxs-lookup"><span data-stu-id="0ef4e-114">Terminate outstanding actions.</span></span>                                                                                                         |



 

 

 
