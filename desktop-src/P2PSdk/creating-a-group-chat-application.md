---
description: En este tema se proporcionan ejemplos de código relevantes para los principales pasos del desarrollo de una aplicación de chat con la API de agrupación del mismo nivel, que proporciona un contexto para cada llamada de API.
ms.assetid: 47bb8606-0b7b-4e71-9d6f-c400d6a82e43
title: Creación de una aplicación de chat de grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 676d4e9913934024df3131c0f965a5d85477d148
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360707"
---
# <a name="creating-a-group-chat-application"></a><span data-ttu-id="ebf1f-103">Creación de una aplicación de chat de grupo</span><span class="sxs-lookup"><span data-stu-id="ebf1f-103">Creating a Group Chat Application</span></span>

<span data-ttu-id="ebf1f-104">En este tema se proporcionan ejemplos de código relevantes para los principales pasos del desarrollo de una aplicación de chat con la API de agrupación del mismo nivel, que proporciona un contexto para cada llamada de API.</span><span class="sxs-lookup"><span data-stu-id="ebf1f-104">This topic provides relevant code samples for the major steps of developing a chat application with the Peer Grouping API, providing a context for each API call.</span></span> <span data-ttu-id="ebf1f-105">No se incluyen los comportamientos de la interfaz de usuario ni la estructura general de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ebf1f-105">UI behaviors and overall application structure are not included.</span></span>

> [!Note]  
> <span data-ttu-id="ebf1f-106">La aplicación de ejemplo completa de chat de grupo del mismo nivel se proporciona en el SDK del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="ebf1f-106">The complete Peer Group Chat sample application is provided in the Peer SDK.</span></span> <span data-ttu-id="ebf1f-107">En este tema se hace referencia a las funciones proporcionadas en el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ebf1f-107">This topic references functions provided within the sample.</span></span>

 

## <a name="initializing-a-group"></a><span data-ttu-id="ebf1f-108">Inicialización de un grupo</span><span class="sxs-lookup"><span data-stu-id="ebf1f-108">Initializing a Group</span></span>

<span data-ttu-id="ebf1f-109">El primer paso al crear una aplicación de chat es inicializar la infraestructura de agrupación del mismo nivel llamando a [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) con la versión más alta admitida.</span><span class="sxs-lookup"><span data-stu-id="ebf1f-109">The first step when constructing a chat application is to initialize the Peer Grouping Infrastructure by calling [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) with the highest supported version.</span></span> <span data-ttu-id="ebf1f-110">En este caso, **la \_ \_ versión del grupo del mismo nivel** se definirá en el archivo de encabezado de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ebf1f-110">In this case, **PEER\_GROUP\_VERSION** will be defined in the application header file.</span></span> <span data-ttu-id="ebf1f-111">La versión admitida realmente por la infraestructura se devuelve en **peerVersion**.</span><span class="sxs-lookup"><span data-stu-id="ebf1f-111">The version actually supported by the infrastructure is returned in **peerVersion**.</span></span>


```C++
    PEER_VERSION_DATA peerVersion;

    hr = PeerGroupStartup(PEER_GROUP_VERSION, &peerVersion);
    if (FAILED(hr))
    {
        return hr;
    }
```



## <a name="creating-a-group"></a><span data-ttu-id="ebf1f-112">Creación de un grupo</span><span class="sxs-lookup"><span data-stu-id="ebf1f-112">Creating a Group</span></span>

<span data-ttu-id="ebf1f-113">Una aplicación de chat debe ser capaz de crear un grupo del mismo nivel si no hay ningún grupo disponible para unirse o si el usuario de la aplicación desea crear uno nuevo.</span><span class="sxs-lookup"><span data-stu-id="ebf1f-113">A chat application must be able to create a peer group if no group is available to join, or if the application user wants to create a new one.</span></span> <span data-ttu-id="ebf1f-114">Para ello, debe crear una estructura de [**\_ \_ propiedades de grupo del mismo nivel**](/windows/desktop/api/P2P/ns-p2p-peer_group_properties) y rellenarla con la configuración inicial del grupo, incluido el clasificador del grupo del mismo nivel, el nombre descriptivo, el nombre del mismo nivel del creador y la duración de la presencia.</span><span class="sxs-lookup"><span data-stu-id="ebf1f-114">To do this, you must create a [**PEER\_GROUP\_PROPERTIES**](/windows/desktop/api/P2P/ns-p2p-peer_group_properties) structure and populate it with the initial settings for the group, including the classifier for the peer group, the friendly name, the creator's peer name, and the presence lifetime.</span></span> <span data-ttu-id="ebf1f-115">Una vez que se ha rellenado esta estructura, se pasa a [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate).</span><span class="sxs-lookup"><span data-stu-id="ebf1f-115">Once this structure has been populated, you pass it to [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate).</span></span>


