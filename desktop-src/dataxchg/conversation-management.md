---
title: Administración de conversaciones
description: En este tema se describen las conversaciones entre un cliente y un servidor.
ms.assetid: 4e5ff1a1-d46a-4e2a-a37c-8df951f2a1ee
keywords:
- Interfaz de usuario de Windows, Intercambio dinámico de datos (DDE)
- Intercambio dinámico de datos (DDE), conversaciones
- DDE (Intercambio dinámico de datos), conversaciones
- intercambio de datos, Intercambio dinámico de datos (DDE)
- Interfaz de usuario de Windows, biblioteca de administración de Intercambio dinámico de datos (DDEML)
- Biblioteca de administración de Intercambio dinámico de datos (DDEML), conversaciones
- DDEML (biblioteca de administración de Intercambio dinámico de datos), conversaciones
- intercambio de datos, biblioteca de administración de Intercambio dinámico de datos (DDEML)
- Intercambio dinámico de datos (DDE), varias conversaciones
- DDE (Intercambio dinámico de datos), varias conversaciones
- Biblioteca de administración de Intercambio dinámico de datos (DDEML), varias conversaciones
- DDEML (biblioteca de administración de Intercambio dinámico de datos), varias conversaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ca1a0a8e02bceb6b2f69051d89df289871fdd42
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105720089"
---
# <a name="conversation-management"></a><span data-ttu-id="b6904-115">Administración de conversaciones</span><span class="sxs-lookup"><span data-stu-id="b6904-115">Conversation Management</span></span>

<span data-ttu-id="b6904-116">Siempre se establece una conversación entre un cliente y un servidor a petición del cliente.</span><span class="sxs-lookup"><span data-stu-id="b6904-116">A conversation between a client and a server is always established at the request of the client.</span></span> <span data-ttu-id="b6904-117">Cuando se establece una conversación, cada asociado recibe un identificador que identifica la conversación.</span><span class="sxs-lookup"><span data-stu-id="b6904-117">When a conversation is established, each partner receives a handle that identifies the conversation.</span></span> <span data-ttu-id="b6904-118">Los asociados usan este identificador en otras funciones de la biblioteca de administración de Intercambio dinámico de datos (DDEML) para enviar transacciones y administrar la conversación.</span><span class="sxs-lookup"><span data-stu-id="b6904-118">The partners use this handle in other Dynamic Data Exchange Management Library (DDEML) functions to send transactions and manage the conversation.</span></span> <span data-ttu-id="b6904-119">Un cliente puede solicitar una conversación con un solo servidor o puede solicitar varias conversaciones con uno o más servidores.</span><span class="sxs-lookup"><span data-stu-id="b6904-119">A client can request a conversation with a single server, or it can request multiple conversations with one or more servers.</span></span>

<span data-ttu-id="b6904-120">En los temas siguientes se describe cómo una aplicación establece nuevas conversaciones y cómo obtiene información acerca de las conversaciones existentes.</span><span class="sxs-lookup"><span data-stu-id="b6904-120">The following topics describe how an application establishes new conversations and gets information about existing conversations.</span></span>

