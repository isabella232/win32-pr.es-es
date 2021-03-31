---
description: Hay nueve operaciones asincrónicas relacionadas con los teléfonos.
ms.assetid: b255bdde-1677-401f-b02d-4850e0e98dc4
title: Operaciones telefónicas asincrónicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba4a70a1d980c4f0d42d5160ee020531b538f488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911217"
---
# <a name="asynchronous-phone-operations"></a>Operaciones telefónicas asincrónicas

Hay nueve operaciones asincrónicas relacionadas con los teléfonos. Los inician las funciones [**TSPI \_ phoneDevSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_phonedevspecific), [**TSPI \_ phoneSetButtonInfo**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetbuttoninfo), [**TSPI \_**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetdata)phoneSetData, [**TSPI \_ phoneSetDisplay**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetdisplay), [**TSPI \_ phoneSetGain**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetgain), [**TSPI \_ phoneSetHookSwitch**](/windows/win32/api/tspi/nf-tspi-tspi_phonesethookswitch), [**TSPI \_ phoneSetLamp**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetlamp), [**TSPI \_ phoneSetRing**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetring)y [**TSPI \_ phoneSetVolume**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetvolume) . Si una aplicación llama a la función [**phoneClose**](/windows/win32/api/tapi/nf-tapi-phoneclose) de TAPI y tiene el único identificador del teléfono, TAPI llama a la función [**TSPI \_ phoneClose**](/windows/win32/api/tspi/nf-tspi-tspi_phoneclose) para indicar al proveedor de servicios que termine las operaciones asincrónicas y llame a la función de devolución de llamada del [*\_ procedimiento de finalización*](/windows/win32/api/tspi/nc-tspi-async_completion) según corresponda. Si la aplicación no tiene el único identificador del teléfono, el proveedor de servicios no recibe ninguna notificación de la solicitud y las operaciones asincrónicas pendientes permanecen activas.

 

 
