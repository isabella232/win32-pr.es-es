---
description: Se puede especificar la rutina de devolución de llamada de cola predeterminada para controlar las notificaciones enviadas por SetupCommitFileQueue, o bien una rutina de devolución de llamada personalizada que se basa en la funcionalidad de la rutina de devolución de llamada de cola predeterminada.
ms.assetid: df8ae7b5-f3a2-4343-a603-440ab5c02b88
title: Usar la rutina de devolución de llamada de cola predeterminada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51bceadf309257b9faf2b3ce3b8a12771572664
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667183"
---
# <a name="using-the-default-queue-callback-routine"></a><span data-ttu-id="e9d7c-103">Usar la rutina de devolución de llamada de cola predeterminada</span><span class="sxs-lookup"><span data-stu-id="e9d7c-103">Using the Default Queue Callback Routine</span></span>

<span data-ttu-id="e9d7c-104">Se puede especificar la rutina de devolución de llamada de cola predeterminada para controlar las notificaciones enviadas por [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), o bien una rutina de devolución de llamada personalizada que se basa en la funcionalidad de la rutina de devolución de llamada de cola predeterminada.</span><span class="sxs-lookup"><span data-stu-id="e9d7c-104">The default queue callback routine can be specified to handle notifications sent by [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), or it can be called by a custom callback routine that builds on the functionality of the default queue callback routine.</span></span>

<span data-ttu-id="e9d7c-105">En las secciones siguientes se explica cómo inicializar y finalizar el contexto utilizado por una rutina de devolución de llamada de cola predeterminada.</span><span class="sxs-lookup"><span data-stu-id="e9d7c-105">The following sections explain how to initialize and terminate the context used by a default queue callback routine.</span></span> <span data-ttu-id="e9d7c-106">En las secciones también se describe cómo usar la rutina de devolución de llamada de cola predeterminada con [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) o una rutina de devolución de llamada personalizada.</span><span class="sxs-lookup"><span data-stu-id="e9d7c-106">The sections also describe how to use the default queue callback routine with [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) or a custom callback routine.</span></span>

-   [<span data-ttu-id="e9d7c-107">Inicialización y finalización del contexto de devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="e9d7c-107">Initializing and Terminating the Callback Context</span></span>](initializing-and-terminating-the-callback-context.md)
-   [<span data-ttu-id="e9d7c-108">Llamar a la rutina de devolución de llamada de cola predeterminada</span><span class="sxs-lookup"><span data-stu-id="e9d7c-108">Calling the Default Queue Callback Routine</span></span>](calling-the-default-queue-callback-routine.md)

 

 