```C++
//-----------------------------------------------------------------------------
// Function: CreateGroup
//
// Purpose:  Creates a new group with the friendly name.
//
// Returns:  HRESULT
//
HRESULT CreateGroup(PCWSTR pwzName, PCWSTR pwzIdentity)
{
    HRESULT hr = S_OK;
    PEER_GROUP_PROPERTIES props = {0};

    if (SUCCEEDED(hr))
    {
        if ((NULL == pwzName) || (0 == *pwzName))
        {
            hr = E_INVALIDARG;
            DisplayHrError(L"Please enter a group name.", hr);
        }
    }

    if (SUCCEEDED(hr))
    {
        CleanupGroup( );

        props.dwSize = sizeof(props);
        props.pwzClassifier = L"SampleChatGroup";
        props.pwzFriendlyName = (PWSTR) pwzName;
        props.pwzCreatorPeerName = (PWSTR) pwzIdentity;

        hr = PeerGroupCreate(&props, &g_hGroup);
        if (FAILED(hr))
        {
            DisplayHrError(L"Failed to create a new group.", hr);
        }
    }

    if (SUCCEEDED(hr))
    {
        hr = PrepareToChat( );
    }

    return hr;
}
```



## <a name="issuing-invitations"></a><span data-ttu-id="ebf1f-116">Emitir invitaciones</span><span class="sxs-lookup"><span data-stu-id="ebf1f-116">Issuing Invitations</span></span>

<span data-ttu-id="ebf1f-117">Al emitir una invitación, se debe obtener el GMCs de los invitados.</span><span class="sxs-lookup"><span data-stu-id="ebf1f-117">When issuing an invitation, the GMCs of the invitees must be obtained.</span></span> <span data-ttu-id="ebf1f-118">Estos se pueden obtener llamando a [**PeerIdentityGetXML**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml) en la invitación con su nombre de identidad.</span><span class="sxs-lookup"><span data-stu-id="ebf1f-118">These can obtained by calling [**PeerIdentityGetXML**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml) on the invitee with their identity name.</span></span> <span data-ttu-id="ebf1f-119">Si se realiza correctamente, la información de identidad (el XML que contiene el certificado codificado en base 64 con la clave pública RSA) se escribe en una ubicación externa (un archivo, en este ejemplo) en el que el invitador puede obtenerlo y usarlo para crear una invitación.</span><span class="sxs-lookup"><span data-stu-id="ebf1f-119">If successful, the identity information (the XML that contains the base-64 encoded certificate with the RSA public key) is written to an external location (a file, in this sample) where the inviter can obtain it and use it to create an invitation.</span></span>

<span data-ttu-id="ebf1f-120">En este momento, se debe establecer un mecanismo para la entrega de la invitación al invitado.</span><span class="sxs-lookup"><span data-stu-id="ebf1f-120">At this point, a mechanism for the delivery of the invitation to the invitee must be established.</span></span> <span data-ttu-id="ebf1f-121">Puede ser correo electrónico u otro método seguro de intercambio de archivos.</span><span class="sxs-lookup"><span data-stu-id="ebf1f-121">This can be email or another secure method of file exchange.</span></span> <span data-ttu-id="ebf1f-122">En el ejemplo siguiente, la invitación se escribe en un archivo que se puede transferir al equipo del invitado.</span><span class="sxs-lookup"><span data-stu-id="ebf1f-122">In the sample below, the invitation is written to a file which can then be transferred to the invitee's computer.</span></span>


