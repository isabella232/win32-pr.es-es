---
description: configuración regional \_ ITIMEMARKPOSN
ms.assetid: 4aef2631-c05b-41e8-8f4d-f40da4143ab4
title: LOCALE_ITIMEMARKPOSN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0182235754d8f5b6b95bad6c58b4fee87d394d4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105689564"
---
# <a name="locale_itimemarkposn"></a><span data-ttu-id="57606-103">configuración regional \_ ITIMEMARKPOSN</span><span class="sxs-lookup"><span data-stu-id="57606-103">LOCALE\_ITIMEMARKPOSN</span></span>

<span data-ttu-id="57606-104">Especificador que indica si la cadena de marcador de hora (AM o PM) precede o sigue a la cadena de hora.</span><span class="sxs-lookup"><span data-stu-id="57606-104">Specifier indicating whether the time marker string (AM or PM) precedes or follows the time string.</span></span> <span data-ttu-id="57606-105">El valor del registro es iTimePrefix para la compatibilidad con versiones asiáticas anteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="57606-105">The registry value is iTimePrefix for compatibility with previous Asian versions of Windows.</span></span> <span data-ttu-id="57606-106">El especificador debe tener uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="57606-106">The specifier must have one of the following values.</span></span> <span data-ttu-id="57606-107">No se permiten valores especificados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="57606-107">No user-specified values are allowed.</span></span> <span data-ttu-id="57606-108">Es preferible que la aplicación use la constante [ \_ STIMEFORMAT de configuración regional](locale-stime-constants.md) en lugar de la configuración regional \_ ITIMEMARKPOSN.</span><span class="sxs-lookup"><span data-stu-id="57606-108">It is preferred for your application to use the [LOCALE\_STIMEFORMAT](locale-stime-constants.md) constant instead of LOCALE\_ITIMEMARKPOSN.</span></span>



| <span data-ttu-id="57606-109">Value</span><span class="sxs-lookup"><span data-stu-id="57606-109">Value</span></span> | <span data-ttu-id="57606-110">Significado</span><span class="sxs-lookup"><span data-stu-id="57606-110">Meaning</span></span>        |
|-------|----------------|
| <span data-ttu-id="57606-111">0</span><span class="sxs-lookup"><span data-stu-id="57606-111">0</span></span>     | <span data-ttu-id="57606-112">Use como sufijo.</span><span class="sxs-lookup"><span data-stu-id="57606-112">Use as suffix.</span></span> |
| <span data-ttu-id="57606-113">1</span><span class="sxs-lookup"><span data-stu-id="57606-113">1</span></span>     | <span data-ttu-id="57606-114">Use como prefijo.</span><span class="sxs-lookup"><span data-stu-id="57606-114">Use as prefix.</span></span> |



 

 

 



