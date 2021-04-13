---
title: Usar Intercambio dinámico de datos
description: En este tema se proporcionan ejemplos de código relacionados con el intercambio dinámico de datos.
ms.assetid: 6d94403b-64b4-4763-868a-3b94431dab79
keywords:
- Intercambio dinámico de datos (DDE), conversaciones
- DDE (Intercambio dinámico de datos), conversaciones
- intercambio de datos, Intercambio dinámico de datos (DDE)
- Intercambio dinámico de datos (DDE), ejemplos
- DDE (Intercambio dinámico de datos), ejemplos
- Intercambio dinámico de datos (DDE), comandos de aplicaciones de servidor
- DDE (Intercambio dinámico de datos), comandos en aplicaciones de servidor
- Intercambio dinámico de datos (DDE), vínculos de datos
- DDE (Intercambio dinámico de datos), vínculos de datos
- Intercambio dinámico de datos (DDE), elementos
- DDE (Intercambio dinámico de datos), elementos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fe20c4dedc38303fe9bcb9c4b0fae42d03ee536
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359083"
---
# <a name="using-dynamic-data-exchange"></a><span data-ttu-id="70ff2-114">Usar Intercambio dinámico de datos</span><span class="sxs-lookup"><span data-stu-id="70ff2-114">Using Dynamic Data Exchange</span></span>

<span data-ttu-id="70ff2-115">Esta sección contiene ejemplos de código sobre las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="70ff2-115">This section has code samples on the following tasks:</span></span>