```C++
//-----------------------------------------------------------------------------
// Function: SaveIdentityInfo
//
// Purpose:  Saves the information for an identity to a file.
//           Displays a message if there was an error.
//
// Returns:  HRESULT
//
HRESULT SaveIdentityInfo(PCWSTR pwzIdentity, PCWSTR pwzFile)
{
    PWSTR pwzXML = NULL;
    HRESULT hr = PeerIdentityGetXML(pwzIdentity, &pwzXML);

    if (FAILED(hr))
    {
        DisplayHrError(L"Unable to retrieve the XML data for the identity.", hr);
    }
    else
    {
        FILE *fp = NULL;
        errno_t err = 0;

        err = _wfopen_s(&fp, pwzFile, L"wb");
        if (err != 0)
        {
            hr = E_FAIL;
            DisplayHrError(L"Please choose a valid path", hr);
        }
        else
        {
            if (fputws(pwzXML, fp) == WEOF)
            {
                hr = E_FAIL;
                DisplayHrError(L"End of file error.", hr);
            }
            fclose(fp);
        }

        PeerFreeData(pwzXML);
    }

    return hr;
}
```



<span data-ttu-id="ebf1f-123">Las invitaciones, como las identidades, también se emiten externamente.</span><span class="sxs-lookup"><span data-stu-id="ebf1f-123">Invitations, like identities, are also issued externally.</span></span> <span data-ttu-id="ebf1f-124">En este ejemplo, la invitación se escribe en un archivo con **fputws** donde el invitado puede obtenerlo y usarlo cuando llama a [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).</span><span class="sxs-lookup"><span data-stu-id="ebf1f-124">In this example, the invitation is written to a file with **fputws** where the invitee can obtain it and use it when it calls [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).</span></span>


```C++
//-----------------------------------------------------------------------------
// Function: CreateInvitation
//
// Purpose:  Creates an invitation file for an identity.
//           Displays a message if there was an error.
//
// Returns:  HRESULT
//
HRESULT CreateInvitation(PCWSTR wzIdentityInfoPath, PCWSTR wzInvitationPath)
{
    HRESULT hr = S_OK;
    WCHAR wzIdentityInfo[MAX_INVITATION] = {0};
    PWSTR pwzInvitation = NULL;
    errno_t  err  = 0;
    FILE *file = NULL;
        
    err = _wfopen_s(&file, wzIdentityInfoPath, L"rb");
    if (err != 0)
    {
        hr = E_FAIL;
        DisplayHrError(L"Please choose a valid path to the identity information file.", hr);
    }
    else
    {
        fread(wzIdentityInfo, sizeof(WCHAR), MAX_INVITATION, file);
        if (ferror(file))
        {
            hr = E_FAIL;
            DisplayHrError(L"File read error occurred.", hr);
        }
        fclose(file);
    }

    if (SUCCEEDED(hr))
    {
        ULONGLONG ulExpire; // adjust time using this structure
        GetSystemTimeAsFileTime((FILETIME *)&ulExpire);

        // 15days in 100 nanoseconds resolution
        ulExpire += ((ULONGLONG) (60 * 60 * 24 * 15)) * ((ULONGLONG)1000*1000*10);

        hr = PeerGroupCreateInvitation(g_hGroup, wzIdentityInfo, (FILETIME*)&ulExpire, 1, (PEER_ROLE_ID*) &PEER_GROUP_ROLE_MEMBER, &pwzInvitation);
        if (FAILED(hr))
        {
            DisplayHrError(L"Failed to create the invitation.", hr);
        }
    }

    if (SUCCEEDED(hr))
    {
        err = _wfopen_s(&file, wzInvitationPath, L"wb");
        if (err != 0)
        {
            hr = E_FAIL;
            DisplayHrError(L"Please choose a valid path to the invitation file.", hr);
        }
        else
        {
            if (fputws(pwzInvitation, file) == WEOF)
            {
                hr = E_FAIL;
                DisplayHrError(L"End of file error.", hr);
            }
            fclose(file);
        }
    }

    PeerFreeData(pwzInvitation);
    return hr;
}
```



## <a name="joining-a-peer-group"></a><span data-ttu-id="ebf1f-125">Unirse a un grupo del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="ebf1f-125">Joining a Peer Group</span></span>

