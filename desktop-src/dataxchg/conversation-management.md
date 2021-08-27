---
title: Administración de conversaciones
description: En este tema se de abordan las conversaciones entre un cliente y un servidor.
ms.assetid: 4e5ff1a1-d46a-4e2a-a37c-8df951f2a1ee
keywords:
- Windows Interfaz de usuario,datos dinámicos Exchange (DDE)
- datos dinámicos Exchange (DDE), conversaciones
- DDE (datos dinámicos Exchange),conversaciones
- intercambio de datos, datos dinámicos Exchange (DDE)
- Windows Interfaz de usuario,datos dinámicos Exchange Management Library (DDEML)
- datos dinámicos Exchange Management Library (DDEML),conversations
- DDEML (datos dinámicos Exchange management library),conversations
- data exchange,datos dinámicos Exchange Management Library (DDEML)
- datos dinámicos Exchange (DDE), varias conversaciones
- DDE (datos dinámicos Exchange),varias conversaciones
- datos dinámicos Exchange Management Library (DDEML), varias conversaciones
- DDEML (datos dinámicos Exchange management library), varias conversaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a3531cc396a3b4d0eca5d7c11e3677aec9ea2ee35dcdac110455daee252f798
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991335"
---
# <a name="conversation-management"></a>Administración de conversaciones

Siempre se establece una conversación entre un cliente y un servidor a petición del cliente. Cuando se establece una conversación, cada asociado recibe un identificador que identifica la conversación. Los asociados usan este identificador en otras datos dinámicos Exchange Management Library (DDEML) para enviar transacciones y administrar la conversación. Un cliente puede solicitar una conversación con un solo servidor o puede solicitar varias conversaciones con uno o varios servidores.

En los temas siguientes se describe cómo una aplicación establece nuevas conversaciones y obtiene información sobre las conversaciones existentes.

