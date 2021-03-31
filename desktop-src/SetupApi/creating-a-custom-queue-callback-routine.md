---
description: Además de usar la devolución de llamada de cola predeterminada, puede escribir una rutina de devolución de llamada personalizada.
ms.assetid: 68781565-71a2-43bf-ad01-7c1cdc514f7b
title: Crear una rutina de devolución de llamada de cola personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a119836e994709ff2d0fa21e12489af947394119
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911558"
---
# <a name="creating-a-custom-queue-callback-routine"></a><span data-ttu-id="786d2-103">Crear una rutina de devolución de llamada de cola personalizada</span><span class="sxs-lookup"><span data-stu-id="786d2-103">Creating a Custom Queue Callback Routine</span></span>

<span data-ttu-id="786d2-104">Además de usar la devolución de llamada de cola predeterminada, puede escribir una rutina de devolución de llamada personalizada.</span><span class="sxs-lookup"><span data-stu-id="786d2-104">In addition to using the default queue callback, you can write a custom callback routine.</span></span> <span data-ttu-id="786d2-105">Esta función debe tener el mismo formato que [*FileCallback*](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span><span class="sxs-lookup"><span data-stu-id="786d2-105">This function must have the same form as [*FileCallback*](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span></span> <span data-ttu-id="786d2-106">Esto resulta útil si necesita una rutina de devolución de llamada para controlar una notificación de una manera distinta de la que proporciona la rutina de devolución de llamada de cola predeterminada.</span><span class="sxs-lookup"><span data-stu-id="786d2-106">This is useful if you need a callback routine to handle a notification in a manner other than that provided by the default queue callback routine.</span></span>

<span data-ttu-id="786d2-107">Si solo es necesario cambiar una pequeña parte del comportamiento de la rutina de devolución de llamada de cola predeterminada, puede crear una rutina de devolución de llamada personalizada para filtrar las notificaciones, controlar solo aquellas que requieren un comportamiento especial y llamar a [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) para los demás.</span><span class="sxs-lookup"><span data-stu-id="786d2-107">If only a small portion of the default queue callback routine's behavior needs to be changed, you can create a custom callback routine to filter the notifications, handling only those that require special behavior and calling [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) for the others.</span></span>

<span data-ttu-id="786d2-108">Por ejemplo, si deseara personalizar el control de errores de eliminación de archivos, podría crear una función de devolución de llamada personalizada, *DoCallBack*.</span><span class="sxs-lookup"><span data-stu-id="786d2-108">For example, if you wanted to custom-handle file delete errors, you could create a custom callback function, *MyCallback*.</span></span> <span data-ttu-id="786d2-109">Esta función interceptará y procesará las notificaciones de [**SPFILENOTIFY \_ DELETEERROR**](spfilenotify-deleteerror.md) y llamará a la función de devolución de llamada de cola predeterminada para todas las demás notificaciones.</span><span class="sxs-lookup"><span data-stu-id="786d2-109">This function would intercept and process [**SPFILENOTIFY\_DELETEERROR**](spfilenotify-deleteerror.md) notifications, and call the default queue callback function for all other notifications.</span></span> <span data-ttu-id="786d2-110">*DoCallBack* devuelve un valor para las notificaciones de error de eliminación.</span><span class="sxs-lookup"><span data-stu-id="786d2-110">*MyCallback* returns a value for the delete error notifications.</span></span> <span data-ttu-id="786d2-111">Para todas las demás notificaciones, la *devolución de llamada* pasa cualquier valor que la rutina de devolución de llamada de cola predeterminada devuelva a la cola.</span><span class="sxs-lookup"><span data-stu-id="786d2-111">For all other notifications, *MyCallback* passes whatever value the default queue callback routine returned to the queue.</span></span>

<span data-ttu-id="786d2-112">Este flujo de control se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="786d2-112">This flow of control is illustrated in the following diagram.</span></span>

![flechas y cuadros que muestran el flujo de datos para la función de devolución de llamada personalizada](images/callback.png)

> [!IMPORTANT]
> <span data-ttu-id="786d2-114">Si la función de devolución de llamada personalizada llama a la rutina de devolución de llamada de cola predeterminada, debe pasar el puntero void devuelto por [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) o [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) a la rutina de devolución de llamada predeterminada.</span><span class="sxs-lookup"><span data-stu-id="786d2-114">If the custom callback function calls the default queue callback routine, it must pass the void pointer returned by [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) or [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) to the default callback routine.</span></span>

 

 

 