<span data-ttu-id="ebf1f-126">Si el elemento del mismo nivel está intentando unirse a un grupo del mismo nivel creado por otro elemento del mismo nivel, necesitará una invitación de ese mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="ebf1f-126">If the peer is attempting to join a peer group created by another peer, it will need an invitation from that peer.</span></span> <span data-ttu-id="ebf1f-127">Las invitaciones se entregan mediante un proceso externo o una aplicación al invitado y se guardan en un archivo local, especificado en el ejemplo siguiente como *pwzFileName*.</span><span class="sxs-lookup"><span data-stu-id="ebf1f-127">Invitations are delivered by an external process or application to the invitee and saved to a local file, specified in the sample below as *pwzFileName*.</span></span> <span data-ttu-id="ebf1f-128">El BLOB XML de invitación se lee desde el archivo en **wzInvitation** y se pasa a [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).</span><span class="sxs-lookup"><span data-stu-id="ebf1f-128">The invitation XML blob is read from the file into **wzInvitation** and passed to [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).</span></span>


```C++
//-----------------------------------------------------------------------------
// Function: JoinGroup
//
// Purpose:  Uses the invitation to join a group with a specific identity.
//           Displays a message if there was an error.
//
// Returns:  HRESULT
//
HRESULT JoinGroup(PCWSTR pwzIdentity, PCWSTR pwzFileName)
{
    HRESULT hr = S_OK;
    WCHAR wzInvitation[MAX_INVITATION] = {0};
    FILE        *file = NULL;
    errno_t     err;

    err = _wfopen_s(&file, pwzFileName, L"rb");
    if (err !=  0)
    {
        hr = E_FAIL;
        DisplayHrError(L"Error opening group invitation file", hr);
        return hr;
    }
    else
    {
        fread(wzInvitation, sizeof(WCHAR), MAX_INVITATION, file);
        if (ferror(file))
        {
            hr = E_FAIL;
            DisplayHrError(L"File read error occurred.", hr);
        }
        fclose(file);

        hr = PeerGroupJoin(pwzIdentity, wzInvitation, NULL, &g_hGroup);
        if (FAILED(hr))
        {
            DisplayHrError(L"Failed to join group.", hr);
        }
    }

    if (SUCCEEDED(hr))
    {
        hr = PrepareToChat( );
    }

    return hr;
}
```



## <a name="register-for-peer-events"></a><span data-ttu-id="ebf1f-129">Registrar para eventos del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="ebf1f-129">Register for Peer Events</span></span>

<span data-ttu-id="ebf1f-130">Antes de conectarse, debe registrarse para cada evento del mismo nivel correspondiente a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ebf1f-130">Before connecting, you should register for every peer event pertinent to the application.</span></span> <span data-ttu-id="ebf1f-131">En el ejemplo siguiente, se registra para los siguientes eventos:</span><span class="sxs-lookup"><span data-stu-id="ebf1f-131">In the example below, you register for the following events:</span></span>

