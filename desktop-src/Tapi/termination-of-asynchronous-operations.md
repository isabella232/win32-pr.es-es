---
description: Cuando una aplicación llama a la función lineClose con una o más operaciones asincrónicas pendientes, TAPI puede indicar al proveedor de servicios que termine las operaciones asincrónicas asociadas a una llamada.
ms.assetid: b26ce074-76dc-4a50-8c17-d3412c336d59
title: Terminación de operaciones asincrónicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8ed2acb0f442e5f4f07427f0e224d7a288087d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678555"
---
# <a name="termination-of-asynchronous-operations"></a>Terminación de operaciones asincrónicas

Cuando una aplicación llama a la función [**lineClose**](/windows/win32/api/tapi/nf-tapi-lineclose) con una o más operaciones asincrónicas pendientes, TAPI puede indicar al proveedor de servicios que termine las operaciones asincrónicas asociadas a una llamada, en función de si la aplicación es el único propietario de la llamada y tiene el único identificador de la llamada.

Si la aplicación es el único propietario de una llamada, TAPI llama a [**TSPI \_ LineDropOnClose**](./tspi-linedroponclose.md) o [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) (dependiendo del proveedor) para cada una de estas llamadas. El proveedor de servicios debe comprobar si hay operaciones asincrónicas pendientes asociadas a la llamada que se va a quitar. Si existe una operación pendiente, el proveedor de servicios debe llevar a cabo la acción adecuada, posiblemente finalizando la operación en curso.

Si la aplicación tiene el único identificador de una llamada (es decir, no hay otros propietarios o monitores), TAPI llama a la [**función \_ LineCloseCall de TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) . El proveedor de servicios debe considerar que esta llamada es la indicación absoluta de que se deben abandonar las operaciones asincrónicas pendientes. El proveedor de servicios debe garantizar una finalización ordenada de la llamada y debe llamar a la función de devolución de llamada de [**\_ finalización asincrónica**](/windows/win32/api/tspi/nc-tspi-async_completion) para todas las operaciones asincrónicas pendientes, especificando el valor de error de LINEERR \_ OPERATIONFAILED. Si TAPI anteriormente llamó a la función [**TSPI \_ LineDropOnClose**](./tspi-linedroponclose.md) o [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) , llama a **TSPI \_ lineCloseCall** inmediatamente después de que el proveedor de servicios vuelva de la otra llamada; no espera a que se complete la operación asincrónica asociada a la función **TSPI \_ lineDrop** .

Si la aplicación no es el único propietario de la llamada, TAPI no llama a [**TSPI \_ LineDropOnClose**](./tspi-linedroponclose.md) o [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop). Si la aplicación no tiene el único identificador de la llamada, TAPI no llama a la función [**\_ LineCloseCall de TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) . Si la aplicación no es el único propietario ni el único poseedor de un identificador de la llamada, TAPI no envía ninguna notificación al proveedor de servicios y, por tanto, las operaciones asincrónicas pendientes permanecen intactas. Esto significa que estas aplicaciones no pueden finalizar las operaciones asincrónicas que se han iniciado mediante la función [**lineClose**](/windows/win32/api/tapi/nf-tapi-lineclose) . Sin embargo, dado que cada operación asincrónica requiere que la aplicación que realiza la invocación sea propietaria de la llamada, la probabilidad de que una aplicación no pueda finalizar las operaciones asincrónicas es muy poco frecuente. En caso de que se produzca, los demás propietarios de las llamadas deben asumir la responsabilidad de la disposición de las llamadas.

Si TAPI llama a [**TSPI \_ LineDropOnClose**](./tspi-linedroponclose.md) o [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop), el proveedor de servicios debe enviar finalmente un \_ mensaje de inactividad de LINECALLSTATE para la llamada asociada (a menos que se llame a [**TSPI \_ lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) primero) para que los monitores de la llamada puedan realizar la limpieza. Cuando el último monitor ha llamado a la función [**lineDeallocateCall**](/windows/win32/api/tapi/nf-tapi-linedeallocatecall) , TAPI llama a la función **TSPI \_ lineCloseCall** ; todas las operaciones pendientes se deben completar o finalizar y se ha llamado a la [**\_ finalización asincrónica**](/windows/win32/api/tspi/nc-tspi-async_completion) , tal y como se ha descrito anteriormente.

 

 
