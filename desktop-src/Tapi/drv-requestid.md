---
description: El tipo de los \_ tipos de DataType DRV REQUESTID se usa para proporcionar un identificador único para una solicitud al proveedor de servicios.
ms.assetid: cef6a42a-2e40-4f65-8fab-79cfba143206
title: DRV_REQUESTID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f9c0db093b06b263bcdc702ff14af7e308033f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687513"
---
# <a name="drv_requestid"></a>DRV \_ REQUESTID

El tipo de los tipos de DataType **DRV \_ REQUESTID** se usa para proporcionar un identificador único para una solicitud al proveedor de servicios. Un valor de este tipo se pasa como parámetro a cada función que permite la operación asincrónica. Si la operación es asincrónica, el proveedor de servicios devuelve este valor como el valor devuelto de la función. Siempre que el proveedor de servicios marca una solicitud como asincrónica de esta manera, se debe notificar el final de la operación mediante una llamada a la función de devolución de llamada del [*\_ procedimiento de finalización*](/windows/win32/api/tspi/nc-tspi-async_completion) .

TAPI garantiza que los valores de **DRV \_ REQUESTID** que suministra son estrictamente positivos, es decir, entre los valores de 0x00000001 y 0x7FFFFFFF, ambos incluidos. Además, los valores son únicos en que ningún valor devuelto por una función para marcar la solicitud como asincrónica se volverá a usar antes de que se notifique a la operación como completada.

 

 
