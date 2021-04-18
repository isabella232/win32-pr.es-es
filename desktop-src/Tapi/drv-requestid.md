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
# <a name="drv_requestid"></a><span data-ttu-id="f9d4f-103">DRV \_ REQUESTID</span><span class="sxs-lookup"><span data-stu-id="f9d4f-103">DRV\_REQUESTID</span></span>

<span data-ttu-id="f9d4f-104">El tipo de los tipos de DataType **DRV \_ REQUESTID** se usa para proporcionar un identificador único para una solicitud al proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="f9d4f-104">The **DRV\_REQUESTID** datatype is used to supply a unique identifier for a request to the service provider.</span></span> <span data-ttu-id="f9d4f-105">Un valor de este tipo se pasa como parámetro a cada función que permite la operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="f9d4f-105">A value of this type is passed as a parameter to every function that allows for asynchronous operation.</span></span> <span data-ttu-id="f9d4f-106">Si la operación es asincrónica, el proveedor de servicios devuelve este valor como el valor devuelto de la función.</span><span class="sxs-lookup"><span data-stu-id="f9d4f-106">If the operation is asynchronous, the service provider returns this value as the return value of the function.</span></span> <span data-ttu-id="f9d4f-107">Siempre que el proveedor de servicios marca una solicitud como asincrónica de esta manera, se debe notificar el final de la operación mediante una llamada a la función de devolución de llamada del [*\_ procedimiento de finalización*](/windows/win32/api/tspi/nc-tspi-async_completion) .</span><span class="sxs-lookup"><span data-stu-id="f9d4f-107">Whenever the service provider flags a request as asynchronous in this way, it must eventually report the operation is complete by calling the [*Completion\_Proc*](/windows/win32/api/tspi/nc-tspi-async_completion) callback function.</span></span>

<span data-ttu-id="f9d4f-108">TAPI garantiza que los valores de **DRV \_ REQUESTID** que suministra son estrictamente positivos, es decir, entre los valores de 0x00000001 y 0x7FFFFFFF, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="f9d4f-108">TAPI ensures that the **DRV\_REQUESTID** values it supplies are strictly positive, that is, between the values of 0x00000001 and 0x7FFFFFFF, inclusive.</span></span> <span data-ttu-id="f9d4f-109">Además, los valores son únicos en que ningún valor devuelto por una función para marcar la solicitud como asincrónica se volverá a usar antes de que se notifique a la operación como completada.</span><span class="sxs-lookup"><span data-stu-id="f9d4f-109">Furthermore, the values are unique in that no value returned from a function to flag the request as asynchronous will be re-used before the operation is reported complete.</span></span>

 

 
