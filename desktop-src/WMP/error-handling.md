---
title: Control de errores (SDK de Windows Media Player)
description: Tratamiento de errores
ms.assetid: f0567c77-a855-4b93-9fb7-a36cde63859f
keywords:
- Windows Media Player, control de errores
- Modelo de objetos de Windows Media Player, control de errores
- modelo de objetos, control de errores
- Control ActiveX de Windows Media Player, control de errores
- Control ActiveX, control de errores
- Control ActiveX de Windows Media Player Mobile, control de errores
- Windows Media Player Mobile, control de errores
- Guía de migración, control de errores
- control de errores en el modelo de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f3b96e04d24009ee4b7e5819fdb26dfd6effd63
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104149766"
---
# <a name="error-handling-windows-media-player-sdk"></a><span data-ttu-id="5e2ee-112">Control de errores (SDK de Windows Media Player)</span><span class="sxs-lookup"><span data-stu-id="5e2ee-112">Error Handling (Windows Media Player SDK)</span></span>

<span data-ttu-id="5e2ee-113">El control ActiveX de Windows Media Player 6,4 proporciona un control de errores predeterminado al mostrar los mensajes de error en los cuadros de diálogo y en la barra de estado.</span><span class="sxs-lookup"><span data-stu-id="5e2ee-113">The Windows Media Player 6.4 ActiveX control provides default error handling by displaying error messages in dialog boxes and on the status bar.</span></span> <span data-ttu-id="5e2ee-114">También puede proporcionar un control de errores personalizado mediante el procesamiento de errores en el script.</span><span class="sxs-lookup"><span data-stu-id="5e2ee-114">You can also provide custom error handling by processing errors in your script.</span></span> <span data-ttu-id="5e2ee-115">El control de errores se basa en eventos, lo que significa que recibe una notificación para cada error y debe decidir cómo tratar cada evento de error cuando se produce.</span><span class="sxs-lookup"><span data-stu-id="5e2ee-115">Error handling is event driven, which means you receive a notification for each error, and must decide how to deal with each error event when it occurs.</span></span> <span data-ttu-id="5e2ee-116">Para obtener más información sobre el control de errores con el modelo de objetos de la versión 6,4, consulte la sección control de errores de la guía del modelo de objetos del reproductor de la versión 6,4, que forma parte del SDK de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="5e2ee-116">For more information about handling errors using the version 6.4 object model, see the Error Handling section of the Version 6.4 Player Object Model Guide, which is part of the Windows Media Player SDK.</span></span>

<span data-ttu-id="5e2ee-117">El modelo de objetos de Windows Media Player 7 o posterior proporciona el objeto de **error** y el objeto **ErrorItem** para controlar los errores.</span><span class="sxs-lookup"><span data-stu-id="5e2ee-117">The Windows Media Player 7 or later object model provides the **Error** object and the **ErrorItem** object to handle errors.</span></span> <span data-ttu-id="5e2ee-118">Estos dos objetos funcionan juntos para proporcionar un mecanismo de control de errores que le proporciona un control completo y flexible del proceso de control de errores.</span><span class="sxs-lookup"><span data-stu-id="5e2ee-118">These two objects work together to provide you with an error handling mechanism that gives you complete and flexible control of the error handling process.</span></span> <span data-ttu-id="5e2ee-119">El objeto **error** proporciona acceso a una colección de objetos **ErrorItem** ; cada objeto **ErrorItem** proporciona detalles sobre un mensaje de error individual.</span><span class="sxs-lookup"><span data-stu-id="5e2ee-119">The **Error** object provides access to a collection of **ErrorItem** objects; each **ErrorItem** object provides details about an individual error message.</span></span>

<span data-ttu-id="5e2ee-120">Cuando se produce un error, la información de error se envía a una cola de errores.</span><span class="sxs-lookup"><span data-stu-id="5e2ee-120">When an error occurs, the error information is posted to an error queue.</span></span> <span data-ttu-id="5e2ee-121">La cola es una colección de objetos **ErrorItem** .</span><span class="sxs-lookup"><span data-stu-id="5e2ee-121">The queue is a collection of **ErrorItem** objects.</span></span> <span data-ttu-id="5e2ee-122">A medida que se agrega cada error a la cola, se asocia a un número de índice (a partir de cero) que se puede utilizar para identificar el objeto **ErrorItem** determinado.</span><span class="sxs-lookup"><span data-stu-id="5e2ee-122">As each error is added to the queue, it is associated with an index number (beginning with zero) that can be used to identify the particular **ErrorItem** object.</span></span> <span data-ttu-id="5e2ee-123">El *error*. la propiedad **errorCount** recupera el número de errores en la cola de errores.</span><span class="sxs-lookup"><span data-stu-id="5e2ee-123">The *Error*.**errorCount** property retrieves the number of errors in the error queue.</span></span> <span data-ttu-id="5e2ee-124">Dado que los números de índice son de base cero, el error más reciente expuesto en la cola siempre tendrá un valor de índice igual a *error*. **errorCount** menos uno.</span><span class="sxs-lookup"><span data-stu-id="5e2ee-124">Since the index numbers are zero-based, the most recent error posted to the queue will always have an index value equal to *Error*.**errorCount** minus one.</span></span>

