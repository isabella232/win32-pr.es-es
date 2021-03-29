---
description: Hay cinco operaciones asincrónicas que no están relacionadas con ninguna llamada determinada.
ms.assetid: d7107834-07e4-40ed-91ea-2e6127597c13
title: Operaciones asincrónicas con menos llamadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32f4a246ab4a9022ce01d9707a7c5dc5cdc6e9e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360738"
---
# <a name="call-less-asynchronous-operations"></a>Operaciones asincrónicas con menos llamadas

Hay cinco operaciones asincrónicas que no están relacionadas con ninguna llamada determinada. Las funciones [**lineDevSpecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific), [**lineDevSpecificFeature**](/windows/win32/api/tapi/nf-tapi-linedevspecificfeature), [**lineForward**](/windows/win32/api/tapi/nf-tapi-lineforward), [**lineSetTerminal**](/windows/win32/api/tapi/nf-tapi-linesetterminal)y [**lineUncompleteCall**](/windows/win32/api/tapi/nf-tapi-lineuncompletecall) de TAPI 2. x inician estas operaciones. Si una aplicación inicia una de estas operaciones asincrónicas y llama a [**lineClose**](/windows/win32/api/tapi/nf-tapi-lineclose), es posible que el proveedor de servicios no reciba ninguna indicación de que la aplicación ha abandonado la función. Esto puede ocurrir si la aplicación no era la única aplicación que tiene abierta la línea. Si la aplicación llama a **lineClose** con una de estas operaciones pendientes y es la única aplicación con un identificador a la línea, TAPI llama a la función [**TSPI \_ lineClose**](/windows/win32/api/tspi/nf-tspi-tspi_lineclose) y el proveedor de servicios debe finalizar la operación asincrónica, llamando a la función de devolución de llamada del [*\_ procedimiento de finalización*](/windows/win32/api/tspi/nc-tspi-async_completion) para cada operación pendiente con el valor de error LINEERR \_ OPERATIONFAILED.

 

 