-   [<span data-ttu-id="b6904-121">Conversaciones únicas</span><span class="sxs-lookup"><span data-stu-id="b6904-121">Single Conversations</span></span>](#single-conversations)
-   [<span data-ttu-id="b6904-122">Varias conversaciones</span><span class="sxs-lookup"><span data-stu-id="b6904-122">Multiple Conversations</span></span>](#multiple-conversations)

## <a name="single-conversations"></a><span data-ttu-id="b6904-123">Conversaciones únicas</span><span class="sxs-lookup"><span data-stu-id="b6904-123">Single Conversations</span></span>

<span data-ttu-id="b6904-124">Una aplicación cliente solicita una sola conversación con un servidor llamando a la función [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) y especificando identificadores de cadena que identifican las cadenas que contienen el nombre de servicio de la aplicación de servidor y el nombre de tema de la conversación.</span><span class="sxs-lookup"><span data-stu-id="b6904-124">A client application requests a single conversation with a server by calling the [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) function and specifying string handles that identify the strings containing the service name of the server application and the topic name for the conversation.</span></span> <span data-ttu-id="b6904-125">El DDEML responde mediante el envío de la transacción [**XTYP \_ Connect**](xtyp-connect.md) a la función de devolución de llamada intercambio dinámico de datos (DDE) de cada aplicación de servidor que haya registrado un nombre de servicio que coincida con el especificado en **DdeConnect** o que haya desactivado el filtrado de nombres de servicio mediante una llamada a [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice).</span><span class="sxs-lookup"><span data-stu-id="b6904-125">The DDEML responds by sending the [**XTYP\_CONNECT**](xtyp-connect.md) transaction to the Dynamic Data Exchange (DDE) callback function of each server application that either has registered a service name that matches the one specified in **DdeConnect** or has turned service name filtering off by calling [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice).</span></span> <span data-ttu-id="b6904-126">Un servidor también puede filtrar las transacciones de **\_ conexión de XTYP** especificando la \_ marca de filtro CBF FAIL \_ Connections en la función [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="b6904-126">A server can also filter **XTYP\_CONNECT** transactions by specifying the CBF\_FAIL\_CONNECTIONS filter flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span> <span data-ttu-id="b6904-127">Durante la transacción **XTYP \_ Connect** , ddeml pasa el nombre del servicio y el nombre del tema al servidor.</span><span class="sxs-lookup"><span data-stu-id="b6904-127">During the **XTYP\_CONNECT** transaction, the DDEML passes the service name and the topic name to the server.</span></span> <span data-ttu-id="b6904-128">El servidor debe examinar los nombres y devolver **true** si admite el par nombre del servicio y nombre del tema, o **false** si no lo hace.</span><span class="sxs-lookup"><span data-stu-id="b6904-128">The server must examine the names and return **TRUE** if it supports the service name and topic name pair or **FALSE** if it does not.</span></span>

<span data-ttu-id="b6904-129">Si ningún servidor responde positivamente a la solicitud del cliente para conectarse, el cliente recibe un **valor null** de [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) y no se establece ninguna conversación.</span><span class="sxs-lookup"><span data-stu-id="b6904-129">If no server responds positively to the client's request to connect, the client receives **NULL** from [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) and no conversation is established.</span></span> <span data-ttu-id="b6904-130">Si un servidor devuelve **true**, se establece una conversación y el cliente recibe un identificador de conversación, un valor **DWORD** que identifica la conversación.</span><span class="sxs-lookup"><span data-stu-id="b6904-130">If a server returns **TRUE**, a conversation is established and the client receives a conversation handle — a **DWORD** value that identifies the conversation.</span></span> <span data-ttu-id="b6904-131">El cliente utiliza el identificador en las llamadas a DDEML posteriores para obtener datos del servidor.</span><span class="sxs-lookup"><span data-stu-id="b6904-131">The client uses the handle in subsequent DDEML calls to obtain data from the server.</span></span> <span data-ttu-id="b6904-132">El servidor recibe la transacción de [**\_ \_ confirmación de conexión de XTYP**](xtyp-connect-confirm.md) (a menos que el servidor especifique la marca de filtro CBF \_ SKIP \_ Connect \_ Confirmations).</span><span class="sxs-lookup"><span data-stu-id="b6904-132">The server receives the [**XTYP\_CONNECT\_CONFIRM**](xtyp-connect-confirm.md) transaction (unless the server specified the CBF\_SKIP\_CONNECT\_CONFIRMS filter flag).</span></span> <span data-ttu-id="b6904-133">Esta transacción pasa el identificador de conversación al servidor.</span><span class="sxs-lookup"><span data-stu-id="b6904-133">This transaction passes the conversation handle to the server.</span></span>

<span data-ttu-id="b6904-134">En el ejemplo siguiente se solicita una conversación en el tema del sistema con un servidor que reconoce el nombre del servicio de servidor.</span><span class="sxs-lookup"><span data-stu-id="b6904-134">The following example requests a conversation on the System topic with a server that recognizes the service name MyServer.</span></span> <span data-ttu-id="b6904-135">Los parámetros *hszServName* y *hszSysTopic* se han creado previamente como identificadores de cadena.</span><span class="sxs-lookup"><span data-stu-id="b6904-135">The *hszServName* and *hszSysTopic* parameters are previously created string handles.</span></span>


```
HCONV hConv;         // conversation handle 
HWND hwndParent;     // parent window handle 
HSZ hszServName;     // service name string handle 
HSZ hszSysTopic;     // System topic string handle 
 
hConv = DdeConnect( 
    idInst,               // instance identifier 
    hszServName,          // service name string handle 
    hszSysTopic,          // System topic string handle 
    (PCONVCONTEXT) NULL); // use default context 
 
if (hConv == NULL) 
{ 
    MessageBox(hwndParent, "MyServer is unavailable.", 
        (LPSTR) NULL, MB_OK); 
    return FALSE; 
} 
```



<span data-ttu-id="b6904-136">En el ejemplo anterior, [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) hace que la función de devolución de llamada DDE de la aplicación de mi servidor reciba una transacción [**XTYP \_ Connect**](xtyp-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="b6904-136">In the preceding example, [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) causes the DDE callback function of the MyServer application to receive an [**XTYP\_CONNECT**](xtyp-connect.md) transaction.</span></span>

<span data-ttu-id="b6904-137">En el ejemplo siguiente, el servidor responde a la transacción [**XTYP \_ Connect**](xtyp-connect.md) mediante la comparación de la cadena del nombre de tema que controla el ddeml que se pasa al servidor con cada elemento de la matriz de nombres de tema cadena de identificadores admitidos por el servidor.</span><span class="sxs-lookup"><span data-stu-id="b6904-137">In the following example, the server responds to the [**XTYP\_CONNECT**](xtyp-connect.md) transaction by comparing the topic name string handle the DDEML passed to the server with each element in the array of topic name string handles the server supports.</span></span> <span data-ttu-id="b6904-138">Si el servidor encuentra una coincidencia, establece la conversación.</span><span class="sxs-lookup"><span data-stu-id="b6904-138">If the server finds a match, it establishes the conversation.</span></span>


```
#define CTOPICS 5 
 
HSZ hsz1;                  // string handle passed by DDEML 
HSZ ahszTopics[CTOPICS];   // array of supported topics 
int i;                     // loop counter 
 
// Use a switch statement to examine transaction types. 
// Here is the connect case.
 
    case XTYP_CONNECT: 
        for (i = 0; i < CTOPICS; i++) 
        { 
            if (hsz1 == ahszTopics[i]) 
                return TRUE;   // establish a conversation 
        } 
 
        return FALSE; // Topic not supported; deny conversation.  
 
// Process other transaction types. 
```



<span data-ttu-id="b6904-139">Si el servidor devuelve **true** en respuesta a la transacción [**XTYP \_ Connect**](xtyp-connect.md) , el ddeml envía una transacción de [**\_ \_ confirmación XTYP Connect**](xtyp-connect-confirm.md) a la función de devolución de llamada DDE del servidor.</span><span class="sxs-lookup"><span data-stu-id="b6904-139">If the server returns **TRUE** in response to the [**XTYP\_CONNECT**](xtyp-connect.md) transaction, the DDEML sends an [**XTYP\_CONNECT\_CONFIRM**](xtyp-connect-confirm.md) transaction to the server's DDE callback function.</span></span> <span data-ttu-id="b6904-140">El servidor puede obtener el identificador de la conversación procesando esta transacción.</span><span class="sxs-lookup"><span data-stu-id="b6904-140">The server can obtain the handle to the conversation by processing this transaction.</span></span>

<span data-ttu-id="b6904-141">Un cliente puede establecer una conversación comodín especificando **null** para el identificador de cadena del nombre de servicio, el identificador de cadena de nombre de tema o ambos en una llamada a [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect).</span><span class="sxs-lookup"><span data-stu-id="b6904-141">A client can establish a wildcard conversation by specifying **NULL** for the service name string handle, the topic name string handle, or both in a call to [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect).</span></span> <span data-ttu-id="b6904-142">Si al menos uno de los identificadores de cadena es **null**, ddeml envía la transacción [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md) a las funciones de devolución de llamada de todas las aplicaciones DDE (excepto las que filtran la transacción **XTYP \_ WILDCONNECT** ).</span><span class="sxs-lookup"><span data-stu-id="b6904-142">If at least one of the string handles is **NULL**, the DDEML sends the [**XTYP\_WILDCONNECT**](xtyp-wildconnect.md) transaction to the callback functions of all DDE applications (except those that filter the **XTYP\_WILDCONNECT** transaction).</span></span> <span data-ttu-id="b6904-143">Cada aplicación de servidor debe responder devolviendo un identificador de datos que identifica una matriz terminada en NULL de estructuras [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) .</span><span class="sxs-lookup"><span data-stu-id="b6904-143">Each server application should respond by returning a data handle that identifies a null-terminated array of [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) structures.</span></span> <span data-ttu-id="b6904-144">Si la aplicación de servidor no ha llamado a [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) para registrar sus nombres de servicio y si el filtrado está activado, el servidor no recibe transacciones de **XTYP \_ WILDCONNECT** .</span><span class="sxs-lookup"><span data-stu-id="b6904-144">If the server application has not called [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) to register its service names and if filtering is on, the server does not receive **XTYP\_WILDCONNECT** transactions.</span></span> <span data-ttu-id="b6904-145">Para obtener más información sobre los identificadores de datos, vea [Administración de datos](data-management.md).</span><span class="sxs-lookup"><span data-stu-id="b6904-145">For more information about data handles, see [Data Management](data-management.md).</span></span>

<span data-ttu-id="b6904-146">La matriz debe contener una estructura para cada par nombre de servicio y nombre de tema que coincida con el par especificado por el cliente.</span><span class="sxs-lookup"><span data-stu-id="b6904-146">The array must contain one structure for each service name and topic name pair that matches the pair specified by the client.</span></span> <span data-ttu-id="b6904-147">DDEML selecciona uno de los pares para establecer una conversación y devuelve al cliente un identificador que identifica la conversación.</span><span class="sxs-lookup"><span data-stu-id="b6904-147">The DDEML selects one of the pairs to establish a conversation and returns to the client a handle that identifies the conversation.</span></span> <span data-ttu-id="b6904-148">El DDEML envía la transacción de [**\_ \_ confirmación de conexión de XTYP**](xtyp-connect-confirm.md) al servidor (a menos que el servidor filtre esta transacción).</span><span class="sxs-lookup"><span data-stu-id="b6904-148">The DDEML sends the [**XTYP\_CONNECT\_CONFIRM**](xtyp-connect-confirm.md) transaction to the server (unless the server filters this transaction).</span></span> <span data-ttu-id="b6904-149">En el ejemplo siguiente se muestra una respuesta de servidor típica a la transacción [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="b6904-149">The following example shows a typical server response to the [**XTYP\_WILDCONNECT**](xtyp-wildconnect.md) transaction.</span></span>


```
#define CTOPICS 2 
 
UINT uType; 
HSZPAIR ahszp[(CTOPICS + 1)]; 
HSZ ahszTopicList[CTOPICS]; 
HSZ hszServ, hszTopic; 
WORD i, j; 
 
if (uType == XTYP_WILDCONNECT) 
{ 
    // Scan the topic list and create an array of HSZPAIR structures. 
 
    j = 0; 
    for (i = 0; i < CTOPICS; i++) 
    { 
        if (hszTopic == (HSZ) NULL || 
                hszTopic == ahszTopicList[i]) 
        { 
            ahszp[j].hszSvc = hszServ; 
            ahszp[j++].hszTopic = ahszTopicList[i]; 
        } 
    } 
 
    // End the list with an HSZPAIR structure that contains NULL 
    // string handles as its members. 
 
    ahszp[j].hszSvc = NULL; 
    ahszp[j++].hszTopic = NULL; 
 
    // Return a handle to a global memory object containing the 
    // HSZPAIR structures. 
 
    return DdeCreateDataHandle( 
        idInst,          // instance identifier 
        (LPBYTE) &ahszp, // pointer to HSZPAIR array 
        sizeof(HSZ) * j, // length of the array 
        0,               // start at the beginning 
        (HSZ) NULL,      // no item name string 
        0,               // return the same format 
        0);              // let the system own it 
} 
```



<span data-ttu-id="b6904-150">Tanto el cliente como el servidor pueden finalizar una conversación en cualquier momento llamando a la función [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) .</span><span class="sxs-lookup"><span data-stu-id="b6904-150">Either the client or the server can terminate a conversation at any time by calling the [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) function.</span></span> <span data-ttu-id="b6904-151">Esta función hace que la función de devolución de llamada del asociado de la conversación reciba la transacción de desconexión [**XTYP \_**](xtyp-disconnect.md) (a menos que el asociado especifique la \_ marca de filtro omitir \_ desconexiones de CBF).</span><span class="sxs-lookup"><span data-stu-id="b6904-151">This function causes the callback function of the partner in the conversation to receive the [**XTYP\_DISCONNECT**](xtyp-disconnect.md) transaction (unless the partner specified the CBF\_SKIP\_DISCONNECTS filter flag).</span></span> <span data-ttu-id="b6904-152">Normalmente, una aplicación responde a la transacción **XTYP \_ Disconnect** mediante la función [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) para obtener información sobre la conversación que finalizó.</span><span class="sxs-lookup"><span data-stu-id="b6904-152">Typically, an application responds to the **XTYP\_DISCONNECT** transaction by using the [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) function to obtain information about the conversation that terminated.</span></span> <span data-ttu-id="b6904-153">Después de que la función de devolución de llamada devuelva el procesamiento de la transacción **XTYP \_ Disconnect** , el identificador de conversación ya no es válido.</span><span class="sxs-lookup"><span data-stu-id="b6904-153">After the callback function returns from processing the **XTYP\_DISCONNECT** transaction, the conversation handle is no longer valid.</span></span>

<span data-ttu-id="b6904-154">Una aplicación cliente que recibe una transacción [**XTYP \_ Disconnect**](xtyp-disconnect.md) en su función de devolución de llamada DDE puede intentar restablecer la conversación mediante una llamada a la función [**DdeReconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddereconnect) .</span><span class="sxs-lookup"><span data-stu-id="b6904-154">A client application that receives an [**XTYP\_DISCONNECT**](xtyp-disconnect.md) transaction in its DDE callback function can attempt to reestablish the conversation by calling the [**DdeReconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddereconnect) function.</span></span> <span data-ttu-id="b6904-155">El cliente debe llamar a **DdeReconnect** desde la función de devolución de llamada DDE.</span><span class="sxs-lookup"><span data-stu-id="b6904-155">The client must call **DdeReconnect** from within its DDE callback function.</span></span>

## <a name="multiple-conversations"></a><span data-ttu-id="b6904-156">Varias conversaciones</span><span class="sxs-lookup"><span data-stu-id="b6904-156">Multiple Conversations</span></span>

<span data-ttu-id="b6904-157">Una aplicación cliente puede utilizar la función [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) para determinar si hay algún servidor de interés disponible en el sistema.</span><span class="sxs-lookup"><span data-stu-id="b6904-157">A client application can use the [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) function to determine whether any servers of interest are available in the system.</span></span> <span data-ttu-id="b6904-158">Un cliente especifica un nombre de servicio y un nombre de tema cuando llama a **DdeConnectList**, lo que hace que el ddeml emita la transacción [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md) a las funciones de devolución de llamada DDE de todos los servidores que coincidan con el nombre de servicio (excepto los que filtran la transacción).</span><span class="sxs-lookup"><span data-stu-id="b6904-158">A client specifies a service name and topic name when it calls **DdeConnectList**, causing the DDEML to broadcast the [**XTYP\_WILDCONNECT**](xtyp-wildconnect.md) transaction to the DDE callback functions of all servers that match the service name (except those that filter the transaction).</span></span> <span data-ttu-id="b6904-159">La función de devolución de llamada de un servidor debe devolver un identificador de datos que identifique una matriz terminada en NULL de estructuras [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) .</span><span class="sxs-lookup"><span data-stu-id="b6904-159">A server's callback function should return a data handle that identifies a null-terminated array of [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) structures.</span></span> <span data-ttu-id="b6904-160">La matriz debe contener una estructura para cada par nombre de servicio y nombre de tema que coincida con el par especificado por el cliente.</span><span class="sxs-lookup"><span data-stu-id="b6904-160">The array should contain one structure for each service name and topic name pair that matches the pair specified by the client.</span></span> <span data-ttu-id="b6904-161">DDEML establece una conversación para cada estructura **HSZPAIR** rellenada por el servidor y devuelve un identificador de la lista de conversaciones al cliente.</span><span class="sxs-lookup"><span data-stu-id="b6904-161">The DDEML establishes a conversation for each **HSZPAIR** structure filled by the server and returns a conversation list handle to the client.</span></span> <span data-ttu-id="b6904-162">El servidor recibe el identificador de conversación por medio de la transacción [**XTYP \_ Connect**](xtyp-connect.md) (a menos que el servidor filtre esta transacción).</span><span class="sxs-lookup"><span data-stu-id="b6904-162">The server receives the conversation handle by way of the [**XTYP\_CONNECT**](xtyp-connect.md) transaction (unless the server filters this transaction).</span></span>

<span data-ttu-id="b6904-163">Un cliente puede especificar **null** para el nombre del servicio, el nombre del tema o ambos cuando llama a [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist).</span><span class="sxs-lookup"><span data-stu-id="b6904-163">A client can specify **NULL** for the service name, topic name, or both when it calls [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist).</span></span> <span data-ttu-id="b6904-164">Si el nombre del servicio es **null**, todos los servidores del sistema que admitan el nombre de tema especificado responderán.</span><span class="sxs-lookup"><span data-stu-id="b6904-164">If the service name is **NULL**, all servers in the system that support the specified topic name respond.</span></span> <span data-ttu-id="b6904-165">Se establece una conversación con cada servidor que responde, incluidas varias instancias del mismo servidor.</span><span class="sxs-lookup"><span data-stu-id="b6904-165">A conversation is established with each responding server, including multiple instances of the same server.</span></span> <span data-ttu-id="b6904-166">Si el nombre del tema es **null**, se establece una conversación en cada tema reconocido por cada servidor que coincida con el nombre del servicio.</span><span class="sxs-lookup"><span data-stu-id="b6904-166">If the topic name is **NULL**, a conversation is established on each topic recognized by each server that matches the service name.</span></span>

<span data-ttu-id="b6904-167">Un cliente puede usar las funciones [**DdeQueryNextServer**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) y [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) para identificar los servidores que responden a [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist).</span><span class="sxs-lookup"><span data-stu-id="b6904-167">A client can use the [**DdeQueryNextServer**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) and [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) functions to identify the servers that respond to [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist).</span></span> <span data-ttu-id="b6904-168">**DdeQueryNextServer** devuelve el siguiente identificador de conversación en una lista de conversaciones y **DdeQueryConvInfo** rellena una estructura [**CONVINFO**](/windows/win32/api/ddeml/ns-ddeml-convinfo) con información sobre la conversación.</span><span class="sxs-lookup"><span data-stu-id="b6904-168">**DdeQueryNextServer** returns the next conversation handle in a conversation list, and **DdeQueryConvInfo** fills a [**CONVINFO**](/windows/win32/api/ddeml/ns-ddeml-convinfo) structure with information about the conversation.</span></span> <span data-ttu-id="b6904-169">El cliente puede mantener los identificadores de conversación que necesita y descartar el resto de la lista de conversaciones.</span><span class="sxs-lookup"><span data-stu-id="b6904-169">The client can keep the conversation handles that it needs and discard the rest from the conversation list.</span></span>

<span data-ttu-id="b6904-170">En el ejemplo siguiente se usa [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) para establecer conversaciones con todos los servidores que admiten el tema del sistema y, a continuación, se usan las funciones [**DdeQueryNextServer**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) y [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) para obtener los identificadores de cadena del nombre de servicio de los servidores y almacenarlos en un búfer.</span><span class="sxs-lookup"><span data-stu-id="b6904-170">The following example uses [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) to establish conversations with all servers that support the System topic and then uses the [**DdeQueryNextServer**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) and [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) functions to obtain the servers' service name string handles and store them in a buffer.</span></span>


```
HCONVLIST hconvList; // conversation list 
DWORD idInst;        // instance identifier 
HSZ hszSystem;       // System topic 
HCONV hconv = NULL;  // conversation handle 
CONVINFO ci;         // holds conversation data 
UINT cConv = 0;      // count of conv. handles 
HSZ *pHsz, *aHsz;    // point to string handles 
 
// Connect to all servers that support the System topic. 
 
hconvList = DdeConnectList(idInst, NULL, hszSystem, NULL, NULL); 
 
// Count the number of handles in the conversation list. 
 
while ((hconv = DdeQueryNextServer(hconvList, hconv)) != NULL) 
    cConv++; 
 
// Allocate a buffer for the string handles. 
 
hconv = NULL; 
aHsz = (HSZ *) LocalAlloc(LMEM_FIXED, cConv * sizeof(HSZ)); 
 
// Copy the string handles to the buffer. 
 
pHsz = aHsz; 
while ((hconv = DdeQueryNextServer(hconvList, hconv)) != NULL) 
{ 
    DdeQueryConvInfo(hconv, QID_SYNC, (PCONVINFO) &ci); 
    DdeKeepStringHandle(idInst, ci.hszSvcPartner); 
    *pHsz++ = ci.hszSvcPartner; 
} 
 
// Use the handles; converse with the servers. 
 
// Free the memory and terminate the conversations. 
 
LocalFree((HANDLE) aHsz); 
DdeDisconnectList(hconvList); 
```



<span data-ttu-id="b6904-171">Una aplicación puede finalizar una conversación individual en una lista de conversaciones llamando a la función [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) .</span><span class="sxs-lookup"><span data-stu-id="b6904-171">An application can terminate an individual conversation in a conversation list by calling the [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) function.</span></span> <span data-ttu-id="b6904-172">Una aplicación puede finalizar todas las conversaciones de una lista de conversaciones llamando a la función [**DdeDisconnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnectlist) .</span><span class="sxs-lookup"><span data-stu-id="b6904-172">An application can terminate all conversations in a conversation list by calling the [**DdeDisconnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnectlist) function.</span></span> <span data-ttu-id="b6904-173">Ambas funciones hacen que el DDEML envíe transacciones de [**\_ desconexión de XTYP**](xtyp-disconnect.md) a la función de devolución de llamada DDE de cada socio.</span><span class="sxs-lookup"><span data-stu-id="b6904-173">Both functions cause the DDEML to send [**XTYP\_DISCONNECT**](xtyp-disconnect.md) transactions to each partner's DDE callback function.</span></span> <span data-ttu-id="b6904-174">**DdeDisconnectList** envía una transacción de **\_ desconexión de XTYP** para cada identificador de conversación de la lista.</span><span class="sxs-lookup"><span data-stu-id="b6904-174">**DdeDisconnectList** sends an **XTYP\_DISCONNECT** transaction for each conversation handle in the list.</span></span>

<span data-ttu-id="b6904-175">Un cliente puede recuperar una lista de identificadores de conversación en una lista de conversaciones pasando un identificador de lista de conversación existente a [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist).</span><span class="sxs-lookup"><span data-stu-id="b6904-175">A client can retrieve a list of the conversation handles in a conversation list by passing an existing conversation list handle to [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist).</span></span> <span data-ttu-id="b6904-176">El proceso de enumeración quita los identificadores de las conversaciones terminadas de la lista y se agregan las conversaciones no duplicadas que se ajustan al nombre de servicio y el nombre de tema especificados.</span><span class="sxs-lookup"><span data-stu-id="b6904-176">The enumeration process removes the handles of terminated conversations from the list, and nonduplicate conversations that fit the specified service name and topic name are added.</span></span>

<span data-ttu-id="b6904-177">Si [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) especifica un identificador de lista de conversaciones existente, la función crea una nueva lista de conversación que contiene los identificadores de las nuevas conversaciones y los identificadores de la lista existente.</span><span class="sxs-lookup"><span data-stu-id="b6904-177">If [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) specifies an existing conversation list handle, the function creates a new conversation list that contains the handles of any new conversations and the handles from the existing list.</span></span>

<span data-ttu-id="b6904-178">Si existen conversaciones duplicadas, [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) intenta evitar los identificadores de conversación duplicados en la lista de conversaciones.</span><span class="sxs-lookup"><span data-stu-id="b6904-178">If duplicate conversations exist, [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) attempts to prevent duplicate conversation handles in the conversation list.</span></span> <span data-ttu-id="b6904-179">Una conversación duplicada es una segunda conversación con el mismo servidor en el mismo nombre de servicio y el mismo nombre de tema.</span><span class="sxs-lookup"><span data-stu-id="b6904-179">A duplicate conversation is a second conversation with the same server on the same service name and topic name.</span></span> <span data-ttu-id="b6904-180">Dos de estas conversaciones tendrían controladores diferentes, pero identificarían la misma conversación.</span><span class="sxs-lookup"><span data-stu-id="b6904-180">Two such conversations would have different handles, yet they would identify the same conversation.</span></span>

 

 




