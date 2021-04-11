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
# <a name="async-replies-versus-events-on-new-call-handles"></a>Respuestas asincrónicas frente a eventos en los nuevos identificadores de llamada

TSPI incluye una serie de operaciones que inician la duración de un identificador de llamada. Si el proveedor de servicios devuelve SUCCEss para este tipo de operación, debe rellenar el identificador opaco del tipo **HDRVCALL**, que usa para la nueva llamada antes de que se devuelva. TAPI no realiza nunca operaciones en la llamada antes de que se haya recibido el [*\_ procedimiento de finalización*](/windows/win32/api/tspi/nc-tspi-async_completion) de la búsqueda de coincidencias. Si el proveedor de servicios devuelve un error, el identificador deja de ser válido automáticamente (es decir, sin [**TSPI \_ lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall)). En efecto, TAPI trata el identificador como "todavía no es válido" hasta la finalización asincrónica.

El proveedor de servicios también debe tratar el identificador como "todavía no es válido" hasta que se reciba el [*\_ procedimiento de finalización*](/windows/win32/api/tspi/nc-tspi-async_completion) de la coincidencia. En otras palabras, no debe emitir ninguna función [*de \_ evento de línea*](/windows/win32/api/tspi/nc-tspi-lineevent) para la nueva llamada o incluirla en los recuentos de llamadas de mensajes o estructuras de datos de estado de la línea.

El nivel de TAPI también se ajusta a estas restricciones del ciclo de vida; no se devuelve un nuevo identificador de llamada o es válido hasta que el mensaje de [**\_ respuesta de línea**](./line-reply.md) coincidente, y no se entrega ningún evento para la nueva llamada a la aplicación hasta después del mensaje de respuesta de línea \_ .

Las operaciones de TSPI a las que se aplica este principio de "vigencia inicial" son las siguientes:

-   [**TSPI \_ lineCompleteTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linecompletetransfer)
-   [**TSPI \_ lineForward**](/windows/win32/api/tspi/nf-tspi-tspi_lineforward)
-   [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)
-   [**TSPI \_ linePickup**](/windows/win32/api/tspi/nf-tspi-tspi_linepickup)
-   [**TSPI \_ linePrepareAddToConference**](/windows/win32/api/tspi/nf-tspi-tspi_lineprepareaddtoconference)
-   [**TSPI \_ lineSetupConference**](/windows/win32/api/tspi/nf-tspi-tspi_linesetupconference)
-   [**TSPI \_ lineSetupTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer)
-   [**TSPI \_ lineUnpark**](/windows/win32/api/tspi/nf-tspi-tspi_lineunpark)

 

 