-   <span data-ttu-id="ebf1f-132">cambio de registro de evento de grupo del mismo nivel \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ebf1f-132">PEER\_GROUP\_EVENT\_RECORD\_CHANGED.</span></span> <span data-ttu-id="ebf1f-133">Dado que los registros se usarán para contener mensajes públicos de chat, se debe notificar a la aplicación cada vez que se agrega una nueva.</span><span class="sxs-lookup"><span data-stu-id="ebf1f-133">Since records will be used to contain public chat messages, the application must be notified every time a new one is added.</span></span> <span data-ttu-id="ebf1f-134">Cuando se recibe este evento del mismo nivel, los datos de evento exponen el registro con el mensaje de chat.</span><span class="sxs-lookup"><span data-stu-id="ebf1f-134">When this peer event is received, the event data exposes the record with the chat message.</span></span> <span data-ttu-id="ebf1f-135">Las aplicaciones solo deben registrarse para los tipos de registro que pretenden controlar directamente.</span><span class="sxs-lookup"><span data-stu-id="ebf1f-135">Applications should only register for those record types they intend to handle directly.</span></span>
-   <span data-ttu-id="ebf1f-136">miembro de evento de grupo del mismo nivel \_ \_ \_ \_ cambiado.</span><span class="sxs-lookup"><span data-stu-id="ebf1f-136">PEER\_GROUP\_EVENT\_MEMBER\_CHANGED.</span></span> <span data-ttu-id="ebf1f-137">Se debe notificar a la aplicación cuando los miembros se unen o salen del grupo del mismo nivel, por lo que la lista de participantes puede actualizarse en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="ebf1f-137">The application must be notified when members join or leave the peer group so the list of participants can be updated accordingly.</span></span>
-   <span data-ttu-id="ebf1f-138">Estado de evento de grupo del mismo nivel \_ \_ \_ \_ cambiado.</span><span class="sxs-lookup"><span data-stu-id="ebf1f-138">PEER\_GROUP\_EVENT\_STATUS\_CHANGED.</span></span> <span data-ttu-id="ebf1f-139">Los cambios en el estado del grupo del mismo nivel deben transmitirse a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ebf1f-139">Changes to the peer group status must be conveyed to the application.</span></span> <span data-ttu-id="ebf1f-140">Solo se considera que un miembro del grupo del mismo nivel está disponible dentro del grupo del mismo nivel cuando su estado indica que está conectado al grupo, sincronizado con la base de datos de registros de grupo del mismo nivel y escuchando activamente las actualizaciones del registro.</span><span class="sxs-lookup"><span data-stu-id="ebf1f-140">A peer group member is only considered to be available within the peer group when its status indicates that it is connected to the group, synchronized with the peer group record database, and actively listening to record updates.</span></span>
-   <span data-ttu-id="ebf1f-141">conexión directa de eventos de grupo del mismo nivel \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ebf1f-141">PEER\_GROUP\_EVENT\_DIRECT\_CONNECTION.</span></span> <span data-ttu-id="ebf1f-142">Los mensajes privados entre dos miembros y los intercambios de datos se deben realizar a través de una conexión directa, por lo que la aplicación debe ser capaz de controlar las solicitudes de conexión directas.</span><span class="sxs-lookup"><span data-stu-id="ebf1f-142">Private messages between two members and exchanges of data must be conducted over a direct connection, so the application must be able to handle direct connection requests.</span></span>
-   <span data-ttu-id="ebf1f-143">\_ \_ datos entrantes del evento de grupo del mismo nivel \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ebf1f-143">PEER\_GROUP\_EVENT\_INCOMING\_DATA.</span></span> <span data-ttu-id="ebf1f-144">Una vez iniciada una conexión directa, este evento del mismo nivel alerta a la aplicación de que se ha recibido un mensaje privado.</span><span class="sxs-lookup"><span data-stu-id="ebf1f-144">After a direct connection is initiated, this peer event alerts the application that a private message has been received.</span></span>


```C++
//-----------------------------------------------------------------------------
// Function: RegisterForEvents
//
// Purpose:  Registers the EventCallback function so it will be called for only
//           those events that are specified.
//
// Returns:  HRESULT
//
HRESULT RegisterForEvents(void)
{
    HRESULT hr = S_OK;
    PEER_GROUP_EVENT_REGISTRATION regs[] = {
        { PEER_GROUP_EVENT_RECORD_CHANGED, &RECORD_TYPE_CHAT_MESSAGE },
        { PEER_GROUP_EVENT_MEMBER_CHANGED, 0 },
        { PEER_GROUP_EVENT_STATUS_CHANGED, 0 },
        { PEER_GROUP_EVENT_DIRECT_CONNECTION, &DATA_TYPE_WHISPER_MESSAGE },
        { PEER_GROUP_EVENT_INCOMING_DATA, 0 },
    };

    g_hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
    if (g_hEvent == NULL)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }
    else
    {
        hr = PeerGroupRegisterEvent(g_hGroup, g_hEvent, celems(regs), regs,  &g_hPeerEvent);
    }

    if (SUCCEEDED(hr))
    {
        if (!RegisterWaitForSingleObject(&g_hWait, g_hEvent, EventCallback, NULL, INFINITE, WT_EXECUTEDEFAULT))
        {
            hr = E_UNEXPECTED;
        }
    }

    return hr;
}
```



## <a name="connecting-to-a-peer-group"></a><span data-ttu-id="ebf1f-145">Conexión a un grupo del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="ebf1f-145">Connecting to a Peer Group</span></span>

