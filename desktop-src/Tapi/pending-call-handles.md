---
description: Se necesita un proveedor de servicios para crear uno o varios identificadores de llamada (variables de tipo HDRVCALL) siempre que TAPI llame a una de las siguientes funciones.
ms.assetid: 0a9d9afd-9786-4d9e-b0a2-12c9a1e13887
title: Identificadores de llamadas pendientes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c021ff10f2a1a812c46fb77663ac1a3a3a8d791
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677345"
---
# <a name="pending-call-handles"></a>Identificadores de llamadas pendientes

Se necesita un proveedor de servicios para crear uno o varios identificadores de llamada (variables de tipo [HDRVCALL](hdrvline.md)) siempre que TAPI llame a una de estas funciones: [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall), [**TSPI \_ lineCompleteTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linecompletetransfer), [**TSPI \_ lineForward**](/windows/win32/api/tspi/nf-tspi-tspi_lineforward), [**TSPI \_ linePickup**](/windows/win32/api/tspi/nf-tspi-tspi_linepickup), [**TSPI \_ linePrepareAddToConference**](/windows/win32/api/tspi/nf-tspi-tspi_lineprepareaddtoconference), [**TSPI \_ lineSetupConference**](/windows/win32/api/tspi/nf-tspi-tspi_linesetupconference), [**TSPI \_ lineSetupTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer)y [**TSPI \_ lineUnpark**](/windows/win32/api/tspi/nf-tspi-tspi_lineunpark). Cuando un proveedor de servicios recibe esta llamada, el proveedor de servicios debe establecer la variable proporcionada por TAPI en el valor del identificador antes de volver de la llamada. TAPI considera que este "identificador de llamada pendiente" es válido provisionalmente. Cuando el proveedor de servicios crea realmente la llamada, debe llamar a la devolución de llamada de [**\_ finalización asincrónica**](/windows/win32/api/tspi/nc-tspi-async_completion) para validar el identificador formalmente.

Si TAPI llama a la función [**\_ LineCloseCall de TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) antes de que el proveedor de servicios valide formalmente un identificador de llamada pendiente, el proveedor de servicios debe detener todo el procesamiento asociado al identificador de llamada y llamar a la función de devolución de llamada de [**\_ finalización asincrónica**](/windows/win32/api/tspi/nc-tspi-async_completion) mediante el valor de error LINEERR \_ OPERATIONFAILED.

 

 
