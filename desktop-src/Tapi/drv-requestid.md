---
description: El tipo de datos REQUESTID de DRV \_ se usa para proporcionar un identificador único para una solicitud al proveedor de servicios.
ms.assetid: cef6a42a-2e40-4f65-8fab-79cfba143206
title: DRV_REQUESTID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e75e593ccbf2d9d8135fbb52762a83a539dc29f8ef9446735d0898d3437e37c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118866545"
---
# <a name="drv_requestid"></a>REQUESTID de DRV \_

El **tipo de datos \_ REQUESTID** de DRV se usa para proporcionar un identificador único para una solicitud al proveedor de servicios. Un valor de este tipo se pasa como un parámetro a cada función que permite el funcionamiento asincrónico. Si la operación es asincrónica, el proveedor de servicios devuelve este valor como el valor devuelto de la función. Cada vez que el proveedor de servicios marca una solicitud como asincrónica de esta manera, finalmente debe notificar que la operación se ha completado mediante una llamada a la función de devolución de llamada [*Proc \_*](/windows/win32/api/tspi/nc-tspi-async_completion) de finalización.

TAPI garantiza que los valores **\_ REQUESTID** de DRV que proporciona son estrictamente positivos, es decir, entre los valores de 0x00000001 y 0x7FFFFFFF, ambos inclusive. Además, los valores son únicos en que ningún valor devuelto por una función para marcar la solicitud como asincrónica se volverá a usar antes de que se informe de que la operación se ha completado.

 

 