-   [Conversaciones únicas](#single-conversations)
-   [Varias conversaciones](#multiple-conversations)

## <a name="single-conversations"></a>Conversaciones únicas

Una aplicación cliente solicita una sola conversación con un servidor llamando a la función [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) y especificando identificadores de cadena que identifican las cadenas que contienen el nombre de servicio de la aplicación de servidor y el nombre del tema para la conversación. DDEML responde enviando la transacción [**XTYP \_ CONNECT**](xtyp-connect.md) a la función de devolución de llamada de datos dinámicos Exchange (DDE) de cada aplicación de servidor que haya registrado un nombre de servicio que coincida con el especificado en **DdeConnect** o que haya desactivado el filtrado de nombres de servicio mediante una llamada a [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice). Un servidor también puede filtrar las **transacciones XTYP \_ CONNECT** especificando la marca de filtro CBF FAIL CONNECTIONS en la \_ función \_ [**DdeInitialize.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) Durante la **transacción XTYP \_ CONNECT,** DDEML pasa el nombre del servicio y el nombre del tema al servidor. El servidor debe examinar los nombres y devolver **TRUE** si admite el nombre de servicio y el par de nombres de tema o **FALSE** si no lo hace.

Si ningún servidor responde positivamente a la solicitud del cliente para conectarse, el cliente recibe **NULL** de [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) y no se establece ninguna conversación. Si un servidor devuelve **TRUE,** se establece una conversación y el cliente recibe un identificador de conversación, un **valor DWORD** que identifica la conversación. El cliente usa el identificador en llamadas DDEML posteriores para obtener datos del servidor. El servidor recibe la [**transacción \_ XTYP CONNECT \_ CONFIRM**](xtyp-connect-confirm.md) (a menos que el servidor haya especificado la marca de filtro CBF \_ SKIP CONNECT \_ \_ CONFIRMS). Esta transacción pasa el identificador de conversación al servidor.

En el ejemplo siguiente se solicita una conversación sobre el tema Sistema con un servidor que reconoce el nombre de servicio MyServer. Los *parámetros hszServName y* *hszSysTopic* se han creado previamente identificadores de cadena.


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



En el ejemplo anterior, [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) hace que la función de devolución de llamada DDE de la aplicación MyServer reciba una [**transacción XTYP \_ CONNECT.**](xtyp-connect.md)

En el ejemplo siguiente, el servidor responde a la transacción [**XTYP \_ CONNECT**](xtyp-connect.md) comparando el identificador de cadena de nombre de tema que el DDEML pasado al servidor con cada elemento de la matriz de cadenas de nombre de tema controla el servidor. Si el servidor encuentra una coincidencia, establece la conversación.


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



Si el servidor devuelve **TRUE en** respuesta a la transacción [**XTYP \_ CONNECT,**](xtyp-connect.md) DDEML envía una transacción [**XTYP \_ CONNECT \_ CONFIRM**](xtyp-connect-confirm.md) a la función de devolución de llamada DDE del servidor. El servidor puede obtener el identificador de la conversación procesando esta transacción.

Un cliente puede establecer una conversación con caracteres comodín especificando **NULL** para el identificador de cadena de nombre de servicio, el identificador de cadena de nombre de tema o ambos en una llamada a [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect). Si al menos uno de los identificadores de cadena es **NULL,** DDEML envía la transacción [**\_ XTYP WILDCONNECT**](xtyp-wildconnect.md) a las funciones de devolución de llamada de todas las aplicaciones DDE (excepto las que filtran la transacción **\_ XTYP WILDCONNECT).** Cada aplicación de servidor debe responder devolviendo un identificador de datos que identifica una matriz terminada en NULL de [**estructuras HSZPAIR.**](/windows/win32/api/ddeml/ns-ddeml-hszpair) Si la aplicación de servidor no ha llamado a [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) para registrar sus nombres de servicio y si el filtrado está en, el servidor no recibe transacciones **\_ WILDCONNECT de XTYP.** Para obtener más información sobre los identificadores de datos, [vea Administración de datos](data-management.md).

La matriz debe contener una estructura para cada par de nombre de servicio y nombre de tema que coincida con el par especificado por el cliente. DDEML selecciona uno de los pares para establecer una conversación y devuelve al cliente un identificador que identifica la conversación. DDEML envía la transacción [**XTYP \_ CONNECT \_ CONFIRM**](xtyp-connect-confirm.md) al servidor (a menos que el servidor filtra esta transacción). En el ejemplo siguiente se muestra una respuesta típica del servidor a la [**transacción \_ WILDCONNECT de XTYP.**](xtyp-wildconnect.md)


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



El cliente o el servidor pueden finalizar una conversación en cualquier momento mediante una llamada a la [**función DdeDisconnect.**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) Esta función hace que la función de devolución de llamada del asociado de la conversación reciba la transacción [**XTYP \_ DISCONNECT**](xtyp-disconnect.md) (a menos que el asociado especifique la marca de filtro CBF \_ SKIP \_ DISCONNECTS). Normalmente, una aplicación responde a la transacción **XTYP \_ DISCONNECT** mediante la función [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) para obtener información sobre la conversación que finalizó. Una vez que la función de devolución de llamada vuelve del procesamiento de la **transacción XTYP \_ DISCONNECT,** el identificador de conversación ya no es válido.

Una aplicación cliente que recibe una transacción [**XTYP \_ DISCONNECT**](xtyp-disconnect.md) en su función de devolución de llamada DDE puede intentar restablecer la conversación llamando a la función [**DdeReconnect.**](/windows/desktop/api/Ddeml/nf-ddeml-ddereconnect) El cliente debe llamar a **DdeReconnect desde** su función de devolución de llamada de DDE.

## <a name="multiple-conversations"></a>Varias conversaciones

Una aplicación cliente puede usar la [**función DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) para determinar si los servidores de interés están disponibles en el sistema. Un cliente especifica un nombre de servicio y un nombre de tema cuando llama a **DdeConnectList,** lo que hace que DDEML difusione la transacción [**\_ XTYP WILDCONNECT**](xtyp-wildconnect.md) a las funciones de devolución de llamada de DDE de todos los servidores que coinciden con el nombre del servicio (excepto los que filtran la transacción). La función de devolución de llamada de un servidor debe devolver un identificador de datos que identifique una matriz terminada en NULL de [**estructuras HSZPAIR.**](/windows/win32/api/ddeml/ns-ddeml-hszpair) La matriz debe contener una estructura para cada par de nombre de servicio y nombre de tema que coincida con el par especificado por el cliente. La DDEML establece una conversación para cada estructura **HSZPAIR** rellenada por el servidor y devuelve un identificador de lista de conversaciones al cliente. El servidor recibe el identificador de conversación mediante la transacción [**XTYP \_ CONNECT**](xtyp-connect.md) (a menos que el servidor filtra esta transacción).

Un cliente puede especificar **NULL para** el nombre del servicio, el nombre del tema o ambos cuando llama a [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist). Si el nombre del servicio es **NULL,** todos los servidores del sistema que admiten el nombre de tema especificado responden. Se establece una conversación con cada servidor de respuesta, incluidas varias instancias del mismo servidor. Si el nombre del tema **es NULL,** se establece una conversación en cada tema reconocido por cada servidor que coincida con el nombre del servicio.

Un cliente puede usar las funciones [**DdeQueryNextServer**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) y [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) para identificar los servidores que responden a [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist). **DdeQueryNextServer** devuelve el siguiente identificador de conversación en una lista de conversaciones y **DdeQueryConvInfo** rellena una estructura [**CONVINFO**](/windows/win32/api/ddeml/ns-ddeml-convinfo) con información sobre la conversación. El cliente puede mantener los identificadores de conversación que necesita y descartar el resto de la lista de conversaciones.

En el ejemplo siguiente se usa [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) para establecer conversaciones con todos los servidores que admiten el tema System y, a continuación, se usan las funciones [**DdeQueryNextServer**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) y [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) para obtener los identificadores de cadena de nombre de servicio de los servidores y almacenarlos en un búfer.


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



Una aplicación puede finalizar una conversación individual en una lista de conversaciones mediante una llamada a la [**función DdeDisconnect.**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) Una aplicación puede finalizar todas las conversaciones de una lista de conversaciones llamando a la [**función DdeDisconnectList.**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnectlist) Ambas funciones hacen que DDEML envíe transacciones [**XTYP \_ DISCONNECT**](xtyp-disconnect.md) a la función de devolución de llamada DDE de cada asociado. **DdeDisconnectList envía** una **transacción XTYP \_ DISCONNECT** para cada identificador de conversación de la lista.

Un cliente puede recuperar una lista de los identificadores de conversación de una lista de conversaciones pasando un identificador de lista de conversación existente a [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist). El proceso de enumeración quita los identificadores de las conversaciones terminadas de la lista y se agregan las conversaciones no duplicadas que se ajustan al nombre de servicio y al nombre del tema especificados.

Si [**DdeConnectList especifica**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) un identificador de lista de conversaciones existente, la función crea una nueva lista de conversaciones que contiene los identificadores de las conversaciones nuevas y los identificadores de la lista existente.

Si existen conversaciones duplicadas, [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) intenta evitar identificadores de conversación duplicados en la lista de conversaciones. Una conversación duplicada es una segunda conversación con el mismo servidor en el mismo nombre de servicio y nombre de tema. Dos de estas conversaciones tendrían identificadores diferentes, pero identificarían la misma conversación.

 

 




