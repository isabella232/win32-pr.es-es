---
description: Se requiere un proveedor de servicios para crear uno o varios identificadores de llamada (variables de tipo HDRVCALL) cada vez que TAPI llama a una de las siguientes funciones.
ms.assetid: 0a9d9afd-9786-4d9e-b0a2-12c9a1e13887
title: Identificadores de llamadas pendientes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d082c0b9111d6d58debacec01d20ffe9af2d024aafd61b3f1085267e62d3d6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518595"
---
# <a name="pending-call-handles"></a>Identificadores de llamadas pendientes

Se requiere un proveedor de servicios para crear uno o varios identificadores de llamada (variables de tipo [HDRVCALL](hdrvline.md)) cada vez que TAPI llame a una de estas funciones: [**TSPI \_ lineMakeCall,**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) [**TSPI \_ lineCompleteTransfer,**](/windows/win32/api/tspi/nf-tspi-tspi_linecompletetransfer) [**TSPI \_ lineForward**](/windows/win32/api/tspi/nf-tspi-tspi_lineforward), [**TSPI \_ linePickup**](/windows/win32/api/tspi/nf-tspi-tspi_linepickup), [**TSPI \_ linePrepareAddToConference,**](/windows/win32/api/tspi/nf-tspi-tspi_lineprepareaddtoconference) [**TSPI \_ lineSetupConference,**](/windows/win32/api/tspi/nf-tspi-tspi_linesetupconference) [**TSPI \_ lineSetupTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer)y [**TSPI \_ lineUnpark.**](/windows/win32/api/tspi/nf-tspi-tspi_lineunpark) Cuando un proveedor de servicios recibe una llamada de este tipo, el proveedor de servicios debe establecer la variable proporcionada por TAPI en el valor del identificador antes de volver de la llamada. TAPI considera que este "identificador de llamada pendiente" es provisionalmente válido. Cuando el proveedor de servicios crea realmente la llamada, debe llamar a la devolución de llamada [**\_ ASYNC COMPLETION**](/windows/win32/api/tspi/nc-tspi-async_completion) para validar formalmente el identificador.

Si TAPI llama a la función [**\_ lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) de TSPI antes de que el proveedor de servicios valide formalmente un identificador de llamada pendiente, el proveedor de servicios debe detener todo el procesamiento adicional asociado al identificador de llamada y llamar a la función de devolución de llamada [**ASYNC \_ COMPLETION**](/windows/win32/api/tspi/nc-tspi-async_completion) con el valor de error LINEERR \_ OPERATIONFAILED.

 

 
