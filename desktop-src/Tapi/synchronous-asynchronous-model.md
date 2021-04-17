---
description: La naturaleza interactiva de telefonía requiere que TAPI sea un entorno operativo en tiempo real.
ms.assetid: b8512588-ec28-4fbe-b47f-b900e2dba1f2
title: Modelo sincrónico/asincrónico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02b3d3b58e9704719e502fa3efc11bc4dc216479
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687494"
---
# <a name="synchronousasynchronous-model"></a>Modelo sincrónico/asincrónico

La naturaleza interactiva de telefonía requiere que TAPI sea un entorno operativo en tiempo real. Muchas de las funciones TAPI son necesarias para completar rápidamente y devolver los resultados a la aplicación de forma sincrónica. Es posible que otras funciones (como el marcado) no se puedan completar tan rápidamente y, por tanto, funcionen de forma asincrónica.

Las operaciones de telefonía se completan de forma sincrónica o asincrónica. Estos dos modelos difieren como se indica a continuación. Las *funciones sincrónicas* ejecutan toda la solicitud antes de que se permita que el subproceso del llamador vuelva de la llamada de función. *Las funciones asincrónicas* devuelven antes de que la solicitud se ejecute en su totalidad. Cuando se completa la solicitud asincrónica más tarde, el proveedor de servicios informa de la finalización mediante una llamada a un procedimiento de devolución de llamada que TAPI proporcionó originalmente en la secuencia de inicialización.

-   Las operaciones asincrónicas tienen un parámetro denominado *dwRequestID* del tipo definido [DRV \_ REQUESTID](./drv-requestid.md) como su primer parámetro. Este tipo de operación realiza parte de su procesamiento en la llamada de función y el resto de su procesamiento en un subproceso de ejecución independiente después de que se devuelva la llamada de función. Cuando la función devuelve, devuelve un resultado de error negativo o el *dwRequestID* (positivo) que se pasó en la llamada de función. El resultado del error negativo indica que la operación ha finalizado (y ha generado un error). El *dwRequestID* positivo devuelto indica que la operación continúa en el subproceso independiente. En tal caso, el proveedor de servicios llama finalmente al procedimiento de [**\_ finalización asincrónica**](/windows/win32/api/tspi/nc-tspi-async_completion) , pasando el *dwRequestID* y un código de resultado para indicar el resultado de la operación. El código de resultado es cero para el éxito o uno del mismo conjunto de resultados de error (negativos). En cualquier caso, el proveedor de servicios nunca debe devolver cero o un valor positivo distinto de *dwRequestID* de una función designada como asincrónica, ya que esto puede producir resultados inesperados. Los proveedores de servicios siempre deben copiar los datos de entrada de la memoria de la aplicación en la memoria del proveedor de servicios antes de volver de una función asincrónica.
-   Las operaciones sincrónicas no tienen *dwRequestID* como primer parámetro. Este tipo de operación realiza todo su procesamiento en el subproceso de ejecución del llamador y devuelve el resultado final cuando vuelve. El resultado es cero para el éxito o un código de error negativo para el error. El proveedor de servicios no llama a la [**\_ finalización asincrónica**](/windows/win32/api/tspi/nc-tspi-async_completion) para las operaciones sincrónicas.

Es interesante considerar el control de tiempo de una devolución de llamada de "finalización" con respecto a cuando se devuelve la solicitud original. El proveedor de servicios implementará una solicitud asincrónica típica como en el siguiente pseudocódigo:

``` syntax
Some_request(Request_ID, ...) {
  check parameters for validity
  check device state for validity
  store Request_ID for Completion Interrupt Handler's use
  manipulate device registers to start physical operation
  return Request_ID  // to indicate asynch operation
}
Operation Completion Interrupt Handler: {
  if operation was successful then
    call "completion" callback passing Request_ID and "success"
  else
    call "completion" callback passing Request_ID and "error num"
  endif
}
```

Si la operación se completa muy rápidamente (o la solicitud original se devuelve muy lentamente), es posible que el controlador de interrupción que se ejecuta cuando se completa una operación física se desencadene antes de que la solicitud original se devuelva a la aplicación o incluso a TAPI. Se permite este comportamiento. TAPI garantiza que se entregue la notificación de finalización eventual a la aplicación después de que se devuelva la solicitud original.

**TAPI 2. x:** Muestra el estado de si cada función se completa de forma sincrónica o asincrónica en [referencia de función rápida de TAPI](./tapi-quick-function-reference.md).

 

 
