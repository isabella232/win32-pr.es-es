---
description: TSPI incluye una serie de operaciones que inician la duración de un identificador de llamada.
ms.assetid: 28e171a3-db47-40fd-9c5a-d7b76d834a99
title: Respuestas asincrónicas frente a eventos en los nuevos identificadores de llamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02511a083c318afb227e3e172191d3ab84a69fed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911221"
---
# <a name="async-replies-versus-events-on-new-call-handles"></a><span data-ttu-id="8051c-103">Respuestas asincrónicas frente a eventos en los nuevos identificadores de llamada</span><span class="sxs-lookup"><span data-stu-id="8051c-103">Async Replies versus Events on New Call Handles</span></span>

<span data-ttu-id="8051c-104">TSPI incluye una serie de operaciones que inician la duración de un identificador de llamada.</span><span class="sxs-lookup"><span data-stu-id="8051c-104">TSPI includes a number of operations that start the lifetime of a call handle.</span></span> <span data-ttu-id="8051c-105">Si el proveedor de servicios devuelve SUCCEss para este tipo de operación, debe rellenar el identificador opaco del tipo **HDRVCALL**, que usa para la nueva llamada antes de que se devuelva.</span><span class="sxs-lookup"><span data-stu-id="8051c-105">If the service provider returns SUCCESS for such an operation, it must fill in the opaque handle of type **HDRVCALL**, which it uses for the new call before it returns.</span></span> <span data-ttu-id="8051c-106">TAPI no realiza nunca operaciones en la llamada antes de que se haya recibido el [*\_ procedimiento de finalización*](/windows/win32/api/tspi/nc-tspi-async_completion) de la búsqueda de coincidencias.</span><span class="sxs-lookup"><span data-stu-id="8051c-106">TAPI never performs operations on the call before the matching [*Completion\_Proc*](/windows/win32/api/tspi/nc-tspi-async_completion) has been received.</span></span> <span data-ttu-id="8051c-107">Si el proveedor de servicios devuelve un error, el identificador deja de ser válido automáticamente (es decir, sin [**TSPI \_ lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall)).</span><span class="sxs-lookup"><span data-stu-id="8051c-107">If the service provider returns FAILURE, the handle automatically becomes invalid (that is, without [**TSPI\_lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall)).</span></span> <span data-ttu-id="8051c-108">En efecto, TAPI trata el identificador como "todavía no es válido" hasta la finalización asincrónica.</span><span class="sxs-lookup"><span data-stu-id="8051c-108">In effect, TAPI treats the handle as "not yet valid" until the asynchronous completion.</span></span>

<span data-ttu-id="8051c-109">El proveedor de servicios también debe tratar el identificador como "todavía no es válido" hasta que se reciba el [*\_ procedimiento de finalización*](/windows/win32/api/tspi/nc-tspi-async_completion) de la coincidencia.</span><span class="sxs-lookup"><span data-stu-id="8051c-109">The service provider must also treat the handle as "not yet valid" until after the matching [*Completion\_Proc*](/windows/win32/api/tspi/nc-tspi-async_completion) is received.</span></span> <span data-ttu-id="8051c-110">En otras palabras, no debe emitir ninguna función [*de \_ evento de línea*](/windows/win32/api/tspi/nc-tspi-lineevent) para la nueva llamada o incluirla en los recuentos de llamadas de mensajes o estructuras de datos de estado de la línea.</span><span class="sxs-lookup"><span data-stu-id="8051c-110">In other words, it must not issue any [*Line\_Event*](/windows/win32/api/tspi/nc-tspi-lineevent) functions for the new call or include it in call counts in messages or status data structures for the line.</span></span>

<span data-ttu-id="8051c-111">El nivel de TAPI también se ajusta a estas restricciones del ciclo de vida; no se devuelve un nuevo identificador de llamada o es válido hasta que el mensaje de [**\_ respuesta de línea**](./line-reply.md) coincidente, y no se entrega ningún evento para la nueva llamada a la aplicación hasta después del mensaje de respuesta de línea \_ .</span><span class="sxs-lookup"><span data-stu-id="8051c-111">The TAPI level also conforms to these life cycle restrictions; a new call handle is not returned or valid until the matching [**LINE\_REPLY**](./line-reply.md) message, and no events for the new call are delivered to the application until after the LINE\_REPLY message.</span></span>

<span data-ttu-id="8051c-112">Las operaciones de TSPI a las que se aplica este principio de "vigencia inicial" son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="8051c-112">The TSPI operations to which this "start lifetime" principle applies are the following:</span></span>

-   [<span data-ttu-id="8051c-113">**TSPI \_ lineCompleteTransfer**</span><span class="sxs-lookup"><span data-stu-id="8051c-113">**TSPI\_lineCompleteTransfer**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linecompletetransfer)
-   [<span data-ttu-id="8051c-114">**TSPI \_ lineForward**</span><span class="sxs-lookup"><span data-stu-id="8051c-114">**TSPI\_lineForward**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineforward)
-   [<span data-ttu-id="8051c-115">**TSPI \_ lineMakeCall**</span><span class="sxs-lookup"><span data-stu-id="8051c-115">**TSPI\_lineMakeCall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)
-   [<span data-ttu-id="8051c-116">**TSPI \_ linePickup**</span><span class="sxs-lookup"><span data-stu-id="8051c-116">**TSPI\_linePickup**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linepickup)
-   [<span data-ttu-id="8051c-117">**TSPI \_ linePrepareAddToConference**</span><span class="sxs-lookup"><span data-stu-id="8051c-117">**TSPI\_linePrepareAddToConference**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineprepareaddtoconference)
-   [<span data-ttu-id="8051c-118">**TSPI \_ lineSetupConference**</span><span class="sxs-lookup"><span data-stu-id="8051c-118">**TSPI\_lineSetupConference**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetupconference)
-   [<span data-ttu-id="8051c-119">**TSPI \_ lineSetupTransfer**</span><span class="sxs-lookup"><span data-stu-id="8051c-119">**TSPI\_lineSetupTransfer**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer)
-   [<span data-ttu-id="8051c-120">**TSPI \_ lineUnpark**</span><span class="sxs-lookup"><span data-stu-id="8051c-120">**TSPI\_lineUnpark**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineunpark)

 

 