<span data-ttu-id="ebf1f-146">Una vez que haya creado o combinado el grupo y registrado para los eventos adecuados, es el momento de conectarse y comenzar una sesión de chat activa.</span><span class="sxs-lookup"><span data-stu-id="ebf1f-146">Having either created or joined the group and registered for the appropriate events, it's time to go online and begin an active chat session.</span></span> <span data-ttu-id="ebf1f-147">Para ello, llame a [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) y pase el identificador de grupo Obtenido de [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate) o [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).</span><span class="sxs-lookup"><span data-stu-id="ebf1f-147">To do this, you call [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) and pass in the group handle obtained from [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate) or [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).</span></span> <span data-ttu-id="ebf1f-148">Después de llamar a, se recibirán mensajes de chat como eventos de cambio de registro de evento de grupo del mismo nivel \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ebf1f-148">After calling this, chat messages will be received as PEER\_GROUP\_EVENT\_RECORD\_CHANGED events.</span></span>

## <a name="obtaining-a-list-of-peer-group-members"></a><span data-ttu-id="ebf1f-149">Obtener una lista de miembros del grupo del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="ebf1f-149">Obtaining a List of Peer Group Members</span></span>

<span data-ttu-id="ebf1f-150">Obtener una lista de miembros conectados al grupo del mismo nivel es simple: llamar a [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers) para recuperar la lista de miembros del grupo y, a continuación, llamar a [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) de forma iterativa hasta que se recuperen todos los miembros.</span><span class="sxs-lookup"><span data-stu-id="ebf1f-150">Obtaining a list of members connected to the peer group is simple: call [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers) to retrieve the list of group members, and then iteratively call [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) until all members are retrieved.</span></span> <span data-ttu-id="ebf1f-151">Debe llamar a [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata) después de procesar cada estructura de miembro y debe cerrar la enumeración mediante una llamada a [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) cuando el procesamiento haya finalizado.</span><span class="sxs-lookup"><span data-stu-id="ebf1f-151">You should call [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata) after you process each member structure, and you must close the enumeration by calling [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) when processing is complete.</span></span>


```C++
//-----------------------------------------------------------------------------
// Function: UpdateParticipantList
//
// Purpose:  Update the list of partipants.
//
// Returns:  nothing
//
void UpdateParticipantList(void)
{
    HRESULT          hr = S_OK;
    HPEERENUM        hPeerEnum = NULL;
    PEER_MEMBER   ** ppMember = NULL;

    ClearParticipantList( );
    if (NULL == g_hGroup)
    {
        return;
    }

    // Retrieve only the members currently present in the group.
    hr = PeerGroupEnumMembers(g_hGroup, PEER_MEMBER_PRESENT, NULL, &hPeerEnum);
    if (SUCCEEDED(hr))
    {
        while (SUCCEEDED(hr))
        {
            ULONG cItem = 1;
            hr = PeerGetNextItem(hPeerEnum, &cItem, (PVOID **) &ppMember);
            if (SUCCEEDED(hr))
            {
                if (0 == cItem)
                {
                    PeerFreeData(ppMember);
                    break;
                }
            }

            if (SUCCEEDED(hr))
            {
                if (0 != ((*ppMember)->dwFlags & PEER_MEMBER_PRESENT))
                {
                    AddParticipantName((*ppMember)->pwzIdentity, (*ppMember)->pCredentialInfo->pwzFriendlyName);
                }
                PeerFreeData(ppMember);
            }
        }

        PeerEndEnumeration(hPeerEnum);
    }
}
```



## <a name="sending-a-chat-message"></a><span data-ttu-id="ebf1f-152">Envío de un mensaje de chat</span><span class="sxs-lookup"><span data-stu-id="ebf1f-152">Sending a Chat Message</span></span>

<span data-ttu-id="ebf1f-153">En este ejemplo, se envía un mensaje de chat colocándolo en el campo de **datos** de una estructura de [**\_ registro del mismo nivel**](/windows/desktop/api/P2P/ns-p2p-peer_record) .</span><span class="sxs-lookup"><span data-stu-id="ebf1f-153">In this example, a chat message is sent by placing it in the **data** field of a [**PEER\_RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record) structure.</span></span> <span data-ttu-id="ebf1f-154">El registro se agrega a los registros de grupo del mismo nivel mediante una llamada a [**PeerGroupAddRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord), que lo publicará y generará el \_ \_ \_ evento de cambio de registro de evento de grupo del mismo nivel \_ en todos los elementos del mismo nivel que participan en el grupo del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="ebf1f-154">The record is added to the peer group records by calling [**PeerGroupAddRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord), which will publish it and raise the PEER\_GROUP\_EVENT\_RECORD\_CHANGED event on all peers participating in the peer group.</span></span>


