---
description: La naturaleza interactiva de la telefonía requiere que TAPI sea un entorno operativo en tiempo real.
ms.assetid: b8512588-ec28-4fbe-b47f-b900e2dba1f2
title: Modelo sincrónico/asincrónico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 354bc8e32cdd1bb2bcefac0fe3e4d77361f3be9e37cd6a1549aa157d4b997f43
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975525"
---
# <a name="synchronousasynchronous-model"></a>Modelo sincrónico/asincrónico

La naturaleza interactiva de la telefonía requiere que TAPI sea un entorno operativo en tiempo real. Muchas de las funciones TAPI son necesarias para completarse rápidamente y devolver sus resultados a la aplicación de forma sincrónica. Es posible que otras funciones (como la marcación) no se puedan completar tan rápido y, por tanto, funcionen de forma asincrónica.

Las operaciones de telefonía se completan de forma sincrónica o asincrónica. Estos dos modelos difieren como se muestra a continuación. *Las funciones sincrónicas* ejecutan toda la solicitud antes de que el subproceso del autor de la llamada devuelva de la llamada de función. *Las funciones asincrónicas* devuelven antes de que la solicitud se haya ejecutado en su totalidad. Cuando la solicitud asincrónica se completa más adelante, el proveedor de servicios notifica la finalización mediante una llamada a un procedimiento de devolución de llamada que TAPI le proporcionó originalmente al principio de la secuencia de inicialización.

-   Las operaciones asincrónicas tienen un parámetro *denominado dwRequestID* del tipo [definido DRV \_ REQUESTID](./drv-requestid.md) como su primer parámetro. Esta operación realiza parte de su procesamiento en la llamada de función y el resto de su procesamiento en un subproceso de ejecución independiente después de que se haya devuelto la llamada de función. Cuando la función devuelve un resultado de error negativo o el *dwRequestID* (positivo) que se pasó en la llamada de función. El resultado negativo del error indica que la operación se ha completado (y se ha producido un error). El *dwRequestID positivo* devuelto indica que la operación continúa en el subproceso independiente. En tal caso, el proveedor de servicios finalmente llama al procedimiento [**\_ ASYNC COMPLETION,**](/windows/win32/api/tspi/nc-tspi-async_completion) pasando *dwRequestID* y un código de resultado para indicar el resultado de la operación. El código de resultado es cero para correcto o uno del mismo conjunto de resultados de error (negativos). En cualquier caso, el proveedor de servicios nunca debe devolver cero ni ningún valor positivo que no sea *dwRequestID* de una función designada como asincrónica, ya que puede producir resultados inesperados. Los proveedores de servicios siempre deben copiar los datos de entrada de la memoria de la aplicación en la memoria del proveedor de servicios antes de volver de una función asincrónica.
-   Las operaciones sincrónicas no *tienen dwRequestID* como primer parámetro. Esta operación realiza todo su procesamiento en el subproceso de ejecución del autor de la llamada y devuelve el resultado final cuando vuelve. El resultado es cero si se ha producido un error o un código de error negativo. El proveedor de servicios no llama a [**ASYNC \_ COMPLETION para**](/windows/win32/api/tspi/nc-tspi-async_completion) las operaciones sincrónicas.

Es interesante tener en cuenta el tiempo de una devolución de llamada de "finalización" en relación con el momento en que se devuelve la solicitud original. El proveedor de servicios implementaría una solicitud asincrónica típica como en el pseudocódigo siguiente:

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

Si la operación se completa muy rápidamente (o la solicitud original se devuelve muy lentamente), es posible que se desencadene el controlador de interrupciones que se ejecuta cuando se completa una operación física antes de que la solicitud original vuelva a la aplicación o incluso a TAPI. Se permite este comportamiento. TAPI garantiza que la notificación de finalización final a la aplicación se entrega después de que se devuelva la solicitud original.

**TAPI 2.x:** Muestra qué estado indica si cada función se completa de forma sincrónica o asincrónica en referencia de [función rápida de TAPI.](./tapi-quick-function-reference.md)

 

 