-   [<span data-ttu-id="70ff2-116">Iniciar una conversación</span><span class="sxs-lookup"><span data-stu-id="70ff2-116">Initiating a Conversation</span></span>](#initiating-a-conversation)
-   [<span data-ttu-id="70ff2-117">Transferir un solo elemento</span><span class="sxs-lookup"><span data-stu-id="70ff2-117">Transferring a Single Item</span></span>](#transferring-a-single-item)
    -   [<span data-ttu-id="70ff2-118">Recuperación de un elemento del servidor</span><span class="sxs-lookup"><span data-stu-id="70ff2-118">Retrieving an Item from the Server</span></span>](#retrieving-an-item-from-the-server)
    -   [<span data-ttu-id="70ff2-119">Envío de un elemento al servidor</span><span class="sxs-lookup"><span data-stu-id="70ff2-119">Submitting an Item to the Server</span></span>](#submitting-an-item-to-the-server)
-   [<span data-ttu-id="70ff2-120">Establecer un vínculo de datos permanente</span><span class="sxs-lookup"><span data-stu-id="70ff2-120">Establishing a Permanent Data Link</span></span>](#establishing-a-permanent-data-link)
    -   [<span data-ttu-id="70ff2-121">Iniciar un vínculo de datos</span><span class="sxs-lookup"><span data-stu-id="70ff2-121">Initiating a Data Link</span></span>](#initiating-a-data-link)
    -   [<span data-ttu-id="70ff2-122">Iniciar un vínculo de datos con el comando pegar vínculo</span><span class="sxs-lookup"><span data-stu-id="70ff2-122">Initiating a Data Link with the Paste Link Command</span></span>](#initiating-a-data-link-with-the-paste-link-command)
    -   [<span data-ttu-id="70ff2-123">Notificación al cliente de que los datos han cambiado</span><span class="sxs-lookup"><span data-stu-id="70ff2-123">Notifying the Client that Data Has Changed</span></span>](#notifying-the-client-that-data-has-changed)
    -   [<span data-ttu-id="70ff2-124">Finalización de un vínculo de datos</span><span class="sxs-lookup"><span data-stu-id="70ff2-124">Terminating a Data Link</span></span>](#terminating-a-data-link)
-   [<span data-ttu-id="70ff2-125">Ejecutar comandos en una aplicación de servidor</span><span class="sxs-lookup"><span data-stu-id="70ff2-125">Carrying Out Commands in a Server Application</span></span>](#carrying-out-commands-in-a-server-application)
-   [<span data-ttu-id="70ff2-126">Finalizar una conversación</span><span class="sxs-lookup"><span data-stu-id="70ff2-126">Terminating a Conversation</span></span>](#terminating-a-conversation)

## <a name="initiating-a-conversation"></a><span data-ttu-id="70ff2-127">Iniciar una conversación</span><span class="sxs-lookup"><span data-stu-id="70ff2-127">Initiating a Conversation</span></span>

<span data-ttu-id="70ff2-128">Para iniciar una conversación Intercambio dinámico de datos (DDE), el cliente envía un mensaje de [**\_ \_ Inicio de WM DDE**](wm-dde-initiate.md) .</span><span class="sxs-lookup"><span data-stu-id="70ff2-128">To initiate a Dynamic Data Exchange (DDE) conversation, the client sends a [**WM\_DDE\_INITIATE**](wm-dde-initiate.md) message.</span></span> <span data-ttu-id="70ff2-129">Normalmente, el cliente difunde este mensaje mediante una llamada a [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage), con – 1 como primer parámetro.</span><span class="sxs-lookup"><span data-stu-id="70ff2-129">Usually, the client broadcasts this message by calling [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage), with –1 as the first parameter.</span></span> <span data-ttu-id="70ff2-130">Si la aplicación ya tiene el identificador de ventana de la aplicación de servidor, puede enviar el mensaje directamente a esa ventana.</span><span class="sxs-lookup"><span data-stu-id="70ff2-130">If the application already has the window handle to the server application, it can send the message directly to that window.</span></span> <span data-ttu-id="70ff2-131">El cliente prepara los átomos para el nombre de la aplicación y el nombre del tema mediante una llamada a [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma).</span><span class="sxs-lookup"><span data-stu-id="70ff2-131">The client prepares atoms for the application name and topic name by calling [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma).</span></span> <span data-ttu-id="70ff2-132">El cliente puede solicitar conversaciones con cualquier posible aplicación de servidor y para cualquier tema potencial proporcionando átomos **null** (comodín) para la aplicación y el tema.</span><span class="sxs-lookup"><span data-stu-id="70ff2-132">The client can request conversations with any potential server application and for any potential topic by supplying **NULL** (wildcard) atoms for the application and topic.</span></span>

<span data-ttu-id="70ff2-133">En el ejemplo siguiente se muestra cómo el cliente inicia una conversación, donde se especifican tanto la aplicación como el tema.</span><span class="sxs-lookup"><span data-stu-id="70ff2-133">The following example illustrates how the client initiates a conversation, where both the application and topic are specified.</span></span>


```
    static BOOL fInInitiate = FALSE; 
    char *szApplication; 
    char *szTopic; 
    atomApplication = *szApplication == 0 ? 
    NULL     : GlobalAddAtom((LPSTR) szApplication); 
    atomTopic = *szTopic == 0 ? 
    NULL     : GlobalAddAtom((LPSTR) szTopic); 
 
    fInInitiate = TRUE; 
    SendMessage((HWND) HWND_BROADCAST, // broadcasts message 
        WM_DDE_INITIATE,               // initiates conversation 
        (WPARAM) hwndClientDDE,        // handle to client DDE window 
        MAKELONG(atomApplication,      // application-name atom 
            atomTopic));               // topic-name atom 
    fInInitiate = FALSE; 
    if (atomApplication != NULL) 
        GlobalDeleteAtom(atomApplication); 
    if (atomTopic != NULL) 
        GlobalDeleteAtom(atomTopic);
```



> [!Note]  
> <span data-ttu-id="70ff2-134">Si la aplicación usa átomos **null** , no es necesario usar las funciones [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) y [**GlobalDeleteAtom**](/windows/desktop/api/Winbase/nf-winbase-globaldeleteatom) .</span><span class="sxs-lookup"><span data-stu-id="70ff2-134">If your application uses **NULL** atoms, you need not use the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) and [**GlobalDeleteAtom**](/windows/desktop/api/Winbase/nf-winbase-globaldeleteatom) functions.</span></span> <span data-ttu-id="70ff2-135">En este ejemplo, la aplicación cliente crea dos átomos globales que contienen el nombre del servidor y el nombre del tema, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="70ff2-135">In this example, the client application creates two global atoms containing the name of the server and the name of the topic, respectively.</span></span>

 

<span data-ttu-id="70ff2-136">La aplicación cliente envía un mensaje de [**\_ \_ Inicio de WM DDE**](wm-dde-initiate.md) con estos dos átomos en el parámetro *lParam* del mensaje.</span><span class="sxs-lookup"><span data-stu-id="70ff2-136">The client application sends a [**WM\_DDE\_INITIATE**](wm-dde-initiate.md) message with these two atoms in the *lParam* parameter of the message.</span></span> <span data-ttu-id="70ff2-137">En la llamada a la función [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) , el identificador de ventana especial – 1 indica al sistema que envíe este mensaje a todas las demás aplicaciones activas.</span><span class="sxs-lookup"><span data-stu-id="70ff2-137">In the call to the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function, the special window handle –1 directs the system to send this message to all other active applications.</span></span> <span data-ttu-id="70ff2-138">**SendMessage** no vuelve a la aplicación cliente hasta que todas las aplicaciones que reciben el mensaje, a su vez, devuelven el control al sistema.</span><span class="sxs-lookup"><span data-stu-id="70ff2-138">**SendMessage** does not return to the client application until all applications that receive the message have, in turn, returned control to the system.</span></span> <span data-ttu-id="70ff2-139">Esto significa que se garantiza que el cliente ha procesado todos los mensajes de [**\_ \_ confirmación DDE de WM**](wm-dde-ack.md) enviados en respuesta por las aplicaciones del servidor en el momento en que se devuelve la llamada **SendMessage** .</span><span class="sxs-lookup"><span data-stu-id="70ff2-139">This means that all [**WM\_DDE\_ACK**](wm-dde-ack.md) messages sent in reply by the server applications are guaranteed to have been processed by the client by the time the **SendMessage** call has returned.</span></span>

<span data-ttu-id="70ff2-140">Una vez que [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) devuelve, la aplicación cliente elimina los átomos globales.</span><span class="sxs-lookup"><span data-stu-id="70ff2-140">After [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) returns, the client application deletes the global atoms.</span></span>

<span data-ttu-id="70ff2-141">Las aplicaciones de servidor responden según la lógica que se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="70ff2-141">Server applications respond according to the logic illustrated in the following diagram.</span></span>

![lógica de respuesta de la aplicación de servidor](images/csdde-01.png)

<span data-ttu-id="70ff2-143">Para confirmar uno o más temas, el servidor debe crear átomos para cada conversación (requiere átomos de nombre de aplicación duplicados si hay varios temas) y enviar un mensaje de [**\_ \_ confirmación de WM DDE**](wm-dde-ack.md) para cada conversación, como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="70ff2-143">To acknowledge one or more topics, the server must create atoms for each conversation (requiring duplicate application-name atoms if there are multiple topics) and send a [**WM\_DDE\_ACK**](wm-dde-ack.md) message for each conversation, as illustrated in the following example.</span></span>


```
if ((atomApplication = GlobalAddAtom("Server")) != 0) 
{ 
    if ((atomTopic = GlobalAddAtom(szTopic)) != 0) 
    { 
        SendMessage(hwndClientDDE, 
            WM_DDE_ACK, 
            (WPARAM) hwndServerDDE, 
            MAKELONG(atomApplication, atomTopic)); 
        GlobalDeleteAtom(atomApplication); 
    } 
 
    GlobalDeleteAtom(atomTopic); 
} 
 
if ((atomApplication == 0) || (atomTopic == 0)) 
{ 
    // Handle errors. 
}
```



<span data-ttu-id="70ff2-144">Cuando un servidor responde con un mensaje [**de \_ \_ confirmación DDE de WM**](wm-dde-ack.md) , la aplicación cliente debe guardar un identificador en la ventana del servidor.</span><span class="sxs-lookup"><span data-stu-id="70ff2-144">When a server responds with a [**WM\_DDE\_ACK**](wm-dde-ack.md) message, the client application should save a handle to the server window.</span></span> <span data-ttu-id="70ff2-145">El cliente que recibe el identificador como el parámetro *wParam* del mensaje de **confirmación de \_ DDE \_ de WM** envía entonces todos los mensajes DDE subsiguientes a la ventana del servidor que identifica.</span><span class="sxs-lookup"><span data-stu-id="70ff2-145">The client receiving the handle as the *wParam* parameter of the **WM\_DDE\_ACK** message then sends all subsequent DDE messages to the server window this handle identifies.</span></span>

<span data-ttu-id="70ff2-146">Si la aplicación cliente usa un átomo **nulo** para el nombre de la aplicación o el nombre del tema, se espera que la aplicación reciba confirmaciones de más de una aplicación de servidor.</span><span class="sxs-lookup"><span data-stu-id="70ff2-146">If your client application uses a **NULL** atom for the application name or topic name, expect the application to receive acknowledgments from more than one server application.</span></span> <span data-ttu-id="70ff2-147">Varias confirmaciones también pueden provienen de varias instancias de un servidor DDE, incluso si la aplicación cliente no **es null** usar átomos.</span><span class="sxs-lookup"><span data-stu-id="70ff2-147">Multiple acknowledgements can also come from multiple instances of a DDE server, even if your client application does not **NULL** use atoms.</span></span> <span data-ttu-id="70ff2-148">Un servidor siempre debe usar una ventana única para cada conversación.</span><span class="sxs-lookup"><span data-stu-id="70ff2-148">A server should always use a unique window for each conversation.</span></span> <span data-ttu-id="70ff2-149">El procedimiento de ventana de la aplicación cliente puede usar un identificador de la ventana del servidor (que se proporciona como el parámetro *lParam* de [**WM \_ DDE \_ INITIATE**](wm-dde-initiate.md)) para realizar el seguimiento de varias conversaciones.</span><span class="sxs-lookup"><span data-stu-id="70ff2-149">The window procedure in the client application can use a handle to the server window (provided as the *lParam* parameter of [**WM\_DDE\_INITIATE**](wm-dde-initiate.md)) to track multiple conversations.</span></span> <span data-ttu-id="70ff2-150">Esto permite que una sola ventana de cliente procese varias conversaciones sin necesidad de finalizar y volver a conectar con una nueva ventana de cliente para cada conversación.</span><span class="sxs-lookup"><span data-stu-id="70ff2-150">This allows a single client window to process several conversations without needing to terminate and reconnect with a new client window for each conversation.</span></span>

## <a name="transferring-a-single-item"></a><span data-ttu-id="70ff2-151">Transferir un solo elemento</span><span class="sxs-lookup"><span data-stu-id="70ff2-151">Transferring a Single Item</span></span>

<span data-ttu-id="70ff2-152">Una vez establecida una conversación DDE, el cliente puede recuperar el valor de un elemento de datos del servidor emitiendo el mensaje de solicitud de [**WM \_ DDE \_**](wm-dde-request.md) o enviar un valor de elemento de datos al servidor emitiendo [**WM \_ DDE \_**](wm-dde-poke.md).</span><span class="sxs-lookup"><span data-stu-id="70ff2-152">Once a DDE conversation has been established, the client can either retrieve the value of a data item from the server by issuing the [**WM\_DDE\_REQUEST**](wm-dde-request.md) message, or submit a data-item value to the server by issuing [**WM\_DDE\_POKE**](wm-dde-poke.md).</span></span>

-   [<span data-ttu-id="70ff2-153">Recuperación de un elemento del servidor</span><span class="sxs-lookup"><span data-stu-id="70ff2-153">Retrieving an Item from the Server</span></span>](#retrieving-an-item-from-the-server)
-   [<span data-ttu-id="70ff2-154">Envío de un elemento al servidor</span><span class="sxs-lookup"><span data-stu-id="70ff2-154">Submitting an Item to the Server</span></span>](#submitting-an-item-to-the-server)

### <a name="retrieving-an-item-from-the-server"></a><span data-ttu-id="70ff2-155">Recuperación de un elemento del servidor</span><span class="sxs-lookup"><span data-stu-id="70ff2-155">Retrieving an Item from the Server</span></span>

<span data-ttu-id="70ff2-156">Para recuperar un elemento del servidor, el cliente envía al servidor un mensaje [**de \_ \_ solicitud de DDE de WM**](wm-dde-request.md) que especifica el elemento y el formato que se va a recuperar, tal como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="70ff2-156">To retrieve an item from the server, the client sends the server a [**WM\_DDE\_REQUEST**](wm-dde-request.md) message specifying the item and format to retrieve, as shown in the following example.</span></span>


```
if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
{ 
    if (!PostMessage(hwndServerDDE, 
            WM_DDE_REQUEST, 
            (WPARAM) hwndClientDDE, 
            PackDDElParam(WM_DDE_REQUEST, CF_TEXT, atomItem))) 
    {
        GlobalDeleteAtom(atomItem); 
    }
} 
 
if (atomItem == 0) 
{ 
    // Handle errors. 
}
```



<span data-ttu-id="70ff2-157">En este ejemplo, el cliente especifica el formato del portapapeles para el **\_ texto CF** como el formato preferido para el elemento de datos solicitado.</span><span class="sxs-lookup"><span data-stu-id="70ff2-157">In this example, the client specifies the clipboard format **CF\_TEXT** as the preferred format for the requested data item.</span></span>

<span data-ttu-id="70ff2-158">El receptor (servidor) del mensaje [**de \_ \_ solicitud de DDE de WM**](wm-dde-request.md) normalmente debe eliminar el elemento Atom, pero si se produce un error en la llamada [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) , el cliente debe eliminar el átomo.</span><span class="sxs-lookup"><span data-stu-id="70ff2-158">The receiver (server) of the [**WM\_DDE\_REQUEST**](wm-dde-request.md) message typically must delete the item atom, but if the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) call fails, the client must delete the atom.</span></span>

<span data-ttu-id="70ff2-159">Si el servidor tiene acceso al elemento solicitado y puede representarlo en el formato solicitado, el servidor copia el valor del elemento como un objeto de memoria compartida y envía al cliente un mensaje de [**\_ \_ datos de WM DDE**](wm-dde-data.md) , tal como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="70ff2-159">If the server has access to the requested item and can render it in the requested format, the server copies the item value as a shared memory object and sends the client a [**WM\_DDE\_DATA**](wm-dde-data.md) message, as illustrated in the following example.</span></span>


```
// Allocate the size of the DDE data header, plus the data: a 
// string,<CR><LF><NULL>. The byte for the string's terminating 
// null character is counted by DDEDATA.Value[1].

size_t* pcch;
HRESULT hResult;
 
hResult = StringCchLength(szItemValue,STRSAFE_MAX_CCH, pcch);
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
if (!(hData = GlobalAlloc(GMEM_MOVEABLE,
  (LONG) sizeof(DDEDATA) + *pcch + 2)))  
{
    return; 
}
 
if (!(lpData = (DDEDATA FAR*) GlobalLock(hData)))  
{
    GlobalFree(hData); 
    return; 
} 
 
lpData->cfFormat = CF_TEXT;
hResult = StringCchCopy((LPSTR) lpData->Value, *pcch +1, (LPCSTR) szItemValue); // copies value to be sent
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
 
// Each line of CF_TEXT data is terminated by CR/LF. 
hResult = StringCchCat((LPSTR) lpData->Value, *pcch + 3, (LPCSTR) "\r\n");
if (FAILED(hResult)
{
// TODO: Write error handler.
 return;
} 
GlobalUnlock(hData); 
if ((atomItem = GlobalAddAtom((LPSTR) szItemName)) != 0) 
{ 
    lParam = PackDDElParam(WM_DDE_ACK, (UINT) hData, atomItem); 
    if (!PostMessage(hwndClientDDE, 
            WM_DDE_DATA, 
            (WPARAM) hwndServerDDE, 
            lParam)) 
    { 
        GlobalFree(hData); 
        GlobalDeleteAtom(atomItem); 
        FreeDDElParam(WM_DDE_ACK, lParam); 
    } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors.  
}
```



<span data-ttu-id="70ff2-160">En este ejemplo, la aplicación de servidor asigna un objeto de memoria para que contenga el elemento de datos.</span><span class="sxs-lookup"><span data-stu-id="70ff2-160">In this example, the server application allocates a memory object to contain the data item.</span></span> <span data-ttu-id="70ff2-161">El objeto de datos se inicializa como una estructura [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) .</span><span class="sxs-lookup"><span data-stu-id="70ff2-161">The data object is initialized as a [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure.</span></span>

<span data-ttu-id="70ff2-162">A continuación, la aplicación de servidor establece el miembro **cfFormat** de la estructura en el \_ texto CF para informar a la aplicación cliente de que los datos están en formato de texto.</span><span class="sxs-lookup"><span data-stu-id="70ff2-162">The server application then sets the **cfFormat** member of the structure to CF\_TEXT to inform the client application that the data is in text format.</span></span> <span data-ttu-id="70ff2-163">El cliente responde copiando el valor de los datos solicitados en el miembro de **valor** de la estructura [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) .</span><span class="sxs-lookup"><span data-stu-id="70ff2-163">The client responds by copying the value of the requested data into the **Value** member of the [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure.</span></span> <span data-ttu-id="70ff2-164">Una vez que el servidor ha rellenado el objeto de datos, el servidor Desbloquea los datos y crea un átomo global que contiene el nombre del elemento de datos.</span><span class="sxs-lookup"><span data-stu-id="70ff2-164">After the server has filled the data object, the server unlocks the data and creates a global atom containing the name of the data item.</span></span>

<span data-ttu-id="70ff2-165">Por último, el servidor emite el mensaje de [**\_ \_ datos DDE de WM**](wm-dde-data.md) llamando a [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea).</span><span class="sxs-lookup"><span data-stu-id="70ff2-165">Finally, the server issues the [**WM\_DDE\_DATA**](wm-dde-data.md) message by calling [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea).</span></span> <span data-ttu-id="70ff2-166">El identificador del objeto de datos y el átomo que contiene el nombre del elemento se empaquetan en el parámetro *lParam* del mensaje mediante la función [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) .</span><span class="sxs-lookup"><span data-stu-id="70ff2-166">The handle to the data object and the atom containing the item name are packed into the *lParam* parameter of the message by the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function.</span></span>

<span data-ttu-id="70ff2-167">Si se produce un error en [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) , el servidor debe utilizar la función [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) para liberar el parámetro *lParam* empaquetado.</span><span class="sxs-lookup"><span data-stu-id="70ff2-167">If [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) fails, the server must use the [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) function to free the packed *lParam* parameter.</span></span> <span data-ttu-id="70ff2-168">El servidor también debe liberar el parámetro *lParam* empaquetado para el mensaje de [**\_ \_ solicitud de DDE de WM**](wm-dde-request.md) que recibió.</span><span class="sxs-lookup"><span data-stu-id="70ff2-168">The server must also free the packed *lParam* parameter for the [**WM\_DDE\_REQUEST**](wm-dde-request.md) message it received.</span></span>

<span data-ttu-id="70ff2-169">Si el servidor no puede satisfacer la solicitud, envía un mensaje [**de \_ \_ confirmación DDE de WM**](wm-dde-ack.md) negativo al cliente, tal y como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="70ff2-169">If the server cannot satisfy the request, it sends a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message to the client, as shown in the following example.</span></span>


```
// Negative acknowledgment. 
 
PostMessage(hwndClientDDE, 
    WM_DDE_ACK, 
    (WPARAM) hwndServerDDE, 
    PackDDElParam(WM_DDE_ACK, 0, atomItem));
```



<span data-ttu-id="70ff2-170">Al recibir un mensaje de [**\_ \_ datos DDE de WM**](wm-dde-data.md) , el cliente procesa el valor del elemento de datos según corresponda.</span><span class="sxs-lookup"><span data-stu-id="70ff2-170">Upon receiving a [**WM\_DDE\_DATA**](wm-dde-data.md) message, the client processes the data-item value as appropriate.</span></span> <span data-ttu-id="70ff2-171">Después, si el miembro de **fAckReq** al que se apunta en el mensaje de **\_ \_ datos DDE de WM** es 1, el cliente debe enviar al servidor un mensaje de [**\_ \_ confirmación de DDE de WM**](wm-dde-ack.md) positivo, como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="70ff2-171">Then, if the **fAckReq** member pointed to in the **WM\_DDE\_DATA** message is 1, the client must send the server a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message, as shown in the following example.</span></span>


```
UnpackDDElParam(WM_DDE_DATA, lParam, (PUINT) &hData, 
    (PUINT) &atomItem); 
if (!(lpDDEData = (DDEDATA FAR*) GlobalLock(hData)) 
        || (lpDDEData->cfFormat != CF_TEXT)) 
{ 
    PostMessage(hwndServerDDE, 
        WM_DDE_ACK, 
        (WPARAM) hwndClientDDE, 
        PackDDElParam(WM_DDE_ACK, 0, atomItem)); // Negative ACK. 
} 
 
// Copy data from lpDDEData here. 
 
if (lpDDEData->fAckReq) 
{ 
    PostMessage(hwndServerDDE, 
        WM_DDE_ACK, 
        (WPARAM) hwndClientDDE, 
        PackDDElParam(WM_DDE_ACK, 0x8000, 
            atomItem)); // Positive ACK 
} 
 
bRelease = lpDDEData->fRelease; 
GlobalUnlock(hData); 
if (bRelease) 
    GlobalFree(hData);
```



<span data-ttu-id="70ff2-172">En este ejemplo, el cliente examina el formato de los datos.</span><span class="sxs-lookup"><span data-stu-id="70ff2-172">In this example, the client examines the format of the data.</span></span> <span data-ttu-id="70ff2-173">Si el formato no es **el \_ texto CF** (o si el cliente no puede bloquear la memoria de los datos), el cliente envía un mensaje de [**\_ \_ confirmación DDE de WM**](wm-dde-ack.md) negativo para indicar que no puede procesar los datos.</span><span class="sxs-lookup"><span data-stu-id="70ff2-173">If the format is not **CF\_TEXT** (or if the client cannot lock the memory for the data), the client sends a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message to indicate that it cannot process the data.</span></span> <span data-ttu-id="70ff2-174">Si el cliente no puede bloquear un identificador de datos porque el identificador contiene el miembro **fAckReq** , el cliente no debería enviar un mensaje de **\_ \_ confirmación DDE de WM** negativo.</span><span class="sxs-lookup"><span data-stu-id="70ff2-174">If the client cannot lock a data handle because the handle contains the **fAckReq** member, the client should not send a negative **WM\_DDE\_ACK** message.</span></span> <span data-ttu-id="70ff2-175">En su lugar, el cliente debe finalizar la conversación.</span><span class="sxs-lookup"><span data-stu-id="70ff2-175">Instead, the client should terminate the conversation.</span></span>

<span data-ttu-id="70ff2-176">Si un cliente envía una confirmación negativa en respuesta a un mensaje de [**\_ \_ datos de DDE de WM**](wm-dde-data.md) , el servidor es responsable de liberar la memoria (pero no el parámetro *lParam* ) a la que hace referencia el mensaje de **\_ \_ datos de DDE de WM** asociado a la confirmación negativa.</span><span class="sxs-lookup"><span data-stu-id="70ff2-176">If a client sends a negative acknowledgment in response to a [**WM\_DDE\_DATA**](wm-dde-data.md) message, the server is responsible for freeing the memory (but not the *lParam* parameter) referenced by the **WM\_DDE\_DATA** message associated with the negative acknowledgment.</span></span>

<span data-ttu-id="70ff2-177">Si puede procesar los datos, el cliente examina el miembro **fAckReq** de la estructura [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) para determinar si el servidor ha solicitado que se le informará de que el cliente ha recibido y procesado los datos correctamente.</span><span class="sxs-lookup"><span data-stu-id="70ff2-177">If it can process the data, the client examines the **fAckReq** member of the [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure to determine whether the server requested that it be informed that the client received and processed the data successfully.</span></span> <span data-ttu-id="70ff2-178">Si el servidor solicitó esta información, el cliente envía al servidor un mensaje [**de \_ \_ confirmación DDE de WM**](wm-dde-ack.md) positivo.</span><span class="sxs-lookup"><span data-stu-id="70ff2-178">If the server did request this information, the client sends the server a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span>

<span data-ttu-id="70ff2-179">Dado que el desbloqueo de datos invalida el puntero a los datos, el cliente guarda el valor del miembro **fRelease** antes de desbloquear el objeto de datos.</span><span class="sxs-lookup"><span data-stu-id="70ff2-179">Because unlocking data invalidates the pointer to the data, the client saves the value of the **fRelease** member before unlocking the data object.</span></span> <span data-ttu-id="70ff2-180">Después de guardar el valor, el cliente lo examina para determinar si la aplicación de servidor solicitó al cliente liberar la memoria que contiene los datos. el cliente actúa en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="70ff2-180">After saving the value, the client then examines it to determine whether the server application requested the client to free the memory containing the data; the client acts accordingly.</span></span>

<span data-ttu-id="70ff2-181">Al recibir un mensaje [**de \_ \_ confirmación DDE de WM**](wm-dde-ack.md) negativo, el cliente puede pedir el mismo valor de elemento de nuevo, especificando un formato de Portapapeles diferente.</span><span class="sxs-lookup"><span data-stu-id="70ff2-181">Upon receiving a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message, the client can ask for the same item value again, specifying a different clipboard format.</span></span> <span data-ttu-id="70ff2-182">Normalmente, un cliente solicitará primero el formato más complejo que pueda admitir y, a continuación, devolverá el paso abajo si es necesario a través de formatos progresivamente más sencillos hasta encontrar uno que el servidor pueda proporcionar.</span><span class="sxs-lookup"><span data-stu-id="70ff2-182">Typically, a client will first ask for the most complex format it can support, then step down if necessary through progressively simpler formats until it finds one the server can provide.</span></span>

<span data-ttu-id="70ff2-183">Si el servidor admite el elemento formatos del tema sistema, el cliente puede determinar una vez qué formatos del portapapeles admite el servidor, en lugar de determinarlos cada vez que el cliente solicita un elemento.</span><span class="sxs-lookup"><span data-stu-id="70ff2-183">If the server supports the Formats item of the system topic, the client can determine once what clipboard formats the server supports, instead of determining them each time the client requests an item.</span></span>

### <a name="submitting-an-item-to-the-server"></a><span data-ttu-id="70ff2-184">Envío de un elemento al servidor</span><span class="sxs-lookup"><span data-stu-id="70ff2-184">Submitting an Item to the Server</span></span>

<span data-ttu-id="70ff2-185">El cliente puede enviar un valor de elemento al servidor mediante el mensaje de anuncio de [**\_ \_ DDE de WM**](wm-dde-poke.md) .</span><span class="sxs-lookup"><span data-stu-id="70ff2-185">The client may send an item value to the server by using the [**WM\_DDE\_POKE**](wm-dde-poke.md) message.</span></span> <span data-ttu-id="70ff2-186">El cliente representa el elemento que se va a enviar y envía el mensaje de anuncio de **WM \_ DDE \_** , tal y como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="70ff2-186">The client renders the item to be sent and sends the **WM\_DDE\_POKE** message, as illustrated in the following example.</span></span>


```
size_t* pcch;
HRESULT hResult;
 
hResult = StringCchLength(szValue,STRSAFE_MAX_CCH, pcch);
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
if (!(hPokeData = GlobalAlloc(GMEM_MOVEABLE,
  (LONG) sizeof(DDEPOKE) + *pcch + 2))) 
{
    return; 
}
 
if (!(lpPokeData = (DDEPOKE *) GlobalLock(hPokeData))) 
{ 
    GlobalFree(hPokeData); 
    return; 
} 
 
lpPokeData->fRelease = TRUE; 
lpPokeData->cfFormat = CF_TEXT;
hResult = StringCchCopy((LPSTR) lpPokeData->Value, *pcch +1, (LPCSTR) szValue); // copies value to be sent
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}  
 
// Each line of CF_TEXT data is terminated by CR/LF. 
hResult = StringCchCat((LPSTR) lpPokeData->Value, *pcch + 3, (LPCSTR) "\r\n");
if (FAILED(hResult)
{
// TODO: Write error handler.
 return;
}
GlobalUnlock(hPokeData); 
if ((atomItem = GlobalAddAtom((LPSTR) szItem)) != 0) 
{ 
 
        if (!PostMessage(hwndServerDDE, 
                WM_DDE_POKE, 
                (WPARAM) hwndClientDDE, 
                PackDDElParam(WM_DDE_POKE, (UINT) hPokeData, 
                    atomItem))) 
        { 
            GlobalDeleteAtom(atomItem); 
            GlobalFree(hPokeData); 
        } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors. 
} 
```



> [!Note]  
> <span data-ttu-id="70ff2-187">El envío de datos mediante el uso de un mensaje de la función de correo de datos [**\_ DDE \_ de WM**](wm-dde-poke.md) es esencialmente el mismo que el envío mediante [**\_ \_ datos DDE de WM**](wm-dde-data.md), excepto que se envía el mensaje de correo de **WM \_ DDE \_** a través del cliente al servidor.</span><span class="sxs-lookup"><span data-stu-id="70ff2-187">Sending data by using a [**WM\_DDE\_POKE**](wm-dde-poke.md) message is essentially the same as sending it by using [**WM\_DDE\_DATA**](wm-dde-data.md), except that **WM\_DDE\_POKE** is sent from the client to the server.</span></span>

 

<span data-ttu-id="70ff2-188">Si el servidor puede aceptar el valor del elemento de datos en el formato representado por el cliente, el servidor procesa el valor del elemento según corresponda y envía al cliente un mensaje [**de \_ \_ confirmación de DDE de WM**](wm-dde-ack.md) positivo.</span><span class="sxs-lookup"><span data-stu-id="70ff2-188">If the server is able to accept the data-item value in the format rendered by the client, the server processes the item value as appropriate and sends the client a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span> <span data-ttu-id="70ff2-189">Si no puede procesar el valor del elemento, debido a su formato o por otros motivos, el servidor envía al cliente un mensaje de **\_ \_ confirmación DDE de WM** negativo.</span><span class="sxs-lookup"><span data-stu-id="70ff2-189">If it is unable to process the item value, because of its format or for other reasons, the server sends the client a negative **WM\_DDE\_ACK** message.</span></span>


```
UnpackDDElParam(WM_DDE_POKE, lParam, (PUINT) &hPokeData, 
    (PUINT) &atomItem); 
GlobalGetAtomName(atomItem, szItemName, ITEM_NAME_MAX_SIZE); 
if (!(lpPokeData = (DDEPOKE *) GlobalLock(hPokeData)) 
        || lpPokeData->cfFormat != CF_TEXT 
        || !IsItemSupportedByServer(szItemName)) 
{ 
    PostMessage(hwndClientDDE, 
        WM_DDE_ACK, 
        (WPARAM) hwndServerDDE, 
        PackDDElParam(WM_DDE_ACK, 0, atomItem)); // negative ACK  
}
hResult = StringCchLength(szItemValue,STRSAFE_MAX_CCH, pcch);
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
} 
hResult = StringCchCopy(szItemValue, *pcch +1, lpPokeData->Value); // copies value 
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}  
bRelease = lpPokeData->fRelease; 
GlobalUnlock(hPokeData); 
if (bRelease) 
{ 
    GlobalFree(hPokeData); 
} 
 
PostMessage(hwndClientDDE, 
    WM_DDE_ACK, 
    (WPARAM) hwndServerDDE, 
    PackDDElParam(WM_DDE_ACK, 
         0x8000, atomItem));    // positive ACK.
```



<span data-ttu-id="70ff2-190">En este ejemplo, el servidor llama a [**GlobalGetAtomName**](/windows/desktop/api/Winbase/nf-winbase-globalgetatomnamea) para recuperar el nombre del elemento enviado por el cliente.</span><span class="sxs-lookup"><span data-stu-id="70ff2-190">In this example, the server calls [**GlobalGetAtomName**](/windows/desktop/api/Winbase/nf-winbase-globalgetatomnamea) to retrieve the name of the item the client sent.</span></span> <span data-ttu-id="70ff2-191">A continuación, el servidor determina si admite el elemento y si el elemento se representa en el formato correcto (es decir, el \_ texto CF).</span><span class="sxs-lookup"><span data-stu-id="70ff2-191">The server then determines whether it supports the item and whether the item is rendered in the correct format (that is, CF\_TEXT).</span></span> <span data-ttu-id="70ff2-192">Si el elemento no se admite y no se representa en el formato correcto, o si el servidor no puede bloquear la memoria de los datos, el servidor envía una confirmación negativa de nuevo a la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="70ff2-192">If the item is not supported and not rendered in the correct format, or if the server cannot lock the memory for the data, the server sends a negative acknowledgment back to the client application.</span></span> <span data-ttu-id="70ff2-193">Tenga en cuenta que, en este caso, el envío de una confirmación negativa es correcto porque siempre se supone que los mensajes de salida de la [**\_ DDE \_ de WM**](wm-dde-poke.md) tienen el conjunto de miembros **fAckReq** .</span><span class="sxs-lookup"><span data-stu-id="70ff2-193">Note that in this case, sending a negative acknowledgment is correct because [**WM\_DDE\_POKE**](wm-dde-poke.md) messages are always assumed to have the **fAckReq** member set.</span></span> <span data-ttu-id="70ff2-194">El servidor debe omitir el miembro.</span><span class="sxs-lookup"><span data-stu-id="70ff2-194">The server should ignore the member.</span></span>

<span data-ttu-id="70ff2-195">Si un servidor envía una confirmación negativa en respuesta a un mensaje de salida de [**WM \_ DDE \_**](wm-dde-poke.md) , el cliente es responsable de liberar la memoria (pero no el parámetro *lParam* ) al que hace referencia el mensaje de salida de **\_ DDE \_ de WM** asociado a la confirmación negativa.</span><span class="sxs-lookup"><span data-stu-id="70ff2-195">If a server sends a negative acknowledgment in response to a [**WM\_DDE\_POKE**](wm-dde-poke.md) message, the client is responsible for freeing the memory (but not the *lParam* parameter) referenced by the **WM\_DDE\_POKE** message associated with the negative acknowledgment.</span></span>

## <a name="establishing-a-permanent-data-link"></a><span data-ttu-id="70ff2-196">Establecer un vínculo de datos permanente</span><span class="sxs-lookup"><span data-stu-id="70ff2-196">Establishing a Permanent Data Link</span></span>

<span data-ttu-id="70ff2-197">Una aplicación cliente puede utilizar DDE para establecer un vínculo a un elemento de una aplicación de servidor.</span><span class="sxs-lookup"><span data-stu-id="70ff2-197">A client application can use DDE to establish a link to an item in a server application.</span></span> <span data-ttu-id="70ff2-198">Después de establecer este tipo de vínculo, el servidor envía actualizaciones periódicas del elemento vinculado al cliente, normalmente, siempre que cambia el valor del elemento.</span><span class="sxs-lookup"><span data-stu-id="70ff2-198">After such a link is established, the server sends periodic updates of the linked item to the client, typically, whenever the value of the item changes.</span></span> <span data-ttu-id="70ff2-199">Por lo tanto, se establece un flujo de datos permanente entre las dos aplicaciones: Este flujo de datos permanece en vigor hasta que se desconecta explícitamente.</span><span class="sxs-lookup"><span data-stu-id="70ff2-199">Thus, a permanent data stream is established between the two applications; this data stream remains in place until it is explicitly disconnected.</span></span>

### <a name="initiating-a-data-link"></a><span data-ttu-id="70ff2-200">Iniciar un vínculo de datos</span><span class="sxs-lookup"><span data-stu-id="70ff2-200">Initiating a Data Link</span></span>

<span data-ttu-id="70ff2-201">El cliente inicia un vínculo de datos mediante la publicación de un mensaje de [**\_ \_ aviso de DDE de WM**](wm-dde-advise.md) , tal como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="70ff2-201">The client initiates a data link by posting a [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message, as shown in the following example.</span></span>


```
if (!(hOptions = GlobalAlloc(GMEM_MOVEABLE, 
        sizeof(DDEADVISE)))) 
    return; 
if (!(lpOptions = (DDEADVISE FAR*) GlobalLock(hOptions))) 
{ 
    GlobalFree(hOptions); 
    return; 
} 
 
lpOptions->cfFormat = CF_TEXT; 
lpOptions->fAckReq = TRUE; 
lpOptions->fDeferUpd = FALSE; 
GlobalUnlock(hOptions); 
if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
{ 
    if (!(PostMessage(hwndServerDDE, 
            WM_DDE_ADVISE, 
            (WPARAM) hwndClientDDE, 
            PackDDElParam(WM_DDE_ADVISE, (UINT) hOptions, 
                atomItem)))) 
    { 
        GlobalDeleteAtom(atomItem); 
        GlobalFree(hOptions); 
        FreeDDElParam(WM_DDE_ADVISE, lParam); 
    } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors 
 
}
```



<span data-ttu-id="70ff2-202">En este ejemplo, la aplicación cliente establece la marca **fDeferUpd** del mensaje [**de \_ \_ aviso de DDE de WM**](wm-dde-advise.md) en **false**.</span><span class="sxs-lookup"><span data-stu-id="70ff2-202">In this example, the client application sets the **fDeferUpd** flag of the [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message to **FALSE**.</span></span> <span data-ttu-id="70ff2-203">Esto indica a la aplicación de servidor que envíe los datos al cliente cada vez que cambien los datos.</span><span class="sxs-lookup"><span data-stu-id="70ff2-203">This directs the server application to send the data to the client whenever the data changes.</span></span>

<span data-ttu-id="70ff2-204">Si el servidor no puede dar servicio a la solicitud de [**\_ \_ aviso de DDE de WM**](wm-dde-advise.md) , envía al cliente un mensaje de [**\_ \_ confirmación DDE de WM**](wm-dde-ack.md) negativo.</span><span class="sxs-lookup"><span data-stu-id="70ff2-204">If the server is unable to service the [**WM\_DDE\_ADVISE**](wm-dde-advise.md) request, it sends the client a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span> <span data-ttu-id="70ff2-205">Pero si el servidor tiene acceso al elemento y puede representarlo en el formato solicitado, el servidor anota el nuevo vínculo (recuperando las marcas especificadas en el parámetro *hOptions* ) y envía al cliente un mensaje **de \_ \_ confirmación DDE de WM** positivo.</span><span class="sxs-lookup"><span data-stu-id="70ff2-205">But if the server has access to the item and can render it in the requested format, the server notes the new link (recalling the flags specified in the *hOptions* parameter) and sends the client a positive **WM\_DDE\_ACK** message.</span></span> <span data-ttu-id="70ff2-206">A partir de ese momento, hasta que el cliente emita un mensaje de [**\_ \_ desaconsejaje de WM DDE**](wm-dde-unadvise.md) que coincida, el servidor enviará los datos nuevos al cliente cada vez que cambie el valor del elemento en el servidor.</span><span class="sxs-lookup"><span data-stu-id="70ff2-206">From then on, until the client issues a matching [**WM\_DDE\_UNADVISE**](wm-dde-unadvise.md) message, the server sends the new data to the client every time the value of the item changes in the server.</span></span>

<span data-ttu-id="70ff2-207">El mensaje de [**\_ \_ aviso de DDE de WM**](wm-dde-advise.md) establece el formato de los datos que se intercambiarán durante el vínculo.</span><span class="sxs-lookup"><span data-stu-id="70ff2-207">The [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message establishes the format of the data to be exchanged during the link.</span></span> <span data-ttu-id="70ff2-208">Si el cliente intenta establecer otro vínculo con el mismo elemento pero usa un formato de datos diferente, el servidor puede decidir rechazar el segundo formato de datos o intentar admitirlo.</span><span class="sxs-lookup"><span data-stu-id="70ff2-208">If the client attempts to establish another link with the same item but is using a different data format, the server can choose to reject the second data format or attempt to support it.</span></span> <span data-ttu-id="70ff2-209">Si se ha establecido un vínculo activo para cualquier elemento de datos, el servidor solo puede admitir un formato de datos cada vez.</span><span class="sxs-lookup"><span data-stu-id="70ff2-209">If a warm link has been established for any data item, the server can support only one data format at a time.</span></span> <span data-ttu-id="70ff2-210">Esto se debe a que el mensaje de [**\_ \_ datos DDE de WM**](wm-dde-data.md) para un vínculo cálido tiene un identificador de datos **nulo** que, de lo contrario, contiene la información de formato.</span><span class="sxs-lookup"><span data-stu-id="70ff2-210">This is because the [**WM\_DDE\_DATA**](wm-dde-data.md) message for a warm link has a **NULL** data handle, which otherwise contains the format information.</span></span> <span data-ttu-id="70ff2-211">Por lo tanto, un servidor debe rechazar todos los vínculos cálidos de un elemento ya vinculado y debe rechazar todos los vínculos de un elemento que tenga vínculos cálidos.</span><span class="sxs-lookup"><span data-stu-id="70ff2-211">Thus, a server must reject all warm links for an item already linked, and must reject all links for an item that has warm links.</span></span> <span data-ttu-id="70ff2-212">Otra interpretación puede ser que el servidor cambie el formato y el estado activo o activo de un vínculo cuando se solicite un segundo vínculo para el mismo elemento de datos.</span><span class="sxs-lookup"><span data-stu-id="70ff2-212">Another interpretation may be that the server changes the format and the hot or warm state of a link when a second link is requested for the same data item.</span></span>

<span data-ttu-id="70ff2-213">En general, las aplicaciones cliente no deben intentar establecer más de un vínculo a la vez para un elemento de datos.</span><span class="sxs-lookup"><span data-stu-id="70ff2-213">In general, client applications should not attempt to establish more than one link at a time for a data item.</span></span>

### <a name="initiating-a-data-link-with-the-paste-link-command"></a><span data-ttu-id="70ff2-214">Iniciar un vínculo de datos con el comando pegar vínculo</span><span class="sxs-lookup"><span data-stu-id="70ff2-214">Initiating a Data Link with the Paste Link Command</span></span>

<span data-ttu-id="70ff2-215">Las aplicaciones que admiten vínculos de datos activos o semiactivos suelen admitir un formato de Portapapeles registrado denominado Link.</span><span class="sxs-lookup"><span data-stu-id="70ff2-215">Applications that support hot or warm data links typically support a registered clipboard format named Link.</span></span> <span data-ttu-id="70ff2-216">Cuando se asocian a los comandos de copiar y pegar vínculo de la aplicación, este formato del portapapeles permite al usuario establecer conversaciones DDE entre aplicaciones con solo copiar un elemento de datos en la aplicación de servidor y pegarlo en la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="70ff2-216">When associated with the application's Copy and Paste Link commands, this clipboard format enables the user to establish DDE conversations between applications simply by copying a data item in the server application and pasting it into the client application.</span></span>

<span data-ttu-id="70ff2-217">Una aplicación de servidor admite el formato del Portapapeles del vínculo colocando en el portapapeles una cadena que contiene la aplicación, el tema y los nombres de elemento cuando el usuario elige el comando **copiar** en el menú **edición** .</span><span class="sxs-lookup"><span data-stu-id="70ff2-217">A server application supports the Link clipboard format by placing in the clipboard a string containing the application, topic, and item names when the user chooses the **Copy** command from the **Edit** menu.</span></span> <span data-ttu-id="70ff2-218">A continuación se encuentra el formato de vínculo estándar:</span><span class="sxs-lookup"><span data-stu-id="70ff2-218">Following is the standard Link format:</span></span>

<span data-ttu-id="70ff2-219">*aplicación ***\\ 0*** tema ***\\ 0*** elemento \* \* \* \\ 0 \\ 0*\*</span><span class="sxs-lookup"><span data-stu-id="70ff2-219">*application ***\\0*** topic ***\\0*** item\*\*\*\\0\\0*\*</span></span>

<span data-ttu-id="70ff2-220">Un solo carácter nulo separa los nombres y dos caracteres nulos terminan toda la cadena.</span><span class="sxs-lookup"><span data-stu-id="70ff2-220">A single null character separates the names, and two null characters terminate the entire string.</span></span>

<span data-ttu-id="70ff2-221">Las aplicaciones cliente y servidor deben registrar el formato del Portapapeles del vínculo, como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="70ff2-221">Both the client and server applications must register the Link clipboard format, as shown:</span></span>


```
cfLink = RegisterClipboardFormat("Link");
```



<span data-ttu-id="70ff2-222">Una aplicación cliente admite el formato del Portapapeles del vínculo por medio de un comando pegar vínculo en el menú edición.</span><span class="sxs-lookup"><span data-stu-id="70ff2-222">A client application supports the Link clipboard format by means of a Paste Link command on its Edit menu.</span></span> <span data-ttu-id="70ff2-223">Cuando el usuario elige este comando, la aplicación cliente analiza los nombres de aplicación, tema y elemento de los datos del Portapapeles con formato de vínculo.</span><span class="sxs-lookup"><span data-stu-id="70ff2-223">When the user chooses this command, the client application parses the application, topic, and item names from the Link-format clipboard data.</span></span> <span data-ttu-id="70ff2-224">Con estos nombres, la aplicación cliente inicia una conversación para la aplicación y el tema, si tal conversación no existe todavía.</span><span class="sxs-lookup"><span data-stu-id="70ff2-224">Using these names, the client application initiates a conversation for the application and topic, if such a conversation does not already exist.</span></span> <span data-ttu-id="70ff2-225">A continuación, la aplicación cliente envía un mensaje de [**\_ \_ aviso de DDE de WM**](wm-dde-advise.md) a la aplicación de servidor, especificando el nombre del elemento contenido en los datos del Portapapeles con formato de vínculo.</span><span class="sxs-lookup"><span data-stu-id="70ff2-225">The client application then sends a [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message to the server application, specifying the item name contained in the Link-format clipboard data.</span></span>

<span data-ttu-id="70ff2-226">A continuación se puede obtener un ejemplo de la respuesta de una aplicación cliente cuando el usuario elige el comando pegar vínculo.</span><span class="sxs-lookup"><span data-stu-id="70ff2-226">Following is an example of a client application's response when the user chooses the Paste Link command.</span></span>


```
void DoPasteLink(hwndClientDDE) 
HWND hwndClientDDE; 
{ 
    HANDLE hData; 
    LPSTR lpData; 
    HWND hwndServerDDE; 
    CHAR szApplication[APP_MAX_SIZE + 1]; 
    CHAR szTopic[TOPIC_MAX_SIZE + 1]; 
    CHAR szItem[ITEM_MAX_SIZE + 1]; 
    size_t * nBufLen; 
 HRESULT hResult;
 
    if (OpenClipboard(hwndClientDDE)) 
    { 
        if (!(hData = GetClipboardData(cfLink)) || 
                !(lpData = GlobalLock(hData))) 
        { 
            CloseClipboard(); 
            return; 
        } 
 
        // Parse the clipboard data.
  hResult = StringCchLength(lpData, STRSAFE_MAX_CCH, nBufLen);
 if (FAILED(hResult) || nBufLen == NULL)
 {
// TODO: Write error handler.
  return;
 }
 if (*nBufLen >= APP_MAX_SIZE)
        { 
            CloseClipboard(); 
            GlobalUnlock(hData); 
            return; 
        }
 hResult = StringCchCopy(szApplication, APP_MAX_SIZE +1, lpData);
 if (FAILED(hResult)
 {
// TODO: Write error handler.
  return;
 }
        lpData += (*nBufLen + 1); // skips over null
 hResult = StringCchLength(lpData, STRSAFE_MAX_CCH, nBufLen);
 if (FAILED(hResult) || nBufLen == NULL)
 {
 // TODO: Write error handler.
  return;
 }
 if (*nBufLen >= TOPIC_MAX_SIZE)
        { 
            CloseClipboard(); 
            GlobalUnlock(hData); 
            return; 
        }
 hResult = StringCchCopy(szTopic, TOPIC_MAX_SIZE +1, lpData);
 if (FAILED(hResult)
 {
 // TODO: Write error handler.
  return;
 }
        lpData += (nBufLen + 1); // skips over null
 hResult = StringCchLength(lpData, STRSAFE_MAX_CCH, nBufLen);
 if (FAILED(hResult) || nBufLen == NULL)
 {
 // TODO: Write error handler.
  return;
 }
 if (*nBufLen >= ITEM_MAX_SIZE)
        { 
            CloseClipboard(); 
            GlobalUnlock(hData); 
            return; 
        }

 hResult = StringCchCopy(szItem, ITEM_MAX_SIZE +1, lpData);
 if (FAILED(hResult)
 {
 // TODO: Write error handler.
  return;
 } 
        GlobalUnlock(hData); 
        CloseClipboard(); 
 
        if (hwndServerDDE = 
                FindServerGivenAppTopic(szApplication, szTopic)) 
        { 
            // App/topic conversation is already started. 
 
            if (DoesAdviseAlreadyExist(hwndServerDDE, szItem)) 
            {
                MessageBox(hwndMain, 
                    "Advisory already established", 
                    "Client", MB_ICONEXCLAMATION | MB_OK); 
            }
            else SendAdvise(hwndClientDDE, hwndServerDDE, szItem); 
        } 
        else 
        { 
            // Client must initiate a new conversation first. 
            SendInitiate(szApplication, szTopic); 
            if (hwndServerDDE = 
                    FindServerGivenAppTopic(szApplication, 
                        szTopic)) 
            {
                SendAdvise(hwndClientDDE, hwndServerDDE, szItem); 
            }
        } 
    } 
    return; 
}
```



<span data-ttu-id="70ff2-227">En este ejemplo, la aplicación cliente abre el portapapeles y determina si contiene datos en el formato de vínculo (es decir, cfLink) que se había registrado previamente.</span><span class="sxs-lookup"><span data-stu-id="70ff2-227">In this example, the client application opens the clipboard and determines whether it contains data in the Link format (that is, cfLink) it had previously registered.</span></span> <span data-ttu-id="70ff2-228">Si no es así, o si no puede bloquear los datos en el portapapeles, el cliente devuelve.</span><span class="sxs-lookup"><span data-stu-id="70ff2-228">If not, or if it cannot lock the data in the clipboard, the client returns.</span></span>

<span data-ttu-id="70ff2-229">Una vez que la aplicación cliente recupera un puntero a los datos del portapapeles, analiza los datos para extraer la aplicación, el tema y los nombres de los elementos.</span><span class="sxs-lookup"><span data-stu-id="70ff2-229">After the client application retrieves a pointer to the clipboard data, it parses the data to extract the application, topic, and item names.</span></span>

<span data-ttu-id="70ff2-230">La aplicación cliente determina si ya existe una conversación en el tema entre ella y la aplicación de servidor.</span><span class="sxs-lookup"><span data-stu-id="70ff2-230">The client application determines whether a conversation on the topic already exists between it and the server application.</span></span> <span data-ttu-id="70ff2-231">Si existe una conversación, el cliente comprueba si ya existe un vínculo para el elemento de datos.</span><span class="sxs-lookup"><span data-stu-id="70ff2-231">If a conversation does exist, the client checks whether a link already exists for the data item.</span></span> <span data-ttu-id="70ff2-232">Si existe este tipo de vínculo, el cliente muestra un cuadro de mensaje al usuario; de lo contrario, llama a su propia función *SendAdvise* para enviar un mensaje de [**aviso de WM \_ DDE \_**](wm-dde-advise.md) al servidor para el elemento.</span><span class="sxs-lookup"><span data-stu-id="70ff2-232">If such a link exists, the client displays a message box to the user; otherwise, it calls its own *SendAdvise* function to send a [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message to the server for the item.</span></span>

<span data-ttu-id="70ff2-233">Si no existe ya una conversación en el tema entre el cliente y el servidor, el cliente llama primero a su propia función *SendInitiate* para difundir el mensaje de [**Inicio de WM \_ \_ DDE**](wm-dde-initiate.md) para solicitar una conversación y, en segundo lugar, llama a su propia función *FindServerGivenAppTopic* para establecer la conversación con la ventana que responde en nombre de la aplicación de servidor.</span><span class="sxs-lookup"><span data-stu-id="70ff2-233">If a conversation on the topic does not already exist between the client and the server, the client first calls its own *SendInitiate* function to broadcast the [**WM\_DDE\_INITIATE**](wm-dde-initiate.md) message to request a conversation and, second, calls its own *FindServerGivenAppTopic* function to establish the conversation with the window that responds on behalf of the server application.</span></span> <span data-ttu-id="70ff2-234">Una vez iniciada la conversación, la aplicación cliente llama a *SendAdvise* para solicitar el vínculo.</span><span class="sxs-lookup"><span data-stu-id="70ff2-234">After the conversation has begun, the client application calls *SendAdvise* to request the link.</span></span>

### <a name="notifying-the-client-that-data-has-changed"></a><span data-ttu-id="70ff2-235">Notificación al cliente de que los datos han cambiado</span><span class="sxs-lookup"><span data-stu-id="70ff2-235">Notifying the Client that Data Has Changed</span></span>

<span data-ttu-id="70ff2-236">Cuando el cliente establece un vínculo con el mensaje [**de \_ \_ aviso de DDE de WM**](wm-dde-advise.md) , con el miembro **fDeferUpd** no establecido (es decir, igual a cero) en la estructura [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) , el cliente ha solicitado al servidor que envíe el elemento de datos cada vez que cambie el valor del elemento.</span><span class="sxs-lookup"><span data-stu-id="70ff2-236">When the client establishes a link by using the [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message, with the **fDeferUpd** member not set (that is, equal to zero) in the [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure, the client has requested the server send the data item each time the item's value changes.</span></span> <span data-ttu-id="70ff2-237">En tales casos, el servidor representa el nuevo valor del elemento de datos en el formato especificado previamente y envía al cliente un mensaje [**de \_ \_ datos de WM DDE**](wm-dde-data.md) , tal como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="70ff2-237">In such cases, the server renders the new value of the data item in the previously specified format and sends the client a [**WM\_DDE\_DATA**](wm-dde-data.md) message, as shown in the following example.</span></span>


```
// Allocate the size of a DDE data header, plus data (a string), 
// plus a <CR><LF><NULL> 

size_t* pcch;
HRESULT hResult;
 
hResult = StringCchLength(szItemValue,STRSAFE_MAX_CCH, pcch);
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
if (!(hData = GlobalAlloc(GMEM_MOVEABLE,
  sizeof(DDEDATA) + *pcch + 3))) 
{
    return; 
}
if (!(lpData = (DDEDATA FAR*) GlobalLock(hData))) 
{ 
    GlobalFree(hData); 
    return; 
} 
lpData->fAckReq = bAckRequest;       // as in original WM_DDE_ADVISE 
lpData->cfFormat = CF_TEXT;
hResult = StringCchCopy(lpData->Value, *pcch +1, szItemValue); // copies value to be sent
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
// add CR/LF for CF_TEXT format
hResult = StringCchCat(lpData->Value, *pcch + 3, "\r\n");
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
GlobalUnlock(hData); 
if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
{ 
    if (!PostMessage(hwndClientDDE, 
            WM_DDE_DATA, 
            (WPARAM) hwndServerDDE, 
            PackDDElParam(WM_DDE_DATA, (UINT) hData, atomItem))) 
    { 
        GlobalFree(hData); 
        GlobalDeleteAtom(atomItem); 
        FreeDDElParam(WM_DDE_DATA, lParam); 
    } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors. 
 
}
```



<span data-ttu-id="70ff2-238">En este ejemplo, el cliente procesa el valor del elemento según corresponda.</span><span class="sxs-lookup"><span data-stu-id="70ff2-238">In this example, the client processes the item value as appropriate.</span></span> <span data-ttu-id="70ff2-239">Si se establece la marca **fAckReq** para el elemento, el cliente envía al servidor un mensaje [**de \_ \_ confirmación DDE de WM**](wm-dde-ack.md) positivo.</span><span class="sxs-lookup"><span data-stu-id="70ff2-239">If the **fAckReq** flag for the item is set, the client sends the server a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span>

<span data-ttu-id="70ff2-240">Cuando el cliente establece el vínculo con el conjunto de miembros **fDeferUpd** (es decir, es igual a 1), el cliente ha solicitado que solo se envíe una notificación, no los datos en sí, cada vez que cambien los datos.</span><span class="sxs-lookup"><span data-stu-id="70ff2-240">When the client establishes the link, with the **fDeferUpd** member set (that is, equal to 1), the client has requested that only a notification, not the data itself, be sent each time the data changes.</span></span> <span data-ttu-id="70ff2-241">En tales casos, cuando el valor del elemento cambia, el servidor no representa el valor, sino que simplemente envía el cliente a un mensaje de [**\_ \_ datos de WM DDE**](wm-dde-data.md) con un identificador de datos null, como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="70ff2-241">In such cases, when the item value changes, the server does not render the value but simply sends the client a [**WM\_DDE\_DATA**](wm-dde-data.md) message with a null data handle, as illustrated in the following example.</span></span>


```
if (bDeferUpd)      // check whether flag was set in WM_DDE_ADVISE
{
    if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
    { 
        if (!PostMessage(hwndClientDDE, 
                WM_DDE_DATA, 
                (WPARAM) hwndServerDDE, 
                PackDDElParam(WM_DDE_DATA, 0, 
                    atomItem)))                  // NULL data
        {
            GlobalDeleteAtom(atomItem); 
            FreeDDElParam(WM_DDE_DATA, lParam); 
        } 
    } 
} 
 
if (atomItem == 0) 
{ 
     // Handle errors. 
} 
```



<span data-ttu-id="70ff2-242">Según sea necesario, el cliente puede solicitar el valor más reciente del elemento de datos mediante la emisión de un mensaje de [**\_ \_ solicitud de DDE de WM**](wm-dde-request.md) normal o simplemente pasar por alto el aviso del servidor de que los datos han cambiado.</span><span class="sxs-lookup"><span data-stu-id="70ff2-242">As necessary, the client can request the latest value of the data item by issuing a normal [**WM\_DDE\_REQUEST**](wm-dde-request.md) message, or it can simply ignore the notice from the server that the data has changed.</span></span> <span data-ttu-id="70ff2-243">En cualquier caso, si **fAckReq** es igual a 1, se espera que el cliente envíe un mensaje [**de \_ \_ confirmación DDE de WM**](wm-dde-ack.md) positivo al servidor.</span><span class="sxs-lookup"><span data-stu-id="70ff2-243">In either case, if **fAckReq** is equal to 1, the client is expected to send a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message to the server.</span></span>

### <a name="terminating-a-data-link"></a><span data-ttu-id="70ff2-244">Finalización de un vínculo de datos</span><span class="sxs-lookup"><span data-stu-id="70ff2-244">Terminating a Data Link</span></span>

<span data-ttu-id="70ff2-245">Si el cliente solicita que se termine un vínculo de datos específico, el cliente envía al servidor un mensaje de [**\_ \_ desaconsejad DDE de WM**](wm-dde-unadvise.md) , tal como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="70ff2-245">If the client requests that a specific data link be terminated, the client sends the server a [**WM\_DDE\_UNADVISE**](wm-dde-unadvise.md) message, as shown in the following example.</span></span>


```
if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
{ 
    if (!PostMessage(hwndServerDDE, 
            WM_DDE_UNADVISE, 
            (WPARAM) hwndClientDDE, 
            PackDDElParam(WM_DDE_UNADVISE, 0, atomItem))) 
    { 
        GlobalDeleteAtom(atomItem); 
        FreeDDElParam(WM_DDE_UNADVISE, lParam); 
    } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors. 
}
```



<span data-ttu-id="70ff2-246">El servidor comprueba si el cliente tiene actualmente un vínculo al elemento específico en esta conversación.</span><span class="sxs-lookup"><span data-stu-id="70ff2-246">The server checks whether the client currently has a link to the specific item in this conversation.</span></span> <span data-ttu-id="70ff2-247">Si existe un vínculo, el servidor envía al cliente un mensaje [**de \_ \_ confirmación de DDE de WM**](wm-dde-ack.md) positivo; el servidor ya no es necesario para enviar actualizaciones sobre el elemento.</span><span class="sxs-lookup"><span data-stu-id="70ff2-247">If a link exists, the server sends the client a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message; the server is then no longer required to send updates about the item.</span></span> <span data-ttu-id="70ff2-248">Si no existe ningún vínculo, el servidor envía al cliente un mensaje de **\_ \_ confirmación DDE de WM** negativo.</span><span class="sxs-lookup"><span data-stu-id="70ff2-248">If no link exists, the server sends the client a negative **WM\_DDE\_ACK** message.</span></span>

<span data-ttu-id="70ff2-249">El mensaje de [**\_ \_ desaconsejar DDE de WM**](wm-dde-unadvise.md) especifica un formato de datos.</span><span class="sxs-lookup"><span data-stu-id="70ff2-249">The [**WM\_DDE\_UNADVISE**](wm-dde-unadvise.md) message specifies a data format.</span></span> <span data-ttu-id="70ff2-250">Un formato de cero informa al servidor de que detenga todos los vínculos del elemento especificado, incluso si se establecen varios vínculos activos y cada uno de ellos usa un formato diferente.</span><span class="sxs-lookup"><span data-stu-id="70ff2-250">A format of zero informs the server to stop all links for the specified item, even if several hot links are established and each uses a different format.</span></span>

<span data-ttu-id="70ff2-251">Para finalizar todos los vínculos de una conversación, la aplicación cliente envía el mensaje [**de \_ \_ desaconsejar DDE de WM**](wm-dde-unadvise.md) al servidor con un átomo de elemento nulo.</span><span class="sxs-lookup"><span data-stu-id="70ff2-251">To terminate all links for a conversation, the client application sends the server a [**WM\_DDE\_UNADVISE**](wm-dde-unadvise.md) message with a null item atom.</span></span> <span data-ttu-id="70ff2-252">El servidor determina si la conversación tiene al menos un vínculo establecido actualmente.</span><span class="sxs-lookup"><span data-stu-id="70ff2-252">The server determines whether the conversation has at least one link currently established.</span></span> <span data-ttu-id="70ff2-253">Si existe un vínculo, el servidor envía al cliente un mensaje [**de \_ \_ confirmación de DDE de WM**](wm-dde-ack.md) positivo; el servidor deja de tener que enviar actualizaciones en la conversación.</span><span class="sxs-lookup"><span data-stu-id="70ff2-253">If a link exists, the server sends the client a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message; the server then no longer has to send any updates in the conversation.</span></span> <span data-ttu-id="70ff2-254">Si no existe ningún vínculo, el servidor envía al cliente un mensaje de **\_ \_ confirmación DDE de WM** negativo.</span><span class="sxs-lookup"><span data-stu-id="70ff2-254">If no link exists, the server sends the client a negative **WM\_DDE\_ACK** message.</span></span>

## <a name="carrying-out-commands-in-a-server-application"></a><span data-ttu-id="70ff2-255">Ejecutar comandos en una aplicación de servidor</span><span class="sxs-lookup"><span data-stu-id="70ff2-255">Carrying Out Commands in a Server Application</span></span>

<span data-ttu-id="70ff2-256">Las aplicaciones pueden usar el mensaje de [**\_ \_ ejecución de WM DDE**](wm-dde-execute.md) para hacer que un comando o una serie de comandos determinados se lleven a cabo en otra aplicación.</span><span class="sxs-lookup"><span data-stu-id="70ff2-256">Applications can use the [**WM\_DDE\_EXECUTE**](wm-dde-execute.md) message to cause a certain command or series of commands to be carried out in another application.</span></span> <span data-ttu-id="70ff2-257">Para ello, el cliente envía un mensaje de **\_ \_ ejecución de WM DDE** de servidor que contiene un identificador a una cadena de comandos, tal y como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="70ff2-257">To do this, the client sends the server a **WM\_DDE\_EXECUTE** message containing a handle to a command string, as shown in the following example.</span></span>


```
HRESULT hResult;
  
if (!(hCommand = GlobalAlloc(GMEM_MOVEABLE, 
        sizeof(szCommandString) + 1))) 
{
    return; 
}
if (!(lpCommand = GlobalLock(hCommand))) 
{ 
    GlobalFree(hCommand); 
    return; 
} 

hResult = StringCbCopy(lpCommand, sizeof(szCommandString), szCommandString);
if (hResult != S_OK)
{
// TODO: Write error handler.
 return;
}
 
GlobalUnlock(hCommand); 
if (!PostMessage(hwndServerDDE, 
        WM_DDE_EXECUTE, 
        (WPARAM) hwndClientDDE, 
        PackDDElParam(WM_DDE_EXECUTE, 0, (UINT) hCommand))) 
{ 
    GlobalFree(hCommand); 
    FreeDDElParam(WM_DDE_EXECUTE, lParam); 
}
```



<span data-ttu-id="70ff2-258">En este ejemplo, el servidor intenta llevar a cabo la cadena de comandos especificada.</span><span class="sxs-lookup"><span data-stu-id="70ff2-258">In this example, the server attempts to carry out the specified command string.</span></span> <span data-ttu-id="70ff2-259">Si se realiza correctamente, el servidor envía al cliente un mensaje [**de \_ \_ confirmación de DDE de WM**](wm-dde-ack.md) positivo; de lo contrario, envía un mensaje de **\_ \_ confirmación DDE de WM** negativo.</span><span class="sxs-lookup"><span data-stu-id="70ff2-259">If it succeeds, the server sends the client a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message; otherwise, it sends a negative **WM\_DDE\_ACK** message.</span></span> <span data-ttu-id="70ff2-260">Este mensaje de **\_ \_ confirmación de DDE de WM** reutiliza el identificador *hCommand* pasado en el mensaje de [**ejecución de WM \_ DDE \_**](wm-dde-execute.md) original.</span><span class="sxs-lookup"><span data-stu-id="70ff2-260">This **WM\_DDE\_ACK** message reuses the *hCommand* handle passed in the original [**WM\_DDE\_EXECUTE**](wm-dde-execute.md) message.</span></span>

<span data-ttu-id="70ff2-261">Si la cadena de ejecución del comando del cliente solicita que el servidor finalice, el servidor debe responder mediante el envío de un mensaje de [**\_ \_ confirmación DDE de WM**](wm-dde-ack.md) positivo y después publicar un mensaje de [**\_ \_ finalización de WM DDE**](wm-dde-terminate.md) antes de finalizar.</span><span class="sxs-lookup"><span data-stu-id="70ff2-261">If the client's command execution string requests that the server terminate, the server should respond by sending a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message and then post a [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) message before terminating.</span></span> <span data-ttu-id="70ff2-262">El resto de los comandos que se envían con un mensaje de [**\_ \_ ejecución de WM DDE**](wm-dde-execute.md) deben ejecutarse sincrónicamente; es decir, el servidor debería enviar un mensaje de **\_ \_ confirmación de WM DDE** solo después de completar correctamente el comando.</span><span class="sxs-lookup"><span data-stu-id="70ff2-262">All other commands sent with a [**WM\_DDE\_EXECUTE**](wm-dde-execute.md) message should be executed synchronously; that is, the server should send a **WM\_DDE\_ACK** message only after successfully completing the command.</span></span>

## <a name="terminating-a-conversation"></a><span data-ttu-id="70ff2-263">Finalizar una conversación</span><span class="sxs-lookup"><span data-stu-id="70ff2-263">Terminating a Conversation</span></span>

<span data-ttu-id="70ff2-264">Tanto el cliente como el servidor pueden emitir un mensaje de [**\_ \_ finalización de WM DDE**](wm-dde-terminate.md) para finalizar una conversación en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="70ff2-264">Either the client or the server can issue a [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) message to terminate a conversation at any time.</span></span> <span data-ttu-id="70ff2-265">Del mismo modo, las aplicaciones cliente y servidor deben estar preparadas para recibir este mensaje en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="70ff2-265">Similarly, both the client and server applications should be prepared to receive this message at any time.</span></span> <span data-ttu-id="70ff2-266">Una aplicación debe finalizar todas sus conversaciones antes de cerrarse.</span><span class="sxs-lookup"><span data-stu-id="70ff2-266">An application must terminate all of its conversations before shutting down.</span></span>

<span data-ttu-id="70ff2-267">En el ejemplo siguiente, la aplicación que finaliza la conversación envía un mensaje de [**\_ \_ finalización de WM DDE**](wm-dde-terminate.md) .</span><span class="sxs-lookup"><span data-stu-id="70ff2-267">In the following example, the application terminating the conversation posts a [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) message.</span></span>


```
PostMessage(hwndServerDDE, WM_DDE_TERMINATE, 
    (WPARAM) hwndClientDDE, 0);
```



<span data-ttu-id="70ff2-268">Esto informa a la otra aplicación de que la aplicación emisora no enviará más mensajes y el destinatario puede cerrar su ventana.</span><span class="sxs-lookup"><span data-stu-id="70ff2-268">This informs the other application that the sending application will send no further messages and the recipient can close its window.</span></span> <span data-ttu-id="70ff2-269">En todos los casos, se espera que el destinatario responda rápidamente mediante el envío de un mensaje de [**\_ \_ finalización de WM DDE**](wm-dde-terminate.md) .</span><span class="sxs-lookup"><span data-stu-id="70ff2-269">The recipient is expected in all cases to respond promptly by sending a [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) message.</span></span> <span data-ttu-id="70ff2-270">El destinatario no debe enviar un mensaje de [**\_ \_ confirmación del DDE de WM**](wm-dde-ack.md) negativo, ocupado o positivo.</span><span class="sxs-lookup"><span data-stu-id="70ff2-270">The recipient must not send a negative, busy, or positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span>

<span data-ttu-id="70ff2-271">Una vez que una aplicación ha enviado el mensaje de [**\_ \_ terminación de WM DDE**](wm-dde-terminate.md) al asociado en una conversación DDE, no debe responder a los mensajes de ese asociado, ya que es posible que el socio haya destruido la ventana a la que se enviará la respuesta.</span><span class="sxs-lookup"><span data-stu-id="70ff2-271">After an application has sent the [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) message to the partner in a DDE conversation, it must not respond to messages from that partner, since the partner might have destroyed the window to which the response would be sent.</span></span>

<span data-ttu-id="70ff2-272">Si una aplicación recibe un mensaje DDE distinto de [**la \_ \_ terminación de WM DDE**](wm-dde-terminate.md) después de haber publicado la **terminación de WM \_ DDE \_**, debe liberar todos los objetos asociados a los mensajes recibidos, excepto los identificadores de datos para los mensajes de [**WM \_ DDE \_ Data**](wm-dde-data.md) o [**WM \_ DDE \_**](wm-dde-poke.md) , que **no** tienen el conjunto de miembros **fRelease** .</span><span class="sxs-lookup"><span data-stu-id="70ff2-272">If an application receives a DDE message other than [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) after it has posted **WM\_DDE\_TERMINATE**, it should free all objects associated with the received messages except the data handles for [**WM\_DDE\_DATA**](wm-dde-data.md) or [**WM\_DDE\_POKE**](wm-dde-poke.md) messages that do **not** have the **fRelease** member set.</span></span>

<span data-ttu-id="70ff2-273">Cuando una aplicación está a punto de finalizar, debe terminar todas las conversaciones DDE activas antes de completar el procesamiento del mensaje de [**\_ destrucción de WM**](/windows/desktop/winmsg/wm-destroy) .</span><span class="sxs-lookup"><span data-stu-id="70ff2-273">When an application is about to terminate, it should end all active DDE conversations before completing processing of the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message.</span></span> <span data-ttu-id="70ff2-274">Sin embargo, si una aplicación no finaliza sus conversaciones DDE activas, el sistema finalizará cualquier conversación DDE asociada a una ventana cuando se destruya la ventana.</span><span class="sxs-lookup"><span data-stu-id="70ff2-274">However, if an application does not end its active DDE conversations, the system will terminate any DDE conversations associated with a window when the window is destroyed.</span></span> <span data-ttu-id="70ff2-275">En el ejemplo siguiente se muestra cómo una aplicación de servidor finaliza todas las conversaciones DDE.</span><span class="sxs-lookup"><span data-stu-id="70ff2-275">The following example shows how a server application terminates all DDE conversations.</span></span>


```
void TerminateConversations(hwndServerDDE) 
HWND hwndServerDDE; 
{ 
    HWND hwndClientDDE; 
 
    // Terminate each active conversation. 
 
    while (hwndClientDDE = GetNextLink(hwndClientDDE)) 
    { 
        SendTerminate(hwndServerDDE, hwndClientDDE); 
    } 
    return; 
} 
 
BOOL AtLeastOneLinkActive(VOID) 
{ 
    return TRUE; 
} 
 
HWND GetNextLink(hwndDummy) 
    HWND hwndDummy; 
{ 
    return (HWND) 1; 
} 
 
VOID SendTerminate(HWND hwndServerDDE, HWND hwndClientDDE) 
{ 
    return; 
}
```



 

 