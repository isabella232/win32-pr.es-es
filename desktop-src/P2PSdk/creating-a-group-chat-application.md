---
description: En este tema se proporcionan ejemplos de código pertinentes para los pasos principales para desarrollar una aplicación de chat con la API de agrupación del mismo nivel, lo que proporciona un contexto para cada llamada API.
ms.assetid: 47bb8606-0b7b-4e71-9d6f-c400d6a82e43
title: Creación de una aplicación de chat de grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcb8f9458f8e01bea86e42f0cd976395e951bda52f13af46952479d5810e46c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011663"
---
# <a name="creating-a-group-chat-application"></a>Creación de una aplicación de chat de grupo

En este tema se proporcionan ejemplos de código pertinentes para los pasos principales para desarrollar una aplicación de chat con la API de agrupación del mismo nivel, lo que proporciona un contexto para cada llamada API. No se incluyen los comportamientos de la interfaz de usuario ni la estructura general de la aplicación.

> [!Note]  
> La aplicación de ejemplo chat de grupo del mismo nivel completa se proporciona en el SDK del mismo nivel. En este tema se hace referencia a las funciones proporcionadas en el ejemplo.

 

## <a name="initializing-a-group"></a>Inicialización de un grupo

El primer paso al construir una aplicación de chat es inicializar la infraestructura de agrupación del mismo nivel mediante una llamada a [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) con la versión más alta admitida. En este caso, **LA VERSIÓN DEL GRUPO \_ \_ DEL** MISMO NIVEL se definirá en el archivo de encabezado de la aplicación. La versión admitida realmente por la infraestructura se devuelve en **peerVersion**.


```C++
    PEER_VERSION_DATA peerVersion;

    hr = PeerGroupStartup(PEER_GROUP_VERSION, &peerVersion);
    if (FAILED(hr))
    {
        return hr;
    }
```



## <a name="creating-a-group"></a>Crear un grupo

Una aplicación de chat debe ser capaz de crear un grupo del mismo nivel si no hay ningún grupo disponible para unirse o si el usuario de la aplicación desea crear uno nuevo. Para ello, debe crear una estructura [**PROPIEDADES \_ \_**](/windows/desktop/api/P2P/ns-p2p-peer_group_properties) DE GRUPO DEL MISMO NIVEL y rellenarla con la configuración inicial del grupo, incluido el clasificador del grupo del mismo nivel, el nombre descriptivo, el nombre del mismo nivel del creador y la duración de la presencia. Una vez que se ha rellenado esta estructura, se pasa a [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate).


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



## <a name="issuing-invitations"></a>Emisión de invitaciones

Al emitir una invitación, se deben obtener los GFC de los invitados. Para obtenerlos, llame a [**PeerIdentityGetXML**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml) en el invitado con su nombre de identidad. Si se realiza correctamente, la información de identidad (el XML que contiene el certificado codificado en base 64 con la clave pública RSA) se escribe en una ubicación externa (un archivo, en este ejemplo) donde el invitador puede obtenerlo y usarlo para crear una invitación.

En este punto, se debe establecer un mecanismo para la entrega de la invitación al invitado. Puede ser un correo electrónico u otro método seguro de intercambio de archivos. En el ejemplo siguiente, la invitación se escribe en un archivo que, a continuación, se puede transferir al equipo del invitado.


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



Las invitaciones, como las identidades, también se emiten externamente. En este ejemplo, la invitación se escribe en un archivo con **fputws** donde el invitado puede obtenerla y usarla cuando llama a [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).


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



## <a name="joining-a-peer-group"></a>Unión a un grupo del mismo nivel

Si el elemento del mismo nivel intenta unirse a un grupo del mismo nivel creado por otro elemento del mismo nivel, necesitará una invitación de ese mismo nivel. Las invitaciones las entrega un proceso externo o una aplicación al invitado y se guardan en un archivo local, especificado en el ejemplo siguiente *como pwzFileName*. El blob XML de invitación se lee del archivo en **wzInvitation** y se pasa a [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).


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



## <a name="register-for-peer-events"></a>Registro para eventos del mismo nivel