<span data-ttu-id="5e2ee-125">Puede crear un controlador de eventos de error para Windows Media Player mediante un script.</span><span class="sxs-lookup"><span data-stu-id="5e2ee-125">You can create an error event handler for Windows Media Player using script.</span></span> <span data-ttu-id="5e2ee-126">En el siguiente ejemplo de JScript se muestra cómo recuperar el elemento de error más reciente de la cola de errores y mostrar el código de error y la descripción del error mediante el modelo de objetos de Windows Media Player 7 o posterior.</span><span class="sxs-lookup"><span data-stu-id="5e2ee-126">The following JScript example shows how to retrieve the most recent error item from the error queue and display the error code and error description using the Windows Media Player 7 or later object model.</span></span> <span data-ttu-id="5e2ee-127">El objeto **Player** se creó con ID = "WMP9".</span><span class="sxs-lookup"><span data-stu-id="5e2ee-127">The **Player** object was created with ID = "WMP9".</span></span>


```C++
<!-- Create an error event handler for Windows Media Player 7 or later errors. -->
<SCRIPT  LANGUAGE = "JScript"  FOR = WMP9  EVENT = error()>

// Store the number of errors in the error queue.
var max = WMP9.error.errorCount;

// Retrieve most recent ErrorItem object.
var err = WMP9.error.item(max-1)

// Store the error code number.
var errNum = err.errorCode;

// Store the error description string.
var errDesc = err.errorDescription;

// Build a message string to notify the user.
var msg = "Error number: " + errNum + "\n";
msg += "Error description: " + errDesc;

// Display the message box.
alert(msg);

</SCRIPT>

```



<span data-ttu-id="5e2ee-128">El objeto de **error** tiene dos métodos adicionales que puede usar.</span><span class="sxs-lookup"><span data-stu-id="5e2ee-128">The **Error** object has two additional methods that you can use.</span></span> <span data-ttu-id="5e2ee-129">El *error*. el método **clearErrorQueue** permite quitar todos los errores de la cola de errores y restablecer el número de índice en cero.</span><span class="sxs-lookup"><span data-stu-id="5e2ee-129">The *Error*.**clearErrorQueue** method allows you to remove all the errors from the error queue and reset the index number to zero.</span></span> <span data-ttu-id="5e2ee-130">Tiene un control total sobre este proceso; puede mantener los errores en la cola mientras necesite que estén disponibles y, a continuación, vaciar la cola cuando haya terminado de controlar los errores.</span><span class="sxs-lookup"><span data-stu-id="5e2ee-130">You have complete control over this process; you can keep errors in the queue for as long as you need them to be available, and then empty the queue when you're finished handling the errors.</span></span>

<span data-ttu-id="5e2ee-131">El *error*. **WebHelp** Method proporciona una manera de mostrar la información de error más reciente al usuario mediante Internet.</span><span class="sxs-lookup"><span data-stu-id="5e2ee-131">The *Error*.**webHelp** method provides a way to display the most current error information to the user by using the Internet.</span></span> <span data-ttu-id="5e2ee-132">Cuando se llama, este método transfiere toda la información relevante sobre el primer error de la cola (el que tiene el índice cero) a la ayuda Web de Microsoft Windows Media Player, que muestra más información sobre el error en la ventana del explorador actual.</span><span class="sxs-lookup"><span data-stu-id="5e2ee-132">When called, this method transfers all relevant information about the first error in the queue (the one with index zero) to Microsoft Windows Media Player Web Help, which displays further information about the error in the current browser window.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5e2ee-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5e2ee-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e2ee-134">**Objeto de error**</span><span class="sxs-lookup"><span data-stu-id="5e2ee-134">**Error Object**</span></span>](error-object.md)
</dt> <dt>

[<span data-ttu-id="5e2ee-135">**Objeto ErrorItem**</span><span class="sxs-lookup"><span data-stu-id="5e2ee-135">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> <dt>

[<span data-ttu-id="5e2ee-136">**Guía de migración del modelo de objetos**</span><span class="sxs-lookup"><span data-stu-id="5e2ee-136">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> </dl>

 

 




