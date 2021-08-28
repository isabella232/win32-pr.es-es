---
description: TSPI incluye una serie de operaciones que inician la duración de un identificador de llamada.
ms.assetid: 28e171a3-db47-40fd-9c5a-d7b76d834a99
title: Respuestas asincrónicas frente a eventos en nuevos identificadores de llamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55104ea99bd1c6160bd6341cb776c3a86338619363b8e673c95112c8a2d07d04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117948834"
---
# <a name="async-replies-versus-events-on-new-call-handles"></a>Respuestas asincrónicas frente a eventos en nuevos identificadores de llamada

TSPI incluye una serie de operaciones que inician la duración de un identificador de llamada. Si el proveedor de servicios devuelve SUCCESS para esta operación, debe rellenar el identificador opaco de tipo **HDRVCALL**, que usa para la nueva llamada antes de que vuelva. TAPI nunca realiza operaciones en la llamada antes de que se reciba el procedimiento de [*\_ finalización*](/windows/win32/api/tspi/nc-tspi-async_completion) correspondiente. Si el proveedor de servicios devuelve FAILURE, el identificador deja de ser válido automáticamente (es decir, sin [**la línea \_ TSPICloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall)). En efecto, TAPI trata el identificador como "aún no válido" hasta la finalización asincrónica.

El proveedor de servicios también debe tratar el identificador como "aún no válido" hasta que se reciba el procedimiento de [*\_ finalización*](/windows/win32/api/tspi/nc-tspi-async_completion) correspondiente. En otras palabras, no [*\_*](/windows/win32/api/tspi/nc-tspi-lineevent) debe emitir ninguna función de evento de línea para la nueva llamada ni incluirla en recuentos de llamadas en mensajes o estructuras de datos de estado para la línea.

El nivel tapi también se ajusta a estas restricciones del ciclo de vida; No se devuelve un nuevo identificador de llamada ni es válido hasta que el mensaje [**LINE \_ REPLY**](./line-reply.md) correspondiente y no se entrega ningún evento para la nueva llamada a la aplicación hasta después del mensaje LINE \_ REPLY.

Las operaciones TSPI a las que se aplica este principio de "duración de inicio" son las siguientes:

-   [**Línea \_ TSPICompleteTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linecompletetransfer)
-   [**Línea \_ TSPIForward**](/windows/win32/api/tspi/nf-tspi-tspi_lineforward)
-   [**Línea \_ TSPIMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)
-   [**LinePickup de TSPI \_**](/windows/win32/api/tspi/nf-tspi-tspi_linepickup)
-   [**Línea \_ TSPIPrepareAddToConference**](/windows/win32/api/tspi/nf-tspi-tspi_lineprepareaddtoconference)
-   [**Línea \_ TSPISetupConference**](/windows/win32/api/tspi/nf-tspi-tspi_linesetupconference)
-   [**Línea \_ TSPISetupTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer)
-   [**Línea \_ TSPIUnpark**](/windows/win32/api/tspi/nf-tspi-tspi_lineunpark)

 

 
