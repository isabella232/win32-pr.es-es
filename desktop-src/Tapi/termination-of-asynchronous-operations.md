---
description: Cuando una aplicación llama a la función lineClose con una o varias operaciones asincrónicas pendientes, TAPI puede dirigir al proveedor de servicios a finalizar las operaciones asincrónicas asociadas a una llamada.
ms.assetid: b26ce074-76dc-4a50-8c17-d3412c336d59
title: Finalización de operaciones asincrónicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d026754af75743314fbdbf7a2a3c82f9935f9b053f2a7186f095e4f452a0bdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773005"
---
# <a name="termination-of-asynchronous-operations"></a>Finalización de operaciones asincrónicas

Cuando una aplicación llama a la función [**lineClose**](/windows/win32/api/tapi/nf-tapi-lineclose) con una o varias operaciones asincrónicas pendientes, TAPI puede dirigir al proveedor de servicios a finalizar las operaciones asincrónicas asociadas a una llamada, en función de si la aplicación es el único propietario de la llamada y tiene el único identificador de la llamada.

Si la aplicación es el único propietario de una llamada, TAPI llama a la línea [**\_ TSPIDropOnClose**](./tspi-linedroponclose.md) o [**a la línea \_ TSPIDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) (según el proveedor) para cada llamada de este tipo. El proveedor de servicios debe comprobar si hay operaciones asincrónicas pendientes asociadas a la llamada que se va a descartar. Si existe una operación pendiente, el proveedor de servicios debe realizar la acción adecuada, posiblemente finalizando la operación en curso.

Si la aplicación tiene el único identificador para una llamada (es decir, no hay otros propietarios o monitores), TAPI llama a la función [**\_ TSPI lineCloseCall.**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) El proveedor de servicios debe considerar esta llamada como la indicación absoluta de que las operaciones asincrónicas pendientes deben abandonarse. El proveedor de servicios debe asegurarse de que la llamada se completa correctamente y debe llamar a la función de devolución de llamada [**ASYNC \_ COMPLETION**](/windows/win32/api/tspi/nc-tspi-async_completion) para todas las operaciones asincrónicas pendientes, especificando el valor de error LINEERR \_ OPERATIONFAILED. Si TAPI llamó previamente a la función [**TSPI \_ lineDropOnClose**](./tspi-linedroponclose.md) o [**TSPI \_ lineDrop,**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) llama a **TSPI \_ lineCloseCall** inmediatamente después de que el proveedor de servicios vuelva de la otra llamada; no espera a que se complete la operación asincrónica asociada a la función **\_ lineDrop de TSPI.**

Si la aplicación no es el único propietario de la llamada, TAPI no llama a la línea [**\_ TSPIDropOnClose**](./tspi-linedroponclose.md) ni [**a la línea \_ TSPIDrop.**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) Si la aplicación no tiene el único identificador de la llamada, TAPI no llama a la función [**\_ lineCloseCall de TSPI.**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) Si la aplicación no es el único propietario ni el único propietario de un identificador para la llamada, TAPI no envía ninguna notificación al proveedor de servicios y, por tanto, las operaciones asincrónicas pendientes permanecen intactas. Esto significa que estas aplicaciones no pueden finalizar las operaciones asincrónicas que han iniciado mediante la [**función lineClose.**](/windows/win32/api/tapi/nf-tapi-lineclose) Sin embargo, dado que cada operación asincrónica requiere que la aplicación que invoca sea propietaria de la llamada, la probabilidad de que una aplicación no pueda finalizar las operaciones asincrónicas es muy poco frecuente. Si se produce, los demás propietarios de las llamadas deben asumir la responsabilidad de la disposición de las llamadas.

Si TAPI llama a las líneas [**\_ TSPIDropOnClose**](./tspi-linedroponclose.md) o [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop), el proveedor de servicios debe enviar finalmente un mensaje LINECALLSTATE IDLE para la llamada asociada (a menos que se llame primero a \_ [**TSPI \_ lineCloseCall)**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) para que los monitores de la llamada puedan limpiar. Cuando el último monitor ha llamado a la función [**lineDeallocateCall,**](/windows/win32/api/tapi/nf-tapi-linedeallocatecall) TAPI llama a la función **\_ lineCloseCall de TSPI;** todas las operaciones pendientes deben completarse o finalizarse y se llama a [**ASYNC \_ COMPLETION,**](/windows/win32/api/tspi/nc-tspi-async_completion) como se ha descrito anteriormente.

 

 