Antes de conectarse, debe registrarse para cada evento del mismo nivel pertinente para la aplicación. En el ejemplo siguiente, se registra para los siguientes eventos:

-   SE HA \_ CAMBIADO EL REGISTRO DE EVENTOS DEL GRUPO DEL MISMO \_ \_ \_ NIVEL. Puesto que los registros se usarán para contener mensajes de chat públicos, se debe notificar a la aplicación cada vez que se agrega uno nuevo. Cuando se recibe este evento del mismo nivel, los datos del evento exponen el registro con el mensaje de chat. Las aplicaciones solo deben registrarse para los tipos de registro que pretenden controlar directamente.
-   MIEMBRO DE \_ EVENTO DEL GRUPO DEL MISMO NIVEL \_ \_ \_ CAMBIADO. La aplicación debe recibir una notificación cuando los miembros se unan o abandonen el grupo del mismo nivel para que la lista de participantes se pueda actualizar en consecuencia.
-   SE HA \_ CAMBIADO EL ESTADO DEL EVENTO DEL GRUPO DEL MISMO \_ \_ \_ NIVEL. Los cambios en el estado del grupo del mismo nivel se deben transmitir a la aplicación. Un miembro del grupo del mismo nivel solo se considera disponible dentro del grupo del mismo nivel cuando su estado indica que está conectado al grupo, sincronizado con la base de datos de registros del grupo del mismo nivel y escuchando activamente las actualizaciones de registros.
-   CONEXIÓN \_ DIRECTA DE EVENTOS DE GRUPO DEL MISMO \_ \_ \_ NIVEL. Los mensajes privados entre dos miembros y los intercambios de datos deben realizarse a través de una conexión directa, por lo que la aplicación debe ser capaz de controlar las solicitudes de conexión directa.
-   DATOS \_ \_ ENTRANTES DE \_ EVENTOS DE GRUPO DEL MISMO \_ NIVEL. Después de iniciar una conexión directa, este evento del mismo nivel avisa a la aplicación de que se ha recibido un mensaje privado.


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



## <a name="connecting-to-a-peer-group"></a>Conexión a un grupo del mismo nivel

Una vez creado o unido al grupo y registrado para los eventos adecuados, es el momento de irse en línea y comenzar una sesión de chat activa. Para ello, llame a [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) y pase el identificador de grupo obtenido de [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate) o [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin). Después de llamar a esto, los mensajes de chat se recibirán como eventos DE REGISTRO DE EVENTOS DE GRUPO DEL MISMO NIVEL \_ \_ \_ \_ CAMBIADOS.

## <a name="obtaining-a-list-of-peer-group-members"></a>Obtener una lista de miembros del grupo del mismo nivel

Obtener una lista de miembros conectados al grupo del mismo nivel es sencillo: llame a [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers) para recuperar la lista de miembros del grupo y, a continuación, llame iterativamente a [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) hasta que se recuperen todos los miembros. Debe llamar a [**PeerFreeData después**](/windows/desktop/api/P2P/nf-p2p-peerfreedata) de procesar cada estructura de miembro y debe cerrar la enumeración llamando a [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) cuando se complete el procesamiento.


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



## <a name="sending-a-chat-message"></a>Envío de un mensaje de chat

En este ejemplo, se envía un mensaje de chat colocándolo en el campo **de datos** de una estructura [**PEER \_ RECORD.**](/windows/desktop/api/P2P/ns-p2p-peer_record) El registro se agrega a los registros del grupo del mismo nivel mediante una llamada a [**PeerGroupAddRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord), que lo publicará y genera el evento PEER GROUP EVENT RECORD CHANGED en todos los pares que participan en el grupo del mismo \_ \_ \_ \_ nivel.


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



## <a name="receiving-a-chat-message"></a>Recepción de un mensaje de chat

Para recibir el mensaje de chat, cree una función de devolución de llamada para el evento PEER GROUP EVENT RECORD CHANGED que llama \_ a una función similar a la \_ \_ \_ siguiente. El registro se obtiene mediante una llamada a [**PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) en los datos de evento recibidos por una llamada anterior a [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) en la función de devolución de llamada. El mensaje de chat se almacena en el **campo de** datos de este registro.


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



 

 