```C++
//-----------------------------------------------------------------------------
// Function: AddChatRecord
//
// Purpose:  This adds a new chat message record to the group.
//
// Returns:  HRESULT
//
HRESULT AddChatRecord(PCWSTR pwzMessage)
{
    HRESULT     hr = S_OK;
    PEER_RECORD record = {0};
    GUID        idRecord;
    ULONGLONG   ulExpire;
    ULONG cch = (ULONG) wcslen(pwzMessage);

    GetSystemTimeAsFileTime((FILETIME *) &ulExpire);

    // Calculate a 2 minute expiration time in 100 nanosecond resolution
    ulExpire += ((ULONGLONG) 60 * 2) * ((ULONGLONG)1000*1000*10);

    // Set up the record
    record.dwSize = sizeof(record);
    record.data.cbData = (cch+1) * sizeof(WCHAR);
    record.data.pbData = (PBYTE) pwzMessage;
    memcpy(&record.ftExpiration, &ulExpire, sizeof(ulExpire));

    PeerGroupUniversalTimeToPeerTime(g_hGroup, &record.ftExpiration, &record.ftExpiration);

    // Set the record type GUID
    record.type = RECORD_TYPE_CHAT_MESSAGE;

    // Add the record to the database
    hr = PeerGroupAddRecord(g_hGroup, &record, &idRecord);
    if (FAILED(hr))
    {
        DisplayHrError(L"Failed to add a chat record to the group.", hr);
    }

    return hr;
}
```



## <a name="receiving-a-chat-message"></a><span data-ttu-id="ebf1f-155">Recibir un mensaje de chat</span><span class="sxs-lookup"><span data-stu-id="ebf1f-155">Receiving a Chat Message</span></span>

<span data-ttu-id="ebf1f-156">Para recibir el mensaje de chat, cree una función de devolución de llamada para el evento de cambio de registro de evento de grupo del mismo nivel \_ \_ \_ \_ que llama a una función similar a la siguiente.</span><span class="sxs-lookup"><span data-stu-id="ebf1f-156">To receive the chat message, create a callback function for the PEER\_GROUP\_EVENT\_RECORD\_CHANGED event that calls a function similar to one below.</span></span> <span data-ttu-id="ebf1f-157">El registro se obtiene llamando a [**PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) en los datos de evento recibidos por una llamada anterior a [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) en la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="ebf1f-157">The record is obtained by calling [**PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) on the event data received by a previous call to [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) in the callback function.</span></span> <span data-ttu-id="ebf1f-158">El mensaje de chat se almacena en el campo de **datos** de este registro.</span><span class="sxs-lookup"><span data-stu-id="ebf1f-158">The chat message is stored in the **data** field of this record.</span></span>


```C++
//-----------------------------------------------------------------------------
// Function: ProcessRecordChanged
//
// Purpose:  Processes the PEER_GROUP_EVENT_RECORD_CHANGED event.
//
// Returns:  nothing
//
void ProcessRecordChanged(PEER_EVENT_RECORD_CHANGE_DATA * pData)
{
    switch (pData->changeType)
    {
        case PEER_RECORD_ADDED:
            if (IsEqualGUID(&pData->recordType, &RECORD_TYPE_CHAT_MESSAGE))
            {
                PEER_RECORD * pRecord = {0};
                HRESULT hr = PeerGroupGetRecord(g_hGroup, &pData->recordId, &pRecord);
                if (SUCCEEDED(hr))
                {
                    DisplayChatMessage(pRecord->pwzCreatorId, (PCWSTR) pRecord->data.pbData);
                    PeerFreeData(pRecord);
                }
            }
            break;

        case PEER_RECORD_UPDATED:
        case PEER_RECORD_DELETED:
        case PEER_RECORD_EXPIRED:
            break;

        default:
            break;
    }
}
```



 

 



