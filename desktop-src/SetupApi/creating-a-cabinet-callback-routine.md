---
description: Dado que la API de instalación no proporciona una rutina de devolución de llamada del archivo. cab predeterminada, debe proporcionar una rutina. La rutina de devolución de llamada que requiere la función SetupIterateCabinet debe tener la misma forma que la que señala FileCallback.
ms.assetid: 45a2690e-1db6-4a09-a141-9e68ebc2a6d8
title: Crear una rutina de devolución de llamada de archivador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f25d59515a6afdd68cef4458868fbfb62335aed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277142"
---
# <a name="creating-a-cabinet-callback-routine"></a><span data-ttu-id="a00e1-104">Crear una rutina de devolución de llamada de archivador</span><span class="sxs-lookup"><span data-stu-id="a00e1-104">Creating a Cabinet Callback Routine</span></span>

<span data-ttu-id="a00e1-105">Dado que la API de instalación no proporciona una rutina de devolución de llamada del archivo. cab predeterminada, debe proporcionar una rutina.</span><span class="sxs-lookup"><span data-stu-id="a00e1-105">Because the Setup API does not supply a default cabinet callback routine, you need to supply a routine.</span></span> <span data-ttu-id="a00e1-106">La rutina de devolución de llamada que requiere la función [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) debe tener la misma forma que la que señala [FileCallback](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span><span class="sxs-lookup"><span data-stu-id="a00e1-106">The callback routine that the [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) function requires must have the same form as those pointed to by [FileCallback](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span></span>

<span data-ttu-id="a00e1-107">A continuación se encuentra la sintaxis que usa [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) para enviar una notificación a la rutina de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="a00e1-107">Following is the syntax that [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) uses to send a notification to the callback routine.</span></span>

``` syntax
MsgHandler(          //the specified callback routine
    Context,         //context used by the callback routine
    Notification,    //cabinet notification
    Param1,          //additional notification information
    Param2           //additional notification information
);
```

<span data-ttu-id="a00e1-108">El parámetro de *contexto* es un puntero nulo a una estructura o variable de contexto que puede usar la rutina de devolución de llamada para almacenar información que debe persistir entre las llamadas subsiguientes a la rutina de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="a00e1-108">The *Context* parameter is a void pointer to a context variable or structure that can be used by the callback routine to store information that needs to persist between subsequent calls to the callback routine.</span></span>

<span data-ttu-id="a00e1-109">La implementación de este contexto se especifica mediante la rutina de devolución de llamada y nunca se hace referencia a él ni se modifica mediante [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span><span class="sxs-lookup"><span data-stu-id="a00e1-109">This context's implementation is specified by the callback routine, and it is never referenced or altered by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span></span>

<span data-ttu-id="a00e1-110">El parámetro de *notificación* es un entero sin signo y tendrá uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="a00e1-110">The *Notification* parameter is an unsigned integer and will be one of the following values.</span></span>



| <span data-ttu-id="a00e1-111">notificación</span><span class="sxs-lookup"><span data-stu-id="a00e1-111">Notification</span></span>                                                        | <span data-ttu-id="a00e1-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="a00e1-112">Description</span></span>                                        |
|---------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="a00e1-113">**SPFILENOTIFY \_ FILEEXTRACTED**</span><span class="sxs-lookup"><span data-stu-id="a00e1-113">**SPFILENOTIFY\_FILEEXTRACTED**</span></span>](spfilenotify-fileextracted.md)   | <span data-ttu-id="a00e1-114">El archivo se ha extraído del archivo. cab.</span><span class="sxs-lookup"><span data-stu-id="a00e1-114">The file has been extracted from the cabinet.</span></span>      |
| [<span data-ttu-id="a00e1-115">**SPFILENOTIFY \_ FILEINCABINET**</span><span class="sxs-lookup"><span data-stu-id="a00e1-115">**SPFILENOTIFY\_FILEINCABINET**</span></span>](spfilenotify-fileincabinet.md)   | <span data-ttu-id="a00e1-116">Se encuentra un archivo en el archivo. cab.</span><span class="sxs-lookup"><span data-stu-id="a00e1-116">A file is encountered in the cabinet.</span></span>              |
| [<span data-ttu-id="a00e1-117">**SPFILENOTIFY \_ NEEDNEWCABINET**</span><span class="sxs-lookup"><span data-stu-id="a00e1-117">**SPFILENOTIFY\_NEEDNEWCABINET**</span></span>](spfilenotify-neednewcabinet.md) | <span data-ttu-id="a00e1-118">El archivo actual continúa en el siguiente archivo. cab.</span><span class="sxs-lookup"><span data-stu-id="a00e1-118">The current file is continued in the next cabinet.</span></span> |



 

<span data-ttu-id="a00e1-119">Los dos parámetros finales, *Param1* y *Param2*, son también enteros sin signo y contienen información adicional relevante para la notificación.</span><span class="sxs-lookup"><span data-stu-id="a00e1-119">The final two parameters, *Param1* and *Param2*, are also unsigned integers and contain additional information relevant to the notification.</span></span> <span data-ttu-id="a00e1-120">Para obtener más información sobre las notificaciones enviadas por [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta), consulte [notificaciones de archivo. cab](cabinet-file-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="a00e1-120">For more information about the notifications sent by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta), see [Cabinet File Notifications](cabinet-file-notifications.md).</span></span>

<span data-ttu-id="a00e1-121">Una \_ rutina de devolución de llamada de notificación de archivo Sp \_ \_ devuelve un entero sin signo.</span><span class="sxs-lookup"><span data-stu-id="a00e1-121">A SP\_FILE\_NOTIFY\_CALLBACK routine returns an unsigned integer.</span></span> <span data-ttu-id="a00e1-122">La rutina de devolución de llamada del archivo. cab debe devolver uno de los valores siguientes en función de la notificación.</span><span class="sxs-lookup"><span data-stu-id="a00e1-122">The cabinet callback routine should return one of the following values depending on the notification.</span></span>

<span data-ttu-id="a00e1-123">En el caso de la notificación de FILEINCABINET de SPFILENOTIFY \_ , [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) espera que la rutina de devolución de llamada devuelva uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="a00e1-123">For the SPFILENOTIFY\_FILEINCABINET notification, [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) expects one of the following values to be returned by the callback routine.</span></span>



| <span data-ttu-id="a00e1-124">Value</span><span class="sxs-lookup"><span data-stu-id="a00e1-124">Value</span></span>         | <span data-ttu-id="a00e1-125">Significado</span><span class="sxs-lookup"><span data-stu-id="a00e1-125">Meaning</span></span>                   |
|---------------|---------------------------|
| <span data-ttu-id="a00e1-126">\_anulación de FILEOP</span><span class="sxs-lookup"><span data-stu-id="a00e1-126">FILEOP\_ABORT</span></span> | <span data-ttu-id="a00e1-127">Anular el procesamiento del archivo. cab.</span><span class="sxs-lookup"><span data-stu-id="a00e1-127">Abort cabinet processing.</span></span> |
| <span data-ttu-id="a00e1-128">FILEOP \_ Doit</span><span class="sxs-lookup"><span data-stu-id="a00e1-128">FILEOP\_DOIT</span></span>  | <span data-ttu-id="a00e1-129">Extraiga el archivo actual.</span><span class="sxs-lookup"><span data-stu-id="a00e1-129">Extract the current file.</span></span> |
| <span data-ttu-id="a00e1-130">FILEOP \_ SKIP</span><span class="sxs-lookup"><span data-stu-id="a00e1-130">FILEOP\_SKIP</span></span>  | <span data-ttu-id="a00e1-131">Omitir el archivo actual.</span><span class="sxs-lookup"><span data-stu-id="a00e1-131">Skip the current file.</span></span>    |



 

<span data-ttu-id="a00e1-132">En el caso de \_ las notificaciones de SPFILENOTIFY NEEDNEWCABINET y SPFILENOTIFY \_ FILEEXTRACTED, **SetupIterateCabinet** espera que la rutina de devolución de llamada devuelva uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="a00e1-132">For SPFILENOTIFY\_NEEDNEWCABINET and SPFILENOTIFY\_FILEEXTRACTED notifications, **SetupIterateCabinet** expects one of the following values to be returned by the callback routine.</span></span>



| <span data-ttu-id="a00e1-133">Value</span><span class="sxs-lookup"><span data-stu-id="a00e1-133">Value</span></span>      | <span data-ttu-id="a00e1-134">Significado</span><span class="sxs-lookup"><span data-stu-id="a00e1-134">Meaning</span></span>                                                                                                                                                                                                                           |
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a00e1-135">SIN \_ errores</span><span class="sxs-lookup"><span data-stu-id="a00e1-135">NO\_ERROR</span></span>  | <span data-ttu-id="a00e1-136">No se encontró ningún error y continúe procesando el archivo. cab.</span><span class="sxs-lookup"><span data-stu-id="a00e1-136">No error was encountered, continue processing the cabinet.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="a00e1-137">ERROR \_ XXX</span><span class="sxs-lookup"><span data-stu-id="a00e1-137">ERROR\_XXX</span></span> | <span data-ttu-id="a00e1-138">Se produjo un error del tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="a00e1-138">An error of the specified type occurred.</span></span> <span data-ttu-id="a00e1-139">La función [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) devolverá **false** y el código de error especificado será devuelto por una llamada a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="a00e1-139">The [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) function will return **FALSE**, and the specified error code will be returned by a call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span> |



 

<span data-ttu-id="a00e1-140">Si la rutina de devolución de llamada devuelve FILEOP \_ doit, la rutina también debe proporcionar una ruta de acceso de destino completa.</span><span class="sxs-lookup"><span data-stu-id="a00e1-140">If the callback routine returns FILEOP\_DOIT, the routine must also provide a full target path.</span></span> <span data-ttu-id="a00e1-141">Para obtener más información, vea [**SPFILENOTIFY \_ FILEINCABINET**](spfilenotify-fileincabinet.md).</span><span class="sxs-lookup"><span data-stu-id="a00e1-141">For more information see [**SPFILENOTIFY\_FILEINCABINET**](spfilenotify-fileincabinet.md).</span></span>

 

 
